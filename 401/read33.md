# Read: 33 - GraphQL @connection

## API (GraphQL)

**relationships between types**

+ The @connection directive enables you to specify relationships between @model types.
+ supports one-to-one, one-to-many, and many-to-one relationships.
+ You may implement many-to-many relationships using two one-to-many connections and a joining @model type.

 **Usage**

+ Relationships between types are specified by annotating fields on an @model object type with the @connection directive.
+ The fields argument can be provided and indicates which fields can be queried by to get connected objects.
+ When specifying a keyName, the fields argument should be provided to indicate which field(s) will be used to get connected objects.

**Has one**

```
type Project @model {
  id: ID!
  name: String
  team: Team @connection
}

type Team @model {
  id: ID!
  name: String!
}
```

**Has many**

```
type Post @model {
  id: ID!
  title: String!
  comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
}

type Comment @model
  @key(name: "byPost", fields: ["postID", "content"]) {
  id: ID!
  postID: ID!
  content: String!
}
```

**Many-to-many connections**

```
type Post @model {
  id: ID!
  title: String!
  editors: [PostEditor] @connection(keyName: "byPost", fields: ["id"])
}

# Create a join model and disable queries as you don't need them
# and can query through Post.editors and User.posts
type PostEditor
  @model(queries: null)
  @key(name: "byPost", fields: ["postID", "editorID"])
  @key(name: "byEditor", fields: ["editorID", "postID"]) {
  id: ID!
  postID: ID!
  editorID: ID!
  post: Post! @connection(fields: ["postID"])
  editor: User! @connection(fields: ["editorID"])
}

type User @model {
  id: ID!
  username: String!
  posts: [PostEditor] @connection(keyName: "byEditor", fields: ["id"])
}
```

**Limit**
The default number of nested objects is 100. You can override this behavior by setting the limit argument. For example:

```
type Post @model {
  id: ID!
  title: String!
  comments: [Comment] @connection(limit: 50)
}

type Comment @model {
  id: ID!
  content: String!
}

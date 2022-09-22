<script>
</script>
<div>
<!--type Blog @model {
  id: ID!
  name: String!
  posts: [Post] @connection(keyName: "byBlog", fields: ["id"])
}

type Recipe @model {
   id: ID!
  name: String!
}

type Ingredient @model {
    id: ID!
  name: String!
  quantity: String!
}

type Instruction @model {
   id: ID!
  info: String!
}
type Ingredient @model @key(name: "byRecipe", fields: ["recipeID"]) {
  id: ID!
  name: String!
  quantity: String!
  recipeID: ID!
  recipe: Recipe @connection(fields: ["recipeID"])
}

type Instruction @model @key(name: "byRecipe", fields: ["recipeID"]) {
  id: ID!
  info: String!
  recipeID: ID!
  recipe: Recipe @connection(fields: ["recipeID"])
}
-->
</div>
<style>
</style>

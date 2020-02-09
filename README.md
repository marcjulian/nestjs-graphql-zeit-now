# Nest Graphql deployed to Zeit Now

Get started by running:

```bash
npm run now:deploy
```

## Graphql

When importing `GraphQLModule` the graphql schema must be generated on-the-fly in memory otherwise it fails to boot in Zeit Now.

```typescript
GraphQLModule.forRoot({
  debug: true,
  playground: true,
  autoSchemaFile: true
}),
```

You can open the Graphql Playground, however, the schema is not fetched. Graphql queries are still correctly processed by nest.

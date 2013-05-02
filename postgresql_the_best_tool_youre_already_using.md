# Postgres: The best tool you're already using

## Tagging
- Defining arrays
- SQL: string[]
- AR: `array: true`
- Define arrays as text instead of strings!
- Can use set operators
  - contains  (@>) - must contain all elements. order doesn't matter
  - overlap - (&&) as long as oe element in common exists
- Add scopes that implement the filtering, parameterized

## Hierarchy
- CREATE table  clubs( id integer primary key, path integer[] )
- Materialized path
  - 1 Top level1. path [1]
    - 3 Child. path [1,3]
  - 2 Top level2
- Depth of nesting is length of array
- Find all children of a node by looking for all records whose path overlaps the given nodes path
- Find all the parents of a node by looking for all records where the ID overlap the full path

## Custom data
- Arbitrary data. Sparse data.
- No need for a column for everything
- hstore - hash
- better than serializing because you can query it
- not installed by default
- add migratioin to create the extension
- default schema in AR does not support. Must change schema to :sql
- options when creating (otherwise new records will have null hstores)
  - default: ''
  - null: false
- syntax similar to rails hash with quoted keys
- very easy to itroduce sql injection vectors. make sure to escape
- Operators
  - defined: defined(custom, 'some_key')
  - -> hash access
- Always stored as strings

## Full Text search
- text field
- to\_tsvector - strips out stopwords (normalized tokens). Stems tokens.
- to\_tsquery
- Operators
  - @@ - search on vectors
  - &&
  - ||
- Wildcard matching (prefixes only)
- Never passs user input to to\_tsquery, must be sanitized
- Create an index on full text search (`gin`)


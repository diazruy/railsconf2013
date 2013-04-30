# Building Extractable Libraries in Rails

- Duality
  - Ruby -> freedom
  - Rails -> conventions
- Rails frees us from making many tedious decisions
- /lib can benefit from conventions
  - Everything that will be extracted into a library should be namespaced
  - Avoid autoload
  -

## Namespacing
- Collisions with top level namespace
  - Use modules instead of prefixing or postfixing

## Avoid autoload
- Add an initializer that requires the top level file in /lib which itself explicitly requires the necessary files inside it

## Separate credentials
- Don't put them in source code (dont VCS)
- Don't use environment vars strewn throughout the code
- Add an initializer that uses the ENV vars (for exaple)
  -::config method

## Keep models focused
- Data Context Interaction (DCI)
  - Separate things that are important to the business from those that aren't

## DCI

### Role
- Wraps the business model
- Mixin into the model
### Context
- Encapsulates the business logic
- Gets initialized with raw data, wraps it in arole

- Good for Create, Update and Destroy, Not so much for Show and Index (Read). Decorator or presenter is better for this


### Test doubles
- Complete double
- OpenStruct
- Mocks



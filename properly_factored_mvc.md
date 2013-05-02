# Properly Factored MVC

- Commonly controllers are taking on way too many responsibilities
  - processing params
  - authentication
  - formatting data
  - authorization
  - data sanitization
  - etc.
- Controller methods should really be no more than a half dozen lines
- Refactoring doesn't add customer facing value (in a sense)

## Exploring a project
- helper methods can easily hide complexity
  - instance variables created in helper methods are not visible in the action

- Characterization test - assume that what you have right now works
  - Write to disk the existing version of an HTML and then compare it after changing
  - Raise errors if differences show up
  - Make sure things like time are kept fixed
  - Can we make the "lockdown" generator a gem?
- As a first step, just move the whole helper method logic to a standalone PORO (e.g. app/models/stats/tag_cloud.rb)
  - Do not remove the actual method code, just inject the new call so the tests still pass
    - Iterate over errors justto make sure the instantiation has all the necessary constants/variables
    - Add attr\_accessors to the PORO to retrieve the instance vars that the controller is expecting
    - Gradually replace code in controller with corresponding accessor
- After everything has been moved to the class, all isntance variables replaced with method calls
  - Good idea to commit at this stage
  - Give things better names
    - Remove redundancy, obviated by being in its own class (prefixes, suffixes)
    - Revisit argument names




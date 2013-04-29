# Maintainable views

## Unmaintanable templates
- Markup repetition
- Logic in templates

### Markup repetition
- Good designers repeat themselves
- Devs don''t
- Abstract interface components
- Use partials

### Logic in templates
- Highly repetitive
  - Other views using same logic are inevitable
- Painful to test
- Helpers
  - Small snippets only
  - Problems
    - Big projects en up with tons of them
    - Difficult to organize
    - Complex logic is not well suited for them
    - Don''t feel right
    - Not very OOP
- Decorator pattern
  - Wrap a single object
  - transparent inteface
  - forward methods to original
  - Add presentational logic
  - Easy to test
  - Easy to grok
  - Draper

- Complex views -> Presentation Models
  - Address complex conditionals or not easily reusable blocks of code
  - PORO with the template and all necessary models
  - #to_s -> renders a partial passing itself as the object (necessary?)
  - Helpers to set up view
  - form_for is a view object
    - Custom form builders are very easy to add custom layouts to a form

## Other tips
- Use i18n
- Gems to explore: simple_form and table_cloth

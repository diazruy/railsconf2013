# Front end Testing for Skeptics

- Third party JavaScript
- Capybara
  - Enable js\_errors = true, and inspector = true
- Phantom JS
- Poltergeist (capybara driver for Phantom JS)
- Capybara can evaluate arbitrary JS in the context of the page execution
- page.driver.debug -> launch web inspector

## Problems
- PhantomJS crashes
- Waiting -> mostly resolved by Capybara 2.
  - Synchronize
- Transactions and DB setup
  - Run all non-JS tests first
  - Run JS tests later so they don't conflict with DB usage

# JS Unit testing
- Frameworks
  - Jasmine
  - QUnit
  - Mocha
- Need to be loaded in a browser
- blog Matthew O'Riordan
- modeset/teabag gem

# Perceptual Diffs
- Visual diff of render to quickly detect incorrect results




# Testing Complex Systems

## Creating Data for tests
- hard when objects are entangled

## Limiting tests to a particular part of the code
- hard when objects are entangled

## Driving modular design with tests

## Where to start?
- Approaches
  - Dive Right In - BAD
  - Outside-in
  - Bottom Up

## What to test first?
- Initialized state
- Basic happy path
- What makes it break?
- Special cases


## When to use Fixtures
- Good for cucumber - global or opaque not important, but speed is

## Factories
- Slow with associations
- Easy to build long slow attribute trees

## Talking to 3rd party services
- Wrap external services (even Ruby libraries) in your own code
  - Different vocabulary from domain

# Collections as model factories *NUGGET*



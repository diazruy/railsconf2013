# Natural Language Processing in Ruby

- NLP - ability to understand and/or generate human language
  - Search
  - Predictive text
  - Spell check
  - Content categorization
  - Machine translation
  - Auto summarization

- Why is it so hard?
  - no perfect solution
  - disagreement on the results
  - fixing one thing breaks another
  - Language is a moving target (new grammar, terms, syntax)
  - Many aspects are computationally complex

- Problem is growing, larger data sets

## Common approaches

- Rule-Based analysis (e.g. Rails pluralization)
- Statistical Analysis
- Machine Learning (AI)

Most effective solutions today rely on human-in-the-loop approach

## Tools and Libraries

- NLP Tookit - Python, De facto tool

## Ruby
  - Chronic - Ruby. For date parsing
  - Linguistics - conjugation, articles, etc
  - Punkt Segmenter - pull apart text and identify sentences. has training mode
  - Ruby stemmer - exposes snowball stemmer API. Find root word of particular words
  - Treat - trying to make an equivalent of NLP Tookit
  - RBWordnet (?) - stopwords, synonyms

## JRuby
- Allows you to leverage established Java libraries (amongst other benefits)
- Many existing NLP java libraries, much more mature, closer to Python's


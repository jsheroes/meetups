# Joyful unit testing with Jest

### Speaker: Andrei Cacio
### Date: 06.03.2018
### Venue: Ve Interactive
### Description:
We are happy to announce that our next meetup will be about unit testing, more exactly about an unit testing framework called Jest.

In this meetup we will talk about the main diferences between other testing solutions like MochaJS with ChaiJS. Also Andrei will highlight the benefits which Jest brought to his coding experience.

Some big topics which we will cover:
- stubing, spying
- module mocking
- snapshot testing
- jest cli

### Slides: 
* http://slides.com/andrei-cacio/deck

### Repo:
  * https://github.com/andrei-cacio/joyful-unit-testing-with-jest

### Meeting notes:
- when used more than 2 level nested `describe()`, performance may suffer because of Jest not beeing able to properly parallelise the tests
- for mocking 3rd party libraries like `lodash` which has nested modules, you can use `moduleNameMapper` to mock them out one by one

Some useful links that people pointed out during the open discussion:
- [jest-axe](https://github.com/nickcolley/jest-axe)
- [jest-extended](https://github.com/jest-community/jest-extended)
- [jest-image-snapshot](https://github.com/americanexpress/jest-image-snapshot)

# Joyful unit testing with Jest ( Andrei Cacio ) 

Slides: http://slides.com/andrei-cacio/deck
Repo which I demoed on: https://github.com/andrei-cacio/joyful-unit-testing-with-jest

Some useful links that people pointed out during the open discussion:
- [jest-axe](https://github.com/nickcolley/jest-axe)
- [jest-extended](https://github.com/jest-community/jest-extended)
- [jest-image-snapshot](https://github.com/americanexpress/jest-image-snapshot)

Notes:
- when used more than 2 level nested `describe()`, performance may suffer because of Jest not beeing able to properly parallelise the tests
- for mocking 3rd party libraries like `lodash` which has nested modules, you can use `moduleNameMapper` to mock them out one by one

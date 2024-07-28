## Introduction

Smiley's Unit Testing framework.

## Dependencies

- Greybel

## Writing Tests

Create unit tests as follows:

    import Sut from ../src/sut.src

    Sut.create(name, unit, desc="").run = function()
        // TEST CODE HERE
    end function

    Sut.start()

A test is considered to have passed if `run` does not return a result (or returns something equivalent to `false`). If a string is returned, it is interpreted as the failure reason. This allows for custom evaluation logic. For more standard checks, *assertions* can be used. This allows for cleaner tests and standardized output. The following types of assertions are available:

- assert(expr, desc='')
- assertFalse(expr, desc='')
- assertEqual(expr1, expr2, desc='')
- assertNotEqual(expr1, expr2, desc='')

Assertions return true on failure and save the result to the unit test. They are used as follows:

    if self.assert(true) then return
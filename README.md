# The Bank Tech Test

### My approach
I take an Outside-In approach to TDD, trying to write tests that describe the User scenario clearly.
This helps me to clarify the requirement to myself, begins to define the public API of my system, and should serve as documentation for the software.
As a result you also get good test coverage which isn't so tightly coupled to the implementation that the tests are brittle.

1. My starting point is to figure out how to test the printing of bank statements.
   The simplest way to do that is to create a new account and immediately print the bank statement.
   
2. Next I wanted to drive out the Deposit API. First test can be satisfied by hard-coded implementation, so a second test is used to drive some print logic.




### Requirements
* Deposits, withdrawal
* Account statement (date, amount, balance)
* Statement printing

### Acceptance criteria

**Given** a client makes a deposit of 1000 on 10-01-2012  
**And** a deposit of 2000 on 13-01-2012  
**And** a withdrawal of 500 on 14-01-2012  
**When** she prints her bank statement  
**Then** she would see  


```
date || credit || debit || balance
14/01/2012 || || 500.00 || 2500.00
13/01/2012 || 2000.00 || || 3000.00
10/01/2012 || 1000.00 || || 1000.00
```

### Additional extensions

* Statement filters (just deposits, withdrawals, date ascending, date descending)
* Graphical interface

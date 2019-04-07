# Testing(Manual and Automatic)

### Differences between Black Box Testing vs White Box Testing.

- Black Box Testing is a software testing method in which the internal structure/ design/ implementation of the item being tested is NOT known to the tester
- White Box Testing is a software testing method in which the internal structure/ design/ implementation of the item being tested is known to the tester.

### Describe what three of the most common types of automated tests.
- Unit tests: A single piece of code (usually an object or a function) is tested, isolated from other pieces
- Integration tests: Multiple pieces are tested together, for example testing database access code against a test database
- Acceptance tests (also called Functional tests): Automatic testing of the entire application, for example using a tool like Selenium(capybara or cucumber) to automatically run a browser.

### Describe TDD?
Test Driven Development can be described with three rules.

- You are not allowed to write any production code unless it is to make a failing unit test pass.
- You are not allowed to write any more of a unit test than is sufficient to fail; and compilation failures are failures.
- You are not allowed to write any more production code than is sufficient to pass the one failing unit test.

Methodogy process can derive to 
- red phase (when we have writed test but not have realization)
- green phase (when we write code that pass test with minimum amount of code required to make the test pass)
- refractor phase

T.D.D. requires much more time than “normal” programming

### Describe BDD?
BDD suggests to test behaviors, so instead of thinking of how the code is implemented, we spend a moment thinking of what the scenario is. 

### What differents with stub and mock?

- The biggest distinction is that a stub you have already written with predetermined behavior. So you would have a class that implements the dependency (abstract class or interface most likely) you are faking for testing purposes and the methods would just be stubbed out with set responses. They would not do anything fancy and you would have already written the stubbed code for it outside of your test.
- A mock is something that as part of your test you have to setup with your expectations. A mock is not setup in a predetermined way so you have code that does it in your test. Mocks in a way are determined at runtime since the code that sets the expectations has to run before they do anything.

### What difference between let and let! in RSPEC
let - использует ленивый вызов перед блоком теста, тобишь то что в методе не будет выполнено, пока мы его не вызовем.
let! -  вызывает метод перед каждым примером или блоком теста, используем мы его или нет.


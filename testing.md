# Testing 

### Describe TDD?
- TODO:answer

### Describe BDD?
- TODO:answer

### What differents with stub and mock?

- I believe the biggest distinction is that a stub you have already written with predetermined behavior. So you would have a class that implements the dependency (abstract class or interface most likely) you are faking for testing purposes and the methods would just be stubbed out with set responses. They would not do anything fancy and you would have already written the stubbed code for it outside of your test.
- A mock is something that as part of your test you have to setup with your expectations. A mock is not setup in a predetermined way so you have code that does it in your test. Mocks in a way are determined at runtime since the code that sets the expectations has to run before they do anything.


### What difference between let and let!
let - использует ленивый вызов перед блоком теста, тобишь то что в методе не будет выполнено, пока мы его не вызовем.
let! -  вызывает метод перед каждым примером или блоком теста, используем мы его или нет.


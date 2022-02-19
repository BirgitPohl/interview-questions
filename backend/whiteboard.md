## Please can you explain in as much detail as you like how a web browser gets a generated page?
1. How does the request reach the backend application?
2. What kind of components are involved and how is a response generated?
3. Describe an arbitrary REST API endpoint.
    1. How do you define the packages?
    2. Rest Controller, Service, Repository, Dao
    3. What kind of HTTP methods would you implement?

## If you need to store a "city" object, what kind of database would you use?

## What do you understand under database normalization? 

# Testing
i. Unit Tests
3. Integration Tests
4. End-to-end tests
5. What kind of classes would you test with which kind of test?
v. What are the benefits of each kind of tests? vi. Experience with TDD/BDD in any project?
1. What is your personal choice?

# API
## What kind of characteristics make up a "good" API for you?
1. Create a draft of the classes involved in such an endpoint.
2. How could the underlying database model look like?
3. What kind of things would you test in such an environment?
4. How many Unit/Integration/End-to-end tests would you write?

## What does idempotency mean in REST APIs?
1. What are the pros
    1. Fast and continuous improvements i. Versatile: different tech stacks
    2. Continuous Delivery iii. Resilience
    3. Scalability
    4. Faster time to market
2. Cons
    1. How do you slice micro-services?
    2. System integration tests are more difficult
    3. Management of too many micro-services is difficult
    4. Architecture is hard to do right

3. Ways of communication between micro-services?
    1. APIs, remote procedure calls, event bus
4. How could the data flow look like, starting with the HTTP request?


##  Let's dive in deeper into the backend, assuming there is Kubernetes cluster or NGINX with a Spring Boot application:
 1. Describe some pros/cons of a micro-service architecture.
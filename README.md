# 3.8-assignment-sgy
## There are benefits to moving to microservices, however, it will also lead to design complexities. These are some complexities and ways to overcome them:
## 1.Overcoming Design Complexity
-Define clear boundaries for microservices to create well defined interfaces.

-Establish stable and versioned APIs between microservices on websites like Github so that you can do a rowback on microservices if there are any compatibility issues.

-Use automated testing for each service and deployment pipelines and use containerization like Docker for consistent deployment across environments.

## 2.Achieving Data Consistency
-Use databases that is compatible with each microservice. Consider databases like SQL or NoSQL based on service's needs for consistency

-For services that require strong consistency use synchronous communication, for less critical data use asynchronous communication.

-Make sure that transactions within a service is consistent. Try to use database transactions to ensure data integrity within single service boundry.

## 3.Need for Testing and Monitoring
-Use comprehensive testing strategies like unit testing, integration testing, End-to-End testing and contract testing.

-Test automation with CI/CD pipelines for automated testing and deployment or use mock services or stubs to simulate behavior and response form dependent services during testing to isolate services.

-Conduct chaos experiments to constantly inject failures into system to test system's resiliency and recovery.

## 4.Increased Operational Complexity
-Implement robust DevOps Practices like: Automated deployment, testing and monitory; Ensuring reproducibility and scalability by define and manage infrastructure as a code; Using tools to ensure consistent configuration across enviroment and services.

-Using container tech like Docker to package apps and dependencies consistently and using orchestrators like Kubernetes to manage container apps, automate deployment and scale services

-Centralize logging and monitoring by using logging systems like Splunk to aggregate logs for services for easier troubleshooting and using tools like Datadog to collect metrics to detect anomalies, trigger lerts for performance issues and failures.

## 5.Inter-Service Communication Breakdown
-Use circuit breaker patterns like Netflix Hystrix to preven cascading failures by failing fast and providing fallback mechanisms when service is unresponsive.

-Configure reasonable timeout values and allow retries for communication between services, to handle failures.

-Use bulkhead patterns to isolate failures to ensure that the failures do not bring down the entire system.

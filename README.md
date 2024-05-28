# Introduction
This comprehensive report presents the findings and insights derived from our rigorous
evaluation of OrangeHRM, a Human Resource Management software. The primary objectives of
this assessment were to conduct thorough Software Performance Testing.
# Objective
The aim of this project was threefold: <br/>
Performance Testing: To assess the system's responsiveness, stability, and scalability under
various load conditions.<br/>
- Tool Selection
JMeter: Employed for load testing and measuring performance metrics under different load
conditions. <br/>
- System and Environment Description
OrangeHRM was installed and operated within a controlled local environment, allowing for
precise monitoring and testing. Our setup ensured an isolated environment conducive to in-depth
testing without external influences. The testing environment was designed to simulate real-world
scenarios while maintaining a secure and stable infrastructure for accurate assessments.
This report encapsulates the comprehensive evaluation of OrangeHRM, revealing insights into
its functionality, performance under varying loads. The subsequent sections provide a detailed
analysis of each testing phase, uncovering observations, challenges faced, and recommendations
for improvement. <br/>

## 5 test suits; Total 25 test cases.
JMeter is an open-source tool for performance testing, analyzing how software or servers handle
various loads to ensure they meet performance benchmarks.<br/> <br/>

#### 5 types of tests performed in each test suit. <br/>
1. Performance Test: Measures how well a system performs under specific conditions. <br/>
2. Load Test: Checks performance under expected loads. <br/>
3. Stress Test: Pushes the system to its limits to identify failure points.<br/>
4. Spike Test: Assesses performance during sudden load spikes.<br/>
5. Endurance Test: Evaluates system stability over prolonged periods.<br/>

Test Suite 1: Employee List Functionality.<br/>
Test Suite 2: Employee Reviews.<br/>
Test Suite 3: Dashboard Functionality.<br/>
Test Suite 4: Admin Functionality.<br/>
Test Suite 5: Add Employee Functionality.<br/>
Test Results for each.<br/>

## Test Case 1: Performance Testing.<br/>
#### Test Scenario: Measure system response time under varying user loads.<br/>
Preconditions:<br/>
- Logged into the OrangeHRM system.
- The system is operational and accessible.
#### Test Steps:<br/>
- Access the module.
- Load the list with different user counts: 50, 100, 150, ..., 700.
- Record the average response time for loading at each user count.
#### Expected Results:
Response time should remain within acceptable limits for increasing user counts.
Analyze the data to identify any trends or performance bottlenecks. <br/>
#### Actual Result
Error Rate: Increased notably at 550 samples, reaching 10.72%, impacting overall throughput.<br/>
Throughput: Experienced a decrease to 8.36 requests per second at 550 samples.<br/>
Average Response Time: Showed stability until 550 samples, averaging 28.043 milliseconds.<br/>

## Test Case 2: Load Testing
#### Test Scenario: Evaluate system behavior under increasing load.<br/>
#### Preconditions:<br/>
- Logged into the OrangeHRM system.
- Access to the module.
#### Test Steps:
- Gradually increase the number of users accessing from 50 to 700.
- Measure the system response time for each increment.
#### Expected Results:
The system should maintain stable response times under increasing user loads.
Monitor the list response times for any anomalies or degradation.<br/>
#### Actual Result
 Effective until 550 samples, beyond which signs of strain emerged.<br/>

## Test Case 3: Stress Testing 
#### Test Scenario: Apply sudden and extreme load.
#### Preconditions:
- Logged into the OrangeHRM system.
- Direct access to the module.
#### Test Steps:
- Simulate a sudden 300% increase in user load.
- Monitor system behavior, response times, and any errors.
#### Expected Results:
The system should handle the sudden load without crashing or significant performance
degradation.
Evaluate system stability during and after the stress test. <br/>
#### Actual Result
Notably struggled at 550 samples, resulting in increased error rates
and reduced throughput.<br/>

## Test Case 4: Spike Testing
#### Test Scenario: Simulate sudden spikes.
#### Preconditions:
- Logged into the OrangeHRM system.
- Access to the module.
#### Test Steps:
- Initiate rapid and significant user actions (e.g., filtering, sorting).
- Monitor system performance and responsiveness.
#### Expected Results:
The system should handle sudden spikes without critical failures or data inconsistencies.
Assess system recovery time after the spike.
#### Actual Result
Vulnerable to sudden load spikes at 550 samples, impacting
performance metrics.<br/>

## Test Case 5: Endurance Testing.
#### Test Scenario: Evaluate system stability under sustained load.
#### Preconditions:
- Logged into the OrangeHRM system.
- Access to the module.
#### Test Steps:
- Maintain a consistent user load (e.g., 500 users) for an extended duration
(e.g., 30 minutes).
- Monitor system performance, memory usage, and any potential degradation.
#### Expected Results:
The system should maintain stable response times and functionalities without significant
memory leaks or performance degradation over time.
#### Actual Result
Stable performance until 550 samples, beyond which stress and spike issues
arose.

![Screenshot 2024-05-28 163901](https://github.com/Rifat-BH/Jmeter_Repository/assets/73948267/9ce45632-8532-4191-b5d0-7234186e8139)


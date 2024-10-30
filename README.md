# Performance Testing_LANS Unit Exchange Hospital

 <img width="199" alt="main_logo" src="https://github.com/user-attachments/assets/066c26ea-bb4f-450b-82ad-298f90435df6">


## Overview

This repository provides a comprehensive suite for performance testing of LANS Unit Exchange Hospital. It enables developers and QA engineers to measure and analyze the performance characteristics of their systems under different load conditions.


## Features

- **Load Testing**: Simulate varying levels of traffic to assess system behavior.
- **Stress Testing**: Determine the system’s breaking point by pushing it beyond normal operational capacity.
- **Benchmarking**: Measure and compare performance metrics over time.
- **Detailed Reporting**: Automatic generation of performance reports with visualizations.

## Technologies Used

- [Apache JMeter](https://jmeter.apache.org/)
- Command Prompt(cmd).

## Prerequisites

Ensure you have the following installed:

- [Java 8+](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html) (for JMeter and Gatling)
- [Python 3.x](https://www.python.org/downloads/) (for Locust)
- Docker (optional, for containerized testing)

## Installation
- windows mac linux
- Check java version -min java 8
- download jmeter
  ```bash
   https://dlcdn.apache.org//jmeter/binaries/apache-jmeter-5.6.3.zip
- unzip and keep jmeter folder in any location 
* don't use GUI mode for performance test only debug and setup 
- start jmeter 
  (download -> unzip -> bin -> jmeter.bat)
   
## Creating JMeter test
- Start JMeter
- Test plan creation
- Thread Group
- Sampler (http)
- Listener
- Run
### Listener
- View results tree
- Summary Report
- Aggregate report
- Graph results
- Backend Listener
### Assertions
- Response assertion
- Duration assertion
- size assertion
- html assertion
- XML JSON assertion
- XPATH Assertion
## Blazemeter
GUI consumes memory, slower Integrating with any external process CI/CD
## Command line Test
- Resource utilization
```bash
   jmeter -n -t LANS_hospital_T100.jmx -l LANS_Report\LANS_hospital_T100.jtl
```
- HTML report generate
```bash
   jmeter -g LANS_Report\LANS_hospital_T100.jtl -o LANS_Report\LANS_hospital_T100.html
```
## Extract data for reporting in jmeter
Dear, 

I’ve completed performance test on frequently used API for test App.<br> 
Test executed for the below mentioned scenario in server 000.000.000.00. 

- 100 Concurrent Request with 2 Loop Count; Avg TPS for Total Samples is ~ 234 And Total Concurrent API requested: 13200.<br>
- 200 Concurrent Request with 2 Loop Count; Avg TPS for Total Samples is ~ 350 And Total Concurrent API requested: 26334.<br>
- 250 Concurrent Request with 2 Loop Count; Avg TPS for Total Samples is ~ 424 And Total Concurrent API requested: 16498.<br>
- 300 Concurrent Request with 5 Loop Count; Avg TPS for Total Samples is ~ 443 And Total Concurrent API requested: 75468.<br>
While executed 300 concurrent request, found  27 request got connection timeout and error rate is 1.19%. <br>
Summary: Server can handle almost concurrent 65000 API call with almost zero (0) error rate.<br>
Please find the details report from the attachment and  let me know if you have any further queries. 

![Screenshot_4](https://github.com/user-attachments/assets/e8d5c8ab-b8b4-4e57-8c6e-02ce8a0d4551)

![Screenshot_3](https://github.com/user-attachments/assets/8c93c011-5154-421a-b192-e444a36e1c45)

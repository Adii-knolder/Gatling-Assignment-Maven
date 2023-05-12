# Gatling Assignment

## Overview:-

```python
The task requires you to create a Gatling performance testing project in IntelliJ using Maven or through the terminal, without using the Gatling recorder. 

The data inputs for the test should be fed from an external CSV file data source. 

You should use proper assertions to validate the response and the time taken for each request made using the HTTP methods POST, GET, and PUT.

You also need to demonstrate the chaining of scenarios in your test. 

Additionally, for each POST API request made, you must generate new values for the request body, ensuring that the value of the 'Json' field is different for each request.

You should generate a user load in the following way: For the first 5 seconds, no users will be injected. 

Then, 50 users will be injected at once, followed by a constant injection rate of 20 users per second for the next 15 seconds. 

Next, the number of users will be ramped up to 100 for the next 30 seconds. The test will run for a fixed duration of 1 minute.

Also, Do not hardcode values of Load simulation instead they should be passed easily from terminal.
```

## Tools used to perform the task:-

```python
IDE - Intellij

Performace Testing Tool - Gatling (without Gatling engine and Gatling recorder)

Language Used - Scala

Build system - Maven
```

## Running the test

clone the repository in your local system
```python
git clone https://github.com/Adii-knolder/Gatling-Assignment.git
```

Navigate to project root directory
```python
cd Gatling-Assignment-Maven
```

On terminal
```python
mvn gatling:test -DforAtOnceUsers=50 -DforConstantUsers=20 -DforRampUpUsers=100 -Dramp=30 -Dsec=15
```

The above command perform the given load simulation:
```python
1- Inject 50 users at once [ -DforAtOnceUsers = 50]
2- Inject the users at a constant rate of 20 for the next 15 seconds [ -DforConstantUsers = 20, -Dsec = 15 ]
3- Ramp up the 100 users for the next 30 seconds [ -DforRampUpUsers=100, -Dramp = 30 ] 
```

## Gatling report Analysis is present in:-

```python
ReportAnalysis.md file
```
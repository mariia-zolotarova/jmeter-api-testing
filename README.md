# jmeter-api-testing

Test Execution Report
Performance & Functional Testing - JSONPlaceholder
1. Test Description
A Test Plan was created in Apache JMeter to test the following endpoints of:
https://jsonplaceholder.typicode.com
Tested Requests:
•	GET /posts
•	POST /posts
•	PUT /posts/1
•	PATCH /posts/1
•	DELETE /posts/1
Thread Group Configuration:
•	Number of Threads (Users): 10
•	Ramp-up Period: 10 seconds
•	Loop Count: 3
The requests were executed over a 10-second ramp-up period with 3 iterations per user.

2. Assertions Used
Three types of assertions were added to each HTTP request:
1. Response Assertion
•	Response Code = 200 (for GET, PUT, PATCH)
•	Response Code = 201 (for POST)
•	Response Message = OK (for DELETE)
2. Duration Assertion
•	Response time does not exceed the defined threshold (600 ms)
3. Size Assertion
•	Response size does not exceed 1500 bytes (for POST, PUT, PATCH, DELETE)
•	Response size does not exceed 30000 bytes (for GET)
All assertions were executed successfully without any failures.

3. Results (View Results Tree)
Using the "View Results Tree" listener, the following was verified:
•	Response Code - all requests returned expected status codes
•	Response Message - OK / Created
•	Assertion Results - all checks passed successfully
•	Response Data - responses contain valid JSON data
No failures were detected.

4. Results (Summary Report)
Using the "Summary Report" listener, the following metrics were obtained:
•	Samples: 30
•	Error %: 0%
•	Average Response Time: within acceptable limits
•	Throughput: stable
•	Received KB/sec: stable
Analysis:
•	All requests were executed successfully
•	The server responded consistently
•	Response times remained within acceptable limits
•	No performance-related errors were detected
5. Conclusion
The JSONPlaceholder API:
•	Operates stably
•	Correctly processes all HTTP methods
•	Returns appropriate status codes
•	Responds within acceptable time limits
•	Does not generate errors under moderate load (3 iterations, 10 seconds ramp-up)
The system successfully passed basic functional and simple load testing.


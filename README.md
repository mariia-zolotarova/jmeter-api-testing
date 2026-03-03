# jmeter-api-testing

API Stress Testing

Performance and stress testing conducted using Apache JMeter.

Scope

GET, POST, PUT, PATCH, DELETE
Response code & size assertions

Load Threshold

≤1000 users — stable

~1500 users — degradation begins

2500+ users — high error rate

3500 users — critical failure

CLI
jmeter.bat -n -t Stress_Test_Plan.jmx -l results.jtl -e -o report

Non-GUI mode used for accurate performance results.


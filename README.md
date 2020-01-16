# hystrix_dashboard

Monitor calling service using Hystrix with Hystrix Dashboard of Spring Cloud Netflix


Now, if you start the application and then request to the address “http://localhost:8082/hystrix/”, you will see the home page where event stream URL needs to be put for monitoring.

In the above page, as you can see, it has a box to enter the URL. This URL is the hystrix.stream that will provide the data for Hystrix Dashboard!

Go back to the Hystrix Dashboard window and enter this URL http://localhost:8085/actuator/hystrix.stream, then press the “Monitor Stream” button, you will see the following result:

You only see the word “Loading …” above because there is no data to display that.

If now, you request to the address “ http://localhost:8085/api/course/get” and http://localhost:8085/api/student/get?courseID=2 and go back to the Hystrix Dashboard window, you’ll see the following result:

The service information we are calling in the COURSE-SERVICE AND STUDENT-SERVICE method of this application has been displayed. There are 7 different information about a called service, displayed including Success, Short-Circuited, Bad Request, Timeout, Rejected, Failure and Error. Each information will have different colors to make it easier for you to grasp.
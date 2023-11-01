# Project-10


DEPLOY YOUR API

By now you should have a working Docker service that consists of multiple containers orchestrated by Docker to work together, and defined using infrastructure-as-code practices.

This week’s assignment will require you to deploy your API in a production environment, using Google Cloud Platform. This should be done using Compute Engine, and configuring GCPLinks to an external site. to deploy the container directly, or provisioning a VM with Google's Container-Optimized OSLinks to an external site. and writing a startup script or init file that will load and run the correct image. You should be prepared to share the publicly-accessible URL to the running service in Slack, and we will test the API using my test suite.

This has a few implications:

Ensure that you have configured your GCP VM to “Allow HTTP Traffic” in the Firewall configuration section. 
In order for your API to be running on the standard HTTP port in your VM, you will need to map your container’s API port (probably 4000) to port 80 on the Docker host.
Since you are now running your containers in GCP, it makes sense to make use of GCP’s native logging and monitoringLinks to an external site. tools. Modify your Docker logging driverLinks to an external site. to use the Google Cloud loggingLinks to an external site., and set up an appropriately relevant Logs Dashboard to monitor your service for health.

GRADING CRITERIA

Using the supplied container images and build artifacts (such as a docker-compose.yml file or equivalent), does the project build and run? 
Does your publicly-deployed API pass all my automated test cases (I will be extending the tests to incorporate the new key-val storage endpoints)? 
Does your automated test suite include sufficient test coverage for the new endpoint?
How did you make use of the Google Logging tools? What do your dashboards tell us about your service?
What does the electronic record of group collaboration in both GitHub and Slack tell me about your team effectiveness? How did you divide and coordinate the work?

# Report
# Dockerized Application Setup and Deployment
## Issues Identified

1. Minor spelling mistakes in configuration files led to misconfigurations, disrupting the setup process.

2. There was an invalid HTML File Path in Dockerfile. The Dockerfile referenced an HTML file that did not exist, resulting in build errors due to the invalid path.

3. The docker-compose up command issued a warning regarding the obsolete version attribute. While not critical, it created potential for confusion.

4. Flask displayed a warning about running in development mode, advising the use of a production-ready WSGI server.

5. After switching to gunicorn, only nginx logs appeared by default, causing python_app logs to be hidden from the main output.
---
## Resolution Steps

1. Addressed spelling errors across configuration files to ensure proper paths and key names, eliminating syntax-related setup issues.

2. Removed the invalid HTML file path from the Dockerfile to resolve image build errors and align file references with the actual directory structure.

3. Deleted the obsolete version line in docker-compose.yaml to clear the warning during deployment.
Switched to Gunicorn for Production Readiness

4. Replaced the Flask development server with gunicorn by updating the Dockerfile.
This provided a production-ready WSGI server to host the application.

5. Enabled Python Application Logs
Used docker logs -f python_app to access logs for python_app independently, allowing for monitoring of both nginx and python_app.
---
The application is now successfully deployed on a cloud server, fully operational with production-level stability using gunicorn.

## Deployment Access(AWS)
Cloud Deployment Endpoint: http://13.51.204.137/

## Attachments
Screenshots of the application's success page confirming assignment completion 
and nginx access logs verifying a successful request to the application 
are attached below.
## Screenshots

### Success Page
![Success Page](./Screenshot%202024-10-29%20183629.png)

### Nginx Access Logs
![Nginx Logs](./Screenshot%202024-10-29%20225027.png)

# Management Service for Algonquin Pet Store

This lab assignment involves developing the **Management Service** for the Algonquin Pet Store. The service handles incoming order messages via **RabbitMQ** and makes them accessible through a **REST API** for the store-admin web application. The implementation adheres to four principles of the **12-Factor App** methodology: **Codebase**, **Dependencies**, **Configuration**, and **Backing Services**.

## `index.js`

The main functionality of the Management Service is defined in this file. It establishes a connection with **RabbitMQ**, processes the incoming order messages, and offers a REST API for the store-admin web application to use the data.

### Implementation Overview:

1. I installed the necessary dependencies to make RabbitMQ work and set up RabbitMQ in the `index.js` file using the **amqplib** library.
2. To manage the requests from the store-admin web application, a **Node.js REST API** framework was created.

## `test-api.http`

This file holds **HTTP requests** to use in testing the REST API endpoints. These requests mimic API calls to ensure that the Management Service is functioning as expected. For these tests, I employed the **REST Client** extension in Visual Studio Code to make API testing more manageable.

## Deployment Process

1. The Management Service was deployed to **Azure Web App**, running on a **Linux** environment.
2. I configured the necessary **environment variables**, including the RabbitMQ connection string, to enable communication between the service and RabbitMQ, which is hosted on an **Azure VM**.
3. **GitHub Actions** was used to automate the deployment process. The repository was connected to Azure, enabling **Continuous Integration and Deployment (CI/CD)**. Each time updates are pushed to the GitHub repository, Azure automatically redeploys the service.

Upon following these steps, the Management Service was successfully deployed and made accessible through the **Azure Web App**.

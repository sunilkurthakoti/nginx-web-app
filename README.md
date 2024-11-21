# nginx-web-app  
**Deploy a Web App on Nginx Server using AWS App Runner** </br>
**By AWS Workshop**  


---



## Steps to Deploy  

### 1. Develop Your Application  
- **HTML File**: Create a basic webpage, e.g., `index.html`, to be hosted as part of the app.
- 
  ![Screenshot (49)](https://github.com/user-attachments/assets/8c4b3dc3-aba6-4357-8b24-35cfbe2a1045)

- **Dockerize the App**: Write a `Dockerfile` to containerize the application using a base image like Nginx.

  ![Screenshot (50)](https://github.com/user-attachments/assets/32131e4d-45a9-4abb-8793-c1473985d911)


---

### 2. Set Up AWS CLI  
- Install AWS CLI on your system and configure it with your credentials and default region.  
- This setup allows interaction with AWS services through your terminal.  

---

### 3. Push Docker Image to ECR  
- **Create ECR Repository**: Use the AWS Management Console to create a container repository for your app.
  
    ![Screenshot (53)](https://github.com/user-attachments/assets/9765a4bb-1420-41f5-a9dc-f7b405fedef0)

- **Follow ECR Steps**:  
  - Authenticate Docker with your ECR registry.  
  - Build the Docker image.  
  - Tag the image for ECR.  
  - Push the image to the ECR repository.

    ![Screenshot (51)](https://github.com/user-attachments/assets/13759b67-45f3-47d5-8b2a-c325b9d56f6d)

    ![Screenshot (52)](https://github.com/user-attachments/assets/e0d1c00c-cfb2-449f-b228-5279caa2f647)

![Screenshot (54)](https://github.com/user-attachments/assets/560df70d-c487-4613-9fc6-a85bb2065632)


---

### 4. Create an App Runner Service  
- Open the AWS App Runner console and click **Create Service**.  
- **Select Source**: Choose **Container Registry (ECR)** as the source and select the image from your ECR repository.

  ![Screenshot (55)](https://github.com/user-attachments/assets/ab3a93b9-1370-4479-8476-7f94b8da1c66)

- **Service Configuration**: Define settings like CPU, memory, and optional environment variables.  
- Click **Deploy** to launch the service.

  ![Screenshot (56)](https://github.com/user-attachments/assets/5f097d27-6ecb-4ef8-9e01-1fdc680d695d)

![Screenshot (58)](https://github.com/user-attachments/assets/63b307e3-b36c-41e2-a559-e3c344d2b658)


---

### 5. Access the Hosted App  
- Once the service is deployed, AWS App Runner will provide a public URL.  
- Use this URL to access your hosted webpage.

  ![Screenshot (57)](https://github.com/user-attachments/assets/0f27b53e-fd26-4bad-b373-3d3d9ba718d5)


---

## Notes  
- Ensure to clean up resources after deployment to avoid unnecessary charges.  
- For additional details, refer to [AWS Documentation](https://aws.amazon.com/getting-started/guides/deploy-webapp-apprunner/).  

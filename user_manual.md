
# 🧑‍💻 User Manual: Deploying Your Application

This manual guides you step-by-step through the process of registering, logging in, deploying your application, and verifying access via the load balancer.

---

## 1. 📝 Create an Account

1. Navigate to the registration page.
2. Fill in your user details: name, email, and password.
3. Click on **Register**.

📷 Image of registration option

[Registration option](assets/images/r1.2.png)


---

## 2. 🔐 Log In

1. Go to the login page.
2. Enter your email and password.
3. Click on **Login**.

📷 Image of login screen here

[Login option](assets/images/r1.1.png)


---

## 3. 🚀 Go to the Deployment Section

1. Once logged in, navigate to the **Deploy** section from the main menu or dashboard.
2. Click on **New Deployment** or **Start Deployment**.

📷 Image of deployment section 

[Deployment Section](assets/images/d1.png)

[Deployment Section](assets/images/d1.1.png)


Extra: if you want to deploy the app and create an automatic repo in your GitHub account, please
use the following option to link to GitHub, and after return to the SpiderOps platform and finish the deployment.

[Deployment Section using GitHub linked account](assets/images/d.20.png)

---

## 4. 🧾 Fill Out Deployment Form

1. Enter the necessary fields such as:
    - Application name
    - GitHub repository link
    - Infraestructure type (e.g., standard)
2. Click on **Deploy**.

📷 Image of deployment form 

[Deployment Form step 1](assets/images/d1.2.png)

[Deployment Form step 2](assets/images/d1.3.png)

[Deployment Form step 3](assets/images/d1.4.png)

[Deployment Form step 4](assets/images/d.15.png)

---

## 5. ⏳ Wait for Deployment

- The deployment process takes approximately **15 minutes**.
- You may monitor logs or a progress bar if available.

📷 Image showing progress/loading status here

[Deployment Progress step 1](assets/images/d.16.png)

[Deployment Progress step 2](assets/images/d.17.png)

[Deployment Progress step 1](assets/images/d.18.png)

---

## 6. 🌐 Access Your Application via Load Balancer

1. Once the deployment is finished, go to the **Load Balancer** or **Access URL** section.
2. Copy the provided URL and open it in your browser.
3. You should see your application running.

📷 Image of access to the app's load balancer 

[Access App](assets/images/d.19.png)

---


Example of a deployed app

[Deployed App example](assets/images/d.21.png)


## 7. 🌐 Monitoring Your Application 

1. Once the deployment is finished, go to the **Monitoring option**.
2. Once here you can see all the monitoring logs.


📷 Image of monitoring app section 

[Monitoring App Logs](assets/images/m.1.png)

---


## 8. 🌐 Review The Quality of Your Application 

1. Once the deployment is finished, go to the **Quality option**.
2. Once here you can see all the quality metrics of each deployed apps.


📷 Image of quality app section 

[Quality of Apps](assets/images/q.1.png)

[Quality of Apps](assets/images/q.2.png)

[Quality of Apps](assets/images/q.3.png)

---

## 8. 🌐 Review The Security of Your Application 

1. Once the deployment is finished, go to the **Security option**.
2. Once here you can see all the security metrics, the scores ranges are from 0 to 100 points for fiability and security metrics.


📷 Image of security app section 

[Security of Apps](assets/images/s.1.png)



---


## ✅ Tips

- Ensure your GitHub repository is public or that you've linked your GitHub account with valid tokens.
- Deployment failures are usually related to invalid repo names or missing secrets.
- For advanced options, refer to the "Advanced Settings" tab during deployment.

---

Let us know if you encounter any issues! 🚀

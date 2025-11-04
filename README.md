# 🌐 Apigee Developer Portfolio

Welcome to my professional portfolio!  
I am an **Apigee Developer** with hands-on experience in **API design, development, and management** using **Google Apigee Hybrid** .
This portfolio showcases my projects, API gateway configurations, and best practices for secure and scalable API solutions.

---
## 👨‍💻 About Me

Hi, I’m **[Vishal Kumar Sharma]**, a passionate API engineer who loves building well-structured and secure API ecosystems.  
I specialize in creating, deploying, and managing APIs using **Apigee**, along with automation via **CI/CD pipelines**.

📍 **Location:** [Kolkata/Bangalore, INDIA]  
📧 **Email:** [vishal.k.sharma22@gmail.com]  
💼 **LinkedIn:** [https://linkedin.com/in/your-profile](https://linkedin.com/in/your-profile)  
💻 **GitHub:** [https://github.com/yourusername](https://github.com/yourusername)  
🌍 **Live Portfolio:** [https://yourusername.github.io/apigee-portfolio](https://yourusername.github.io/apigee-portfolio)

---

## 🧠 Technical Skills

| Category | Tools / Technologies |
|-----------|----------------------|
| **API Platforms** | Apigee Edge, Apigee X, Apigee Hybrid |
| **API Security** | OAuth 2.0, JWT, API Keys, Spike Arrest, Quota |
| **Dev Languages** | JavaScript, Node.js, Python |
| **DevOps & CI/CD** | Jenkins, GitHub Actions, Docker |
| **Documentation** | OpenAPI 3.0, Swagger, Postman |
| **Cloud** | Google Cloud Platform (GCP) |

---

## 🚀 Featured Projects

### 🛒 E-commerce API Gateway
**Goal:** Designed an API gateway for an e-commerce backend using Apigee Edge.  
**Highlights:**
- Created multiple API proxies for products, orders, and payments.
- Implemented **OAuth 2.0**, **Quota**, and **Caching** policies.
- Automated deployments using Jenkins and the Apigee Management API.  
**Repo / Docs:** [View Details →](projects/ecommerce-api.md)

---

### ☁️ Weather Data API
**Goal:** Built a weather data integration proxy on Apigee X using an external public API.  
**Highlights:**
- Configured Spike Arrest and Quota policies for API traffic control.  
- Enabled logging and message transformation policies.  
- Documented using **OpenAPI 3.0** and **Postman Collections**.  
**Repo / Docs:** [View Details →](projects/weather-api.md)

---

## 📄 API Documentation Samples

- [E-commerce API – Swagger Spec](docs/ecommerce-api.yaml)
- [Weather Data API – Swagger Spec](docs/weather-api.yaml)
- [Postman Collection (Sample)](https://www.postman.com/)

---

## 🧰 CI/CD & Automation

I’ve implemented automation pipelines for Apigee API proxy deployments using **Jenkins** and **GitHub Actions**, including:
- Automated export/import of proxies via Apigee Management API
- Deployment validation to `test` and `prod` environments
- Integration with Google Cloud Build for Apigee X

Example YAML snippet:

```yaml
name: Apigee Deploy
on: [push]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy to Apigee
        run: |
          npm install -g apigeetool
          apigeetool deployproxy -u ${{ secrets.APIGEE_USER }} -p ${{ secrets.APIGEE_PASS }} -o my-org -e test -n ecommerce-api -d ./apiproxy

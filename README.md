# 🌟 Azure AI Services on Containers: Professional Samples & Deployment Guide

![Azure Logo](img/logo.jpg)

Welcome to the **Azure AI Containers Samples** repository! This collection provides professional-grade examples, deployment instructions, and technical guidance for leveraging **Azure AI Services** in Docker containers. Run robust AI workloads anywhere—on-premises, in the cloud, or at the edge—with enterprise data governance and flexible scaling.

---

## 🗂️ Table of Contents

1. [👀 Overview: What are Containers?](#overview-what-are-containers)
2. [🤖 Azure AI Containers](#azure-ai-containers)
    - [🎯 Benefits](#benefits)
    - [✅ Supported Services](#supported-services)
    - [🔌 Connectivity Options](#connectivity-options)
3. [🚀 Deployment Options](#deployment-options)
    - [📦 Microsoft Container Registry](#microsoft-container-registry)
    - [🐋 Docker Setup](#docker-setup)
4. [🛠️ Installation Guide](#installation-guide)
5. [🔗 Reference Links](#reference-links)
6. [❓ FAQ](#faq)
7. [🎬 Sample Demos & Learning Resources](#sample-demos--learning-resources)
8. [📞 Contact](#contact)

---

## 👀 Overview: What are Containers?

A **container** is a portable, lightweight unit bundling an application and its dependencies. Containers abstract away infrastructure, allowing consistent deployment across OS/hardware environments.

- 🚚 **Portability:** Deploy on any platform—local, cloud, edge.
- 🏰 **Isolation:** Run securely and independently, side-by-side.
- ⚡ **Efficiency:** Minimal resource overhead, fast startup.
- 🗄️ **Centralized Management:** Discover & manage via registries (Docker Hub, Azure MCR).

---

## 🤖 Azure AI Containers

Azure AI containers deliver Microsoft Cognitive Services and Applied AI features through Docker images, allowing you to run workloads in the environment of your choice.

### 🎯 Benefits

- 🏎️ **Performance:** Low-latency, high throughput for real-time and bulk processing scenarios.
- 🔒 **Data Governance:** Keep data on-premises for maximum compliance (healthcare, finance, regulated verticals).
- 🌐 **Offline & Edge:** Operate in disconnected or remote scenarios; ideal for field and branch deployments.
- 🗂️ **Deployment Control:** Version and update containers at your own pace.

### ✅ Supported Services

See the latest [Azure AI Container Support Matrix](https://learn.microsoft.com/en-us/azure/ai-services/cognitive-services-container-support) for all supported services.

### 🔌 Connectivity Options

- **Connected Containers:**  
  Local data processing; telemetry and billing sent to Azure (pay-as-you-go).  
  ![Connected Architecture](img/arch1.jpg)

- **Disconnected Containers:**  
  Fully offline, annual prepaid license, no cloud connectivity.  
  ![Disconnected Architecture](img/arch2.jpg)

---

## 🚀 Deployment Options

You can run Azure AI containers in various orchestration environments:

- 🐋 **Docker Engine:** [Docs](https://docs.docker.com/)
- ☁️ **Azure Container Instances (ACI):** [Docs](https://learn.microsoft.com/en-us/azure/container-instances/)
- 🧩 **Azure Container Apps (serverless):** [Docs](https://learn.microsoft.com/en-us/azure/container-apps/overview)
- ⚙️ **Azure Kubernetes Service (AKS):** [Docs](https://learn.microsoft.com/en-us/azure/aks/)

### 📦 Microsoft Container Registry

Find official Azure AI images in [Microsoft Artifact Registry (MCR)](https://mcr.microsoft.com/en-us/catalog?search=AI&type=partial).

---

## 🐋 Docker Setup

**Essential Docker Commands:**

1. **⬇️ Pull the Container**
    ```sh
    docker pull mcr.microsoft.com/azure-cognitive-services/form-recognizer/layout-4.0
    ```
2. **▶️ Run the Container**
    ```sh
    docker run --rm -it -p 5000:5000 --memory 18g --cpus 8 \
    mcr.microsoft.com/azure-cognitive-services/form-recognizer/layout-4.0 \
    EULA=accept BILLING=https://<yourendpoint>.cognitiveservices.azure.com <API_KEY>
    ```
3. **🔍 Check Container Status**
    ![Container Running Localhost](img/containerlocalhost.jpg)

---

## 🛠️ Installation Guide

1. **📝 Prerequisites**
    - [Install Docker](https://docs.docker.com/get-docker/)
    - Active [Azure subscription](https://azure.microsoft.com/free/) & endpoint (for connected mode)
    - Sufficient hardware (per container requirements)

2. **🧲 Choose, Pull, and Run Container**
    - Select a service from the [Supported Containers list](https://learn.microsoft.com/en-us/azure/ai-services/cognitive-services-container-support)
    - Use sample commands above

3. **📊 Monitoring & Management**
    - Use Docker CLI or your container orchestration platform of choice

---

## 🔗 Reference Links

- [📖 Azure AI Containers Documentation](https://learn.microsoft.com/en-us/azure/cognitive-services/containers/)
- [🗄️ Register for Disconnected Containers](https://customervoice.microsoft.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR7en2Ais5pxKtso_Pz4b1_xUNDVVMVBPV09ITVBBR0E5T05QQ1VESFlSMCQlQCN0PWcu)
- [📦 Microsoft Container Registry (MCR)](https://mcr.microsoft.com/en-us/)
- [🐙 Microsoft on Docker Hub](https://hub.docker.com/u/microsoft)

---

## ❓ FAQ

- [💡 General Containers FAQ](https://learn.microsoft.com/en-us/azure/cognitive-services/containers/container-faq)
- [🔗 Disconnected Containers FAQ](https://learn.microsoft.com/en-us/azure/ai-services/containers/disconnected-container-faq)

---

## 🎬 Sample Demos & Learning Resources

- [🎥 Demo Videos](https://aka.ms/azureai-edge-demosvideos)
- [📚 Microsoft Learn: AI Containers Module](https://learn.microsoft.com/en-us/training/modules/investigate-container-for-use-with-ai-services/)
- [🧠 AI-KnowlEDGE Accelerator](https://github.com/Azure-Samples/AI-KnowlEDGE)
- [📈 Container Services Overview (PowerPoint)](https://github.com/retkowsky/azure-ai-containers-samples/blob/main/Azure%20AI%20services%20Containers.pdf)

---

## 📞 Contact

Serge Retkowsky  
📧 serge.retkowsky@microsoft.com  
[🔗 LinkedIn](https://www.linkedin.com/in/serger/)

_Last updated: April 10, 2025_

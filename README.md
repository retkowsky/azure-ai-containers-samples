# Azure AI services on containers samples
<img src="img/logo.jpg">

## 1. What is a container?
A container comprises an application or service and the runtime components needed to run it, while abstracting the underlying operating system and hardware. In practice, this abstraction results in two significant benefits:
- **Containers are portable across hosts**, which may be running different operating systems or use different hardware - making it easier to move an application and all its dependencies.
- A single container host can **support multiple isolated containers**, each with its own specific runtime configuration - making it easier to consolidate multiple applications that have different configuration requirement.

A container is encapsulated in a container image that defines the software and configuration it must support. Images can be stored in a central registry, such as Docker Hub, or you can maintain a set of images in your own registry.

## 2. Azure AI containers

- **Azure AI services provide several Docker containers** that let you use the same APIs that are available in **Azure, on-premises**. Using these containers gives you the flexibility to bring Azure AI services closer to your data for compliance, security or other operational reasons. Container support is currently available for a subset of Azure AI services.<br>
- Azure AI containers allow developers to use the same intelligent APIs that are available in Azure, but with the **benefits of containerization**.
Container services offer similar feature capabilities as the corresponding cloud service. **Customers can deploy the containers on-premise**. The core AI technology, pricing tiers, API keys, and API signature are the same between the container and the corresponding cloud services.

### 2.1 Advantages

**1. High Throughput & Low Latency**
Containers remove transaction limits, making them perfect for bulk processing, like digitising documents with OCR or analysing historical data.
Hosting containers close to your infrastructure reduces latency and improves speed.

**2. Control Over Data**
Azure ensures customer data is encrypted and isolated by region, but API calls may be temporarily stored for up to 48 hours.
Some industries, such as healthcare or finance, have strict regulations requiring all data to remain on-premises.

**3. Offline Mode or Reduced Bandwidth Usage**
In scenarios with limited or unstable internet access—like ships at sea or remote regions—containers offer critical offline functionality.
Containers are also suited for high-critical applications such as emergency services requiring real-time speech-to-text transcription.

**4. Customised Control**
Gain full control over updates and versioning. Containers offer version-controlled, isolated environments, giving flexibility over when and how updates are applied.
Containers can be created and removed dynamically.

### 2.2 List of Azure AI services containers
https://learn.microsoft.com/en-us/azure/ai-services/cognitive-services-container-support

## 2.3 Types of Containers
There are two types of container offerings: 
- **Connected containers:** keeps all the data processing locally but **send the billing data to the cloud so you are charged as you use the service**.
<br><img src="img/arch1.jpg"><br>
- **Disconnected containers:** enable you to use several of these APIs disconnected from the internet, with the customer making an **upfront payment for a year's worth of consumption** with no data sent to the cloud!
<br><img src="img/arch2.jpg"><br>

## 3. Container deployment
To use a container, you typically pull the container image from a registry and deploy it to a container host, specifying any required configuration settings. The container host can be in the cloud, in a private network, or on your local computer. For example:

- A Docker* server<br>
  https://docs.docker.com/
- An Azure Container Instance (ACI)<br>
  https://learn.microsoft.com/en-us/azure/container-instances/
- An Azure Container Apps (full serverless with scaling to 0)<br>
  https://learn.microsoft.com/en-us/azure/container-apps/overview
- An Azure Kubernetes Service (AKS) cluster<br>
  https://learn.microsoft.com/en-us/azure/container-apps/overview
  
*Docker is an open source solution for container development and management that includes a server engine that you can use to host containers. There are versions of the Docker server for common operating systems, including Microsoft Windows and Linux.

### 3.1 Microsoft Artifact Registry
<img src="img/mcr.jpg">
https://mcr.microsoft.com/en-us/catalog?search=AI&type=partial

### 3.2 Docker pull command
<img src="img/docker3.jpg">

### 3.3 Some docker images
<img src="img/docker1.jpg"><br>

### 3.4 Some docker containers
<img src="img/docker2.jpg"><br>

## 4. Connected container installation
1. Docker pull
```sh
docker pull mcr.microsoft.com/azure-cognitive-services/form-recognizer/layout-4.0
```
2. Docker run
```sh
docker run --rm -it -p 5000:5000 --memory 18g --cpus 8 mcr.microsoft.com/azure-cognitive-services/form-recognizer/layout-4.0 EULA=accept BILLING=https://<yourendpoint>.cognitiveservices.azure.com ApiKey=<yourAPIKey>
```
3. Container is available
<img src="img/containerlocalhost.jpg">
   
## 5. PowerPoint presentation
<a href="https://github.com/retkowsky/azure-ai-containers-samples/blob/main/Azure%20AI%20services%20Containers.pdf">PowerPoint document</a>

## 6. Documentation
- Azure AI Containers documentation<br>
https://learn.microsoft.com/en-us/azure/cognitive-services/containers/
- Application for Disconnected Containers<br>
https://customervoice.microsoft.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR7en2Ais5pxKtso_Pz4b1_xUNDVVMVBPV09ITVBBR0E5T05QQ1VESFlSMCQlQCN0PWcu
- Microsoft containers<br>
https://mcr.microsoft.com/en-us/<br>
https://hub.docker.com/u/microsoft

## 7. FAQ
- FAQ for Azure AI Containers<br>
https://learn.microsoft.com/en-us/azure/cognitive-services/containers/container-faq
- FAQ for Azure AI Disconnected containers<br>
https://learn.microsoft.com/en-us/azure/ai-services/containers/disconnected-container-faq

## 8. Demos videos
https://aka.ms/azureai-edge-demosvideos 

## 9. Training
https://learn.microsoft.com/en-us/training/modules/investigate-container-for-use-with-ai-services/

## 10. Accelerator
https://github.com/Azure-Samples/AI-KnowlEDGE

<br><br><br>
Serge Retkowsky | serge.retkowsky@microsoft.com | https://www.linkedin.com/in/serger/
<br><br>
Date of creation: 08-April-2025<br>
Updated: 10-April-2025

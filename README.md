# Container-Security

# What does Container Security mean?
- <b> Container security </b> is the process of using security tools to protect containers from cyber threats and vulnerabilities through the continous integration/continous delivery (CI/CD) pipeline.
- <b>  Container security </b> requires the security process to be continous.

- <b> Reminder </b> : Container is a package of software and its dependecies - such as code, system tools, settings, and libraries - that can run reliably on any operating systems and infrastructure.

# Why is Container Security important?
- Organizations have begun to recognize that security should be begin to the left in the appliaction development process. This concept of where security begins in the beggining of the development process is referred to as "shift left".
- Shift left security helps prevent vulnearbilities from being the entry point of a breach. 

# How to implement Container Security?
- Following container best practices
- Leveraging Enterprise tools

# What are Container Security best practices?
1. Image Scanning
2. Shift-left security
3. Runtime protection


# Image Scanning
- Container security starts with a secured container image. When developers spin up a container, they use a base image from an external registry to build their images, and these images can contain malware or vulnerable libraries.
- Developers also sometimes forget to remove passwords and secret keys used during development before pushing the image to the registry. If infrastructure is compromised, these passwords are leaked along with the images.
- This is why image scanning is critical. Scanning images before it can be utilized helps developers understand what images are secure to use.

🌎 Real World Analogy: </b>
- - Think of a container image like a seal shipping container arriving at a warehouse.
  - Inside the container:
  -  - Boxes (OS packages, libraries, runtimes)
     - Tools and equipment (frameworks, utilities)
     - Sometimes hidden contraband (known vulnerabilities, malware, hard-coded secrets)
   
<b> Image scanning </b> is like running the container or box in this scenario through customs + X - ray inspection before it's allowed into the warehouse (container registry) or put on a delivery truck.

# Security Benefit of Image Scanning 
- Scanning images early helps organizations
- Prevent known vulnerable images from ever being deployed
- Reduce attack surface before runtime.
- Helps developers find issues early during build, during PR, before deployment.
- Help developers fix issues early and not have to perform rework like rebuilding images, redeploying services, or performing emergency patching.



# Shift-left security
- Shift-left security is the concept of conducting security testing and practices in the earlier stages of the Software Development Cycle (SDLC), rather tahn waiting until the end.
- By integrating security from the very beginning, organizations find and fix vulnerablities sooner, which accelerates delivery, and reduces risk.


# Runtime protection
- To protect application data on a running container, it's important to get visibilty within container itself and its worker nodes.
- An effective container security tool should capture and correlate real-time activity and metadata from both containers and worker nodes.

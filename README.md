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
Scanning images early helps organizations: 
- Prevent known vulnerable images from ever being deployed
- Reduce attack surface before runtime.
- Helps developers find issues early during build, during PR, before deployment.
- Help developers fix issues early and not have to perform rework like rebuilding images, redeploying services, or performing emergency patching.



# Shift-left security
- Shift Left = move security earlier in the development cycle.
- Shift left means:
- 1. Scanning code
- 2. Scanning container images
- 3. Checking IaC templates
- 4. Enforcing policies before deployment
 
- Instead of:
- "We'll secure it after it's deployed in Production phase"

- Application teams will:
- "Let's catch issues before it ever runs in production"

- Left = earlier 
- Right = later (production/runtime)
- <img width="2000" height="1428" alt="image" src="https://github.com/user-attachments/assets/6cba5632-87b4-46a5-b012-e01e7b79288e" />


- Textbook definition of shift-left security = the concept of conducting security testing and practices in the <b> earlier stages </b> of the Software Development Cycle (SDLC), rather tahn waiting until the end.
- By integrating security from the very beginning, organizations find and fix vulnerablities sooner, which accelerates delivery, and reduces risk.


🌎 Real World Analogy: </b>

🚗 Car manufacturing analogy

1. Shift Left = inspecting parts during manufacturing
2. Runtime security = monitoring the car while driving on the road

Shift Left prevents:
- faulty brakes
- weak bolts
- missing airbags

Runtime security detects:
- engine overheating
- brake failure while driving
- someone hijacking the car

👉 Both are needed.


# What is Runtime?
- Runtime = where the container is actually running and doing work. Runtime means "container is alive"
- - processes are executing
- - network connections are happening
- - files are being read / written
- - APIs are being called
 
# What is Runtime security?
- Runtime security answers two questions:
- 1. What is the container doing right now?
- 2. Is it behaving normally or maliciously?

Examples:

1. A container spawning /bin/bash
2. A container making outbound calls to a crypto-mining IP
3. A container accessing /etc/shadow
4. A container escalating privileges
. A container suddenly opening a reverse shell

These are activities you CANNOT fully catch before runtime, because they depend on actual behavior.
  
- To protect application data on a running container, it's important to get visibilty within container itself and its worker nodes.
- An effective container security tool should capture and correlate real-time activity and metadata from both containers and worker nodes.

🌎 Real World Analogy: </b>

🏢 Office building analogy
- Container image = building blueprint
- Container runtime = people actively working in the building
- Runtime security = security guards + cameras inside the building

You can:

1. Inspect the blueprint beforehand (image scanning)
2. But only runtime security can catch:
- 2a. someone breaking into restricted rooms
- 2b. suspicious behavior after hours
- 2c. someone plugging in a rogue device

👉 Runtime security watches behavior, not just design.

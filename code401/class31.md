# Read : 31

## Django REST Framework & Docker

### Docker

- Docker is a set of platform as a service (PaaS) products that use OS-level virtualization to deliver software in packages called containers.

- Containers are isolated from one another and bundle their own software, libraries and configuration files; they can communicate with each other through well-defined channels.

- Because all of the containers share the services of a single operating system kernel, they use fewer resources than virtual machines.

- The service has both free and premium tiers. 

- The software that hosts the containers is called Docker Engine.

- It was first started in 2013 and is developed by Docker, Inc.

- **Docker Operation:**

    - Docker can package an application and its dependencies in a virtual container that can run on any Linux, Windows, or macOS computer. 
    - This enables the application to run in a variety of locations, such as on-premises, in a public cloud, and/or in a private cloud.
    - Because Docker containers are lightweight, a single server or virtual machine can run several containers simultaneously.
    - Docker implements a high-level API to provide lightweight containers that run processes in isolation.

### REST

- Representational state transfer *(REST)* is a software architectural style that was created to guide the design and development of the architecture for the World Wide Web. 

- REST defines a set of constraints for how the architecture of an Internet-scale distributed hypermedia system, such as the Web, should behave. 

- The REST architectural style emphasises the scalability of interactions between components, uniform interfaces, independent deployment of components, and the creation of a layered architecture to facilitate caching components to reduce user-perceived latency, enforce security, and encapsulate legacy systems.

- REST has been employed throughout the software industry and is a widely accepted set of guidelines for creating stateless, reliable web services. 

- Any web service that obeys the REST constraints is informally described as RESTful. 

- **Architectural properties:** The constraints of the REST architectural style affect the following architectural properties:

    - Performance in component interactions, which can be the dominant factor in user-perceived performance and network efficiency.
    - Scalability allowing the support of large numbers of components and interactions among components. 
    - Roy Fielding describes REST's effect on scalability as follows:
        - Simplicity of a uniform interface.
        - Modifiability of components to meet changing needs *(even while the application is running)*.
        - Visibility of communication between components by service agents.
        - Portability of components by moving program code with the data.
        - Reliability in the resistance to failure at the system level in the presence of failures within components, connectors, or data.

- **Six guiding constraints define a RESTful system:**
1. Client–server architecture.
2. Statelessness
3. Cacheability.
4. Layered system.
5. Code on demand *(optional)*.
6. Uniform interface.

##### [Go Back](code_401_reading_notes.md)
# Service Mesh

The term **service mesh** is often used to describe the network of microservices that make up such applications and the interactions between them. As a service mesh grows in size and complexity, it can become harder to understand and manage. Its requirements can include discovery, load balancing, failure recovery, metrics, and monitoring, and often more complex operational requirements such as A/B testing, canary releases, rate limiting, access control, and end-to-end authentication. - [Istio](https://istio.io/docs/concepts/what-is-istio/overview.html)

## The Goal

tl;dr: A service mesh is a dedicated infrastructure layer for making service-to-service communication safe, fast, and reliable. If you’re building a cloud native application, you need a service mesh. - [William Morgan](https://buoyant.io/2017/04/25/whats-a-service-mesh-and-why-do-i-need-one/)

## Mesh Solutions

Bouyant is credited with first term of Service Mesh, used with the Linkerd product this was more of an agnostic Mesh capable of different platforms and technologies (more hybrid cloud). Conduit is also a Bouyany product however it is focused solely on Kubernetes. Istio is also agnostic to a point, able to run in things other then K8's (Cloud Foundry, Nomad, Mesos, ect.) however it uses different proxy technologies then Conduit.

Aspenmesh is based off Istio with backing from F5, adding to it more granular pieces like a Mesh as a SaaS, and support.

- Linkerd (Buoyant)
- Conduit (Buoyant)
- Istio
- Aspenmesh (F5)

A cumulative list from the 4 different solutions about whats required in a Service Mesh, leaving duplicates we can see there is product overlap:

- Service discovery
- Load Balancing
- Failure Handling
- Instrumentation
- Routing of Services
- Traffic Management
- Observability
- Policy Enforcement
- Service Identity and Security
- Load balancing
- Fine-grained traffic policies
- Service discovery
- Service monitoring
- Tracing
- Routing
- Secure service to service communication
- Service Discovery			
- Intelligent Load Balancing			
- Request Routing			
- Circuit Breaking			
- Retries			
- Secure Communication			
- Distributed Tracing			
- Blue/Green Deployments			
- Service Authentication and Identification			
- Canary Testing			
- Sidecar			
- Prometheus Monitoring			
- Hosted SaaS			
- Unified Visibility and Insights Dashboard			
- Datastore			
- Alerting and Notification Service			
- Error and Warning Insights			
- Preemptive Failure Notification			
- Technical Support

## [Principles](http://agilemanifesto.org/)

Commonalities between the products start with participation in the [Cloud Native Computing Foundation](https://www.cncf.io/) this acts as a vender nutral home to work on solutions with a cloud focus.

All tools use a Proxy of some sort, they are used to form the Data Plane layer in which information is gathered and fed into the Control Plane, other things can feed into the Control Plane as well (like Consul in Istio for Service Discovery).

As the Data Plane is responsible for the moving of traffic, the Control Plane is responsible for upper level intelligence, "Is a service available, is a path functional, should this service be elevated into a secure connection, ect". The Control Plane can also provide more direct interaction, injecting the testing pieces called out as requirements, or Access Management as a service to service broker.

![alt text](https://cdn-images-1.medium.com/max/1600/1*CxrqPB-koBk3BhjnB3HDbA.png "Control Plane and Data Plane Players")

## Diagrams

#### - Linkerd
![alt text](https://buoyant.io/wp-content/uploads/2017/04/linkerd-service-mesh-diagram.png "Linkerd Architecture")

#### - Istio
![alt text](https://istio.io/docs/concepts/what-is-istio/img/overview/arch.svg "Istio Architecture")

## Training

- Linkerd - [Getting started guide](https://linkerd.io/getting-started/k8s/)
- Conduit - [Getting started guide](https://conduit.io/getting-started/)
- Istio - [Getting started guide](https://istio.io/docs/setup/kubernetes/quick-start.html)
- [Aspenmesh](http://blog.idonethis.com/two-pizza-team/)

## Notable articles


- [So what even is a Service Mesh? Hot take on Istio and Linkerd](http://redmonk.com/jgovernor/2017/05/31/so-what-even-is-a-service-mesh-hot-take-on-istio-and-linkerd/)
- [Conduit: A Lightweight Service Mesh for Kubernetes](https://thenewstack.io/conduit-lightweight-service-mesh-kubernetes/)
- [Kubernetes Service Mesh](https://akomljen.com/kubernetes-service-mesh/)
- [What’s a service mesh? And why do I need one?](https://buoyant.io/2017/04/25/whats-a-service-mesh-and-why-do-i-need-one/)
- [5 Microservices Trends to Watch in 2018](https://medium.com/memory-leak/5-microservices-trends-to-watch-in-2018-aed135f70e51)

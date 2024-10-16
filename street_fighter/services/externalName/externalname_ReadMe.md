#### The ExternalName service in Kubernetes is a specialized type of Service that allows you to map an in-cluster service name to an external hostname or IP address outside of your Kubernetes cluster.

#### This feature enables seamless integration between your Kubernetes applications and external services or resources, providing a bridge between your containerized workloads and the external environment.

#### The ExternalName service is particularly useful in scenarios where you need to access services hosted outside your Kubernetes cluster, migrate legacy applications to Kubernetes while maintaining dependencies on external systems, or create hybrid deployments where some components run in Kubernetes while others run on external systems.

#### By mapping an internal service name to an external resource, you can transparently access external services from within your Kubernetes applications, simplifying the integration process and enabling a smoother transition to a containerized environment.


### Use Cases
The ExternalName service is useful in the following scenarios:
1. Accessing external services: If you need to access a service that is hosted outside your Kubernetes cluster, you can use an
ExternalName service to map an internal service name to the external service's hostname or IP address.
2. Migrating to Kubernetes: When migrating an application to Kubernetes, you may have dependencies on external services that
cannot be moved to the cluster immediately. The ExternalName service allows you to maintain these dependencies while
gradually migrating the application to Kubernetes.
3. Hybrid deployments: If you have a hybrid deployment where some components run in Kubernetes and others run on external
systems, you can use ExternalName services to connect the in-cluster components to the external ones.



#### _By default no LB feature is not supported on externalName_
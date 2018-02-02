# Máster en Ciencia de Datos e Ingeniería de Computadores. Prácticas de BigData y Cloud Computing. Curso 2016-2017. 

![Header](https://sites.google.com/site/manuparra/home/headerdicits.png)

Manuel J. Parra Royón (manuelparra@decsai.ugr.es) &  José. M. Benítez Sánchez (j.m.benitez@decsai.ugr.es)

[UGR](http://www.ugr.es) | [DICITS](http://dicits.ugr.es) | [SCI2S](http://sci2s.ugr.es) | [DECSAI](http://decsai.ugr.es)



# Starting with OpenStack 

OpenStack enable two ways of interaction:

- Command line applications
  - Using [putty](http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) (from windows) or ssh command (from *NIX systems)
- Web Application
  - From your browser

# Introduction to OpenStack

OpenStack embraces a modular architecture to provide a set of core services that facilitates scalability and elasticity as core design tenets. This chapter briefly reviews OpenStack components, their use cases and security considerations.

![OS](https://docs.openstack.org/security-guide/_images/marketecture-diagram.png)

## Compute (Nova)

OpenStack Compute service (nova) provides services to support the management of virtual machine instances at scale, instances that host multi-tiered applications, dev or test environments, “Big Data” crunching Hadoop clusters, or high-performance computing.

The Compute service facilitates this management through an abstraction layer that interfaces with supported hypervisors (we address this later on in more detail).

Later in the guide, we focus generically on the virtualization stack as it relates to hypervisors.

For information about the current state of feature support, see OpenStack Hypervisor Support Matrix.

Compute security is critical for an OpenStack deployment. Hardening techniques should include support for strong instance isolation, secure communication between Compute sub-components, and resiliency of public-facing API endpoints.

## Object Storage (Swift)

The OpenStack Object Storage service (swift) provides support for storing and retrieving arbitrary data in the cloud. The Object Storage service provides both a native API and an Amazon Web Services S3-compatible API. The service provides a high degree of resiliency through data replication and can handle petabytes of data.

It is important to understand that object storage differs from traditional file system storage. Object storage is best used for static data such as media files (MP3s, images, or videos), virtual machine images, and backup files.

Object security should focus on access control and encryption of data in transit and at rest. Other concerns might relate to system abuse, illegal or malicious content storage, and cross-authentication attack vectors.

## Block Storage (Cinder)

The OpenStack Block Storage service (cinder) provides persistent block storage for compute instances. The Block Storage service is responsible for managing the life-cycle of block devices, from the creation and attachment of volumes to instances, to their release.

Security considerations for block storage are similar to that of object storage

## Network (Neutron)

The OpenStack Networking service (neutron, previously called quantum) provides various networking services to cloud users (tenants) such as IP address management, DNS, DHCP, load balancing, and security groups (network access rules, like firewall policies). This service provides a framework for software defined networking (SDN) that allows for pluggable integration with various networking solutions.

OpenStack Networking allows cloud tenants to manage their guest network configurations. Security concerns with the networking service include network traffic isolation, availability, integrity, and confidentiality.

## Dashboard (Horizon)

The OpenStack Dashboard (horizon) provides a web-based interface for both cloud administrators and cloud tenants. Using this interface, administrators and tenants can provision, manage, and monitor cloud resources. The dashboard is commonly deployed in a public-facing manner with all the usual security concerns of public web portals.

## Identity service (KeyStone)

The OpenStack Identity service (keystone) is a shared service that provides authentication and authorization services throughout the entire cloud infrastructure. The Identity service has pluggable support for multiple forms of authentication.

Security concerns with the Identity service include trust in authentication, the management of authorization tokens, and secure communication.

## Image service (Glance)
The OpenStack Image service (glance) provides disk-image management services, including image discovery, registration, and delivery services to the Compute service, as needed.

Trusted processes for managing the life cycle of disk images are required, as are all the previously mentioned issues with respect to data security.


## Data processing service (Sahara)

The Data Processing service (sahara) provides a platform for the provisioning, management, and usage of clusters running popular processing frameworks.

Security considerations for data processing should focus on data privacy and secure communications to provisioned clusters.





# Start session on OpenStack Horizon

Go to the website: https://atcstack.ugr.es/

and authenticate with your credentials:

´´´
domain: default
login:CD_XXXXXX
password: XXXXXXXX
´´´



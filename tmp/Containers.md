=4

<span>About me...</span>

Sysadmin & DevOp *@ National Research Council* FOSS Evangelist

<span>Agenda</span>

**Containerization and Cloud** - Why containerizing - Most relevant
technologies - Docker containers - Security and Isolation - Clouds stack
integration

<span>-</span> **Use Cases** - Continuous Integration - Cloud for Telco
- Tools to face Complexity - DEMO: LAMP on Swarm cluster

Containers and Cloud
====================

Containers: Why?
----------------

<span>People want!</span>

![image](images/olivetti_centro_studi_meccanica.png){width="\mylen"}

<span>-</span> **Companies $\rightarrow$ and run services on *human
errors prone* systems IT workers $\rightarrow$ plan and use the
*infrastructure*, , Users $\rightarrow$ fulfilling experience, don’t
want platforms**

<span>Epic Fail: </span>

**Under the hood: ASP.NET 2.0 + Windows + IIS + SQL Server**

<span>Modern Platform: End User Panel</span>

<span>Why containers?</span>

<span>-</span>

<span>Aims</span>

-   Shortest **Time To Market**

-   Pay only for used **resources**

-   **Easy** user experience

-   **Standard** and shareable technologies

<span>Why containers?</span>

<span>-</span>

<span>Features</span>

-   **Scalable** Infrastructure

-   **Orchestration**

-   Decentralization and **hybrid** architectures

-   Rapid **error prone** updates for app and infrastructure

What?
-----

<span>Containers</span>

<span>What can containers do?</span>

-   Environment optimized for

-   Fast with Continuous Integration. (dev/stag/prod)

-   Rapid **auto** deployment of

-   virtualization, **portability**

<span>Containers</span>

<span>What can containers do?</span>

-   High : 1 VM = dozens Containers

-   Only **User Data** as extra

-   Network, Computing and Storage

-   Containers: security by design

<span>Containers</span> **alternatives to VM, often running inside them.
**Google** uses containers to run its cloud services (Borg precursor).
Why?**

![image](images/containers_boat.png){width="\mylen"}

<span>-</span>

<span>*Containers and formats* alternatives:</span>

-   Docker

-   Rocket

-   LXD

-   Warden and Garden

-   Other …

<span>Containers: Rocket</span> **choice**

![image](images/rocket-logo.png){width="\mylen"}

<span>-</span>

<span>Key Features</span>

-   App Container Image: **self contained app** in signed/encrypted tgz

-   App Container Runtime: definition of the environment

-   App Container Discovery: a **federated** protocol for finding
    **images**

-   **Security** Focused

<span>Containers: LXD</span> **choice**

![image](images/lxd.png){width="\mylen"}

<span>-</span>

<span>Key Features</span>

-   **LXD**, “lxc” reinvented

-   Container running **on VM** space.

-   Metal as a Service, Juju

-   **Openstack integration** for container provisioning

<span>Containers: Warden and Garden</span> **choice**

![image](images/cloudfoundry.png){width="\mylen"}

<span>-</span>

<span>Key Features</span>

-   Warden, manager of container

-   Garden, platform-agnostic **Go API** management

-   Diego (Garden replacement)

<span>Containers: Docker</span> **choice**

![image](images/docker.png){width="\mylen"}

<span>-</span>

<span>Docker has been chosen by a wide range of players, some of them
are:</span>

-   *Docker implementation*:

    -   , *BlueMix*

    -   , *Triton*

    -   , *Openshift and Atomic Linux*

    -   , *Virtuozzo middleware*

    -   others:

Docker Standard
---------------

<span>What is ?</span>

From https://www.docker.com/what-docker

![image](images/whatisdocker.png){width="\mylen"}

<span>-</span>

<span>Containers</span> include **app and all** of dependencies, but
**share the kernel** with other containers. **Isolated** process in
**userspace** on the host. Docker containers **run on any** computer,
infrastructure or cloud.

<span>Containers: Docker</span> **The large consensus around is based on
its container and image format that is probable a standard-de-facto
solution. It’s modular architecture permits custom learning curve,
starting from the standalone daemon end extending to swarm clusters**

<span>Hype/r ?</span>

**Diffusion**

<span>Containers: Docker</span> **The is a version control system for
images and is another core component making this solution very useful.
It stores images for multpiple node deduplicating common data at early
stage. Nodes can point to local and public registries.**

<span>Containers: Docker</span>

![image](images/docker.png){width="\mylen"}

<span>-</span>

<span>Key Features</span>

-   Scriptable and clear

-   Docker image management,

-   Docker images are made by

-   Same layers are reused,

-   Oriented to application

<span>Containers: Docker</span>

![image](images/docker.png){width="\mylen"}

<span>-</span>

<span>Orchestration</span>

-   : CoreOS, Open Shift Origin …

    -   New Feature

    -   New Bugs

    -   Many Standards

-   : Open Shift, Bluemix, AWS …

    -   Stability

    -   Performance

    -   Lock in danger (in some case)

<span>Docker networking</span>

Clouds
------

<span>Containers: Big Companies </span>

<span>Who’s in?</span> Players running their services or offering them
on containers infrastructure

-   From the early beginning

-   -   -   -   -   Many others …

<span>Aims</span>

**Going to PaaS ad IaaS Integration**

<span>-</span>

<span>IT: Easy experience</span> Users Developers Sysadmin Manager

<span>Integration: </span>

<span>Integration: </span>

<span>Openstack and Openshift</span> **Openstack offers services to
containers infrastructure:**

-   Support *Openshift* templates (*Heat*)

-   Network Abstraction: with *Open vSwitch*

-   Load Balancing: with Layer4 healtchecks

-   Storage Abstraction: like *Cinder or Ceph*

-   Database Abstraction: used by *Heat and Openshift* templates

-   Orchestration: , , proprietary…

<span>Orchestration</span>

<span>Orchestration</span>

<span>**Kubernetes**</span> **Mature choice:** his power resides is in
the for manage **deployments**. A user declares the that should be
maintained for his own project.

<span>Kubernetes</span>

Use Cases
=========

Continuous Integration
----------------------

<span>Continuous Integration </span>

![image](images/dockerci.png){width="50.00000%"}

<span>Why Continuous Integration </span> **Helps maturity of code and
*Blue Green* deployment**
https://github.com/francescou/docker-continuous-deployment

![image](images/bgdeploy.png){width="60.00000%"}

<span>Containers & C.I. </span>

**Automation building system like can deploy images to**

<span>Microservices: Automation</span>

<span>Pipeline</span>

-   Gitlab and Subversion (sources)

-   Jenkins (buildmachine)

-   Maven (artifact repository)

-   Registry (container image repository)

<span>Sample: DIY Continuous Integration</span>

<span>Containers need: DevOps</span> **New IT character skilled both on
developing and systems administration**

![image](images/automation.png){width="\mylen"}

<span>-</span>

<span>**Developer and Sysadmin handshake**</span> To **complexity** and
**big numbers**!

-   scope of interest becomes broader (LOT of technologies)

-   Upgrade without interruption and error prone. ()

-   Sysadmin needs Developer’s procedural skills

-   Keyword: and

Cloud for Telco
---------------

<span>Opportunities</span> **Container Platforms permits**

![image](images/automation_gears.png){width="\mylen"}

<span>-</span>

-   infrastructure thanks to *abstraction and automation*

-   Extra to third party *Clouds*

-   Best for

-   -   still usable

<span>Opportunities</span> **Container Platforms permits**

![image](images/automation_gears.png){width="\mylen"}

<span>-</span>

-   Apps runs on

-   Upgrade without interruption or error deploy

-   service life cycle

-   

<span>Holistic approach</span>

![image](images/specialist_vs_generalist.png)

<span>Pets vs Cattle</span>

![image](images/pets_vs_cattle.png)

<span>IT challenges for Technicians</span>

<span>Habits to **Avoid**: </span>

-   (-) Server is a holy place but

-   (-) Environment

-   (-) of strategy for

-   (-) between teams

-   (-) Cooperation is

-   (-) . Expensive hardware

-   (-) Complexity increases

<span>-</span> ![image](images/specialist.png){width="0.3\mylen"}

<span>IT challenges for Technicians</span>

![image](images/generalist.png){width="\mylen"}

<span>-</span>

<span>Habits to **Acquire**: </span>

-   (+) in production

-   (+) Containers permits isolation,

-   (+) Use system and environment

-   (+) permit coral planning

-   (+) integrated in infrastructure

-   (+) . Commodity hardware

-   (+) Complexity increases

Tools to face Complexity
------------------------

<span>Tools, concepts</span>

<span>**Life easier with Automation and Orchestration!**</span>

-   Provisioning Bare Metal

-   Automation and planning

-   Abstraction from hardware (VMs!)

<span>Tools, Do It Yourself</span> **To face Complexity we need tools**

<span>Community driven</span>

-   Provisioning and configuration management:

    -   +

-   Automation and Planning

    -   +

-   Virtual Machine

    -   + +

<span>Tempest in a teapot</span>

![image](images/docker_ryu.png){width="40.00000%"}

<span>Docker Machine provision virtualbox VM with **swarm**</span>

-   docker-machine create -d virtualbox manager

-   docker-machine create -d virtualbox node1... 2... n

-   …

<span>Tools, concepts</span>

<span>**Life easier with Alerting tecnologies!**</span>

-   Hardware Life cycle management

-   Monitoring

-   Log Analysis

-   Context Separation (Prod, Stag, Dev)

<span>Tools, Do It Yourself</span>

<span>FOSS softwares</span>

-   Physical hardware **inventory**

    -   +

-   Discovery, **monitoring** metrics db

    -   +

-   Log service, parsing monitor and **alert**

    -   -   

DEMO: LAMP on Swarm cluster
---------------------------

<span>DEMO</span>

![image](images/demo.png){width="80.00000%"}

<span>Scenario</span>

![image](images/lamponswarm.png){width="85.00000%"}

**Thanks.\
Question Time**

**Questions?**

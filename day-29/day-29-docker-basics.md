Qus1. What is a container ?

Ans. A container is a lightweight, isolated environment that packages an application along with everything it needs to run, such as:

Application code
Libraries and dependencies
Runtime
Configuration files
Required system tools

**Ques2. Containers vs Virtual Machines — what's the real difference?**

Ans. A Virtual Machine virtualizes the entire operating system, while a container virtualizes/isolate applications while sharing the host OS kernel.
** Vitual Machine**
Physical Server
│
├── Hypervisor
│
├── VM 1
│   ├── Guest OS
│   └── Application
│
├── VM 2
│   ├── Guest OS
│   └── Application
│
└── VM 3
    ├── Guest OS
    └── Application

**Container :**

Physical Server
│
├── Host OS
│
├── Container Runtime (Docker)
│
├── Container 1
│   └── Application + Dependencies
│
├── Container 2
│   └── Application + Dependencies
│
└── Container 3
    └── Application + Dependencies

**Qus 3. What is the Docker architecture? (daemon, client, images, containers, registry)**

Ans.                 Docker Architecture

        ┌──────────────────────┐
        │    Docker Client     │
        │     (docker CLI)     │
        └──────────┬───────────┘
                   │
             Docker API
                   │
                   ▼
        ┌──────────────────────┐
        │    Docker Daemon     │
        │      (dockerd)       │
        └──────────┬───────────┘
                   │
          ┌────────┴─────────┐
          │                  │
          ▼                  ▼
     Docker Images      Containers
          │
          │
          ▼
    Docker Registry
   (Docker Hub / ECR)

   The Docker Client is what you interact with using commands such as: docker run

   The Docker daemon is the main background service that actually performs Docker operations. Client sends the request; daemon does the work.

   A Docker image is a read-only package/template used to create containers.

   A container is a running instance of a Docker image.

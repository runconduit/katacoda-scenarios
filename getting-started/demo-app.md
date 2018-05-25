Finally, it’s time to install a demo application and add it to the service mesh.

Fetch the demo, add conduit to it and apply to your cluster:

`wget  https://raw.githubusercontent.com/runconduit/conduit-examples/master/emojivoto/emojivoto.yml`{{execute}}

`cat emojivoto.yml | conduit inject - > conduit-emojivoto.yml`{{execute}}

`cat conduit-emojivoto.yml | kubectl apply -f -`{{execute}}

These commands download the Kubernetes config for an example gRPC application where users can vote for their favorite emoji, then runs the config through `conduit inject`. The config has the Conduit data plane proxies injected as sidecar containers in the demo's pods. `kubectl` takes care of applying this configuration to your cluster.

As with `conduit install`, in this command, the Conduit CLI is simply doing text transformations, with `kubectl` doing the heavy lifting of actually applying config to the Kubernetes cluster.

The pattern of injecting conduit's configuration in this matter is convenient because you can introduce additional filters into the pipeline, or run the commands separately and inspect the output of each one.

Take a look at what's actually happening by running a diff on the before and after:

`git diff --no-index -- emojivoto.yml conduit-emojivoto.yml`{{execute}}

At this point, you should have an application running on your Kubernetes cluster, and (unbeknownst to it!) also added to the Conduit service mesh.

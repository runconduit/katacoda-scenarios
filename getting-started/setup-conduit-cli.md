As this is your first time running Conduit, you’ll need to download the command-line interface (CLI) onto your local machine. You’ll then use this CLI to install Conduit on a Kubernetes cluster.

`curl https://run.conduit.io/install | sh`{{execute}}

Next, add conduit to your path with:

`export PATH=$PATH:$HOME/.conduit/bin`{{execute}}

Verify the CLI is installed and running correctly with:

`conduit version`{{execute}}

With `Server version: unavailable`, don’t worry, we haven’t added the control plane… yet.

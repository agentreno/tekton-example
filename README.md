# tekton-example

## Setup

Tested with Minikube.

As per Tekton docs, install Tekton itself:

```
kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
```

Create the PersistentVolume it needs:

`kc apply -f persistent-volume.yaml`

Install Tekton CLI:

https://tekton.dev/docs/getting-started/#set-up-the-cli

## Running pipelines

`kc apply -f hello-world/task-hello.yaml hello-world/pipeline-hello.yaml`

`kc create -f hello-world/taskrun-hello.yaml` and observe logs.

`kc create -f hello-world/pipelinerun-hello.yaml`



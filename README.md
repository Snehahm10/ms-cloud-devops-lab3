# Lab 3 — hello-app on Kubernetes with Terraform

Name:

Roll number:

## Part 1: Write it in Terraform

### Terraform Initialization and Validation

- Successfully initialized Terraform using the Kubernetes provider (v3.4.0).
- Executed `terraform fmt` to format the configuration.
- Executed `terraform validate` and confirmed that the configuration is valid.

### Terraform Plan

The execution plan generated the following result:

```text
Plan: 2 to add, 0 to change, 0 to destroy.
```

Resources planned:
1. Kubernetes Deployment – `hello-app` with 3 replicas.
2. Kubernetes Service – `hello-app` with LoadBalancer type.

**Kubernetes Namespace:** default

## Part 1: `terraform output -raw url`

http://localhost:8080

## Part 2: plan for the v1 → v2 image change


image = "shripada/hello-app:v1" -> "shripada/hello-app:v2"

Plan: 0 to add, 1 to change, 0 to destroy.
## Part 3: plan that found the drift after `kubectl scale`
replicas = "5" -> "3"

Plan: 0 to add, 1 to change, 0 to destroy.

## Part 4: `kubectl get svc -A` showing dev and prod

```

```

## Break it: the error after deleting `terraform.tfstate`

```

```

## Break it: the wrong selector

What did you see, and how did you find the cause? One or two sentences.



## Screenshot

Save a browser screenshot as `screenshot.png` in the repository root.

# Lab 3 — hello-app on Kubernetes with Terraform

**Name:** Sneha HM  
**Roll number:** 261100680032

---

## Part 1: Write It in Terraform

### 1.1 Terraform Initialization and Validation

- Successfully initialized Terraform using the Kubernetes provider (v3.4.0).
- Executed `terraform fmt` to format the configuration.
- Executed `terraform validate` and confirmed that the configuration is valid.

### 1.2 Terraform Plan

The execution plan generated the following result:

```text
Plan: 2 to add, 0 to change, 0 to destroy.
```

**Resources planned:**

1. Kubernetes Deployment – `hello-app` with 3 replicas.
2. Kubernetes Service – `hello-app` with LoadBalancer type.

**Kubernetes Namespace:** `default`

### 1.3 Terraform Apply and Verification

- Successfully created the Kubernetes Deployment and Service using Terraform.
- Verified that 3 application Pods were running.
- Accessed the application through the browser using the generated URL.

**Terraform Output:**

```text
http://localhost:8080
```

- Executed `terraform apply` again to verify idempotency.
- Confirmed that Terraform reported no changes because the infrastructure already matched the configuration.

---

## Part 2: Update the Application Image from v1 to v2

Updated the application image in the Terraform configuration from `v1` to `v2`.

**Image change:**

```text
image = "shripada/hello-app:v1"
       ->
image = "shripada/hello-app:v2"
```

**Terraform Plan Result:**

```text
Plan: 0 to add, 1 to change, 0 to destroy.
```

- Terraform detected the image change and proposed an in-place update.
- Executed `terraform apply` to apply the updated configuration.
- Successfully deployed the v2 image.
- Verified the updated application in the browser.

---

## Part 3: Detect and Correct Configuration Drift

### 3.1 Manually Introduce Configuration Drift

Manually scaled the Kubernetes Deployment from 3 replicas to 5 replicas using:

```bash
kubectl scale deployment hello-app --replicas=5
```

### 3.2 Detect Drift Using Terraform

Executed `terraform plan` to
```

## Break it: the error after deleting `terraform.tfstate`

```

```

## Break it: the wrong selector

What did you see, and how did you find the cause? One or two sentences.



## Screenshot

Save a browser screenshot as `screenshot.png` in the repository root.

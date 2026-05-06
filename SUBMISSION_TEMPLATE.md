<div align="center">

# PA4 Submission: TaskFlow Pipeline

<img alt="GitHub only" src="https://img.shields.io/badge/Submit-GitHub%20URL%20Only-10b981?style=for-the-badge">
<img alt="Total points" src="https://img.shields.io/badge/Total-100%20points-7c3aed?style=for-the-badge">

</div>

<div style="background:#f5f3ff;color:#111827;border-left:6px solid #6330bc;padding:14px 18px;border-radius:10px;margin:18px 0;">
Copy this file to <code style="color:#111827;background:#ddd6fe;padding:2px 4px;border-radius:4px;">SUBMISSION.md</code>. Put every screenshot in <code style="color:#111827;background:#ddd6fe;padding:2px 4px;border-radius:4px;">docs/</code>, embed it under the correct task, and write a short description below each image explaining what it proves. The grader should not need any file outside this repository.
</div>

## Student Information

| Field | Value |
|---|---|
| Name | TODO |
| Roll Number | TODO |
| GitHub Repository URL | TODO |
| Resource Group | `rg-sp26-TODO` |
| Assigned Region | TODO: `uaenorth` or `ukwest` |

## Evidence Rules

- Use relative image paths, for example: `![AKS nodes](docs/aks-nodes.png)`.
- Every image must have a 1-3 sentence description below it.
- Azure Portal screenshots must show the resource name and enough page context to identify the service.
- CLI screenshots must show the command and output.
- Mask secrets such as function keys, ACR passwords, and storage connection strings.


## Task 1: App Service Web App (15 points)

### Evidence 1.1: Forked Repository

TODO: Embed screenshot of your forked GitHub repository.

Description: TODO: Explain that this is your working fork and that it contains the PA4 starter structure.
<img width="975" height="701" alt="image" src="https://github.com/user-attachments/assets/24b81357-ab54-483a-affc-00abe9ddc433" />

### Evidence 1.2: App Service Overview

TODO: Embed screenshot of the Web App overview page showing `webapp-<rollnum>` and Running status.
<img width="975" height="701" alt="image" src="https://github.com/user-attachments/assets/9212b59d-d442-4260-a580-76a13e0bb3d0" />

Description: TODO: State the resource group, region, runtime, and public URL.

### Evidence 1.3: Deployment Center / GitHub Actions
<img width="975" height="701" alt="image" src="https://github.com/user-attachments/assets/c39035b5-3f66-49c9-8f7a-f5d47ec27540" />

TODO: Embed screenshot of Deployment Center or the successful GitHub Actions deployment.

Description: TODO: Explain how the Web App is connected to your GitHub fork.

### Evidence 1.4: Live Web UI
<img width="975" height="701" alt="image" src="https://github.com/user-attachments/assets/46318511-b4b8-4868-98f9-bd9a026eb495" />

TODO: Embed screenshot of the TaskFlow page loaded in a browser.

Description: TODO: Explain that the App Service is serving the frontend successfully.

---

## Task 2: Azure Container Registry (15 points)

### Evidence 2.1: ACR Overview

TODO: Embed screenshot of `crpa4<rollnum>` overview.
<img width="911" height="800" alt="image" src="https://github.com/user-attachments/assets/9a6f9a1a-9c1a-4a26-9011-e7284189cde9" />

Description: TODO: Identify the registry SKU and resource group.

### Evidence 2.2: Docker Builds
<img width="911" height="800" alt="image" src="https://github.com/user-attachments/assets/7a299498-e113-4667-917b-60033cb5953f" />

TODO: Embed screenshot showing successful local builds for `validate-api`, `report-job`, and `func-app`.

Description: TODO: Explain which folder produced each image.

### Evidence 2.3: ACR Repositories
<img width="9<img width="975" height="805" alt="image" src="https://github.com/user-attachments/assets/8fe1eda8-28c2-4c1f-931a-70d9a6510eef" />
75" height="805" alt="image" src="https://github.com/user-attachments/assets/dd4cd93c-574c-47f9-9c4e-4fcf87a9c22d" />

TODO: Embed screenshot or CLI output showing all three repositories in ACR.

Description: TODO: Confirm `validate-api:v1`, `report-job:v1`, and `func-app:v1` were pushed.

---

## Task 3: Durable Function Implementation (12 points)

### Evidence 3.1: Completed Function Code

TODO: Link to your completed file: `[function_app.py](function-app/function_app.py)`.

Description: TODO: Summarize how your orchestrator chains validation and report generation.

### Evidence 3.2: Local Function Handler Listing

TODO: Embed screenshot of `func start` showing the HTTP starter, orchestrator, and activities.
<img width="975" height="805" alt="image" src="https://github.com/user-attachments/assets/7f6bb1bf-3090-4341-9120-c0c1a8ff4636" />

Description: TODO: Explain that the Durable Functions runtime discovered your handlers.

---

## Task 4: Function App Container Deployment (8 points)

### Evidence 4.1: Function App Container Configuration

TODO: Embed screenshot showing the Function App uses your `func-app:v1` image from ACR.
<img width="975" height="805" alt="image" src="https://github.com/user-attachments/assets/7e86d972-1540-4363-a512-dcb232098b03" />

Description: TODO: State the Function App name and image URI.

### Evidence 4.2: Orchestration Smoke Test

TODO: Embed screenshot of the `curl` output that starts an orchestration and returns status URLs.

Description: TODO: Explain what the returned `id` and `statusQueryGetUri` prove.
<img width="975" height="805" alt="image" src="https://github.com/user-attachments/assets/306c0157-6ebc-4064-9056-6b96216e201c" />

### Evidence 4.3: Expected Failed Status Before Downstream Wiring

TODO: Embed screenshot of the status query JSON showing the expected failure before `VALIDATE_URL` is configured.
<img width="975" height="805" alt="image" src="https://github.com/user-attachments/assets/d2db11f9-66be-4332-912d-5c068fd65d29" />
<img width="975" height="805" alt="image" src="https://github.com/user-attachments/assets/9e7cac3b-6bad-46f4-b130-4d9fa706cc8d" />

Description: TODO: Explain why this failure is expected at this stage.

---

## Task 5: AKS Validator (15 points)

### Evidence 5.1: AKS Cluster
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/46558fd6-799c-4272-b77c-3dd2fc234c81" />
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/8dc51b4c-17ca-424e-9941-9ccb76b08863" />
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/684568b4-d31a-4706-a557-c26363bd101d" />

TODO: Embed screenshot of AKS overview showing `aks-<rollnum>` succeeded.

Description: TODO: State node count, node size, region, and resource group.

### Evidence 5.2: Kubernetes Nodes and Pods

TODO: Embed screenshot of `kubectl get nodes` and `kubectl get pods`.
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/9441edd4-14e6-4531-ad47-e7a172304a3c" />

Description: TODO: Explain that the validator pod is scheduled and running.

### Evidence 5.3: Kubernetes Service

TODO: Embed screenshot of `kubectl get service validate-service`.
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/5e5cc133-a404-4499-bf79-570f54557c86" />

Description: TODO: Identify the external IP and port exposed by the LoadBalancer.

### Evidence 5.4: Validator API Tests

TODO: Embed screenshot of `curl /health`, a valid `curl /validate`, and an invalid `curl /validate`.

Description: TODO: Explain the accepted path and the `qty > 100` rejection rule.

### Evidence 5.5: Function App `VALIDATE_URL`

TODO: Embed screenshot showing the Function App application setting `VALIDATE_URL`.

Description: TODO: Explain how the Durable Function reaches the AKS validator.

### Evidence 5.6: AKS Idle Behavior

TODO: Embed AKS metrics screenshot and/or `kubectl` output after the service is idle.

Description: TODO: Explain that the AKS node remains running even when there are no orders.

---

## Task 6: ACI Report Job (15 points)
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/a9b066c5-f1b9-4a82-852e-5e635d7aeff9" />
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/d64479ba-0d89-433f-9518-1ba5074ccf58" />
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/61a95c9d-dd83-4e70-b4c6-2c6c3f96ec76" />
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/996fd382-35bf-4010-a23c-ea6c85b87d59" />

### Evidence 6.1:<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/19263cd2-85e0-4cc0-950e-03852c3f65e6" />
 Blob Container

TODO: Embed screenshot of the `reports` blob container.

Description: TODO: Explain where generated PDFs are stored.

### Evidence 6.2: Manual ACI Run

TODO: Embed screenshot of `az container show` for `ci-report-test`.

Description: TODO: State the final container state and why the job exits.

### Evidence 6.3: ACI Logs

TODO: Embed screenshot of `az container logs`.

Description: TODO: Explain what the report job printed after generating and uploading the PDF.

### Evidence 6.4: Generated PDF

TODO: Embed screenshot showing `TEST-001.pdf` in Blob Storage or opened from Blob Storage.

Description: TODO: Explain how this proves the ACI wrote to storage.

### Evidence 6.5: Function App Managed Identity and IAM

TODO: Embed screenshots of system-assigned identity enabled and Contributor role assignment on your resource group.

Description: TODO: Explain why the Function App needs this permission to create ACIs.

### Evidence 6.6: Report App Settings

TODO: Embed screenshot of `REPORT_*`, `ACR_*`, `STORAGE_CONN`, and `SUBSCRIPTION_ID` settings.

Description: TODO: Explain what each group of settings is used for. Mask secrets.

---

## Task 7: End-to-End Pipeline (15 points)

### Evidence 7.1: Web App Wiring

TODO: Embed screenshot showing `FUNCTION_START_URL` and `FUNCTION_STATUS_URL` configured on the Web App.

Description: TODO: Explain how the frontend starts and polls the Durable orchestration.

### Evidence 7.2: Happy Path UI

TODO: Embed screenshots of the form before submit, Running status, and Completed status with report URL.

Description: TODO: Explain the valid order payload and final result.

### Evidence 7.3: Backend Participation

TODO: Embed screenshots showing Function App invocation, AKS validator evidence, ACI evidence, and Blob PDF evidence.

Description: TODO: Trace the same order ID across services.

### Evidence 7.4: Reject Path UI

TODO: Embed screenshot of an order with `qty > 100` being rejected.

Description: TODO: Explain why no report ACI should be created for this order.

---

## Task 8: Write-up and Architecture Diagram (5 points)

### Evidence 8.1: Architecture Diagram
<img width="797" height="119" alt="image" src="https://github.com/user-attachments/assets/f9df8d75-344f-4f69-bd1b-35a911f483bb" />

TODO: Embed your architecture diagram from `docs/`.

Description: TODO: Confirm that it shows GitHub, App Service, Durable Function, AKS, ACI, Blob Storage, ACR, and IAM.

1. Service Selection: Why These Tools?
App Service (Web App): We chose App Service for the frontend because it provides a fully managed environment for long-running web interfaces with built-in CI/CD. It handles scaling automatically and keeps the UI accessible without us managing the underlying server. For this role, a Basic (B1) tier is cost-effective, providing a stable endpoint for users to submit orders.
Durable Functions: This is the "brain" that coordinates the pipeline. It is the right tool because it can handle long-running processes (like waiting a minute for a report) without timing out, unlike standard functions. It uses a stateful operational model, meaning it remembers exactly where it is in the process even if the system restarts.
Azure Kubernetes Service (AKS): We used AKS for the validator because it is designed for long-lived microservices that need high availability. Even with just one node (Standard_B2s), it provides enterprise-grade orchestration and declarative management. It stays "warm" to respond instantly to every validation request.
Azure Container Instances (ACI): ACI is perfect for the report job because it follows a "per-run" cost model. It starts, does the work (generating a PDF), and then deletes itself immediately. This avoids idle costs, making it significantly cheaper than keeping a dedicated server running for a task that only happens occasionally.

2. ACI vs. AKS: Hands-on Comparison
AKS at Idle: When AKS is idle for 10 minutes, the cluster remains fully active. The node is still running, and you are still being billed for the compute power. Because it is a "long-lived" service, it stays ready to handle traffic instantly, regardless of whether orders are coming in.
ACI at Idle: In this pipeline, "idle" for ACI means the resource does not exist. We only create the container when an order is validated. Therefore, during idle periods, ACI costs $0.
The Spam Scenario: If a user submits 1,000 orders in a minute, ACI would incur the most cost. While the AKS cost is capped by the fixed price of the node, ACI would spin up 1,000 separate instances. Since ACI bills per second of execution, a massive spike in usage leads to a massive spike in cost.

3. Durable Functions: Why Not Just HTTP?
Using plain HTTP functions for this pipeline would be very risky. First, standard HTTP functions have timeout limits (often 5–10 minutes); if the report generation or ACI creation took too long, the function might die, leaving the user with no result. Second, plain functions lack built-in state persistence. If a standard function failed halfway through, you would have to manually track which orders were validated but not reported. Durable Functions solve this by "checkpointing" progress, allowing for automatic retries and long-term state management without losing data.

4. Cost Review
Estimated Consumption: Based on the one-week development cycle, the total consumption is approximately $15–$20 USD.
Most Expensive Resource: The AKS Cluster (Standard_B2s node) is the single most expensive item. Even though it is a small node, the fact that it runs 24/7 makes its cumulative cost higher than the ephemeral ACI jobs or the Basic App Service plan.

5. Challenges Faced
Managed Identity Permissions: Initially, the Function App was failing to create the ACI (403 Forbidden). I realized that while I had attached the Managed Identity, the role assignment in Azure takes a few minutes to propagate. I debugged this by checking the Activity Logs in the Resource Group, which showed the "Authorization" failure.
ACR Pull Errors in AKS: My validator pod was stuck in ImagePullBackOff. I discovered that because I couldn't use managed identities for the ACR-AKS link, I had to manually create a Kubernetes Secret (acr-secret) with the ACR admin keys. I used kubectl describe pod to see the exact error message that pointed to the authentication failure.



---

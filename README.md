# job-lease-keeper
Job Lease Keeper to cleanup after configurable time



### Deploying Job Lease Keeper

```
kubectl apply -f https://raw.githubusercontent.com/kube-sailmaker/job-lease-keeper/0.1/deploy/job_controller.yaml
kubectl apply -f https://raw.githubusercontent.com/kube-sailmaker/job-lease-keeper/0.1/deploy/job_role.yaml
kubectl apply -f https://raw.githubusercontent.com/kube-sailmaker/job-lease-keeper/0.1/deploy/job_sa.yaml
kubectl apply -f https://raw.githubusercontent.com/kube-sailmaker/job-lease-keeper/0.1/deploy/job_role_binding.yaml
```

### Configuration

The following environment variables can be configured:

|Environment|Description|
|-----------|-----------|
|JOBS_NAMESPACE |namespace to clean jobs from|
|JOBS_COMPLETION_THRESHOLD_MINUTES|minimum number of minutes to wait before cleaning a finished job |
|CHECK_FREQUENCY_MINUTES |frequency at which the check should be performed |


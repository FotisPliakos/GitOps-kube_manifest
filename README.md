

## Synopsis
- When CircleCI notices any changes in the application code, it executes the jobs we have set up. There are a total of four jobs:

### Test: 
- This job tests the code. After the test job is completed, CircleCI proceeds to the next job. 
- Note: I didn't add this job to save time. 

### Build: 
- In the build job, CircleCI pulls the base Docker images and packages our application code inside the image.

### Push: 
- The push job pushes the newly generated images to Docker Hub with a new tag.

### Update Manifest: 
- After completing the push job, the last job is executed, which updates the Kubernetes manifest repository with the new tag. This enables ArgoCD to detect the change and apply it to the cluster.

Following this pipeline ensures that our application code is thoroughly tested, built into Docker images, and deployed with the updated manifest using the GitOps approach.

**This project contains Three GitHub repositories**

➡️ [App Code] (https://github.com/piyushsachdeva/AppCode)

➡️ [Terraform code] (https://github.com/piyushsachdeva/10weeksofcloudops-week4-tf)

➡️ [Manifest Repo] (https://github.com/piyushsachdeva/kube_manifest)

🙏 Thank you so much for reading.

Steps to Update a Container’s Image with Zero Downtime
Ensure the Deployment is Configured for Rolling Updates

First, make sure your Deployment's update strategy is set to RollingUpdate, which is the default behavior. This ensures that Kubernetes will update the pods incrementally, maintaining availability.

Update the Container Image

Use kubectl to update the container image in the Deployment. This involves changing the image tag in the Deployment specification.


kubectl set image deployment/your-deployment your-container=your-image:new-tag

Monitor the Rolling Update

Check the status of the update using:

kubectl rollout status deployment/your-deployment
This command will provide information on the progress of the update. Ensure it reports that the rollout is complete and successful.

Verify the Update

After the update completes, verify that the new pods are running correctly. Check the status of your pods:

kubectl get pods-n namespace 
Ensure that the new pods are in the Running state and that there are no errors.
All pod should be runnings Status and having traffic ..to check the Traffic we can see KPI as in telecom we use to check the KPI

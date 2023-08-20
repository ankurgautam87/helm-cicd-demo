# helm-cicd-demo

This code has been written to demonstrate creating a automated CICD pipeline for GKE cluster using Helm, Google Cloud Deploy and Google Cloud Build.

Change the following files before creating a Cloud Build trigger

1. cloudbuild.yaml - add cluster locaiton/zone.
2. deploy/dev.yaml, prod.yaml, staging.yaml and edit the location of the cluster.

You can then run the following command from the root folder of the project

    gcloud builds submit --region=<zone> --config cloudbuild.yaml \
    --repo=<repository-name> \
    --branch-pattern="main" \

Please make sure your repository is already connected with your GCP project.

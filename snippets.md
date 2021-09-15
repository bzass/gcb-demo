

cloud-build-local --dryrun=false .

docker run --rm -d --name gcb-demo -p 80:80 gcr.io/bzass-demo-306413/gcb-demo

curl localhost

gcloud builds submit --config cloudbuild.yaml


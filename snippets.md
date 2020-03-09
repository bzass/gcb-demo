

cloud-build-local --dryrun=false .

docker run --rm -d --name gcb-demo -p 80:80 gcr.io/bzass-demo/gcb-demo

curl localhost

gcloud builds submit --config cloudbuild.yaml


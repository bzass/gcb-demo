gcloud config set project bzass-demo
gcloud auth configure-docker
--

cloud-build-local --dryrun=false .

docker run --rm -d --name gcb-demo -p 80:80 gcr.io/bzass-demo-306413/gcb-demo

curl localhost

gcloud builds submit --config cloudbuild.yaml

--
git commit -m "Changes in Dockerfile"

docker stop gcb-demo

docker rm gcb-demo

docker rmi gcr.io/bzass-demo/gcb-demo
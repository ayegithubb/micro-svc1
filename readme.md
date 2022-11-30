CI:
dockerbuild:
    aws ecr login | docker login
    dockerbuild -t ecrrepourl:tag
    docker push ecrrepourl:tag
CD:
kubectl apply -f deployment.yaml services.yaml ingress.yaml    
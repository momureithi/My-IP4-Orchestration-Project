# Git Workflow

#### Clone the repository

```git clone https://github.com/momureithi/My-IP4-Orchestration-Project```

#### Switch to the `My-IP4-Orchestration-Project` directory

```cd My-IP4-Orchestration-Project```

#### Create directory to store the manifest files

```mkdir manifests```

#### Add required manifests to the created directory

```touch deployment.yaml```
```touch pv.yaml```
```touch pvc.yaml```
```touch service.yaml```


#### Commit changes and push to the remote repository:

```git add .```
```git commit -m``` "Add manifests"
```git push origin master```

#### Deploy application using kubectl:

```kubectl apply -f deployment.yaml```
```kubectl apply -f pv.yaml```
```kubectl apply -f pvc.yaml```
```kubectl apply -f service.yaml```

Access your application at the specified IP address and port.

#### Docker image tag naming standards and semver:

```docker build -t momureithi/my-ip4-frontend-image:v0.1.0 .```

#### Push the image to a container registry:

```docker push momureithi/my-ip4-frontend-image:v0.1.0```
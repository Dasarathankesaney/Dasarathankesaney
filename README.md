apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
  namespace: test1
  labels:
    app: nginx
    type: dev
spec:
# spec for the desired state
  containers:
    - name: nginx
      image: nginx
      imagePullPolicy: IfNotPresent
      ports:
        - containerPort: 80

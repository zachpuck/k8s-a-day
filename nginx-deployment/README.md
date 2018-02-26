run the following command to create the configmap:
`kubectl create configmap nginx-conf --from-file=./nginx-deployment/test.conf`

results of configmap in k8s:

```
apiVersion: v1
data:
  test.conf: "location /some/path/ {\r\n    proxy_pass http://www.example.com/link/;\r\n}"
kind: ConfigMap
metadata:
  creationTimestamp: 2018-02-20T07:05:57Z
  name: nginx-conf
  namespace: default
  resourceVersion: "993013"
  selfLink: /api/v1/namespaces/default/configmaps/nginx-conf
  uid: 7ffd3434-180c-11e8-95e8-52540084ed8b
```
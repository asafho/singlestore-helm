https://docs.singlestore.com/db/v7.8/en/deploy.html
Helm chart to deploy singlestore cluster
Using istio ingress


# SingleStore DB Helm Charts
Supported k8s versions > v1.22
The chart deploy singlestore on port 30306 

# prerequisite
- Cluster with istio ingress gateway 
- Istio gateway allow port 30306 
  
''' example: 
- hosts:
   - '*'
  port:
    name: mysql
    number: 30306
    protocol: TCP
'''
- istio service allow traffic to port 30306
''' example: 
  - name: mysql-port
    port: 30306
    protocol: TCP
    targetPort: 3306
'''

Edit values.yaml
- db_url
- license
- istio_gateway
- adminHashedPassword





 
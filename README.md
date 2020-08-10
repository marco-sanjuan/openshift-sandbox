# openshift-sandbox

### Start a Cluster (docker) 
Checkout https://developers.redhat.com/blog/2016/10/11/four-creative-ways-to-create-an-openshiftkubernetes-dev-environment/

1. Download oc origin (https://github.com/openshift/origin/releases). Add oc and kubectl to /usr/bin.
2. Configure docker daemon to accept insecure registries, by adding it to /etc/docker/daemon.json
```
{
    "insecure-registries" : [ "172.30.0.0/16" ]
}
```
3. Restart docker daemon: ```sudo service docker restart```
4. Start the cluster: ```oc cluster up```
5. Access https://127.0.0.1:8443

Check created forders:
* /home/{user}/.kube
* /home/{user}/openshift.local.clusterup

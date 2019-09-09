# Validate  Workshop

Static HTML website hosting the content for the Containers as a Service Workshop focusing on Pivotal Container Service, (PKS), delivered on PRA, (Pivotal Ready Architecture).


# Dynamic Persistent Volumes with vSAN
*Create a Storage Class (SC) for vsphere storage provider: kubectl apply -f vsphere-sc.yml
*Create Persistent Volume Claim (PVC) for redis master: kubectl apply -f redis-master-claim.yml
*Create PVC for redis slave: kubectl apply -f redis-slave-claim.yml
*Show PVC, Persistent Volume (PV), SC: kubectl get pvc,pv,sc --namespace=workshop
*Show redis pods running and wait for them to load: kubectl get po -n workshop -w
*Show volumes in vsphere UI
*Back on app, add a few data entries, should now be working, entries saved in redis.  (Need to click Submit button, enter key doesn’t work)
*Delete the guestbook application: kubectl delete -f guestbook-lb.yml
*Show PVC, PV still exist: kubectl get pvc,pv --namespace=workshop
*Redeploy guestbook application: kubectl apply -f guestbook-lb.yml
*Show data persisted in app.  Note that the IP address for the frontend service may have changed, so use the current value.


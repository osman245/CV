---
title: Storage in Kubernetes
date: 2023-07-12
math: true
image:
  placement: 2
  filename: featured.jpg
---  
At the lowest deployable and manageable unit of Kubernetes, we have pods. In a pod there are containers. If a container is deleted or lost, all of it’s data is gone with it. Thus we use volumes in a pod to maintain its data state for other living containers or future containers in the pod to use.

In Kubernetes, we can mount data from the pod volume to any storage resource(cloud, local and E.T.C).In Kubernetes we can manage storage in other ways such as through the persistent volume subsystem. Through this we utilize two API resources, persistent volume and persistent volume claims. A persistent volume is a volume that is created through an administrator or dynamically created through a persistent volume claim. A persistent volume claim is a request for storage by a user.

The PV and PVC dynamic is similar to their pod and node resources dynamic. Pods consume node resources and PVC’s consume PV resources. We can limit the certain amount of CPU and memory a pod can consume from a node.We can also limit the accessmode, perhaps we request a volume that is ReadWriteOnly rather then ReadWriteMany.

We do persistent volume claims to request a persistent volume with certain properties. If the PVC is not found, the StorageClass automatically generates a PV, with the certain type of specifications the client was looking for. When the PVC finds a PV, they bind to each other and the system stops looking for an available PV with those certain specifications. Some criteria for finding a PV are volume storage, read-write access, and type. Overall the purpose of configuring a Pod with PVC is to decouple site-specific information from a generic pod specification.

A practical example of using a PVC with a Kubernetes Pod

1.) Create a directory for the storage to be held in

2. ) Create a file in the storage


3.) Create a YAML file, including configurations for a Pod, persistent volume Claim, and persistent volume.





In this article, we created a pod that requests a persistent volume with at least a storage of 5GiB, can be accessed by many pods, and has the storageClassName of “manual”. We also created a Persistent Volume that has all these features to suffice the Pod.


# FEDCO  PROJECT

This is the repository where we maintain all the helm charts for fedco project. We have 3 charts (deployment) for this project each of which has it's charts inside the folder of it's namesake.

The modules are:
1. fedco-local
2. fedco-stage
3. fedco-dev




# Clone GIT Repository

Clone the repository via http or ssh first to use the helm charts.

```sh 
  $ git clone https://github.com/sagarshrestha24/fedco-charts.git
```

Now after cloning the git repository we have the following file structure.
 
![image](https://user-images.githubusercontent.com/76894861/129181946-cc8fff0c-a62d-462c-8700-70fd2b04b308.png)

 

The helm charts for each module is inside the folder of the same name.



# INSTALLATION


## fedco-local Deployment

To install the fedco-local deployment do following.

```sh
  $ helm install fedco-local fedco-local/
```
 
This will install the fedco-local helm charts . To verify:

```sh
   $ helm ls (gives the following output)
NAME       	NAMESPACE	REVISION	UPDATED                                  	STATUS  	CHART            	APP VERSION
fedco-local	local    	1       	2021-08-10 21:37:57.797350537 +0545 +0545	deployed	fedco-local-0.1.0	1.16.0     

     
```

Also check the kubernetes resources like pods , deployment , service for the fedco-local has been installed or not.

```sh
   $ kubectl get po 
   $ kubectl get svc
   $ kubectl get deploy
```
 

## fedco-stage Deployment

To install the fedco-stage deployment do following.

```sh
  $ helm install fedco-stage fedco-stage/
```
 
This will install the fedco-stage helm charts . To verify:

```sh
   $ helm ls (gives the following output)
NAME       	NAMESPACE	REVISION	UPDATED                                  	STATUS  	CHART            	APP VERSION
fedco-stage	stage    	1       	2021-08-10 21:37:57.797350537 +0545 +0545	deployed	fedco-stage-0.1.0	1.16.0     

     
```

Also check the kubernetes resources like pods , deployment , service for the fedco-stage has been installed or not.

```sh
   $ kubectl get po 
   $ kubectl get svc
   $ kubectl get deploy
```

## fedco-dev Deployment

To install the fedco-local deployment do following.

```sh
  $ helm install fedco-dev fedco-dev/
```
 
This will install the fedco-dev helm charts . To verify:

```sh
   $ helm ls (gives the following output)
NAME       	NAMESPACE	REVISION	UPDATED                                  	STATUS  	CHART            	APP VERSION
fedco-dev	  dev    	1       	2021-08-10 21:37:57.797350537 +0545 +0545	deployed	fedco-dev-0.1.0	    1.16.0     

     
```

Also check the kubernetes resources like pods , deployment , service for the fedco-dev has been installed or not.

```sh
   $ kubectl get po 
   $ kubectl get svc
   $ kubectl get deploy
```


## To delete all helm charts

```sh
$ helm delete fedco-local fedco-stage fedco-dev

```

it will delete all helm charts



## Common Parameters

| Parameters | Description | Default|
| ------ | ------ | ------ |
| replicaCount | Number of replicas pods to deploy | `number of replicas wanted` |
| imagePullSecrets | Secret containing the image pull credentials | `nil` |
| fullnameOverride | String to fully override ${mbm-module}.fullname	 | `nil` |
| nameOverride |  String to partially override ${mbm-module}.fullname	| `nil` |
| podSecurityContext | Manage security context and access level at pod level  	| `{}`(evaluated as a template) |
| securityContext |  Manage security context and access level	| `{}`(evaluated as a template)|
| resources |  The resources specificitions like imits and request	| `{}`(evaluated as a template) |
| nodeSelector | Node labels for pod assignment	| `{}`(evaluated as a template) |
| tolerations |  Tolerations for pod assignment		| `{}`(evaluated as a template) |
| affinity | Affinity for pod assignment		| `{}`(evaluated as a template) |










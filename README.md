# Container Groups

What are they? 
Serverless functions, Tower feature that runs a playbook on OpenShift/Kubernetes.

## OpenShift Steps

Create a Project/NameSpace (ansible-tower)

Create a ServiceAccount

Create a Role (pod-manager)

Create a RoleBinding

## Ansible Tower Steps 

Create the Credential

`CREDENTIAL TYPE == OpenShift or Kubernetes API Bearer Token

Copy stuff from the service account created in that project (User Management > Service Accounts > The one you made in the earlier steps)

OPENSHIFT OR KUBERNETES API ENDPOINT (short version from oc login with https://api.foo.openshift.io:6443)

API AUTHENTICATION BEARER TOKEN (can be used by itself without cert auth data, you don't need both)

CERTIFICATE AUTHORITY DATA`

Create the Container Group



## Quay/Clair










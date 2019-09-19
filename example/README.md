# Example Build and Deploy


```
This example uses ansible. Windows users use a vm or apply each command manually
```

This section contains an example for how this plugin can be used with Sonarqube

## Instructions

1. Create a project in OpenShift

```
oc new-project sonarqube
```

3. From the example folder run the prerequisites 

* Note: This only needs to be run once to pull in the ansible role needed.

```
ansible-galaxy install -r requirements.yml --roles-path=roles
```

4. From the example folder run the ansible playbook which sets up the build and deploy for Sonarqube including a persistent volume, database and a service account with the proper permissions

```
ansible-playbook -i inventory/ apply.yml
```

## Explore

To explore the how this built, explore the files in the subfolders here, particularly `example/inventory/group_vars/all.yml`

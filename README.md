# Ansible Role: elasticimport

This role will import some data into a running elasticsearch instance.

# Requirements
This role requires:
  - Some elasticsearch instance

# Role Variables

    elasticimport_docs:
      visualization1:
        method: "PUT"
        path: ".kibana/visualization/92933350-87f5-11e7-80a6-b1b72c6699dc"
        doc: "testvis1.json"
      visualization2:
        method: "PUT"
        path: ".kibana/visualization/93933350-87f5-11e7-80a6-b1b72c6699dc"
        doc: "testvis2.json"

One or more files to import. ```doc``` must refer to a file under
```<playbook-path>/templates```.
File must contain a valid JSON document.

# Example Playbook

```
- hosts: monitoring-elk
  roles:
    - { role: solutiondrive.elasticimport }
```


# Maintainer
solutionDrive DevOps <developer@solutiondrive.de>


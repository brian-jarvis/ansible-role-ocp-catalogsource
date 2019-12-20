Role Name
=========

Create a custom `CatalogSource` in OpenShift 4.x

Requirements
------------

Requires the k8s module to be available with ansible.

Role Variables
--------------

  - cat_name: Name of the `CatalogSource`.  Cannot container spaces, must be lowercase.
  - cat_namespace: Namespace to deploy `CatalogSource` to.  Defaults to `openshift-marketplace`
  - display_nm: Display name
  - publisher: Publisher of the `CatalogSource`
  - source_type: [optional] Set the sourceType of the `CatalogSource`, defaults to `grpc`
  - cat_image: [optional] Specifies the image to pull for the catalog.  Defaults to `quay.io/operator-framework/{{ display_nm }}:latest` where `display_nm` is converted to lowercase and all spaces are replaced with dashes. Example `Upstream Community Operators <- becomes -> upstream-community-operators`
  - state: [optional] Allowed either `present` or `absent' to specify if resource should be created or destroyed
  - kube_config_path: Path to the KUBECONFIG file for access

Dependencies
------------


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

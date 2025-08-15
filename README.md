EWC Ansible Role ECMWF Toolbox
==============================

Create a conda environment with the basic ECMWF software packages and libraries such as ecCodes, Metview, Earthkit, Aviso and more. See `files/env.yml` for the specific contents of this environment

Requirements
------------
This ansible role depends on ewc-ansible-role-conda

Role Variables
--------------
 - `ecmwf_toolbox_env_wipe`: Boolean to decide whether to wipe the environment if exists prior to a reinstallation. Default: true
 - `ecmwf_toolbox_env_name`: Name of the environment containing the ECMWF toolbox. Default: ecmwf-toolbox
 - `ecmwf_toolbox_create_ipykernel`: Boolean to create a system-wide kernel available. Default: true
 - `conda_prefix`: Prefix where conda is installed. Default: `/opt/conda`
 - `conda_user`: User owning the conda installation. Default: `root`

Example Playbook
----------------

    - hosts: all
      roles:
         -  ewc-ansible-role-ecmwf-toolbox

License
-------

Apache 2.0.

Author Information
------------------

ECMWF for the European Weather Cloud

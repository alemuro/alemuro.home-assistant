alemuro.homeassistant
=========

This role installs Home Assistant using the Python3 virtualenv way. It creates a folder and installs the dependencies needed. Sometimes we need to install extra packages, like `mysql` when we want to use this as recorder engine, or `ffmpeg` package.

Role Variables
--------------

| Name                                       | Default              | Description                                                                                           |
|--------------------------------------------|----------------------|-------------------------------------------------------------------------------------------------------|
| `alemuro_homeassistant_force_upgrade`      | *no*                 | Set `yes` if you wanna remove and recreate the `.virtualenv` folder                                   |
| `alemuro_homeassistant_version`            | *0.112.4*            | Version to install. [Check available versions here](https://pypi.org/project/homeassistant/#history). |
| `alemuro_homeassistant_path`               | */srv/homeassistant* | The folder where you wanna place the config of for home assistant                                     |
| `alemuro_homeassistant_extra_pip_packages` | *[]*                 | A list of extra pip packages that you wanna install, like `netdisco`                                  |
| `alemuro_homeassistant_extra_apt_packages` | *[]*                 | A list of extra apt packages that you wanna install, like `ffmpeg`                                    |


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
    - hosts: pi
      roles:
         - { role: alemuro.homeassistant }
```

Usage
-----

* Install:

```
$ ansible-galaxy -p roles alemuro.homeassistant
```


License
-------

Apache License

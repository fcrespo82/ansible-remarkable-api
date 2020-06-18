fcrespo82.remarkable-api
=========

Install rmapi to enable cli comunication with your remarkable tablet

Install a printer workflow to enable to send any printed item to your remarkable tablet

Role Variables
--------------

```yml
rmapi_install_dir: "{{ ansible_env.HOME }}/bin" # rmapi install location
rmapi_version: 0.0.11 # rmapi version to install
OneTimeCode: XXXXX # Only needed for first run on the server (https://my.remarkable.com/connect/desktop)
```

Example Playbook
----------------

```yml
- hosts: servers
  roles:
      - { role: fcrespo82.remarkable-api, OneTimeCode: XXXXX }
```

Better than setting the one time code this way is to go to https://my.remarkable.com/connect/desktop and run your play book passing `-e OnetimeCode=XXXXX`
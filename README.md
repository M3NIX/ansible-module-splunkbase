# ansible-module-lunkbase

This ansible module will download an app from https://splunkbase.splunk.com.
If you want to have a look into a ansible role which will download and install apps you can have a look [here](https://github.com/M3NIX/ansible-role-splunkbase.git).

## Usage
```yaml
# download latest app with url
- name: download app
  get_splunk_app:
    app: "https://splunkbase.splunk.com/app/3435/"
    dest: /tmp/
    username: my_user
    password: my_password

# download latest app with id
- name: download app
  get_splunk_app:
    app: 3435
    dest: /tmp/
    username: my_user
    password: my_password

# download specific version of app with url
- name: download app
  get_splunk_app:
    app: "https://splunkbase.splunk.com/app/3435/"
    version: 3.5.0
    dest: /tmp/
    username: my_user
    password: my_password

# download specific version of app with id
- name: download app
  get_splunk_app:
    app: 3435
    version: 3.5.0
    dest: /tmp/
    username: my_user
    password: my_password
```

## Requirements

- python > 3.6
- python-request lib must be installed on target host
- the target host needs access to https://splunkbase.splunk.com
- user account for splunkbase

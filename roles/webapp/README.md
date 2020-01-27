# Ansible Role: Demo web application

Installs Flask demo web application on RedHat/CentOS or Debian/Ubuntu servers.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see [defaults/main.yml](./defaults/main.yml))

```yml
app_user: demo
```

The user under which application runs.

```yml
app_home: /var/flask-demo
```

The home directory of the deployed application.

```yml
app_version: master
```

The version of the deployed application.

```yml
app_virtualenv: "{{ app_home }}/venv"
```

The Python virtual environment used for installation of dependencies.

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

```yml
- hosts: all
  roles:
    - flask_demo
```

## License

MIT / BSD

## Author Information

This role was created in 2020 by Petr Drastil.

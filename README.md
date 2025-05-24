Role Name
=========

This role installs the WordPress.

Requirements
------------

None.

Role Variables
--------------

List of variables in ansible-role-wordpress:

```yaml
---
wordpress_action: install
wordpress_locale: en_US
wordpress_user_linux: root
wordpress_user_admin: root
wordpress_user_admin_password: dpanel
wordpress_user_email: support@devetek.com

wordpress_title: My Wordpress Site

wordpress_domain: wordpress.devetek.app

wordpress_directory: /var/www/wordpress

# Database configuration
wordpress_db_host: localhost
wordpress_db_name: db_mywp
wordpress_db_user: user_mywp
wordpress_db_password: password_mywp

# installation type for singlesite or multisites. Available options: singlesite, multisite
wordpress_install_type: singlesite
# installation for multisites. Available options: subdirectory, subdomain
wordpress_multisite_network_type: subdomain

```

Dependencies
------------

- devetek.wpcli

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - devetek.wordpress
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

[Nedya Prakasa]. Role created for [dPanel].

[dPanel]: https://cloud.terpusat.com/
[Nedya Prakasa]: https://github.com/prakasa1904
[devetek]: https://github.com/devetek
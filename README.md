shibboleth-idp-v3
=================

The role will install the Shibboleth Identity Provider v. 3 with tomcat8 into a debian based machine.
The integration is made with the packaged version of tomcat which has to be installed in the machine.


Requirements
------------

The user database is not installed by this role but it should be created in advance. Currently, only LDAP is supported by this role but MySqL could be integrated in the future. If none is available a role for LDAP is provided (look at the role named *ldap*).

The data time in the machine has to be correct so it would be good to syncronize with a time server using some pre-tasks or roles for the time.

Role Variables
--------------

``idp_attributes_scope``


``LDAP_server_certificate``

``idp_custom_templates_path``

``idp_custom_css_path``

``idp_custom_images_path``


Dependencies
------------

`pexpect >= 3.3` (The version packaged with Debian jessy is too old and not working, it has to be installed with pip)
This role also depends implicitly on the osct.tomcat-8 role.


Example Playbook
----------------

    - hosts: idp
      roles:
         - osct.shibboleth-idp-v3

License
-------

Apache v2.0

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

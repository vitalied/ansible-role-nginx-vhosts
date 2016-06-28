Ansible Role for Nginx VirtualHost
====================

[![Build Status](https://travis-ci.org/vitalied/ansible-role-nginx-vhosts.svg?branch=master)](https://travis-ci.org/vitalied/ansible-role-nginx-vhosts)
[![GitHub tag](https://img.shields.io/github/tag/vitalied/ansible-role-nginx-vhosts.svg)](https://github.com/vitalied/ansible-role-nginx-vhosts)
[![GitHub license](https://img.shields.io/github/license/vitalied/ansible-role-nginx-vhosts.svg)](https://github.com/vitalied/ansible-role-nginx-vhosts/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/9297.svg)](https://galaxy.ansible.com/vitalied/nginx-vhosts)

Ansible Role for Nginx VirtualHost Management.

Requirements
------------

This role require Ansible 2.1 or higher.

This role was designed for Ubuntu Server 14.04+.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>nginx_vhosts_domain</td>
<td>yes</td>
<td>example.com</td>
<td></td>
<td>Nginx VirtualHost domain name.</td>
</tr>
<tr class="even">
<td>nginx_vhosts_root_dir</td>
<td>yes</td>
<td>/srv/apps/example.com</td>
<td></td>
<td>Directory that forms the main document tree visible from the web.</td>
</tr>
<tr class="odd">
<td>nginx_vhosts_http_port</td>
<td>yes</td>
<td>80</td>
<td></td>
<td>Nginx VirtualHost HTTP port.</td>
</tr>
<tr class="even">
<td>nginx_vhosts_https_port</td>
<td>yes</td>
<td>443</td>
<td></td>
<td>Nginx VirtualHost HTTPS port.</td>
</tr>
<tr class="odd">
<td>nginx_vhosts_use_ssl</td>
<td>yes</td>
<td>true</td>
<td><ul>
<li><code>false</code></li>
<li><code>true</code></li>
</ul></td>
<td>Create HTTPS Nginx VirtualHost.</td>
</tr>
<tr class="even">
<td>nginx_vhosts_redirect_to_ssl</td>
<td>yes</td>
<td>true</td>
<td><ul>
<li><code>false</code></li>
<li><code>true</code></li>
</ul></td>
<td>Redirect HTTP Nginx VirtualHost to HTTPS.</td>
</tr>
<tr class="odd">
<td>nginx_vhosts_ssl_protocol</td>
<td>yes</td>
<td>http2</td>
<td><ul>
<li><code>http2</code></li>
<li><code>spdy</code></li>
</ul></td>
<td>SSL protocol to use for HTTPS Nginx VirtualHost.</td>
</tr>
<tr class="even">
<td>nginx_vhosts_use_self_signed_ssl_certs</td>
<td>yes</td>
<td>true</td>
<td><ul>
<li><code>false</code></li>
<li><code>true</code></li>
</ul></td>
<td>Use self signed SSL certificates for HTTPS Nginx VirtualHost.</td>
</tr>
<tr class="odd">
<td>nginx_vhosts_use_dhparam_cert</td>
<td>yes</td>
<td>false</td>
<td><ul>
<li><code>false</code></li>
<li><code>true</code></li>
</ul></td>
<td>Use dhparam certificate for HTTPS Nginx VirtualHost.</td>
</tr>
<tr class="even">
<td>nginx_vhosts_use_passenger</td>
<td>yes</td>
<td>false</td>
<td><ul>
<li><code>false</code></li>
<li><code>true</code></li>
</ul></td>
<td>Nginx VirtualHost use passenger.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: vitalied.nginx-vhosts

License
-------

-   Code released under [MIT](https://github.com/vitalied/ansible-role-nginx-vhosts/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

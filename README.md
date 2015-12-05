Ansible Role for Confluence
===========================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-confluence.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-confluence)
 [![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-confluence.svg)](https://github.com/pantarei/ansible-role-confluence)
 [![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-confluence.svg)](https://github.com/pantarei/ansible-role-confluence/blob/master/LICENSE)
 [![Ansible Role](https://img.shields.io/ansible/role/5990.svg)](https://galaxy.ansible.com/detail#/role/5990)

Ansible Role for Atlassian Confluence Installation.

Requirements
------------

This role require Ansible 1.9 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

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
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">confluence_archive</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-confluence/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Download archive filename for cache during (re)install.</td>
</tr>
<tr class="even">
<td align="left">confluence_catalina</td>
<td align="left">yes</td>
<td align="left">/usr/share/confluence</td>
<td align="left"></td>
<td align="left">Location for the Confluence installation directory.</td>
</tr>
<tr class="odd">
<td align="left">confluence_connector_port</td>
<td align="left">yes</td>
<td align="left">8090</td>
<td align="left"></td>
<td align="left">Confluence Apache Tomcat connector port.</td>
</tr>
<tr class="even">
<td align="left">confluence_home</td>
<td align="left">yes</td>
<td align="left">/var/lib/confluence</td>
<td align="left"></td>
<td align="left">Location for the Confluence home directory.</td>
</tr>
<tr class="odd">
<td align="left">confluence_jvm_maximum_memory</td>
<td align="left">yes</td>
<td align="left">1024m</td>
<td align="left"></td>
<td align="left">Confluence JVM maximum memory usage.</td>
</tr>
<tr class="even">
<td align="left">confluence_jvm_minimum_memory</td>
<td align="left">yes</td>
<td align="left">512m</td>
<td align="left"></td>
<td align="left">Confluence JVM minimum memory usage.</td>
</tr>
<tr class="odd">
<td align="left">confluence_jvm_support_recommended_args</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-confluence/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Atlassian Support recommended JVM arguments.</td>
</tr>
<tr class="even">
<td align="left">confluence_pass</td>
<td align="left">yes</td>
<td align="left">ahle4Boo</td>
<td align="left"></td>
<td align="left">Password for Confluence system user.</td>
</tr>
<tr class="odd">
<td align="left">confluence_proxy_name</td>
<td align="left">no</td>
<td align="left"><code>null</code></td>
<td align="left"></td>
<td align="left">Pass value as <code>proxyName</code> to <a href="https://github.com/pantarei/ansible-role-confluence/blob/master/templates/usr/share/confluence/conf/server.xml.j2">template</a>.</td>
</tr>
<tr class="even">
<td align="left">confluence_scheme</td>
<td align="left">no</td>
<td align="left"><code>null</code></td>
<td align="left"><ul>
<li><code>null</code></li>
<li>http</li>
<li>https</li>
</ul></td>
<td align="left">Install Confluence in standalone mode if <code>null</code>, or integrating with Apache using HTTP if <code>http</code>, or integrating with Apache using HTTPS if <code>https</code>.</td>
</tr>
<tr class="odd">
<td align="left">confluence_server_port</td>
<td align="left">yes</td>
<td align="left">8000</td>
<td align="left"></td>
<td align="left">Confluence Apache Tomcat server port.</td>
</tr>
<tr class="even">
<td align="left">confluence_sha256</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-confluence/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Download archive sha256 checksum for cache during (re)install.</td>
</tr>
<tr class="odd">
<td align="left">confluence_upgrade</td>
<td align="left">no</td>
<td align="left"><code>false</code></td>
<td align="left"><ul>
<li><code>true</code></li>
<li><code>false</code></li>
</ul></td>
<td align="left">If <code>true</code>, trigger upgrade by stop existing Confluence service, purge existing Confluence installation direcoty before normal tasks.</td>
</tr>
<tr class="even">
<td align="left">confluence_url</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-confluence/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">URL for download archive.</td>
</tr>
<tr class="odd">
<td align="left">confluence_user</td>
<td align="left">yes</td>
<td align="left">confluence</td>
<td align="left"></td>
<td align="left">Username for Confluence system user.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.confluence, confluence_user: 'confluence', confluence_pass: 'ahle4Boo', confluence_upgrade: 'false' }

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-confluence/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>


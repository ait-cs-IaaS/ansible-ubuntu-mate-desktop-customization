Role Name
=========

This role allows for customization of a MATE surface.


Role Variables
--------------


| Variable name   | Type   | Default                    | Description                                              |
|-----------------|--------|----------------------------|----------------------------------------------------------|
| customize_user    | string | NA   | Username for whom to customize the desktop |
| customize_theme_name* | string | NA | Themename |
| customize_theme_package* | string | NA | Name of theme-package |
| desktop_bg_src | string | files/wallpaper.jpg | Local image to be set as the backgroud image |
| appendOnly | boolean | true | Wheiter or not the launcher objects should be appended or overwritten |
| override_panel_list | string | [...] | If appendOnly is set to false, this list is used to define the launcher objects |
| launcher_objects | dict | NA | Holds all launcher objects to be created and set |
| &nbsp;&nbsp;&nbsp;&nbsp;∟ object-name | string | NA | Name of the launcher object |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;∟ launcher-location | string | (normally: /usr/share/applications/\<object-name\>.desktop) | Location of the respective .desktop file |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;∟ position* | string | NA | Nummeric indicator for ordering (ASC) |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;∟ object-type* | string | launcher | should remain unchanged |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;∟ toplevel-id* | string | top | 'top' or 'bottom' |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;∟ menu-path* | string | applications:/ | Menu path |

\* optional



Example Playbook
----------------

```yml
- hosts:
    - <ip-address>
  vars:
    ansible_become: yes
  roles:
    - ubuntu-mate-desktop-customization

```


License
-------

MIT

Author Information
------------------

This role was created in 2020 by Lenhard Reuter

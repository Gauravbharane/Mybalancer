Role Name : Mybalancer
=========

This Ansible role configures HAProxy as a load balancer and Apache as a web server. It sets up HAProxy to distribute incoming HTTP requests to multiple backend servers and configures Apache to serve web content.

Requirements
------------

- Ansible-core 
- ansible-galaxy

Role Variables
--------------

- `frontend`: Define frontend configuration.
- `backend_servers`: Define backend servers configuration.

Dependencies
------------

None

Example Playbook
----------------
<code>
  - hosts: servers
  vars:
    frontend:
      name: http-in
      port: 80
      default_backend: servers
    backend_servers:
      - name: server1
        ip: 127.0.0.1
        port: 80
      - name: server2
        ip: 192.168.1.10
        port: 80
      # Add more backend servers as needed
  roles:
    - Mybalancer
</code>


License
-------
MIT License

Copyright (c) 2024 Gaurav Bharane

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


Author Information
------------------

Author: Gaurav Bharane
Contact: gauravbharane1839@gamil.com
Github repository: https://github.com/Gauravbharane/Mybalancer.git
Website: linktr.ee/gauravbharane/

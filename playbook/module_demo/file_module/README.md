ansible.builtin.file – Manage files and file properties
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/file_module.html#file-module


Examples
- name: Create a directory if it does not exist
  ansible.builtin.file:
    path: /etc/some_directory
    state: directory
    mode: '0755'
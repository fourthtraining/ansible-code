ansible.builtin.file – Manage files and file properties
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/file_module.html#file-module


Examples
- name: Create a directory if it does not exist
  ansible.builtin.file:
    path: /etc/some_directory
    state: directory
    mode: '0755'

copy1-file.yml 此play-book作用僅限於copy檔案到遠端，若遠端目錄不存在，此playbook無法作用。
copy2-file.yml 此play-book作用僅限於copy檔案到遠端，若遠端目錄不存在，此playbook會自動建立目錄，並將檔案複製到遠端。
copy3-file.yml 此play-book作用僅限於copy檔案到遠端，若遠端目錄不存在，此playbook會自動建立目錄，並將檔案複製到遠端，若是需要建立在/etc底下，需要加上root權限。
copy4-file.yml 此play-book作用僅限於copy檔案到遠端，若遠端目錄不存在，此playbook會自動建立目錄，並將檔案複製到遠端，若是需要建立在/etc底下，需要加上root權限
，在playbook中加上"backup: yes"會自動備份被覆蓋的檔案。
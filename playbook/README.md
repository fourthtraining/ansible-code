- hosts: test1
  name: play-test
  tasks:
  - name: check host commection
    ping:

hosts = 控制那些HOST，可以在inventory中定義，一個HOST或一個GROUP
#hosts: "test1 = 單一主機" or "test = Group"

tasks = 任務
每一個tasks是由name及module組成
tasks:
- name:
  yum:
    name: http
    state:latest

從整體結構上來看，一個playbook.yml檔，可以由多個play，每個play可以包含多個tasks，每個tasks是執行任務，透過一個module去執行

------------------------------------------------
Ansible Core Concept - ansible 三大核心

Inventory               Playbook               Module


Module Example : https://docs.ansible.com/ansible/2.9/modules/list_of_all_modules.html
# 使用方法
一切以tags区分：

```ansible-playbook site.yml -l '~pattern_for_hostname' --tags jdk -u root```

```ansible-playbook site.yml -l '~pattern_for_hostname' --tags jdk,python-s -U root```


需求：需要一个--list-tags的选项来列出所有tags

# 增加一个play

    $ mkdir -p roles/${PLAY_NAME}/{tasks,vars}

    $ cat roles/${PLAY_NAME}/vars/main.yml
    ---
    tags: wuhahah

    $ cat roles/${PLAY_NAME}/tasks/main.yaml
    ---
    - name: balala
    ...
    - name: xihoho
    ...

# 参考

[http://docs.ansible.com/playbooks_best_practices.html](http://docs.ansible.com/playbooks_best_practices.html)

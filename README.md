To get all tasks use:
ansible-playbook --list-tasks initialize-server.yml

And you will get:
playbook: initialize-server.yml

  play #1 (hetzner): install debian 9.11 minimal        TAGS: []
    tasks:
      hetzner-install-debain-9.11 : configure installation      TAGS: []
      hetzner-install-debain-9.11 : install image       TAGS: []
      hetzner-install-debain-9.11 : reboot into normal mode     TAGS: []

  play #2 (hetzner): install packages   TAGS: []
    tasks:
      install-packages : run apt-get update     TAGS: []
      install-packages : install minimal toolset        TAGS: []
      install-packages : Add Docker GPG key     TAGS: []
      install-packages : Add Docker APT repository      TAGS: []
      install-packages : Install list of packages       TAGS: []
      install-packages : add user mwiget to docker      TAGS: []
      install-packages : install docker-compose TAGS: []

  play #3 (hetzner): final reboot       TAGS: []
    tasks:
      reboot : reboot server    TAGS: []
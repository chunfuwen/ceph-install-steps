1. install rhel7.6
2. Configure repo as attached repo list
3. Install precondition
yum -y install libunwind gdisk python-jinja2 cryptsetup hdparm python-requests redhat-lsb-core python-requests boost-system boost-thread python-flask

4. install all packages in packages foler
5. on ceph-admin:install ceph-deploy
6. ceph-deploy new mon(admin node should be same with mon)
7  /usr/bin/ceph-deploy mon create-initial
8./usr/bin/ceph-deploy disk zap ceph-osd:/dev/vdb
9. /usr/bin/ceph-deploy osd prepare ceph-osd:/dev/vdb
10 ./usr/bin/ceph-deploy osd activate ceph-osd:/dev/vdb1
11./usr/bin/ceph-deploy admin ceph-admin ceph-mon ceph-osd
12. chmod +r /etc/ceph/ceph.client.admin.keyring
13. ceph health

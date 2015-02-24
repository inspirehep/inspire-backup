INSPIRE Backup
=============

Static backup site for INSPIRE in case of maintenance and/or unexpected
downtime.

Install
--------
```console
$ git clone https://github.com/inspirehep/inspire-backup.git
$ cd inspire-backup
$ bower install
```

Branches
--------
* ``master`` - Default development branch.
* ``qa`` - Quality assurance branch, deployed to our QA cluster.
* ``production`` - Production branch, deployed to our production cluster.

Deployment
----------

```console
$ ssh <build host>
$ cd /opt/inspire/scripts/
$ fab backup_bootstrap
$ fab backup_update
$ fab backup_build
$ fab backup_deploy
```

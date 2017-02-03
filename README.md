Google Storage Downloader
=========

Simple playbook for downloading files on gs://URI

Requirements
------------

- Gsutil up and running for ansible user

Role Variables
--------------
```
gs_dl_remote_bucket   : bucket where to download the file       : required
gs_dl_remote_filename : remote filename                         : required
gs_dl_dest_filename   : destination filename                    : optional, default value = gs_dl_remote_filename
gs_dl_tmp_dir         : directory where to download the file    : optional, default value = /tmp
gs_dl_dest_dir        : the downloaded file will be moved here  : optional, default value = /tmp
```


Example
----------------

    - hosts: servers
      roles:
         - { role: gs_downloader, gs_dl_remote_bucket: "gs://mybucket/mydir", gs_dl_remote_filename: "myfile" }

License
-------

MIT




# gitea-upgrade
gitea upgrade

UPGRADE GITEA

0. asumsi :
   ```- versi gitea terbaru 1.16.6
   - install di OS linux centos versi 7 64bit```

1. download versi terbaru :
   ```cd /tmp
   wget https://dl.gitea.io/gitea/1.16.6/gitea-1.16.6-linux-amd64.xz```

2. extract :
   ```xz -d -v gitea-1.16.6-linux-amd64.xz
   chmod +x gitea-1.16.6-linux-amd64```

3. cek versi :
   ```./gitea-1.16.6-linux-amd64 -v```

4. stop service gitea :
   ```systemctl stop gitea```

5. backup versi lama :
   ```
   sudo mv /var/lib/gitea/gitea /var/lib/gitea/gitea_bak_`date '+%Y%m%d'`
   sudo mv /usr/local/bin/gitea /usr/local/bin/gitea_bak_`date '+%Y%m%d'`
   ```

6. copy versi baru :
   ```sudo cp gitea-1.16.6-linux-amd64 /var/lib/gitea/gitea
   sudo cp gitea-1.16.6-linux-amd64 /usr/local/bin/gitea```

7. start service :
   ```sudo systemctl start gitea```

8. cek versi :
   ```gitea -v
   /var/lib/gitea/gitea -v```

9. done.


layout: true
class: inverse, middle, large

---
class: special
# Galaxy Troubleshooting

slides by @martenson, @natefoo

.footnote[\#usegalaxy / @galaxyproject]

---
class: larger

## These slides are trimmed

See the [Melbourne Slides](https://galaxyproject.github.io/dagobah-training/2017-melbourne/22-troubleshooting/troubleshooting.html) for more tips

---
class: special, middle
# Everything always goes wrong

---
# Galaxy UI is slow

- Investigate load
  - Web server(s)
  - Database server
- Investigate memory usage, swapping
- Investigate iowait
  - Use iostat
- Use `gdb`

---
# Galaxy UI is slow

- Use heartbeat (demo!)

---
# Local or Network FS slow/down

- Use `iostat` (demo!)
- Use `time dd` (demo!)

Solutions:
- Don't put the Galaxy server in that FS. Local distribution, CVMFS, ??
- Get a better network FS

---
# Hung server processes

- Use `uwsgitop` (demo!)

- `uwsgitop` state busy?
  -  5      12.7    3453    59962   1       13      0       **busy**    89ms    0       0       536.0M  1       0       450m    09:35:36
- Process state D?
  - g2main    3440 17.2  5.2 1696480 863536 ?      **D**    Nov10 167:46 /cvmfs/main.galaxyproject.org/venv/bin/uwsgi --ini /srv/galaxy/main/config/uwsgi.ini

Kernel uninterruptable sleep - normal unless stuck. Probably IO. Check filesystems, disks.

---
# Hung server processes

- Investigate `/proc/pid` especially `fd`
- Use `strace` (demo!)

---
# Undead processes

```
bind(): Address already in use [core/socket.c line 769]
```

Use `lsof -i :<port>` (demo!)

---
# Remember ALL the log files

All may be relevant:
- uWSGI log
- handler logs
- Pulsar logs
- nginx access, error logs
- syslog/messages
- authlog
- browser console log

---
# Database problems

Slow queries, high load, etc.

Enable query echoing in `galaxy.ini` to extract the SQL query

- Use `EXPLAIN ANALYZE` (demo!)
- Use `VACUUM ANALYZE`

Increase `shared_buffers`. 2GB on Main (16GB of memory on VM)

---
# Where to get help

- [Galaxy Biostar](https://biostar.usegalaxy.org/)
- [galaxy-dev Mailing list](http://dev.list.galaxyproject.org/)
- [IRC](https://wiki.galaxyproject.org/Support/IRC): \#galaxyproject on Freenode
- [Wiki: Support](https://wiki.galaxyproject.org/Support)

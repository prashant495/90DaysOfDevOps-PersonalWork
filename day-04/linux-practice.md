Command 1 : List all the running processes

```ps aux```

```bash
ps aux
```

ps will show you the running process in current terminal and ps aux will show all the processes running on system.

ps   → process status
a    → show processes of all users
u    → show detailed/user-oriented information
x    → include processes without a terminal (TTY)

<img width="1032" height="587" alt="image" src="https://github.com/user-attachments/assets/71057c05-f5c8-465b-9495-d545519b259f" />


Command 2 : top -> top is a very important Linux command used to monitor running processes and system resource usage in real time.

| Column      | Meaning                      |
| ----------- | ---------------------------- |
| **PID**     | Process ID                   |
| **USER**    | User who started the process |
| **PR**      | Process priority             |
| **NI**      | Nice value                   |
| **VIRT**    | Virtual memory used          |
| **RES**     | Physical RAM used            |
| **SHR**     | Shared memory                |
| **S**       | Process state                |
| **%CPU**    | CPU usage                    |
| **%MEM**    | Memory/RAM usage             |
| **TIME+**   | CPU time used by process     |
| **COMMAND** | Process/command name         |



<img width="1052" height="685" alt="image" src="https://github.com/user-attachments/assets/0839ff39-f4cc-4448-9906-06d0e59d509e" />

**Command 3 :** **pgrep** -> pgrep is used to find the PID (Process ID) of a running process by its name.

```bash
ubuntu@ip-172-31-17-118:~/90DaysOfDevOps-PersonalWork/day-04$ pgrep bash
1412
```

**Command 4 :** **systemctl status nginx** -> This command is used to check the current status of the Nginx service on a Linux system.

**Command 5 : systemctl list-units** -> systemctl list-units is used to list the currently loaded systemd units on a Linux system.

UNIT                      LOAD   ACTIVE   SUB       DESCRIPTION
nginx.service             loaded active   running   A high performance web server
ssh.service               loaded active   running   OpenBSD Secure Shell server
cron.service              loaded active   running   Regular background program processing daemon
systemd-logind.service    loaded active   running   User Login Management

| Column          | Meaning                                                |
| --------------- | ------------------------------------------------------ |
| **UNIT**        | Name of the unit                                       |
| **LOAD**        | Whether the unit configuration was loaded successfully |
| **ACTIVE**      | General active/inactive state                          |
| **SUB**         | Detailed state                                         |
| **DESCRIPTION** | Description of the unit                                |

**Command 6 : journalctl -u <service>** -> journalctl is used to view logs collected by systemd.



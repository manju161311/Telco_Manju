# day7-linux-commands

2025-11-17T09:57:21.879483+00:00 Manju systemd[1]: Starting wsl-pro.service - Bridge to Ubuntu Pro agent on Windows...
2025-11-17T09:57:21.933771+00:00 Manju wsl-pro-service[7879]: #033[36mINFO#033[0m Starting WSL Pro Service version 0.1.18-1-g3c35f427-dirty
2025-11-17T09:57:22.065514+00:00 Manju systemd[1]: Started wsl-pro.service - Bridge to Ubuntu Pro agent on Windows.
2025-11-17T09:57:22.590316+00:00 Manju wsl-pro-service[7879]: #033[33mWARNING#033[0m Daemon: could not connect to Windows Agent: could not get address: could not read agent port file "/mnt/c/Users/manju/.ubuntupro/.address": open /mnt/c/Users/manju/.ubuntupro/.address: no such file or directory
2025-11-17T09:57:29.609083+00:00 Manju wsl-pro-service[7879]: message repeated 3 times: [ #033[33mWARNING#033[0m Daemon: could not connect to Windows Agent: could not get address: could not read agent port file "/mnt/c/Users/manju/.ubuntupro/.address": open /mnt/c/Users/manju/.ubuntupro/.address: no such file or directory]

A2025-11-17T09:58:06.817533+00:00 Manju systemd-resolved[6676]: Clock change detected. Flushing caches.
2025-11-17T09:58:24.253633+00:00 Manju wsl-pro-service[7879]: #033[33mWARNING#033[0m Daemon: could not connect to Windows Agent: could not get address: could not read agent port file "/mnt/c/Users/manju/.ubuntupro/.address": open /mnt/c/Users/manju/.ubuntupro/.address: no such file or directory

2025-11-17T09:59:20.320279+00:00 Manju systemd-resolved[6676]: message repeated 3 times: [ Clock change detected. Flushing caches.]
2025-11-17T09:59:22.699545+00:00 Manju wsl-pro-service[7879]: #033[33mWARNING#033[0m Daemon: could not connect to Windows Agent: could not get address: could not read agent port file "/mnt/c/Users/manju/.ubuntupro/.address": open /mnt/c/Users/manju/.ubuntupro/.address: no such file or directory
2025-11-17T09:59:34.725546+00:00 Manju systemd-resolved[6676]: Clock change detected. Flushing caches.

2025-11-17T10:03:17.805305+00:00 Manju wsl-pro-service[7879]: #033[33mWARNING#033[0m Daemon: could not connect to Windows Agent: could not get address: could not read agent port file "/mnt/c/Users/manju/.ubuntupro/.address": open /mnt/c/Users/manju/.ubuntupro/.address: no such file or directory

2025-11-17T10:07:53.222586+00:00 Manju systemd-resolved[6676]: message repeated 3 times: [ Clock change detected. Flushing caches.]
2025-11-17T10:08:11.061877+00:00 Manju wsl-pro-service[7879]: #033[33mWARNING#033[0m Daemon: could not connect to Windows Agent: could not get address: could not read agent port file "/mnt/c/Users/manju/.ubuntupro/.address": open /mnt/c/Users/manju/.ubuntupro/.address: no such file or directory
2025-11-17T10:08:11.062080+00:00 Manju wsl-pro-service[7879]: #033[33mWARNING#033[0m Exiting after <nil>: check if the Windows agent is installed and running.
2025-11-17T10:08:11.070461+00:00 Manju systemd[1]: wsl-pro.service: Deactivated successfully.
2025-11-17T10:08:22.340304+00:00 Manju systemd-resolved[6676]: Clock change detected. Flushing caches.

#ls -l to modify
2025-11-17T10:08:11.062080+00:00 Manju wsl-pro-service[7879]: #033[33mWARNING#033[0m Exiting after <nil>: check if the Windows agent is installed and running.
2025-11-17T10:08:11.070461+00:00 Manju systemd[1]: wsl-pro.service: Deactivated successfully.
2025-11-17T10:08:22.340304+00:00 Manju systemd-resolved[6676]: Clock change detected. Flushing caches.

mod to 750
2025-11-17T10:08:22.340304+00:00 Manju systemd-resolved[6676]: Clock change detected. Flushing caches.
2025-11-17T10:00:33.357208+00:00 Manju kernel: systemd-journald[4998]: Time jumped backwards, rotating.
2025-11-17T10:12:46.800544+00:00 Manju kernel: WSL (237) ERROR: CheckConnection: getaddrinfo() failed: -5
2025-11-17T10:12:46.800621+00:00 Manju kernel: systemd-journald[4998]: Time jumped backwards, rotating.


Day 9
Pipelines and Text Processing, and Filters Commands

-->Filter logs using grep to select only the lines that contain a specific event (like call drops).

-->Extract a required field (such as CELL ID) using awk, which picks specific columns from each log line.

-->Clean or normalize the extracted data using sed by removing labels, symbols, or extra spaces.

-->Sort and count occurrences using sort and uniq -c to find how many times each value appears.

-->Optionally format results by adding a header or limiting the output using head.

-->Identify the IMSIs (mobile subscribers) involved in call drops by filtering log lines and extracting IMSI fields.

-->Perform advanced filtering by selecting only call drops where the signal strength (RSRP) is worse than –105 dBm.

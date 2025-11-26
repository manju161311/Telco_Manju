# day7-linux-commands
**day 7**


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

**Issues**
Missing Parent Directory Error:  Running   without the   option when trying to create a nested structure like   if   or   don't exist

Permission Denied for  / :  The user forgets to use   when attempting to change ownership or group to a system user/group

**Day 8**
**Linux System Administration Users, Groups & System Security**

 Incorrectly placing NOPASSWD: could lead to either a user being prompted for a password when they shouldn't be, or worse, being granted passwordless access to all commands instead of just the intended one (/bin/df).

 Failing to use the full path for a command in the sudoers file (e.g., using ip instead of /usr/sbin/ip) could prevent the rule from working as intended, even if the command runs manually.

 

**Day 9**
**Pipelines and Text Processing, and Filters Commands**

-->Filter logs using grep to select only the lines that contain a specific event (like call drops).

-->Extract a required field (such as CELL ID) using awk, which picks specific columns from each log line.

-->Clean or normalize the extracted data using sed by removing labels, symbols, or extra spaces.

-->Sort and count occurrences using sort and uniq -c to find how many times each value appears.

-->Optionally format results by adding a header or limiting the output using head.

-->Identify the IMSIs (mobile subscribers) involved in call drops by filtering log lines and extracting IMSI fields.

-->Perform advanced filtering by selecting only call drops where the signal strength (RSRP) is worse than –105 dBm.




**Day 10**

Not using double quotes (e.g., echo $name) when a variable contains spaces, leading the shell to split the variable content into multiple arguments, which breaks commands

Forgetting the square brackets or leaving spaces inside them

Misunderstanding that when a function is called, the script's positional arguments ($1, $2, etc.) are replaced by the function's arguments.


**Day 11**
**1) IP Reachability**
import subprocess
import os
ip_list = [
    "192.168.1.1",
    "8.8.8.8",
    "10.0.0.1",
    "192.168.56.1"
]
for ip in ip_list:
    print(f"Checking {ip} ...")
    
    # For Windows use: ping -n 1
    command = ["ping", "-n", "1", ip]

    result = subprocess.run(command, stdout=subprocess.PIPE, stderr=subprocess.PIPE)

    if result.returncode == 0:
        print(f"IP address {ip} is reachable.\n")
    else:
        print(f"IP address {ip} is unreachable.\n")

**2) Latency**
# Step 1: Define Sample Data
latency_values = [12, 15, 14, 20, 18, 10, 30, 25]

# Step 2: Create calculate_average(data) Function
def calculate_average(data):
    if len(data) == 0:
        return 0
    return sum(data) / len(data)

# Step 3 & 4: Create get_summary(data) Function
def get_summary(data):
    summary = {
        "Min": min(data),
        "Max": max(data),
        "Average": calculate_average(data)
    }
    return summary

# Step 5: Test Functions
result = get_summary(latency_values)
print("Network Latency Summary:")
print(result)

**3) Menu Driven CLI**
import subprocess
def check_ip_reachability():
    ip_list = [
        "192.168.1.1",
        "8.8.8.8",
        "10.0.0.1",
        "192.168.56.1"
    ]

    for ip in ip_list:
        print(f"\nChecking {ip} ...")
        command = ["ping", "-n", "1", ip]   
        result = subprocess.run(command, stdout=subprocess.PIPE, stderr=subprocess.PIPE)

        if result.returncode == 0:
            print(f"IP address {ip} is reachable.")
        else:
            print(f"IP address {ip} is unreachable.")

def calculate_average(data):
    return sum(data) / len(data)

def get_summary(data):
    return {
        "Min": min(data),
        "Max": max(data),
        "Average": calculate_average(data)
    }

while True:
    print("\nNetwork Utility Menu ")
    print("1. Test IP Reachability")
    print("2. Latency Summary Calculator")
    print("3. Exit")
    
    choice = input("Enter your choice (1/2/3): ")

    if choice == "1":
        check_ip_reachability()

    elif choice == "2":
        values = input("Enter comma-separated latency values: ")
        values_list = [float(x.strip()) for x in values.split(",")]

        summary = get_summary(values_list)
        print("\nLatency Summary:")
        print(summary)

    elif choice == "3":
        print("Exiting program...")
        break
    else:
        print("Invalid choice! Please enter 1, 2, or 3.")



**Day 11**

Task1
Created the Python Virtual Environment in VS Code to Achieve the Clean, Isolated Development Environment
**python -m venv my_python_env**


Task2
code:
# a = 10
# b = 25.5
# c = (a+b)
# d = 'Manju'
# print (c)
# print (d)

# a=(int(input("Enter Num: ")))
# b=(int(input("Enter Num: ")))
# c = (a + b)
# d = (a/b)
# print(c)
# print(d)

**Task3**
Calculator
import logging
logging.basicConfig(filename='log.txt',level=logging.WARNING)
logging.debug("This is debug")
logging.info("Program Started")
logging.warning("Warning Information")
logging.error("Error Info")
logging.critical("critical info")
num1 = float(input("Enter first number: "))
op = input("Enter operator (+, -, *, /): ")
num2 = float(input("Enter second number: "))

if op == '+':
    print("Result:", num1 + num2)
elif op == '-':
    print("Result:", num1 - num2)
elif op == '*':
    print("Result:", num1 * num2)
elif op == '/':
    if num2 == 0:
        print("Error: Cannot divide by zero!")
    else:
        print("Result:", num1 / num2)
else:
    print("Invalid operator")

**After This **
Done some work on the basic pyton Functions and all
Codes:
from function import add
result = add(5,10)
print("Result: ",result)
def add(a, b):
    return a + b



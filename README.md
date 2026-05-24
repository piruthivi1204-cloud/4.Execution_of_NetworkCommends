# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## program:
## client:
```python
import socket
s = socket.socket()
try:
    s.connect(('localhost', 8000))
    print("Connected to server.")
    print("Type commands or 'exit' to quit.\n")
    while True:
        cmd = input("Enter command: ").strip()
        if not cmd:
            continue
        s.send(cmd.encode())
        if cmd.lower() == 'exit':
            print("Closing connection...")
            break
        data = b""
        while True:
            part = s.recv(4096)
            data += part
            if len(part) < 4096:
                break
        print("\n----- RESULT -----")
        print(data.decode())
        print("------------------\n")
except ConnectionRefusedError:
    print("Server is not running!")
finally:
    s.close()
```
## server:
```python
import socket
import subprocess
s = socket.socket()
s.bind(('localhost', 8000))
s.listen(1)
print("Server listening on port 8000...")
c, addr = s.accept()
print("Connected:", addr)
while True:
    command = c.recv(1024).decode().strip()
    if not command or command.lower() == 'exit':
        print("Client disconnected.")
        break
    try:
        completed = subprocess.run(
            command,
            capture_output=True,
            text=True,
            shell=True
        )
        output = completed.stdout + completed.stderr
        if not output:
            output = "Command executed successfully."
    except Exception as e:
        output = f"Command failed: {e}"
    c.sendall(output.encode())
c.close()
s.close()
```
## Output
## server:
<img width="1464" height="888" alt="image" src="https://github.com/user-attachments/assets/a036e151-8531-400d-961d-f99c96c7291a" />
## client:
<img width="1557" height="811" alt="image" src="https://github.com/user-attachments/assets/1590932e-9bcf-4283-9615-a72045da61fe" />


## Result
Thus Execution of Network commands Performed 

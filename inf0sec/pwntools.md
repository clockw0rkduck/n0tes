
Codium setup required settings.json to contain the following: 
```
"python.analysis.extraPaths": [
    "~/.local/lib/Google/google_appengine",
    "~/.local/lib/Google/google_appengine/lib/flask-0.12" ]
```
in order for codium (VSCode on parrot) to autocomplete with intellisense


## netcat automation
conn = pwn.remote() to connect netcat style
conn.recv() to receive content. 
conn.send() to submit data. 


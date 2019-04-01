# tower-diagnose

tower-diagnose pulls the required details from Ansible Tower using Tower REST API and stores the output in a text file.

## Requirements

- Python 2.7+

## Installation and Setup

- Clone tower-diagnose GitHub repository
```
# git clone https://github.com/Ompragash/tower-diagnose.git
```
- Create tower.ini file adjacent to tower-diagnose script with the below contents or in path `/etc/ansible/tower.ini`

```
[tower]
url = https://tower.example.com
username = admin
password = passwd
```
## How To

- To get the available arguments pass `--help` or `-h` to tower-diagnose script:
```
# ./tower-diagnose -h
```

- To download the details and stdout of a specific job, pass JOB ID with `--jobs`:
```
# ./tower-diagnose --jobs 5
```
 Now, `tower-diagnose` will download details and stdout and store it in `job_5.txt` and `job_5_stdout.txt`.
 
 - Similarly you can pass multiple arguments like below:
 ```
 # ./tower-diagnose --jobs ID --inventory-update ID --project-update ID 
 ```
 

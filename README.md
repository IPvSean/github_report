# github_report
playbook to generate an HTML report on a Github organization

## directions
you need to add a group_vars/all to look something like this->

```
login_info:
  username: ipvsean
  password: YOURPASSWORD
github: "network-automation"
top_repos: 5
```

Explanation of variables
  - **login_info** is your user Github username and password
  - **github** is the github repo you are running the report on (in this case https://github.com/network-automation)
  - **top_repos: 5** is the amount of repos you want to poll for more information, in this case we just care about the top 5

## running the playbook

```
ansible-playbook github.yml
```

## results
Look under the time stamped folder for the HTML file (e.g. `report-2018-06-06-22-13/report-2018-06-06-22-13.html`)

---
title: GitHub Configuration
nav_order: 2
---

# <img style="vertical-align: middle;height:40px; width:40px;" src="https://raw.githubusercontent.com/bxyteam/satellite-test/refs/heads/main/docs/images/github.png"> Github Configuration


### <img style="vertical-align: middle;height:20px; width:20px;"  src="https://raw.githubusercontent.com/bxyteam/satellite-test/refs/heads/main/docs/images/settings.png"> New Repository Settings


> * ###### Add user name in the .env file, key GITHUB_OWNER 
> * ###### Create a new repository
> * ###### Add repository name in the .env file, key GITHUB_REPO 
> * ###### Go to https://github.com/settings/personal-access-tokens
>> - ###### Click generate new token
>>> * ###### Token settings
>>> * ###### Choose Only select repositories and pick your repo
>>> * ###### In Repository permissions select:
>>>> - ###### Commit statuses (Read and Write)
>>>> - ###### Merge queues (Read and Write) 
>>>> - ###### Pull requests (Read and Write)
>>>> - ###### Metadata (Mandatory selected by github)
>>> * ###### Save changes     
>> - ###### Copy token in the .env file, key GITHUB_TOKEN 

### <img style="vertical-align: middle;height:20px; width:20px;"  src="https://raw.githubusercontent.com/bxyteam/satellite-test/refs/heads/main/docs/images/file-key.png"> Update env file

###### fill env file with your github credentials

```bash
# github repository name
GITHUB_REPO=

# github repository owner (github username)
GITHUB_OWNER=

# github personal token
GITHUB_TOKEN=
```

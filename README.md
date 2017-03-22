# shellScripts

TO-DO<BR>
Much of the info hard-coded into the scripts should be placed in a dot file. 

Requirements:
AWS CLI 
>>installed
>>aws acccount credentials configured
>>aws s3 setup
>>aws IAM roles configured

local-s3<br>
Usage: local-s3 [--bucket = ~/Desktop/s3/<dir>/]<br>
Syncs specified local directory with aws bucket of the same name.<br> 
Fires aws sync command with [--acl public-read] and [--delete] flags.<br>

<br>
local-lambda<br>
Usage: local-lambda [--function=~/NetBeansProjects/lambda/<dir>/] [<-update> || <-create>]
Takes lambda functions from local machine, creates respective deploy package and pushes it to aws Lambda.<br>
Depends on running instance of local-s3 process. 

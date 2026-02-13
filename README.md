Task A Workflows
The purpose of this workflow is to demonstrate the concept of dependencies between jobs, meaning, one job cannot start until another job has successfully completed. If the independend job fails, the dependent job will never run.
Task B Workflows
The purpose of this worflow was to demonstrate how multiple jobs, on multiple host Operating Systems, can be run concurrently, to easily and efficiently scale to various operating systems.

Overall, both workflows demonstrate multiple key concepts of GitHub actions, such as runs-on, uses, and needs.

The 'runs-on' action specifies the operating system to run the job on, so for example, 'ubuntu-latest' would run it on the latest version of Ubuntu supported. 

The 'needs' action sets dependencies. If a job 'needs' another job, that job is dependent on the job in the 'needs' action. So if Job B 'uses' Job A, then, Job A must successfully finish before Job B can run. If Job A doesn't successfully complete, Job B will not run.

The uses action specifies a workflow file that can be reused to perform some given action, like 'checkout', for example. The 'checkout' action will checkout the code in the branch the script is being run on.

I didn't use env in this, but I could have used it in either workflow to hold some variable. In workflow A, it could have been the various echo values to their own env variable. Or in workflow B, I could have saved OS info into a variable and echo the variable instead.

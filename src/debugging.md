# Debugging errors and jobs not running 

Sometimes your jobs will fail (I know, sucks!), if you ever find yourself questioning why that happen this may help you: 

First thing to do is to check if your job failed because of some issue related to orca, to do that open the output file in your favorite text-editor and look at the last lines. A quick alternative is to use the `tail` command, which shows you the last lines of a file. 

If some error happened in a SCF procedure (if the issue is related to orca itself) you should see some error message at the very bottom of the output file. This error should at least clarify what went wrong in your calculation.

If the output file doesn't contain any error at the end of the file, then the issue might be hardware related. In this case, try to do the following:

- Resubmit the job and check in what node your job is being run (do that by issuing the `qstat -as` command, once it starts you can see information on what node is running your job), for example:

```
                                                            Req'd  Req'd   Elap
Job ID          Username Queue    Jobname    SessID NDS TSK Memory Time  S Time
--------------- -------- -------- ---------- ------ --- --- ------ ----- - -----
5090.ufsc       giliand* ufsc     tetrazol_*   7964   1   8   10gb 120:0 R 00:59
   Job run at Mon Apr 25 at 10:47 on (himalia:ncpus=8:mem=10485760kb)
5119.ufsc       giliand* ufsc     14_hess.i* 306745   1   8   10gb 120:0 R 32:23
   Job run at Tue Apr 26 at 22:13 on (io:ncpus=8:mem=10485760kb)
```

In this situation, the job 5090.ufsc is running on ***himalia*** and the job 5119.ufsc is running on ***io***.

- Connect through ssh to that node while logged in jupiter (`ssh himalia` for example) and check for temperature issues (running `sensors`). If you see the temperature of the CPU core's reaching 100 degrees, please contact [matheus]() or [vinicius]().


## Asking for help

If you ever cant understand what the hell is going on, or if you ever identify some kind of issue in the cluster, please [open an issue](https://github.com/geem-lab/cluster/issues/new/choose) in our [cluster](https://github.com/geem-lab/cluster) repository, this way we can keep track of what is happening and also have an archive for the solutions, if the problems ever happen again. 

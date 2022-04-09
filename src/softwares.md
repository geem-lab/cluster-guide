# Softwares

- ORCA

Usage: 

In your $HOME/bin folder in [jupiter]() there should already be a `job` script that you can use directly on yout .inp files.

In your .inp it should be specified both the `nprocs` and `maxcore` keywords, i.e. for a h2o_opt.inp file:

```
! HF def2-svp Opt 

%pal
nprocs 8 
end

%maxcore 2000

*xyzfile h2o.xyz 0 1 
```

Any doubts on the input please check the [orca input library](https://sites.google.com/site/orcainputlibrary/home).

To submit this job, run:

```console
$ job h2o.inp 1 8
``` 

Where the **1** means how many machines you're using and **8** means the number of cores. Or more generally:

```console
$ job file.inp $nmachines $nores
```

Use the default values and you'll be fine (1 machine and 8 procs).


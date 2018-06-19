# Singularity config for simg-chip container

A [Singularity Hub](https://www.singularity-hub.org/) definition.
Project specific.


If [Singularity](http://singularity.lbl.gov) is installed locally, the container can be build (needs root access) locally like this:

```bash
sudo singularity build simg-chip.simg Singularity
```

The container can also be downloaded from [Singularity Hub](https://www.singularity-hub.org/) without root access to the local machine like this:

```bash
singularity pull --name "simg-chip.simg" sschmeier/simg-chip:latest 
```

Then, it can be used, e.g.:

```bash
singularity exec simg-chip.simg bedtools --version
```

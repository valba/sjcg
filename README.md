# sjcg
A simple SGE job creator for Gaussian

This script creates a SGE (.job) file for a Gaussian (.gjf) input file for the [CCAR](https://ccar.uned.es/) cluster.

The goal of this script is to keep the log coming out from the SGE subsystem apart from the Gaussian log and to keep temporary files like checkpoint and read-write available for saving.

## Installation

Copy the [sjcg main script](https://github.com/valba/sjcg/blob/main/sjcg) into your '${HOME}/.local/bin/' directory.

Copy the templates directory into your '${HOME}/.local/' directory.

## Template Customization
The Gaussian template
Please, customize all parameters of the Gaussian template (queue, expiration time, etc.) to your needs before using it.

**Warning**: The Gaussian template considers the SCRATCH directory be located at your '${HOME}/SCRATCH/' directory.

## Usage

Once the Gaussian template has been modified to your needs, create a SGE job using the following command:

```
sjcg GAUSSIAN.gjf SGE.job
```

Once the SGE.job is created, review its content before submitting it to the queue.

```
qsub SGE.job
```

## License

GPL3.

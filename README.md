# sjcg
A simple SGE job creator for Gaussian

This script creates a SGE (.job) file for a Gaussian (.gjf) input file for the [CCAR](https://ccar.uned.es/) cluster.

The goal of this script is to keep the log coming out from the SGE subsystem apart from the Gaussian log and to keep temporary files like checkpoint and read-write available for saving.

## Installation

Copy the [sjcg](https://github.com/valba/sjcg/blob/main/sjcg) main script into your '${HOME}/.local/bin/' directory.

Give execution permission to the script:

```
chmod u+x ${HOME}/.local/bin/sjcg
```

Copy the [templates](https://github.com/valba/sjcg/tree/main/templates) directory into your '${HOME}/.local/' directory.

## Template Customization

Please, customize all parameters of the Gaussian template (queue, expiration time, etc.) according to your needs before using it.

**Warning**: The Gaussian template considers the SCRATCH directory be located at your '${HOME}/SCRATCH/' directory.

## Usage

Once the Gaussian template has been modified to your needs, create a SGE job using the following command:

```
sjcg GAUSSIAN.gjf SGE.job
```

Once the SGE.job is created, review its content before submitting it to the queue:

```
qsub SGE.job
```

## License
[![GPLv3_Logo](https://www.gnu.org/graphics/gplv3-or-later.png)](https://www.gnu.org/licenses/gpl-3.0.en.html)

GPLv3 or Later License.

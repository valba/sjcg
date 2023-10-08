# sjcg
SGE job creator for Gaussian

A simple script that creates a SGE (.job) file for a Gaussian (.gjf) input file for the [CCAR](https://ccar.uned.es/) cluster.

## Installation

Copy the sjcg main script into your '${HOME}/.local/bin/' directory.

Copy the templates directory into your '${HOME}/.local/' directory.

## Customization
Please, customize all parameters of the Gaussian template (queue, expiration time, etc.) to your needs before using it.

*Caution*: The template considers the SCRATCH directory be located at your '${HOME}/SCRATCH/' directory.

## Usage

Once the Gaussian template has been modified to your needs, create a SGE job using the following command:

`sjcg GAUSSIAN.gjf SGE.job`

Once the SGE.job is created, review its content before submitting it to the queue.

## License

GPL3.

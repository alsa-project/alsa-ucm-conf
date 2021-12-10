# alsa-ucm-conf
## ALSA Use Case Manager configuration

### Installation

Copy the ucm and ucm2 trees to the alsa-lib configuration directory
(usually located in /usr/share/alsa) including symlinks. The files
in the package root directory (README.md, LICENSE and VERSION)
files are extra (only informational).

### Validation

![Validate UCM configuration](https://github.com/alsa-project/alsa-ucm-conf/workflows/Validate%20UCM%20configuration/badge.svg?branch=master)

The UCM configurations are automatically validated using the UCM validator
available at https://github.com/alsa-project/alsa-tests/tree/master/python/ucm-validator .

If you create a pull request for new hardware, please, add also the
alsa-info.sh output to emulate this hardware in the UCM validator.

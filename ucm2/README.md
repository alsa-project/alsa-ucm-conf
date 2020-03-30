Use Case Configuration files
----------------------------

Library directories:

  platforms/
  codecs/
  dsps/

Those directories are not inspected for the list of available UCM
configurations. They contain files included from other UCMs.

UCM master configuration path lookup (by priority):

- {ucm_card_name}/{long_card_name}.conf
- {ucm_card_name}/{ucm_card_name}.conf
- {driver_name}/{long_card_name}.conf
- {driver_name}/{driver_name}.conf

For example:

- USB-Audio/Dell-WD15-Dock.conf
-- special configuration for the Dell docking station with USB soundcard
- TwoCardsMix/TwoCardsMix.conf
-- virtual UCM from two soundcards

Note: For the driver configurations, use always the real driver name
not the ucm card name configuration paths!

The driver name can be obtained using procfs like:

````
  cat /proc/asound/cards
  1 [NVidia         ]: HDA-Intel - HDA NVidia
                       HDA NVidia at 0xb5080000 irq 17

  driver name: HDA-Intel
  card short name: HDA NVidia
  card long name: HDA NVidia at 0xb5080000 irq 17
````

Syntax, value names
-------------------

https://git.alsa-project.org/?p=alsa-lib.git;a=blob;f=include/use-case.h

Some example gdml creator .py files and config files. 

The gdml files should go in `dunendggd\duneggd\SubDetector` and config files in `dunendggd\duneggd\Config`. When running ndggd, 
if you wish to simulate the whole nd hall (which is recommended if you're trying to have comparable samples to the genie ones), 
you should run `source dunendggd/build_hall.sh -o miniproduction1_tms_nosand`, modifying the TMS config file to the relevant one, and
changing your output file name.

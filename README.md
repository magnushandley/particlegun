# DUNE TMS (or similar) edep-sim particle gun

A description of how to create edep-sim outputs from a geant4 general particle source/particle gun. Most of the stages are better described by other repos, but the broad outline of the process is:

1) Create gdml using dunendggd (https://github.com/DUNE/duneggd), or just use an existing one. A few examples are given for creating the standard TMS gdml, the classic 'hybrid' case, or one where every 6th plane is replaced. Depending on what you need, be careful of ordering planes (i.e. whether you want planes to go xuvxuv or xuvxvu simplifies different things). For any new version of the TMS gdml creator you make, you will also need to create a companion config file (take the TMS one, and then change the module name to whatever you've made your new one).
Various gdml variations can be found in `/exp/dune/data/users/mhandley/full_hall_nosand_geometries`
3) Install edepsim, following the instructions from (https://github.com/ClarkMcGrew/edep-sim). There are some dependencies you will likely need to fight to make this work, but it isn't too painful.
4) Create a particle gun macro of your choosing (broad outline of the gps is given in the edep-sim readme, but more advanced use is well documented elsewhere for the geant4 gps, which is the same). You can specify initial particle distributions to be from a variety of shapes, from a point source, or from something more complicated. I provide macros for muon and pi0 guns generating events from a circle upstream of the front face of TMS.
5) Run TMS reconstruction as you see fit, which applies detector effects and converts to the proper tms reconstruction format.

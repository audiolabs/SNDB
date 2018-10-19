# Create the VSL part

Unforunately, creating the VSL part is a manual process.

To generate the VSL WAV files, the MIDI files have to be sampled with the corresponding VSL samples and saved under a specified filename. The corresponding MIDI files, samples and output WAV files can be found in the following table:


| filenames        | midi files            | samples                                                                |
|:-----------------|:----------------------|:-----------------------------------------------------------------------|
| 01P001Ffnp.wav   | piano_ff_VSL.mid      | / Special Edition patches/32 Keyboards+Mallets/01 Bosendorfer pedal up |
| 01P001Fmnp.wav   | piano_mf_VSL.mid      | / Special Edition patches/32 Keyboards+Mallets/01 Bosendorfer pedal up |
| 04Co001Fmnp.wav  | contrabass_mf_VSL.mid | / Special Edition patches/01 Solo Strings/33S DB sustain               |
| 04Co001Fpnp.wav  | contrabass_pp_VSL.mid | / Special Edition patches/01 Solo Strings/33S DB sustain               |
| 05Tru001Ffnp.wav | trumpet_ff_VSL.mid    | / Special Edition patches/22 Trumpets/12S TrC sustain                  |
| 05Tru001Fmnp.wav | trumpet_mf_VSL.mid    | / Special Edition patches/22 Trumpets/12S TrC sustain                  |
| 05Tru001Fpnp.wav | trumpet_pp_VSL.mid    | / Special Edition patches/22 Trumpets/12S TrC sustain                  |
| 06Tro001Ffnp.wav | trombone_ff_VSL.mid   | / Special Edition patches/23 Trombones/02S TTB sustain                 |
| 06Tro001Fmnp.wav | trombone_mf_VSL.mid   | / Special Edition patches/23 Trombones/02S TTB sustain                 |
| 06Tro001Fpnp.wav | trombone_pp_VSL.mid   | / Special Edition patches/23 Trombones/02S TTB sustain                 |
| 07H001Ffnp.wav   | horn_ff_VSL.mid       | / Special Edition patches/21 Horns/02S HOvn sustain                    |
| 07H001Fmnp.wav   | horn_mf_VSL.mid       | / Special Edition patches/21 Horns/02S HOvn sustain                    |
| 01P001Fpnp.wav   | piano_pp_VSL.mid      | / Special Edition patches/32 Keyboards+Mallets/01 Bosendorfer pedal up |
| 07H001Fpnp.wav   | horn_pp_VSL.mid       | / Special Edition patches/21 Horns/02S HOvn sustain                    |
| 08O001Ffnp.wav   | oboe_ff_VSL.mid       | / Special Edition patches/12 Oboes/12S OBvn sustain                    |
| 08O001Fmnp.wav   | oboe_mf_VSL.mid       | / Special Edition patches/12 Oboes/12S OBvn sustain                    |
| 08O001Fpnp.wav   | oboe_pp_VSL.mid       | / Special Edition patches/12 Oboes/12S OBvn sustain                    |
| 09B001Ffnp.wav   | bassoon_ff_VSL.mid    | / Special Edition patches/14 Bassoons/02S BA sustain                   |
| 09B001Fmnp.wav   | bassoon_mf_VSL.mid    | / Special Edition patches/14 Bassoons/02S BA sustain                   |
| 09B001Fpnp.wav   | bassoon_pp_VSL.mid    | / Special Edition patches/14 Bassoons/02S BA sustain                   |
| 10Cl001Ffnp.wav  | clarinet_ff_VSL.mid   | / Special Edition patches/13 Clarinets/12S CLBb sustain                |
| 10Cl001Fmnp.wav  | clarinet_mf_VSL.mid   | / Special Edition patches/13 Clarinets/12S CLBb sustain                |
| 10Cl001Fpnp.wav  | clarinet_pp_VSL.mid   | / Special Edition patches/13 Clarinets/12S CLBb sustain                |
| 02V001Ffnp.wav   | violin_ff_VSL.mid     | / Special Edition patches/01 Solo Strings/03S VI sustain               |
| 11F001Ffnp.wav   | flute_ff_VSL.mid      | / Special Edition patches/11 Flutes/12S FL1 sustain                    |
| 11F001Fmnp.wav   | flute_mf_VSL.mid      | / Special Edition patches/11 Flutes/12S FL1 sustain                    |
| 11F001Fpnp.wav   | flute_pp_VSL.mid      | / Special Edition patches/11 Flutes/12S FL1 sustain                    |
| 11F002Ffnp.wav   | flute_ff_VSL.mid      | / Special Edition patches/11 Flutes/22S FL2 sustain                    |
| 11F002Fmnp.wav   | flute_mf_VSL.mid      | / Special Edition patches/11 Flutes/22S FL2 sustain                    |
| 11F002Fpnp.wav   | flute_pp_VSL.mid      | / Special Edition patches/11 Flutes/22S FL2 sustain                    |
| 02V001Fmnp.wav   | violin_mf_VSL.mid     | / Special Edition patches/01 Solo Strings/03S VI sustain               |
| 02V001Fpnp.wav   | violin_pp_VSL.mid     | / Special Edition patches/01 Solo Strings/03S VI sustain               |
| 03Ce001Ffnp.wav  | cello_ff_VSL.mid      | / Special Edition patches/01 Solo Strings/23S VC sustain               |
| 03Ce001Fmnp.wav  | cello_mf_VSL.mid      | / Special Edition patches/01 Solo Strings/23S VC sustain               |
| 03Ce001Fpnp.wav  | cello_pp_VSL.mid      | / Special Edition patches/01 Solo Strings/23S VC sustain               |
| 04Co001Ffnp.wav  | contrabass_ff_VSL.mid | / Special Edition patches/01 Solo Strings/33S DB sustain               |

Additionally, this table exists in machine readable format in `build/VSL/VSL.json`

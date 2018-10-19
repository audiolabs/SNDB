# Building the Single Note Database

## Vienna Symphonic Library

Creating the VSL part is a manual process. For more information, please refer to [VSL/README.md](VSL/README.md).

## Remaining Databases

The SNDB consist of short signal excerpts, cut from longer signals in the originating databases. Each signal excerpt is defined in `build/build.json`:

|   ChosenChannel |   CuttingPosition_end |   CuttingPosition_start | FinalFilename          | OriginalFilename   | Stereo   | original_db   |
|----------------:|----------------------:|------------------------:|:-----------------------|:-------------------|:---------|:--------------|
|               0 |                304372 |                   39777 | 01Pia1F013f_np___0.wav | 01P001Ffnp         | False    | F             |
|               0 |                304383 |                   39789 | 01Pia1F013m_np___0.wav | 01P001Fmnp         | False    | F             |
|               0 |               1098379 |                  833793 | 01Pia1F016m_np___0.wav | 01P001Fmnp         | False    | F             |
|               0 |               9036241 |                 8771650 | 01Pia1F046m_np___0.wav | 01P001Fmnp         | False    | F             |
|               0 |               2290697 |                 2198581 | 01Pia1R043p_tr___0.wav | 011PFREP           | False    | R             |
|             ... |                   ... |                     ... |                    ... | ...                | ...      | ...           |

After placing all input files from all databases in a directory structure like

```
SNDB/
├── F/  # VSL
│   ├── 01P001Ffnp.wav
│   └── ...
├── R/  # RWC
│   ├── 011PFREP.wav
│   └── ...
├── G/  # McGill
│   ├── McGill Master Samples - CD 1 - Solo Strings an....wav
│   └── ...
├── M/  # MIS
│   ├── Bass.arco.ff.sulE.E1B1.wav
│   └── ...
└── out/
```

You can process these input files using

```python
import numpy as np
import pandas as pd
import soundfile as sf


df = pd.read_json('build/build.json')

for index, row in df.head().iterrows():
    data, fs = sf.read(
        "{}/{}.wav".format(row['original_db'], row['OriginalFilename']),
        always_2d=True
    )
    data = data[row['CuttingPosition_start']:row['CuttingPosition_end'], row['ChosenChannel']]

    sf.write(
        "out/{}".format(row['FinalFilename']),
        data,
        fs
    )
```

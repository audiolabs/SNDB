# Single Note Database

The SNDB [1] contains of 30883 single tones from **4 datasets** [2-5] holding **11 orchestra instruments**: piano, violin, cello, contrabass, trumpet, trombone, horn, oboe, bassoon, clarinet and flute. There are **5 different dynamics** (pp, p, mf, f and ff) and **42 different articulations** which are explained more fully in the datasheets of the original databases [2,3,5].

## Building

Please refer to [build/README.md](build/README.md) on how to create the SNDB out of the original datasets [2-5].

## Usage

The file `SNDB.json` contains all items and their attributes:

| artic   | db   | dyn   | instr   |   instr_nr | is_ot   |   midi |   multiples_nr | name                   | string   |
|:--------|:-----|:------|:--------|-----------:|:--------|-------:|---------------:|:-----------------------|:---------|
| np      | F    | f_    | Pia     |          1 | False   |     13 |              0 | 01Pia1F013f_np___0.wav | _        |
| np      | F    | m_    | Pia     |          1 | False   |     13 |              0 | 01Pia1F013m_np___0.wav | _        |
| sp      | R    | m_    | Cel     |          1 | False   |     51 |              0 | 03Cel1R051m_sp___0.wav | _        |
| tr      | R    | m_    | Cel     |          1 | False   |     56 |              0 | 03Cel1R056m_tr___0.wav | _        |
| sp      | R    | f_    | Cel     |          2 | False   |     77 |              0 | 03Cel2R077f_sp___0.wav | _        |
| ...     | ...  | ...   | ...     |        ... | ...     |    ... |            ... | ...                    | ...      |

All attributes and their meaning are described in the accompanying paper [1].

You can read this file into Pandas using

```python
import pandas as pd

df = pd.read_json('SNDB.json')
```

## References

 1. E. F. Feichtner and B. Edler, “Description of the Single Note Database SNDB,” in Audio Engineering Society Convention 145, New York, NY, USA, 2018.
 1. M. Goto, H. Hashiguchi, T. Nishimura, and R. Oka, “RWC music database: Music genre database and musical instrument sound database,” 2003.
 1. F. Opolko and J. Wapnick, “Mcgill university master samples (MUMS). 11 cd-rom set,” Faculty of Music, McGill University, Montreal, Canada, 1989.
 1. "Vienna Symphonic Library Special Edition 1 & 2," 2002.
 1. L. Fritts, “University of Iowa musical instrument samples,” http://theremin.music.uiowa.edu/MIS.html, 1997.

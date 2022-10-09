# obookmkr

Create chess opening book files to be read with obooksrv (see https://github.com/gkalab/obooksrv).

## Data format

obookmkr is based on Polyglot 1.4, by Fabien Letouzey. The only change is the output format of the created opening books.

The difference to the Polyglot format is as follows:

#### Original Polyglot format

    key    uint64
    move   uint16 
    weight uint16
    learn  uint32

#### obookmkr format

    key    uint64
    move   uint16 
    wins   uint8    // percentage of wins (0..100) for white in the given position
    draws  uint8    // percentage of draws (o..100) in the given position
    n      uint32   // number of games for the given position

Thus, the created books by obooksrv are not compatible with the Polyglot format.

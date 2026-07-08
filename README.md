# MetaCarvel - Scaffolder for metagenomes

MetaCarvel is an updated version of previous metagenome scaffolder Bambus 2. To run MetaCarvel, you will need:

- [Python 3.7.x](https://www.python.org/downloads/),
- [Samtools](http://samtools.sourceforge.net),
- [Bedtools](http://bedtools.readthedocs.io/en/latest/),
- [NetworkX](https://networkx.github.io/) >= 2.5, and
- [NumPy](http://www.numpy.org/).

Detailed documentation and a tutorial for installing and running MetaCarvel are
given on the [wiki](https://github.com/marbl/MetaCarvel/wiki).

# Usage

```
python run.py -h
usage: run.py [-h] -a ASSEMBLY -m MAPPING -d DIR [-r REPEATS] [-k KEEP]
              [-l LENGTH] [-b BSIZE] [-v VISUALIZATION]

MetaCarvel: A scaffolding tool for metagenomic assemblies

optional arguments:
  -h, --help            show this help message and exit
  -a ASSEMBLY, --assembly ASSEMBLY
                        assembled contigs
  -m MAPPING, --mapping MAPPING
                        mapping of read to contigs in bam format
  -d DIR, --dir DIR     output directory for results
  -r REPEATS, --repeats REPEATS
                        To turn repeat detection on
  -k KEEP, --keep KEEP  Set this to keep temporary files in output directory
  -l LENGTH, --length LENGTH
                        Minimum length of contigs to consider for scaffolding
                        in base pairs (bp)
  -b BSIZE, --bsize BSIZE
                        Minimum mate pair support between contigs to consider
                        for scaffolding
  -v VISUALIZATION, --visualization VISUALIZATION
                        To generate .db file for AsmViz visualization program
```

## Output

Running MetaCarvel will generate many files in the output directory;
if you are interested in the output of each step of the scaffolding process,
these files can be useful.

The **final output files** are:

- `scaffolds.fasta` (scaffold sequences, in FASTA format), and
- `scaffolds.agp` (scaffold paths on contigs, in AGP format).

# Publication and Citation

MetaCarvel is described in
[Ghurye _et al._, 2019](https://link.springer.com/article/10.1186/s13059-019-1791-3),
available in _Genome Biology_.

MetaCarvel can be cited as follows:

```tex
@article{metacarvel,
  title={MetaCarvel: linking assembly graph motifs to biological variants},
  author={Ghurye, Jay and Treangen, Todd and Fedarko, Marcus and Hervey IV, W Judson and Pop, Mihai},
  journal={Genome Biology},
  volume={20},
  number={1},
  pages={174},
  year={2019},
  publisher={Springer}
}
```

# Reporting issues

This tool is still under active development, and may have bugs. Please report
these and other issues as GitHub issues, so that we can continue working to
improve MetaCarvel.

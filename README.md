# HmmPy
HmmPy is a Pure-Python parser of --domtblout output of HMMER3 tested in its current version HMMER 3.1b2.

Inside it contain a single class extensible named HMMparser. It parsed the `HMMfile` in domtblout format from hmmscan or hmmsearch. Then, it can to be filtered (by Evalue, Bitscore, Coverage of HMM model) or it can show only the Best Bitscore domain for each query on hmmscan program output.

## Installation

Just download the file [`HmmPy.py`](https://github.com/EnzoAndree/HmmPy/blob/master/HmmPy.py).

## Usage

HmmPy can run directly without filter:

	python3 HmmPy.py MAPZ01.out.dm

Or with any combination of filters:

	python3 HmmPy.py -e 1e-5 -c 0.4 -u MAPZ01.out

Additionally you can use the python class in your code.

Using `python3 HmmPy.py -h` you can obtain more help.

## Output

The output is a tab separated text (TSV) with the same fields that the input file. This output can be shown in the stdout by default or in a file with -o flag.

### Notes
In this repocitories can be found an example with a run of hmmscan v3.1b2 using [dbCAN HMMs](http://csbl.bmb.uga.edu/dbCAN/download.php). The HmmPy usage was `python3 HmmPy.py MAPZ01.out.dm -e 1e-5 -c 0.4 -u -o test.tsv`

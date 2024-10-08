# GeneMaster Package [DEMO]

## Description

The GeneMaster project is a comprehensive bioinformatics package designed to facilitate the analysis and manipulation of
genetic sequences, including DNA and RNA. It provides a robust set of data types and operations tailored to genomic
research, allowing users to perform tasks such as reverse complement generation, GC content calculation, RNA
transcription, and protein translation. Additionally, it includes advanced algorithms for solving problems like the
shortest superstring, longest common subsequence, and motif finding. The package also supports parsing FASTA format
files and includes thorough testing modules to ensure accuracy and reliability in genetic sequence analysis.

## Install

To get started with GeneMaster, follow these steps to install the package and its dependencies.

### Using pip

The easiest way to install GeneMaster is through pip. Open your terminal or command prompt and

```commandline
pip install GeneMaster
```

## Features

### DNA Sequence

- Manage DNA Sequences with Ease: Effortlessly handle and manipulate DNA sequences with straightforward methods.

```python
from GeneMaster import DNA

dna_seq = DNA('AGCCT')
dna_seq2 = DNA('CGATGA')

print(dna_seq.sequence)
print(dna_seq.complement)
print(dna_seq.length)
print(dna_seq+dna_seq2)
```

```
Output:

AGCCT
AGGCT
5
AGCCTCGATGA
```

- Visualize DNA Sequences: Generate a visual representation of the DNA sequence to aid in understanding.

```python
from GeneMaster import DNA

dna = DNA('AGCCT')
print(dna.visualize)
```

```
Output:

5'   A-G-C-C-T   3'
     │ │ │ │ │   5
3'   T-C-G-G-A   5'
```

### RNA Sequence

- Examine RNA Properties: Similar to DNA, view various properties of RNA sequences.

```python
from GeneMaster import RNA

rna = RNA('AGUUACU')
print(rna.sequence)
print(rna.length)
```

```
Output:

AGUUACU
7
```

- Visualize RNA Sequences: Create a visual representation of the RNA sequence for better analysis.

```python
from GeneMaster import RNA

rna = RNA('AGUUACU')
print(rna.visualize)
```

```
Output:

5'   A-G-U-U-A-C-U   3'
     | | | | | | |   7
```

### DNA & RNA Algorithms

- `revComplement()` Returns the reverse complement of the DNA sequence. 
- `gc_content()` Provides the GC content ratio of the DNA strand.
- `transcribe_to_rna()` Returns the RNA sequence resulting from transcription.
- `transcribe_to_dna()` Returns the DNA sequence resulting from transcription.
- `start_stop_codons()` Identifies the start and stop codons in mRNA, determining where the translation process begins and ends.
- `find_orf()` Identifies open reading frames (ORFs) within a DNA sequence, which are potential regions for protein-coding genes.
- `extract_exons()` Extracts exon regions from a given DNA or RNA sequence.
- `extract_introns()` Extracts intron regions from a DNA or RNA sequence.
- `find_motif(motif)` Searches for occurrences of a specified motif within a DNA or RNA sequence.
- `melting_temperature()` Calculates the melting temperature for DNA sequence.
- `pairwise_align(seq)` Aligns main DNA sequence to another sequence
- `codon_bias()` Analyzes codon usage to determine codon bias within a DNA or RNA sequence.
- `translation()` Translates DNA ot RNA sequence into Protein sequence.
- `kmer()` Analyzes the frequent k-mers within a DNA or RNA sequence.


### Special Algorithms
- `find_shared_motif(sequences)` Returns a shared motif sequence for a list of DNA or RNA sequences.
- `longest_common_subsequence(sequences)` Superfast algorithm returns the longest common subsequence for a list of DNA or RNA sequences.
- `hamming_distance(seq1,seq2)` Computes the difference between two DNA or RNA sequences.
- `shortest_superstring(sequecnes)` Returns the shortest sequence that includes all sequences.

### Credits
The development of GeneMaster would not have been possible without the contributions and support of the following individuals and resources:

**Ahmed Osama**: Creator and primary developer of the GeneMaster package.
For further information about these contributions and resources, please visit their respective websites and repositories.

Repository : [GeneMaster](https://github.com/AhmedOs13/GeneMaster)
PyPi: [GeneMaster](https://pypi.org/project/GeneMaster/)

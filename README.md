# Computational Theory Coursework - Atlantic Technological University

This repository contains my solutions to the Computational Theory problems for my 4th-year module during the Winter 2026 / 2027 semester.

The main submission file is [`problems.ipynb`](problems.ipynb), which develops a complete SHA-256 implementation in Python using NumPy.

## Requirements

- Python 3.10 or later
- Jupyter Notebook or JupyterLab
- NumPy

The packages listed in [`requirements.txt`](requirements.txt) provide the required environment.

## Setup

Clone the repository and move into its directory:
```bash
git clone https://github.com/karoluciecha/c-college-coursework.git
cd computational-theory-coursework
```

Create and activate a virtual environment:
```bash
python3.13 -m venv .venv
source .venv/bin/activate
```

On Windows, activate the environment with:
```bash
.venv\Scripts\activate
```

Install the dependencies:
```bash
python -m pip install -r requirements.txt
```

Verify the installation:
```bash
python -m pip list
which python
```

## Running the Notebook

Start Jupyter Notebook:
```bash
jupyter notebook `problems.ipynb`
```

Run the notebook from top to bottom.

The notebook should be run with a restarted kernel to ensure that all cells execute sequentially and reproducibly.

## Repository Structure
```text
.
├── `AGENTS.md`
├── `problems.ipynb`
├── `README.md`
└── `requirements.txt`
```

## References

The implementation is based on the following sources:

### Standard

1. NIST, [FIPS PUB 180-4: Secure Hash Standard (SHS)](https://doi.org/10.6028/NIST.FIPS.180-4), August 2015. The specification of SHA-256: words, padding, constants and the compression function. A copy is included as `NIST.FIPS.180-4.pdf`.

### Test values

2. NIST, [SHA-256 example](https://csrc.nist.gov/CSRC/media/Projects/Cryptographic-Standards-and-Guidelines/documents/examples/SHA256.pdf). A worked example for the message `"abc"`, including its padded block.

### NumPy

3. NumPy, [Data types](https://numpy.org/doc/stable/user/basics.types.html). Fixed-size integer types such as `uint32`, and how overflow behaves.
4. NumPy, [Data type objects (`dtype`)](https://numpy.org/doc/stable/reference/arrays.dtypes.html). Includes the byte-order codes such as `">u4"`.
5. NumPy, [`numpy.array`](https://numpy.org/doc/stable/reference/generated/numpy.array.html). Creates arrays from lists.
6. NumPy, [`numpy.add`](https://numpy.org/doc/stable/reference/generated/numpy.add.html). Addition with a chosen result type.
7. NumPy, [`numpy.frombuffer`](https://numpy.org/doc/stable/reference/generated/numpy.frombuffer.html). Turns `bytes` into an array.
8. NumPy, [`numpy.reshape`](https://numpy.org/doc/stable/reference/generated/numpy.reshape.html). Cuts a list of words into rows of blocks.

### Python and text encoding

9. Python Software Foundation, [`bytes` objects](https://docs.python.org/3/library/stdtypes.html#bytes-objects), [`str.encode`](https://docs.python.org/3/library/stdtypes.html#str.encode) and [`int.from_bytes`](https://docs.python.org/3/library/stdtypes.html#int.from_bytes). How text becomes bytes, and how bytes become integers.
10. MDN Web Docs, [UTF-8](https://developer.mozilla.org/en-US/docs/Glossary/UTF-8). The text encoding used to turn characters into bytes.

## Progress Tracking

GitHub Issues are used to track the progress of Problems 1 - 6. Each issue records the relevant work, tests, explanations, and completion status for that problem.
### Definition

Given a positive number n. Let V be a set of 2n integers 1, 2, ..., 2n.

A starter balanced tournament design (SBTD) of order n, denoted as S2n, is an n x (2n-1) array of all pairs of set V, such that

- Each cell of the array contains a pair of elements from V .
- Every pair of elements from V is contained in some cell.
- Each element of V is contained in each column.
- Each element is contained at most two times in each row.
- Each column is a starter.

### Directories structure

SBTD schedules are arranged in corresponding S2N instances and they are differentiated by their hash values.

```txt
S2N/
  S2N_schedule_<hashValue0>.txt
  S2N_schedule_<hashValue1>.txt
  S2N_schedule_<hashValue2>.txt
  ...
```

Example of a SBTD S12 schedule `S0012/S0012_schedule_1c63b69a3ce5b4976a37a7af3ec23f16.txt`

```txt
[(   1,   2), (   2,   3), (   3,   4), (   4,   5), (   5,   6), (   6,   7), (   7,   8), (   8,   9), (   9,  10), (  10,  11), (  11,  12)]
[(   5,   7), (   8,  10), (   6,   8), (  10,  12), (   9,  11), (  12,   1), (   1,   3), (   2,   4), (   4,   6), (   7,   9), (   3,   5)]
[(   8,  11), (   6,   9), (   9,  12), (   3,   6), (   4,   7), (   5,   8), (  12,   2), (  11,   1), (   2,   5), (   1,   4), (   7,  10)]
[(   6,  10), (   1,   5), (  10,   1), (   7,  11), (  12,   3), (  11,   2), (   5,   9), (   3,   7), (   8,  12), (   2,   6), (   4,   8)]
[(  12,   4), (   7,  12), (   2,   7), (   9,   1), (  10,   2), (   4,   9), (   6,  11), (   5,  10), (  11,   3), (   3,   8), (   1,   6)]
[(   3,   9), (  11,   4), (   5,  11), (   2,   8), (   8,   1), (  10,   3), (   4,  10), (   6,  12), (   1,   7), (  12,   5), (   9,   2)]
```

### Validating script
The script `validate_solutions.py` is used to validate schedules in all instances. One can pass `max_N` argument to specify the validation range from S8 to S2N.

```sh
$ python3 validate_solutions.py <max_N> # check all instances from S8 to S(2*max_N)
$ python3 validate_solutions.py 30 # check all instances from S8 to S60
$ python3 validate_solutions.py # default value 54 of max_N will be used
```

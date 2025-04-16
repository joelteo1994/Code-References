# 🧠 Python Data Types & Data Structures Cheatsheet

A concise reference for Python primitives, collections, and scientific computing types.

---

## 🔢 Built-in Data Types (Primitives)

| Type       | Example           | Notes                                           |
|------------|-------------------|--------------------------------------------------|
| `int`      | `x = 42`          | Arbitrary precision integers                     |
| `float`    | `y = 3.14`        | 64-bit floating point numbers                   |
| `bool`     | `z = True`        | Boolean values: `True`, `False`                 |
| `str`      | `s = "hello"`     | Immutable sequence of Unicode characters        |
| `bytes`    | `b = b'abc'`      | Immutable sequence of raw bytes                 |
| `complex`  | `c = 3 + 4j`      | Complex numbers with real and imaginary parts   |
| `NoneType` | `None`            | Represents the absence of a value               |

---

## 📦 Built-in Data Structures

| Structure      | Example                           | Key Features                                     |
|----------------|-----------------------------------|--------------------------------------------------|
| `list`         | `[1, 2, 'a']`                     | Ordered, mutable, heterogeneous                  |
| `tuple`        | `(1, 2, 3)`                       | Ordered, immutable                              |
| `set`          | `{1, 2, 3}`                       | Unordered, unique elements                      |
| `frozenset`    | `frozenset([1, 2])`               | Immutable set                                   |
| `dict`         | `{'a': 1, 'b': 2}`                | Key-value pairs, fast lookups                   |
| `range`        | `range(0, 10)`                    | Memory-efficient sequence of integers (lazy)    |
| `enumerate`    | `enumerate(['a', 'b'])`           | Iterable of (index, item) pairs                 |
| `zip`          | `zip([1,2], ['a','b'])`           | Paired iterable tuples                          |

---

## 📊 NumPy Structures

| Type              | Example                                        | Notes                                                    |
|-------------------|------------------------------------------------|----------------------------------------------------------|
| `np.array`        | `np.array([1, 2, 3])`                          | Homogeneous, fast numerical operations                   |
| `dtype`           | `np.array([1], dtype='float32')`              | Controls type precision (`int32`, `float64`, etc.)       |
| `object`          | `np.array([1, 'a'], dtype=object)`             | Catch-all for mixed types, slower performance            |
| `ndim`            | `arr.ndim`                                     | Number of dimensions (axes)                             |
| `shape`           | `arr.shape`                                    | Tuple showing dimensions                                 |
| `reshape`         | `arr.reshape(2, 3)`                            | Change shape without modifying data                      |
| `broadcasting`    | `arr + scalar`                                 | Implicit expansion to match shapes                       |
| `vectorization`   | `arr * 2`                                      | Element-wise ops without loops                          |
| `masked arrays`   | `np.ma.masked_array(data, mask=mask_array)`   | Arrays with invalid entries masked out                   |

---

## 🔥 PyTorch Structures

| Type               | Example                                     | Notes                                                    |
|--------------------|---------------------------------------------|----------------------------------------------------------|
| `torch.tensor`     | `torch.tensor([1, 2, 3])`                   | Multi-dimensional tensor for ML & deep learning          |
| `dtype`            | `torch.float32`, `torch.long`              | Controls tensor precision and internal operations        |
| `device`           | `tensor.to('cuda')`, `tensor.device`       | Controls CPU/GPU memory placement                        |
| `grad`             | `.requires_grad_(True)`                    | Enables autograd for backpropagation                     |
| `shape`            | `tensor.shape`                             | Tensor dimensions                                        |
| `unsqueeze`        | `tensor.unsqueeze(0)`                      | Adds a dimension (e.g., for batch)                       |
| `permute`          | `tensor.permute(1, 0)`                     | Rearranges dimensions                                    |
| `view`             | `tensor.view(-1, 3)`                       | Similar to reshape                                       |
| `detach()`         | `tensor.detach()`                          | Gets a tensor without gradient tracking                  |
| `clone()`          | `tensor.clone()`                           | Deep copy of the tensor                                  |

---

## 🧰 Specialty & Abstract Data Types

| Type                        | Use Case                                                       |
|-----------------------------|------------------------------------------------------------------|
| `collections.deque`        | Double-ended queue, fast append/pop from both ends              |
| `collections.Counter`      | Frequency count of hashable elements                            |
| `collections.defaultdict`  | Dictionary with default factory for missing keys                |
| `collections.OrderedDict`  | Dict that remembers insertion order (Python <3.7)               |
| `collections.namedtuple`   | Tuple subclass with named fields                                |
| `dataclasses.dataclass`    | Declarative, immutable or mutable objects with built-in methods |
| `typing.List`, `Dict`      | Static type hints for code quality and checking                 |
| `pandas.DataFrame`         | Labeled 2D tabular structure for structured data                |
| `pandas.Series`            | Labeled 1D structure, column or single variable                 |
| `array.array`              | Homogeneous numeric arrays (compact alternative to list)        |
| `heapq`                    | Priority queue based on heap queue algorithms                   |
| `queue.Queue`              | Thread-safe FIFO queue                                          |
| `itertools`                | Functional-style iterators for looping logic                    |
| `functools.lru_cache`      | Caching wrapper to memoize expensive function calls             |

---

## 🧪 Optional Extensions (Not Covered Here)

- `TensorFlow`: `tf.Tensor`, `tf.Variable`
- `Polars`: `pl.DataFrame`, `pl.Series`
- `DuckDB`: SQL-engine backed DataFrames
- `xarray`: Labeled N-dimensional arrays

---

> 💡 Tip: Use native Python types for flexibility, NumPy/PyTorch for speed and numerical ops, and Pandas for tabular data!

---
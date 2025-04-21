# 🧠 Python Data Types & Data Structures Cheatsheet

A concise reference for Python primitives, collections, and scientific computing types — with real-world analogies to help you remember.

---

## ✅ Categories

- **Data Types**: Individual atomic values (e.g. `int`, `str`, `bool`)
- **Data Structures**: Containers or systems for organizing multiple values (e.g. `list`, `dict`, `np.array`)

---

## 🔢 Primitive Data Types (Atomic Values)

| Type         | Example       | Analogy 🧠                                      | Description                                |
|--------------|---------------|------------------------------------------------|--------------------------------------------|
| `int`        | `x = 42`      | 💎 A **single pebble**                         | Numeric integer value                      |
| `float`      | `y = 3.14`    | 💎 A **single pebble**                         | Numeric float value                        |
| `bool`       | `z = True`    | 🔘 A **light switch**                          | Binary logic values                        |
| `str`        | `s = "hello"` | 🧵 A **necklace of letters**                   | Sequence of characters                     |
| `bytes`      | `b = b'abc'`  | 📦 A **box of raw data**                       | Immutable binary data                      |
| `complex`    | `c = 3 + 4j`  | 🌪️ A **tornado core**                          | Complex number with real + imaginary parts |
| `NoneType`   | `None`        | ❌ An **empty placeholder**                    | Represents a missing or null value         |

---

## 📦 Built-in Data Structures

| Structure      | Example                        | Analogy 🧠                                    | Key Features                                     |
|----------------|--------------------------------|----------------------------------------------|--------------------------------------------------|
| `list`         | `[1, 2, 'a']`                  | 🪣 A **bucket**                               | Ordered, mutable, heterogeneous                  |
| `tuple`        | `(1, 2, 3)`                    | 📦 A **sealed box**                           | Ordered, immutable                              |
| `set`          | `{1, 2, 3}`                    | 🪪 A **unique-membership club**               | Unordered, unique elements                      |
| `frozenset`    | `frozenset([1, 2])`            | 🧊 An **ice-locked club**                     | Immutable set                                   |
| `dict`         | `{'a': 1, 'b': 2}`             | 📛 A **segmented bucket with labels**         | Key-value pairs, fast lookups                   |
| `range`        | `range(0, 10)`                 | 🚿 A **preset faucet**                        | Memory-efficient sequence of integers (lazy)    |
| `enumerate`    | `enumerate(['a', 'b'])`        | 🪪🔢 A **numbered checklist**                  | Iterable of (index, item) pairs                 |
| `zip`          | `zip([1,2], ['a','b'])`        | 🔗 A **zipper** — pairs items side-by-side    | Paired iterable tuples                          |

---

## 📊 NumPy Structures

| Type              | Example                                        | Analogy 🧠                            | Notes                                                    |
|-------------------|------------------------------------------------|--------------------------------------|----------------------------------------------------------|
| `np.array`        | `np.array([1, 2, 3])`                          | 🔢 A **numeric grid**                 | Homogeneous, fast numerical operations                   |
| `dtype`           | `np.array([1], dtype='float32')`              | 🧬 A **precision label**              | Controls type precision (`int32`, `float64`, etc.)       |
| `object`          | `np.array([1, 'a'], dtype=object)`             | 🎭 A **wildcard container**           | Catch-all for mixed types, slower performance            |
| `ndim`            | `arr.ndim`                                     | 📐 A **dimension ruler**              | Number of dimensions (axes)                             |
| `shape`           | `arr.shape`                                    | 📏 A **size blueprint**               | Tuple showing dimensions                                 |
| `reshape`         | `arr.reshape(2, 3)`                            | 🧱 A **reformed block**               | Change shape without modifying data                      |
| `broadcasting`    | `arr + scalar`                                 | 📡 A **signal spreader**              | Implicit expansion to match shapes                       |
| `vectorization`   | `arr * 2`                                      | 🏎️ A **parallel multiplier**         | Element-wise ops without loops                          |
| `masked arrays`   | `np.ma.masked_array(data, mask=mask_array)`   | 🎭 A **selectively hidden grid**      | Arrays with invalid entries masked out                   |

---

## 🔥 PyTorch Structures

| Type               | Example                                     | Analogy 🧠                                | Notes                                                    |
|--------------------|---------------------------------------------|------------------------------------------|----------------------------------------------------------|
| `torch.tensor`     | `torch.tensor([1, 2, 3])`                   | 🧠💪 A **tensor engine**                   | Multi-dimensional tensor for ML & deep learning          |
| `dtype`            | `torch.float32`, `torch.long`              | 🧬 A **precision label**                  | Controls tensor precision and internal operations        |
| `device`           | `tensor.to('cuda')`, `tensor.device`       | 🧳 A **location tag**                     | Controls CPU/GPU memory placement                        |
| `grad`             | `.requires_grad_(True)`                    | 🔁 A **sensitivity switch**               | Enables autograd for backpropagation                     |
| `shape`            | `tensor.shape`                             | 📏 A **size blueprint**                   | Tensor dimensions                                        |
| `unsqueeze`        | `tensor.unsqueeze(0)`                      | 📦 A **dimensional wrapper**              | Adds a dimension (e.g., for batch)                       |
| `permute`          | `tensor.permute(1, 0)`                     | 🔄 A **dimension rotator**                | Rearranges dimensions                                    |
| `view`             | `tensor.view(-1, 3)`                       | 🧩 A **reshape lens**                     | Similar to reshape                                       |
| `detach()`         | `tensor.detach()`                          | ✂️ A **gradient snipper**                 | Gets a tensor without gradient tracking                  |
| `clone()`          | `tensor.clone()`                           | 📋 A **tensor copy**                      | Deep copy of the tensor                                  |

---

## 🧰 Specialty & Abstract Data Types

| Type                        | Analogy 🧠                                    | Use Case                                                       |
|-----------------------------|----------------------------------------------|------------------------------------------------------------------|
| `collections.deque`        | 🎠 A **carousel bin**                         | Double-ended queue, fast append/pop from both ends              |
| `collections.Counter`      | 🧮 A **tally machine**                        | Frequency count of hashable elements                            |
| `collections.defaultdict`  | 🪄📛 A **magical drawer set**                 | Dictionary with default factory for missing keys                |
| `collections.OrderedDict`  | 🧾 A **historical log**                       | Dict that remembers insertion order (Python <3.7)               |
| `collections.namedtuple`   | 🧱 A **labeled box**                          | Tuple subclass with named fields                                |
| `dataclasses.dataclass`    | 📐 A **blueprint-bound record**              | Declarative, immutable or mutable objects with built-in methods |
| `typing.List`, `Dict`      | 🧭 A **type contract**                        | Static type hints for code quality and checking                 |
| `pandas.DataFrame`         | 📊 A **full spreadsheet**                     | Labeled 2D tabular structure for structured data                |
| `pandas.Series`            | 📋 A **spreadsheet column**                   | One-dimensional labeled array                                   |
| `array.array`              | 💼 A **compact numeric box**                 | Homogeneous numeric arrays (compact alternative to list)        |
| `heapq`                    | ⛏️ A **min-heap excavator**                  | Priority queue based on heap queue algorithms                   |
| `queue.Queue`              | 📬 A **mailbox line**                        | Thread-safe FIFO queue                                          |
| `itertools`                | 🔁 A **combinator toolkit**                  | Functional-style iterators for looping logic                    |
| `functools.lru_cache`      | 🧠 A **smart memory**                         | Caching wrapper to memoize expensive function calls             |

---

## 🧪 Optional Extensions (Not Covered Here)

- `TensorFlow`: `tf.Tensor`, `tf.Variable`
- `Polars`: `pl.DataFrame`, `pl.Series`
- `DuckDB`: SQL-engine backed DataFrames
- `xarray`: Labeled N-dimensional arrays

---

> 💡 Tip: Use native Python types for flexibility, NumPy/PyTorch for speed and numerical ops, and Pandas for tabular data!

---

Contributions welcome 🙌

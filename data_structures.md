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

# 📘 Python Core Collections Cheatsheet

A focused reference on Python's essential built-in collection types:
`tuple`, `list`, `set`, `dict`, `range`, `enumerate`, `zip`

---

## ✅ Summary Table

| Type        | Ordered | Mutable | Allows Duplicates | Indexable | Key Use Case                          |
|-------------|---------|---------|-------------------|-----------|---------------------------------------|
| `tuple`     | ✅       | ❌       | ✅                 | ✅         | Fixed records, coordinates, keys      |
| `list`      | ✅       | ✅       | ✅                 | ✅         | General-purpose sequence              |
| `set`       | ❌       | ✅       | ❌                 | ❌         | Unique membership, deduplication      |
| `dict`      | ✅*      | ✅       | ❌ (keys)          | ✅ (keys) | Fast key-value mapping                |
| `range`     | ✅       | ❌       | ✅                 | ✅         | Memory-efficient integer iteration    |
| `enumerate` | ✅       | ❌       | ✅                 | ✅         | Indexed iteration in `for` loops      |
| `zip`       | ✅       | ❌       | ✅                 | ❌         | Parallel iteration in `for` loops     |

---

## 🔹 `tuple` Methods

```python
t = (1, 2, 3)
```

| Method         | Description                        | Output                | Alters Original? |
|----------------|------------------------------------|------------------------|-------------------|
| `t[0]`         | Indexing                           | `1`                    | ❌                |
| `t.index(2)`   | Find index of element              | `1`                    | ❌                |
| `t.count(3)`   | Count occurrences                  | `1`                    | ❌                |
| `t + (4,)`     | Concatenate with another tuple     | `(1, 2, 3, 4)`         | ❌ (new object)   |

---

## 🔸 `list` Methods

```python
lst = [1, 2, 3]
```

| Method            | Description                          | Output / Effect         | Alters Original? |
|-------------------|--------------------------------------|--------------------------|-------------------|
| `lst.append(4)`   | Add item to end                      | `[1, 2, 3, 4]`           | ✅                |
| `lst.extend([5,6])` | Append multiple items              | `[1, 2, 3, 4, 5, 6]`     | ✅                |
| `lst.insert(1, 10)` | Insert at index 1                  | `[1, 10, 2, 3, 4, 5, 6]` | ✅                |
| `lst.pop()`       | Remove and return last item         | `6`                      | ✅                |
| `lst.remove(10)`  | Remove first occurrence of 10       | `[1, 2, 3, 4, 5]`        | ✅                |
| `lst.index(3)`    | Get index of 3                      | `2`                      | ❌                |
| `lst.count(4)`    | Count occurrences of 4              | `1`                      | ❌                |
| `lst.sort()`      | Sort in-place                       | `[1, 2, 3, 4, 5]`        | ✅                |
| `sorted(lst)`     | Return sorted copy                  | `[1, 2, 3, 4, 5]`        | ❌ (new object)   |
| `len(lst)`        | Number of elements                  | `5`                      | ❌                |

---

## 🪪 `set` Methods

```python
s = {1, 2, 3}
```

| Method             | Description                          | Output / Effect        | Alters Original? |
|--------------------|--------------------------------------|-------------------------|-------------------|
| `s.add(4)`         | Add an element                      | `{1, 2, 3, 4}`           | ✅                |
| `s.update([5, 6])` | Add multiple elements               | `{1, 2, 3, 4, 5, 6}`     | ✅                |
| `s.remove(1)`      | Remove element or raise error       | `{2, 3, 4, 5, 6}`        | ✅                |
| `s.discard(2)`     | Remove element if exists            | `{3, 4, 5, 6}`           | ✅                |
| `s.clear()`        | Remove all elements                 | `set()`                 | ✅                |
| `len(s)`           | Count of elements                   | Integer (e.g. `4`)       | ❌                |
| `3 in s`           | Membership test                     | `True` / `False`         | ❌                |
| `set([1, 1, 2])`   | Remove duplicates from list         | `{1, 2}`                 | ❌ (new object)   |

---

## 📛 `dict` Methods

```python
d = {'a': 1, 'b': 2}
```

| Method              | Description                        | Output / Effect        | Alters Original? |
|---------------------|------------------------------------|-------------------------|-------------------|
| `d['c'] = 3`        | Assign value to key                | `{'a': 1, 'b': 2, 'c': 3}` | ✅              |
| `d.get('d', 0)`     | Get value or default               | `0`                      | ❌                |
| `d.pop('a')`        | Remove key and return value        | `1`, `{'b': 2, 'c': 3}`   | ✅                |
| `d.update({'e': 5})`| Add or overwrite key-value pairs  | `{'b': 2, 'c': 3, 'e': 5}`| ✅                |
| `d.keys()`          | View all keys                      | `dict_keys(['b', 'c', 'e'])` | ❌           |
| `d.values()`        | View all values                    | `dict_values([2, 3, 5])` | ❌                |
| `d.items()`         | View all key-value pairs           | `dict_items([('b', 2), ('c', 3), ('e', 5)])` | ❌ |
| `len(d)`            | Number of key-value pairs          | `3`                      | ❌                |

---

## 🚿 `range` Methods

```python
r = range(1, 6)
```

| Method       | Description                          | Output                | Alters Original? |
|--------------|--------------------------------------|------------------------|-------------------|
| `range(...)` | Create range object                  | `range(1, 6)`          | ❌                |
| `list(r)`    | Convert to list                      | `[1, 2, 3, 4, 5]`       | ❌ (new object)   |
| `r[0]`       | Indexing                             | `1`                    | ❌                |
| `len(r)`     | Number of values                     | `5`                    | ❌                |

> 🔁 Typically used in `for` loops for controlled iteration.

---

## 🔢 `enumerate`

```python
words = ['a', 'b']
```

| Method / Use           | Description                          | Output                          | Alters Original? |
|------------------------|--------------------------------------|----------------------------------|-------------------|
| `enumerate(words)`     | Add index to iterable                | `enumerate` object               | ❌                |
| `list(enumerate(...))` | Convert to list of (index, item)    | `[(0, 'a'), (1, 'b')]`           | ❌ (new object)   |

> 🔁 Best used in `for` loops to access index and value at once.

---

## 🔗 `zip`

```python
names = ['a', 'b']
scores = [10, 20]
```

| Method / Use       | Description                          | Output                          | Alters Original? |
|--------------------|--------------------------------------|----------------------------------|-------------------|
| `zip(names, scores)`| Combine iterables into pairs        | `zip` object                     | ❌                |
| `list(zip(...))`   | Convert to list of tuples            | `[('a', 10), ('b', 20)]`         | ❌ (new object)   |

> 🔁 Ideal for `for` loops to iterate in parallel.

---

> 🧠 Tip: Lists and dicts are go-to structures; use sets for uniqueness, tuples for fixed pairs, and zip/enumerate/range in loops.

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

# 📘 Resumen de métodos y formas en Pandas (Series y DataFrame)

---
## 📌 Series

- **Constructor principal**
  - `pd.Series(data=None, index=None, dtype=None, name=None, copy=False, fastpath=False)`

- **Acceso y atributos**
  - `s.index`
  - `s.dtype`
  - `s.array`
  - `s.to_numpy(dtype=None, copy=False, na_value=NoDefault)`
  - `s.name`

- **Indexación**
  - `s.iloc[...]`
  - `s.loc[...]`
  - `s[...]` (por etiqueta)
  - `s.get(key, default=None)`

- **Operaciones**
  - `np.exp(s)` (ufuncs de NumPy aplicables)
  - `s + s`
  - `s * 2`
  - `s.iloc[...] + s.iloc[...]`

- **Atributos y renombrado**
  - `s.rename(new_name)`
---

## 📌 DataFrame

- **Constructor principal**
  - `pd.DataFrame(data=None, index=None, columns=None, dtype=None, copy=False)`

- **Constructores alternativos**
  - `pd.DataFrame.from_dict(data, orient='columns', dtype=None, columns=None)`
  - `pd.DataFrame.from_records(data, index=None, exclude=None, columns=None, coerce_float=False, nrows=None)`

- **Acceso y atributos**
  - `df.index`
  - `df.columns`
  - `df.T`
  - `df.transpose(*args, **kwargs)`

- **Selección / Indexación**
  - `df[col]`
  - `df.loc[label]`
  - `df.iloc[loc]`
  - `df[5:10]`
  - `df[bool_vec]`

- **Columnas (gestión)**
  - `df[col] = value`
  - `del df[col]`
  - `df.pop(col)`
  - `df.insert(loc, column, value, allow_duplicates=False)`
  - `df.assign(**kwargs)`

- **Operaciones aritméticas y booleanas**
  - `df + df2`
  - `df - df.iloc[0]`
  - `df * scalar`
  - `df ** power`
  - `df1 & df2`
  - `df1 | df2`
  - `df1 ^ df2`
  - `-df1`

- **Interoperabilidad con NumPy**
  - `np.exp(df)`
  - `np.asarray(df)`
  - `np.exp(ser)` (Series también)
---

## 📌 Resumen de formas de creación de DataFrame

- Desde **dict de Series**
- Desde **dict de listas/ndarrays**
- Desde **structured array**
- Desde **list de dicts**
- Desde **dict de tuplas (MultiIndex)**
- Desde **Series**
- Desde **list de namedtuples**
- Desde **list de dataclasses**

---
✅ **Resumen:**  
- Para **Series**, recordar `pd.Series()`, `.iloc`, `.loc`, `.get()`, `.to_numpy()`, `.rename()`.  
- Para **DataFrame**, recordar `pd.DataFrame()`, `.from_dict()`, `.from_records()`, `.assign()`, `.insert()`, `.pop()`, `.transpose()`, y las operaciones aritméticas/booleanas.  
- Ambos interoperan con **ufuncs de NumPy** (`np.exp`, `np.asarray`, etc.).
---

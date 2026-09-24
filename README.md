# 📘 Pandas Playbook
> **The Definitive 28-Module Technical Interview Preparation & Production Mastery Guide**

![Python](https://img.shields.io/badge/Python-3.12%2B-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-3.0%2B-150458?logo=pandas)
![Package Manager](https://img.shields.io/badge/Managed%20by-uv-DE5FE9?logo=astral)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/Tests-0%20Runtime%20Errors-brightgreen)

Welcome to **Pandas Playbook**! This repository is a battle-tested, zero-to-advanced curriculum designed for **Data Scientists, Data Engineers, and Quantitative Analysts** preparing for rigorous technical interviews and building high-throughput production data pipelines.

Every single notebook in this collection is **fully executed with 0 runtime errors**, updated for **Pandas 2.x and 3.0**, and includes:
- 💡 **Executive Mental Models**: Core architectural diagrams and algorithmic complexity ($O(1)$ vs $O(N)$ lookups).
- ⚠️ **Junior Anti-Patterns vs Senior Standards**: Deprecated methods, hidden traps, and memory bloat hazards.
- 🎯 **Technical Interview Corner**: Tricky conceptual interview questions and runnable coding challenges with production-grade solutions.

---

## ⚡ Quickstart with `uv`

This repository uses [**`uv`**](https://github.com/astral-sh/uv), the ultra-fast Python package manager.

```bash
# 1. Clone the repository
git clone https://github.com/CodeRabbitHub/pandas-playbook.git
cd pandas-playbook

# 2. Automatically create the virtual environment and install all dependencies
uv sync

# 3. Launch Jupyter Notebook or JupyterLab
uv run jupyter notebook
```

*Or open directly in VS Code / Cursor and select the **Python (Pandas Pro)** kernel registered in `.venv`.*

---

## 📚 Curriculum Roadmap

The curriculum is structured into 28 focused modules covering the full breadth of data manipulation:

| Module | Title | Core Competencies & Interview Focus |
|:---:|:---|:---|
| **01** | [`01_pandas_overview.ipynb`](./01_pandas_overview.ipynb) | Hash index $O(1)$ vs array scan $O(N)$, `SettingWithCopyWarning`, `shape`/`size`/`count` |
| **02** | [`02_series_object.ipynb`](./02_series_object.ipynb) | Nullable `Int64`, index alignment, membership `in` trap (index vs values), `.to_numpy()` |
| **03** | [`03_user_data_exploration.ipynb`](./03_user_data_exploration.ipynb) | Dot notation hazards (`df.col` vs `df['col']`), postal code string preservation, `describe(include='all')` |
| **04** | [`04_food_orders_exploration.ipynb`](./04_food_orders_exploration.ipynb) | Targeted groupby column slicing, line price vs unit price trap, Average Order Value (AOV) |
| **05** | [`05_food_facts_exploration.ipynb`](./05_food_facts_exploration.ipynb) | Wide-schema streaming, `DtypeWarning` chunking, `df.values[i][j]` anti-pattern, memory profiling |
| **06** | [`06_the_dataframe_object.ipynb`](./06_the_dataframe_object.ipynb) | Accessor matrix (`loc`/`iloc`/`at`/`iat`), duplicate index return types, memory inflection points |
| **07** | [`07_filtering_a_dataframe.ipynb`](./07_filtering_a_dataframe.ipynb) | Silent `astype(bool)` data corruption on `NaN`, `NaN != NaN` IEEE rule, `keep=False` in deduplication |
| **08** | [`08_food_orders_sorting_and_filtering.ipynb`](./08_food_orders_sorting_and_filtering.ipynb) | `mask.sum()` vs `len(df[mask])`, `na=False` in `.str.contains()`, composite filtering & drills |
| **09** | [`09_euro12_sorting_and_filtering.ipynb`](./09_euro12_sorting_and_filtering.ipynb) | Negative 2D slicing `iloc[:, :-3]`, shot conversion efficiency metrics, fixed hardcoded index bug |
| **10** | [`10_fictional_army_filtering_and _sorting.ipynb`](./10_fictional_army_filtering_and%20_sorting.ipynb) | Eliminated chained coordinate indexing `loc[...].iloc[...]`, eliminated `inplace=True`, `get_loc()` bridge |
| **11** | [`11_dealings with strings.ipynb`](./11_dealings%20with%20strings.ipynb) | PyArrow strings (`string[pyarrow]`), `expand=True` DataFrame unpacking, named regex extraction |
| **12** | [`12_the_multiIndex_object.ipynb`](./12_the_multiIndex_object.ipynb) | Lexsort `sort_index()` rule, tuple slicing `loc[(r1, r2)]`, cross-sections `.xs()`, `pd.IndexSlice` |
| **13** | [`13_reshaping_and_pivoting.ipynb`](./13_reshaping_and_pivoting.ipynb) | `pivot()` vs `pivot_table()`, `unstack()`/`stack()`, tidy data melting via `pd.melt()` |
| **14** | [`14_the_groupby_object.ipynb`](./14_the_groupby_object.ipynb) | Split-apply-combine, `size()` vs `count()`, `.transform()` row broadcasting vs `.agg()` reduction |
| **15** | [`15_drinks_groupby.ipynb`](./15_drinks_groupby.ipynb) | Solved legendary North America `'NA'` ingestion bug via `keep_default_na=False`, `dropna=False` in groupby |
| **16** | [`16_occupation_groupby.ipynb`](./16_occupation_groupby.ipynb) | Vectorized boolean mean proportions `(s == 'M').mean()`, `pd.crosstab(..., normalize='index')`, `.nsmallest()` |
| **17** | [`17_regiment_groupby.ipynb`](./17_regiment_groupby.ipynb) | Handled Pandas 3.0 `numeric_only=True` on strings, `.unstack()` matrix grids, `(name, group)` tuple iteration |
| **18** | [`18_student_alcohol_apply.ipynb`](./18_student_alcohol_apply.ipynb) | Replaced deprecated `applymap` with `DataFrame.map()`, `.str.capitalize()` C-speed vectorization, `np.select` |
| **19** | [`19_crime_apply.ipynb`](./19_crime_apply.ipynb) | Modern frequency `'10YS'`, exposed the 2-billion population summation blunder, true per-capita crime rates |
| **20** | [`20_merging_joining_and_concatenating.ipynb`](./20_merging_joining_and_concatenating.ipynb) | Join types, `validate={'1:1', '1:m', 'm:1'}`, SQL anti-joins via `indicator=True`, star-schema joins |
| **21** | [`21_cars_merge.ipynb`](./21_cars_merge.ipynb) | Dynamic column pruning (`dropna(axis=1, how='all')`), duplicate index collision prevention via `ignore_index=True` |
| **22** | [`22_names_merge.ipynb`](./22_names_merge.ipynb) | Suffix collision management (`suffixes=('_batch1', '_batch2')`), 1-to-many merge expansion, coalesce via `.combine_first()` |
| **23** | [`23_housing_market_merge.ipynb`](./23_housing_market_merge.ipynb) | The "index only goes until 99" repetition trap, `reset_index(drop=True)` vs `reindex()`, luxury tiering via `pd.cut()` |
| **24** | [`24_working_with_dates_and_times.ipynb`](./24_working_with_dates_and_times.ipynb) | `.dt` accessor suite, `DateOffset` vs `Timedelta`, `.dt.seconds` (remainder) vs `.dt.total_seconds()` (true duration) |
| **25** | [`25_date_time_pandas.ipynb`](./25_date_time_pandas.ipynb) | Partial string date indexing, `pd.date_range()`, resampling boundaries (`closed` vs `label`), 5-min OHLCV bars |
| **26** | [`26_imports_and_exports.ipynb`](./26_imports_and_exports.ipynb) | Nested JSON flattening (`pd.json_normalize`), missing key safeguarding, multi-sheet Excel, Parquet benchmarking |
| **27** | [`27_options_and_settings.ipynb`](./27_options_and_settings.ipynb) | Scoped `pd.option_context()` vs global mutations, Pandas 3.0 Copy-on-Write (`mode.copy_on_write`), Styler views |
| **28** | [`28_visualization.ipynb`](./28_visualization.ipynb) | OO `fig, ax` architecture vs stateful `plt`, visual ergonomics (why horizontal `barh` dominates), twin-axis plots |

---

## 🎯 Top Technical Interview Takeaways

1. **The Vectorization Performance Hierarchy**:
   $$\text{NumPy SIMD C} \;(1\times) \gg \text{Cython Accessors} \;(5\times) \gg \text{np.select/where} \gg \text{Comprehensions} \gg \text{Series.apply} \;(50\times) \gg \text{df.apply(axis=1)} \;(1000\times)$$
2. **Cardinality & Join Safeguards**:
   Always pass `validate={'one_to_one', 'one_to_many', 'many_to_one'}` to `pd.merge()` to avoid silent $M \times N$ Cartesian multiplications in financial metrics.
3. **Stock vs Flow Aggregations**:
   Flow metrics (revenue, transactions, occurrences) accumulate via `.sum()`. Stock/snapshot metrics (population, balances, headcount) must be aggregated with `.last()`, `.max()`, or `.mean()`.
4. **Copy-on-Write (CoW)**:
   Pandas 3.0 enforces Copy-on-Write by default: slicing produces zero-copy read-only views until mutation, eradicating `SettingWithCopyWarning`.
5. **Timedelta Elapsed Duration**:
   Never divide `td.dt.seconds / 3600` for elapsed hours (it only captures remainder seconds within the day). Always compute `td.dt.total_seconds() / 3600`.

---

## 📄 License
This project is licensed under the MIT License — see the [LICENSE](./LICENSE) file for details.

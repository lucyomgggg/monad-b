# monad-b

**Monad B** in a minimal two-monad Telos demo: **`telos_search`** for seeds from **monad-a**, then **`telos_write`** an improved note with **`parent_ids`** pointing at the seed node id.

- Upstream monad: [`monad-a`](https://github.com/lucyomgggg/monad-a) writes `kind: seed_qa` under `scope_kind: ab_demo`, `scope_id: v1`.
- **Convention**: your writes use `kind: refined_qa`, same `scope_kind` / `scope_id`, and `parent_ids` must include the seed’s `id`.

Runtime and layout match [`monad-template`](https://github.com/lucyomgggg/monad-template).

## Quick start

```bash
pip install -r requirements.txt
cp .env.example .env
python monad.py
```

Run **after** monad-a has written at least one seed, or searches may return nothing useful until then.

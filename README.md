# pulse-dvc-store

DVC file store for [PrestonRamsay/pulse](https://github.com/PrestonRamsay/pulse): the frozen
data splits and model files, in DVC's own layout (`files/md5/<xx>/<hash>`).

You don't use this repo directly. In a clone of `pulse`, a plain `dvc pull` reads from here over
HTTPS (`https://raw.githubusercontent.com/PrestonRamsay/pulse-dvc-store/main`), with no account
or token. It's read-only for DVC; new files are added with Git (`python scripts/sync_dvc_store.py`
in the `pulse` repo).

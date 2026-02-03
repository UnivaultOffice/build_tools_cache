# build_tools_cache

Offline caches used by UnivaultOffice build_tools to avoid external downloads.

## v8_89

Files:
- `v8_89/v8_cache_pack.tgz.part*` — split archive parts (join to get `v8_cache_pack.tgz`)
- `v8_89/v8_cache_pack.sha256` — SHA256 of the joined `v8_cache_pack.tgz`
- `cipd/windows-amd64/cipd.exe` — CIPD client binary (mirror)
- `cipd/windows-amd64/cipd.exe.sha256` — SHA256 of the CIPD client

Join + unpack (Windows):
```
copy /b v8_cache_pack.tgz.part* v8_cache_pack.tgz
tar -xzf v8_cache_pack.tgz
```

Join + unpack (Linux/macOS):
```
cat v8_cache_pack.tgz.part* > v8_cache_pack.tgz
tar -xzf v8_cache_pack.tgz
```

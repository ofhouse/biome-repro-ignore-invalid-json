# Biome 2.0.0-beta.2 ignored files not respected with `--config-path`

It seems like the ignored files are handled differently when `--config-path` parameter is specified:

```plain
biome format .

Checked 2 files in 975µs. No fixes applied.
```

```plain
pnpm biome format --config-path=./biome.jsonc .

invalid-jsons/invalid-json.json:1:1 parse ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ String values must be double quoted.
  
  > 1 │ aGVsbG8gd29ybGQ=
      │ ^^^^^^^^^^^^^^^
    2 │ 
```


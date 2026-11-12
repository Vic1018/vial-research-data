# vial-research-data

Public research peptide catalog for the Vial app. Research text only; no personal or dose-log data. The app fetches `catalog.json` and the detached Ed25519 signature `catalog.json.sig` from `main`. To publish an update, edit `catalog.json`, bump `version` (or `updatedAt`), and sign the exact file bytes with `scripts/sign-catalog.py` from `Vic1018/vial-peptide-tracker` using the signing key on the box (`--key-file /home/box/secrets/vial-catalog-signing.pem`). Commit `catalog.json` and `catalog.json.sig` together. Do not reformat the JSON after signing.

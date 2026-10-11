# Claim_settlement

This repository includes the following upstream projects as Git submodules:

- `projects/claim_settlement_bd` → `https://github.com/SiddhantDas18/claim_settlement_bd.git`
- `projects/claim_settlement_fd` → `https://github.com/SiddhantDas18/claim_settlement_fd.git`

## Clone with submodules

```bash
git clone --recurse-submodules https://github.com/SiddhantDas18/Claim_settlement.git
```

If you already cloned the repository without submodules:

```bash
git submodule update --init --recursive
```

## Pull latest submodule commits from upstream

```bash
git submodule update --remote --recursive
```

To keep submodule pointers recorded in this repository up to date, commit the updated submodule references after running the command above.
# CI Fixes TODO

## Approved Plan Steps

### 1. Update Soroban SDK ✅

- Update Cargo.toml soroban-sdk to latest
- Run `cd contracts/prediction_market && cargo update`
- Verify `cargo audit` passes

### 2. Reduce Stress Test Load for CI ✅

- Edit stress-test.yml: concurrency 5/5/10, short durations
- Test locally with backend running

### 3. Local Verification ✅

- `cd contracts/prediction_market && cargo audit`
- Start backend, `python run-stress-test.py`

### 4. Create/Update PR

- New branch blackboxai/fix-ci
- Commit changes
- `gh pr create --fill` or update PR#193

### 5. Push & Test CI

- Push to GitHub
- Verify all checks pass

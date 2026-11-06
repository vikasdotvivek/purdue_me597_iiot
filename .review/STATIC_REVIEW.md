# Code improvement triage

**Automated first pass, not a complete manual code audit or a safety certification.**

Repository: `vikasdotvivek/purdue_me597_iiot`
Snapshot: `3db9498a0459938d16b8376c2764998f7eece0ff`

- Tracked paths: 880; source files inspected: 41.
- Findings: 5; retained: 5; omitted by cap: 0.
- Priority counts in retained findings: {'P1': 5}.
- No repository code, tests, builds or hardware were executed.

## Scope and limitations

Python findings use AST parsing under the runner Python 3. C/C++/C# findings are lexical review candidates, not compiler-verified defects. Files over 1 MB, designer files, generated/vendor paths, binaries, notebooks, PDFs and other non-source formats are excluded and enumerated in the JSON report. No findings does not establish correctness.

## Build and test follow-up

No conventional build/dependency manifest was detected outside excluded paths. Document the intended compiler/runtime, dependencies, and a reproducible build command; this may be an intentionally partial source archive.

No conventional test paths were detected. Add regression fixtures for the critical calculations and input boundaries; notebook/manual tests may still exist.

## Potential improvements

### 1. P1: Does not parse with the audit runner Python 3
Source: [lab/lab10/lab10_sample_code/lab10_sample1.py:13](https://github.com/vikasdotvivek/purdue_me597_iiot/blob/3db9498a0459938d16b8376c2764998f7eece0ff/lab/lab10/lab10_sample_code/lab10_sample1.py#L13)
Confirm the intended Python version. This may be legacy Python 2 rather than an unintended syntax error; compile with the supported interpreter.

### 2. P1: Does not parse with the audit runner Python 3
Source: [lab/lab10/lab10_sample_code/lab10_sample_adapter.py:18](https://github.com/vikasdotvivek/purdue_me597_iiot/blob/3db9498a0459938d16b8376c2764998f7eece0ff/lab/lab10/lab10_sample_code/lab10_sample_adapter.py#L18)
Confirm the intended Python version. This may be legacy Python 2 rather than an unintended syntax error; compile with the supported interpreter.

### 3. P1: Does not parse with the audit runner Python 3
Source: [lab/lab9/lab9_code/lab9_ML_implementation.py:69](https://github.com/vikasdotvivek/purdue_me597_iiot/blob/3db9498a0459938d16b8376c2764998f7eece0ff/lab/lab9/lab9_code/lab9_ML_implementation.py#L69)
Confirm the intended Python version. This may be legacy Python 2 rather than an unintended syntax error; compile with the supported interpreter.

### 4. P1: Does not parse with the audit runner Python 3
Source: [lab/lab9/lab9_code/lab9_adapter_sample.py:111](https://github.com/vikasdotvivek/purdue_me597_iiot/blob/3db9498a0459938d16b8376c2764998f7eece0ff/lab/lab9/lab9_code/lab9_adapter_sample.py#L111)
Confirm the intended Python version. This may be legacy Python 2 rather than an unintended syntax error; compile with the supported interpreter.

### 5. P1: Does not parse with the audit runner Python 3
Source: [lab/lab9/lab9_code/lab9_sample2.py:58](https://github.com/vikasdotvivek/purdue_me597_iiot/blob/3db9498a0459938d16b8376c2764998f7eece0ff/lab/lab9/lab9_code/lab9_sample2.py#L58)
Confirm the intended Python version. This may be legacy Python 2 rather than an unintended syntax error; compile with the supported interpreter.

## Acceptance gate

Confirm each candidate in its calling context. Add a regression test, make one focused change, and build using the actual target dependencies. For robotics/actuator firmware, verify safe outputs, limit handling, sensor failure and timing on a controlled test rig. Do not merge or deploy a blanket rewrite based on these pattern matches.

Machine-readable scope, exclusions and findings: `static-review.json`.

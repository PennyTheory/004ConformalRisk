# Anonymous Review Repository

This repository is a minimal anonymous verification artifact for peer review.
It contains one frozen archive, its SHA-256 checksum, this usage note, and
repository hygiene rules.

The archive contains only the dependency-closed source, tests, frozen parameter
registry, anonymized retained atomic results, and the verification entry point
needed to assess the supplied program. It intentionally excludes manuscript
files, submission letters, highlights, author information, local filesystem
paths, credentials, private source data, and conversation records.

## Verify

From the repository root:

```bash
sha256sum -c anonymized_review_repository.zip.sha256
unzip -q anonymized_review_repository.zip -d review_artifact
cd review_artifact
./run_verify.sh
```

The verification script checks the packaged source and retained artifacts. It
does not run a new scientific evaluation and the archive does not establish a
field-deployment or real-world certification claim.

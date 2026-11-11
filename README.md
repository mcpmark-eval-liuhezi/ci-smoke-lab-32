# ci-smoke-lab-32
Throwaway sandbox for end-to-end contribution + CI smoke test (fallback name)

## Build artifact

This sandbox demonstrates the contribution + CI loop end to end. The GitHub
Actions workflow (`.github/workflows/ci.yml`, trigger: `workflow_dispatch`)
writes a short text file (`demo-build.txt`) during the `build` job and uploads
it as a build artifact named exactly **demo-build** (retention: 30 days).

CI smoke test complete: the `document-artifact` branch adds this section to
the README and opens a pull request into `main`, while a `workflow_dispatch`
run of the `CI Smoke Test` workflow produced a successful run that upload
the `demo-build` artifact.

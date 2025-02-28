# quack-circle
Composite action to trigger a circleCI pipeline, wait for it t finish and retrieve the output logs.

# How to:
```
jobs:
  trigger:
    runs-on: ubuntu-latest
    steps:
      - name: Trigger CircleCI Pipeline
        uses: ducklabsio/actions/quack-circle@main
        with:
          circleci-org: ${{ github.repository_owner }}
          circleci-token: ${{ secrets.CIRCLECI_TOKEN }}
```
# kubeshop/tracetest-agent-action

> [GitHub Action](https://docs.github.com/en/actions) for running [Tracetest Agent](https://docs.tracetest.io/getting-started/installation#install-the-tracetest-agent) and using [Tracetest CLI](https://docs.tracetest.io/getting-started/open#trigger-1) to trigger trace-based tests against [Tracetest](https://tracetest.io/).

Placing `use: kubeshop/tracetest-agent-action@v1` into a GitHub Action workflow gives you a simple way to run Tracetest Agent. The action installs the Tracetest CLI and starts Tracetest Agent.

The action takes an `API Key` and `Token` as parameters that will tell Tracetest Agent how to connect to Tracetest.

You then proceed to run Tracetest trace-based tests.

## Trace-based Test Example

```yaml
name: example-basic
on: push
jobs:
  trace-based-tests:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Run Tracetest Agent
        uses: kubeshop/tracetest-agent-action@v1
        with:
          apiKey: ${{ secrets.TRACETEST_API_KEY }}
          token: ${{ secrets.TRACETEST_TOKEN}}
      # Start your app
      # Run Tracetest tests
      - name: Run trace-based tests
        run: |
          tracetest run --file path-to-dir/test.yml
```

# kubeshop/tracetest-agent-action

> GitHub Action for running Tracetest trace-based tests. Includes Tracetest Agent with configuration options to run tests against Tracetest.

use: cypress-io/github-action@v6

Placing `use: kubeshop/tracetest-agent-action into a GitHub Action workflow gives you a simple way to run Tracetest Agent. The action installs the Tracetest CLI and starts Tracetest Agent.

The action takes an `API Key` as a parameter that will tell Tracetest Agent how to connect to Tracetest. It then proceeds to run Tracetest trace-based tests and provides a test summary after completion.

TODO:

- Add config example of how to set up the GitHub Action in a workflow.

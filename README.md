# Gemini CLI Extension - AlloyDB for PostgreSQL Observability

> [!NOTE]
> This extension is currently in beta (pre-v1.0), and may see breaking changes until the first stable release (v1.0).

This Gemini CLI extension provides a set of tools to interact with [AlloyDB for PostgreSQL](https://cloud.google.com/alloydb) monitoring metrics. It allows you to fetch a wide range of database metrics, enabling comprehensive monitoring of database performance and health directly from the [Gemini CLI](https://google-gemini.github.io/gemini-cli/), using natural language prompts.

Learn more about [Gemini CLI Extensions](https://github.com/google-gemini/gemini-cli/blob/main/docs/extension.md).

## Why Use the AlloyDB for PostgreSQL Observability Extension?

* **Natural Language Management:** Stop wrestling with complex monitoring queries. Explore monitoring data by describing what you want in plain English.
* **Seamless Workflow:** As a Google-developed extension, it integrates seamlessly into the Gemini CLI environment. No need to constantly switch contexts for common tasks.

## Prerequisites

Before you begin, ensure you have the following:

*   [Gemini CLI](https://github.com/google-gemini/gemini-cli) installed with version **+v0.6.0**.
*   A Google Cloud project with the **Cloud Monitoring API** enabled.
*   IAM Permissions
  * Monitoring Viewer (`roles/monitoring.viewer`)

## Installation

To install the extension, use the command:

```bash
gemini extensions install https://github.com/gemini-cli-extensions/alloydb-observability
```

## Configuration

Ensure [Application Default Credentials](https://cloud.google.com/docs/authentication/gcloud) are available in your environment.

## Usage Examples

Interact with Cloud Monitoring metrics using natural language right from your IDE:

* "What is the memory usage for my Postgres database?"
* "What is the overall system performance for my instance?"
* "What queries have been run for this instance over the last 3 hours?"
* "Provide the execution time for the query X"

## Supported Tools

* `get_system_metrics`: Fetches system level cloud monitoring data (timeseries metrics) for a Postgres instance using a PromQL query.
* `get_query_metrics`: Fetches query level cloud monitoring data (timeseries metrics) for queries running in Postgres instance using a PromQL query.

## Additional Extensions

Find additional extensions to support your entire software development lifecycle at [github.com/gemini-cli-extensions](https://github.com/gemini-cli-extensions).

## Troubleshooting

* "cannot execute binary file": Ensure the correct binary for your OS/Architecture has been downloaded. See [Installing the server](https://googleapis.github.io/genai-toolbox/getting-started/introduction/#installing-the-server) for more information.

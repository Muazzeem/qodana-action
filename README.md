# Qodana Code Analysis

This project uses **Qodana** for automated code analysis and linting. Qodana helps ensure code quality by identifying potential bugs, code smells, and other issues using JetBrains' comprehensive set of inspections. The configuration is managed using the `qodana.yaml` file.

## Getting Started

To set up the environment for Qodana analysis, follow these steps:

1. Install the required Python dependencies:

    ```bash
    pip install -r requirements.txt
    ```

2. The code analysis process is configured in the `qodana.yaml` file.

## Qodana Configuration

The Qodana configuration is defined in the `qodana.yaml` file, and here are the key components:

### Version

```yaml
version: "1.0"
```

### Profile

The inspection profile is set to `qodana.recommended`, which applies JetBrains' recommended inspections.

```yaml
profile:
  name: qodana.recommended
```

### Bootstrap

```yaml
bootstrap: pip install -r requirements.txt
```

### Linter

The Qodana linter used for this project is `jetbrains/qodana-python:latest`, which is suited for Python code analysis.
```
linter: jetbrains/qodana-python:latest
```

### Fixes Strategy

Fixes are applied to the codebase using the `apply` strategy.

```yaml
fixesStrategy: apply
```

### More Configuration Options

For more configuration options, refer to the [Qodana YAML Reference](https://www.jetbrains.com/help/qodana/qodana-yaml.html).
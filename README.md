# jira-deps

A tool for visualizing Jira issue dependencies.

## Installation

### Prerequisites

- Go 1.23 or higher

### Build from source

```bash
go build -o jira-deps main.go
```

## Configuration

Before using jira-deps, you need to have a Jira API Token.
To generate a Jira API token:

1. Log in to your Jira account
2. Go to Account Settings → Security → API tokens
3. Create a new API token

## Usage

Your Jira base URL, username, and token will be prompted for if not found in
the JSON config file located at `${HOME}/.config/jira-deps.json`.

### Basic usage

```bash
./jira-deps <JIRA-ISSUE-KEY>
```

### Examples

```bash
# Analyze dependencies for a single issue
./jira-deps PROJ-123

# Analyze multiple issues
./jira-deps PROJ-123 PROJ-456 PROJ-789
```

## Output

The tool analyzes the specified Jira issues and their dependencies, providing:

- Direct issue links and relationships
- Dependency hierarchy

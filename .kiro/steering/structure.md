# LangChain Project Structure

## Repository Organization

The LangChain repository is organized as a monorepo containing multiple packages and resources:

```
langchain/
├── .devcontainer/       # Development container configuration
├── .github/             # GitHub workflows and templates
├── .kiro/               # Kiro AI assistant configuration
├── cookbook/            # Example notebooks demonstrating usage
├── docs/                # Documentation source
│   ├── api_reference/   # API reference documentation
│   ├── docs/            # Main documentation content
│   └── static/          # Static assets for documentation
├── libs/                # Core library packages
│   ├── core/            # langchain-core package
│   ├── langchain/       # Main langchain package
│   ├── community/       # Community integrations
│   ├── experimental/    # Experimental features
│   ├── text-splitters/  # Text chunking utilities
│   ├── partners/        # Partner integrations
│   └── standard-tests/  # Standard test suite
└── scripts/             # Utility scripts for development
```

## Key Directories

### `libs/`

Contains all the core packages that make up the LangChain ecosystem:

- `core/`: Core abstractions and interfaces
- `langchain/`: Main package that brings together components
- `community/`: Community-contributed integrations
- `partners/`: Official partner integrations (OpenAI, Anthropic, etc.)
- `text-splitters/`: Text chunking utilities
- `experimental/`: Experimental features and prototypes
- `standard-tests/`: Standard test suite for consistency

### `cookbook/`

Contains Jupyter notebooks with examples and tutorials for various use cases:
- RAG implementations
- Agent examples
- Multi-modal applications
- Tool integrations
- Custom chains and workflows

### `docs/`

Contains all documentation:
- `api_reference/`: Auto-generated API documentation
- `docs/`: Main documentation content
- Source for the website at python.langchain.com

## Code Organization Principles

1. **Modular Design**: Functionality is split into focused packages
2. **Clear Interfaces**: Components use standard interfaces for interoperability
3. **Provider Separation**: Provider-specific code is isolated in dedicated packages
4. **Example-Driven**: Complex features include cookbook examples
5. **Documentation First**: New features require documentation
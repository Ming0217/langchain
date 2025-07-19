# LangChain Technical Stack

## Build System & Package Management

- **Build Backend**: PDM (Python Development Master)
- **Package Manager**: UV (fast Python package installer and resolver)
- **Python Version**: Requires Python 3.9+

## Core Dependencies

LangChain is organized as a monorepo with multiple packages:

- `langchain-core`: Core abstractions and interfaces
- `langchain`: Main package that brings together all components
- `langchain-community`: Community integrations
- `langchain-experimental`: Experimental features
- `langchain-text-splitters`: Text chunking utilities
- Various provider-specific packages (e.g., `langchain-openai`, `langchain-anthropic`)

## Development Tools

- **Linting**: Ruff
- **Documentation**: Sphinx, Docusaurus
- **Testing**: Standard Python test suite
- **Spell Checking**: Codespell

## Common Commands

### Installation

```bash
# Install main package
pip install -U langchain

# Install with specific integrations
pip install langchain-openai
pip install langchain-anthropic
```

### Development

```bash
# Install development dependencies
uv run --group dev

# Run linting
make lint

# Format code
make format

# Run spell check
make spell_check
make spell_fix

# Build documentation
make docs_build

# Build API reference
make api_docs_build
```

### Testing

```bash
# Run tests with UV
uv run --group test pytest

# Run specific tests
uv run --group test pytest tests/unit_tests
```

## Documentation

- Main docs: https://python.langchain.com/docs/
- API Reference: https://python.langchain.com/api_reference/
- Cookbook examples: Various Jupyter notebooks in the cookbook directory
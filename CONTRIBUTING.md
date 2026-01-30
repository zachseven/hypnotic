# Contributing to hypnotIC

First off, thanks for wanting to contribute. IC what you're doing there.

## Ways to Contribute

### Report Bugs
Found something broken? Open an issue with:
- What you expected to happen
- What actually happened
- The code that caused it
- Your Python version

### Suggest Features
Got an idea for a new keyword or feature? Open an issue and let's talk about it.

### Submit Code
1. Fork the repo
2. Create a branch (`git checkout -b feature/cool-thing`)
3. Make your changes
4. Add tests if applicable
5. Make sure tests pass (`pytest tests/`)
6. Commit with a clear message
7. Push and open a PR

## Development Setup

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/hypnotic.git
cd hypnotic

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dev dependencies
pip install pytest

# Run tests
pytest tests/ -v

# Try it out
python hypnotic.py
```

## Code Style

- Keep it simple and readable
- Comments are good, especially for tricky parts
- Match the existing style
- Don't over-engineer

## Adding New Keywords

If you want to add a new keyword to the language:

1. Add the token to `KEYWORDS` dict in the Lexer section
2. Handle it in the `tokenize()` method if needed
3. Add parsing logic in the Parser
4. Add execution logic in the Interpreter
5. Add tests
6. Update `SPEC.md` and `README.md`

## Testing

```bash
# Run all tests
pytest tests/ -v

# Run specific test
pytest tests/test_hypnotic.py::TestBasics -v

# Test an example
python hypnotic.py examples/fizzbuzz.ic
```

## Questions?

Open an issue. We don't bite.

---

*"IC what you meant."*

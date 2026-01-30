# hypnotIC

An esoteric programming language with phonetic shortcuts and a forgiving philosophy.

## Quick Reference

### Run the interpreter
```bash
python hypnotic.py                    # REPL
python hypnotic.py file.ic            # Run file
python hypnotic.py -c "* \"hello\""   # One-liner
python hypnotic.py -d file.ic         # Debug mode
```

### Run tests
```bash
pytest tests/ -v
```

### Project Structure
- `hypnotic.py` - The complete interpreter (lexer, parser, interpreter)
- `SPEC.md` - Full language specification
- `examples/` - Example programs
- `tests/` - Test suite

### Key Language Syntax
- `*` = print
- `?`/`file`/`Ls`/`IC` = if/elif/else/end
- `4 i n 10` = for i in range(10)
- `wyl` = while
- `fun`/`re:` = function/return
- `iz`/`aint` = ==/!=
- `fuck` = comment

### Architecture
The interpreter follows a classic 3-stage design:
1. **Lexer** (lines 14-380) - Tokenizes source code
2. **Parser** (lines 383-940) - Builds AST
3. **Interpreter** (lines 943-1252) - Executes AST

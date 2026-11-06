# No-Slop Examples

Concrete before/after examples and templates. Load this when you need illustration of the principles.

## Code: Before vs After

### Before (AI-slop style)
```python
def process_data(data):
    """
    This function processes the data in a powerful and seamless way.
    It is important to note that we handle various edge cases.
    """
    # Let's dive in and process the data
    result = []
    for item in data:
        if item is not None:
            # Process each item carefully
            processed = item * 2
            result.append(processed)
    return result
```

### After (Clean)
```python
def double_values(values: list[float]) -> list[float]:
    return [v * 2 for v in values if v is not None]
```

## README Structure Template

```markdown
# Project Name

One-sentence description of what it does and who it is for.

## Quick Start

```bash
# install
# run
```

## Requirements

- ...

## Usage

Minimal working example.

## Configuration (if needed)

## Contributing

## License
```

## Video Script Template

```markdown
# Video Title

**Target length:** 8–12 min
**Audience:** ...

## Hook (0:00–0:12)
Spoken: ...
Visual: ...

## Promise
By the end you will be able to ...

## Section 1 – Title (0:12–2:30)
Spoken notes:
Visual / screen:
Key point:

## Section 2 – ...
...

## Close + CTA
```

## Technical Explanation Style

Prefer:

> The function returns early when the input is empty. This avoids unnecessary work and keeps the happy path clear.

Over:

> It is important to note that in order to optimize performance and ensure robustness, the function checks for empty input and returns early, which is a best practice in modern software development.

# Multi-Style Snake Generator

Automatically generates 4 different styles of contribution snakes for your GitHub profile.

## Usage
Add this to your `.github/workflows/snake.yml`:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: Pro-Bandey/multi-style-snake-action@v1

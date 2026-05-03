# Turnitin Stamper

Create a realistic looking Turnitin AI/Plaigarism Report
## Like this:
<img width="1988" height="688" alt="image" src="https://github.com/user-attachments/assets/ef855417-ec4a-4599-8f87-41cc5037e0cd" />

## Setup

```bash
# Clone the repository
git clone <repo-url>
cd turnitin-stamper

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
# OR
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

# Ensure NotoSans.ttf is in the project directory
```

## Usage

```bash
python main.py <input.pdf> <output.pdf> [options]
```

## CLI Arguments

| Argument         | Description                               | Default                                     |
| ---------------- | ----------------------------------------- | ------------------------------------------- |
| `input`          | Input PDF file (required)                 | -                                           |
| `output`         | Output PDF file (required)                | -                                           |
| `--image`        | Path to logo/image (1392x417 recommended) | (none)                                      |
| `--left-label`   | Text displayed after page number          | `AI Writing Submission`                     |
| `--right-label`  | Right-aligned label                       | `Submission ID   trn:oid:::###:###########` |
| `--bg-color`     | Header/footer background color (hex)      | (none)                                      |
| `--border-color` | Inner border line color                   | `#cccccc`                                   |
| `--text-color`   | Text color (hex)                          | `#000000`                                   |

## Examples

Basic usage with default labels:
```bash
python main.py your_doc.pdf output.pdf
```

With custom image and labels:
```bash
python main.py your_doc.pdf output.pdf \
  --image your_logo.png \
  --left-label "Your Document Name" \
  --right-label "Custom Right Text"
```

With custom colors:
```bash
python main.py your_doc.pdf output.pdf \
  --bg-color "#f5f5f5" \
  --text-color "#333333"
```

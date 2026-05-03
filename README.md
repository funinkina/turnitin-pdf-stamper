# Turnitin Stamper

Add header and footer bands to PDF documents with page numbers and optional labels.

## Setup

```bash
# Clone the repository
git clone <repo-url>
cd turnitin-stamper

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/macOS
# OR
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

# Ensure NotoSans.ttf is in the project directory
```

## Usage

```bash
python add_header_footer.py <input.pdf> <output.pdf> [options]
```

## CLI Arguments

| Argument | Description | Default |
|----------|-------------|---------|
| `input` | Input PDF file (required) | - |
| `output` | Output PDF file (required) | - |
| `--image` | Path to logo/image (1392x417 recommended) | (none) |
| `--left-label` | Text displayed after page number | `AI Writing Submission` |
| `--right-label` | Right-aligned label | `Submission ID   trn:oid:::###:###########` |
| `--bg-color` | Header/footer background color (hex) | (none) |
| `--text-color` | Text color (hex) | `#000000` |

## Examples

Basic usage with default labels:
```bash
python add_header_footer.py your_doc.pdf output.pdf
```

With custom image and labels:
```bash
python add_header_footer.py your_doc.pdf output.pdf \
  --image your_logo.png \
  --left-label "Your Document Name" \
  --right-label "Custom Right Text"
```

With custom colors:
```bash
python add_header_footer.py your_doc.pdf output.pdf \
  --bg-color "#f5f5f5" \
  --text-color "#333333"
```
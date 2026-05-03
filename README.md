# Turnitin Report Generator

Create a realistic looking Turnitin AI/Plaigarism Report
## Like this:
<img width="1988" height="688" alt="image" src="https://github.com/user-attachments/assets/ef855417-ec4a-4599-8f87-41cc5037e0cd" />

## Setup

```bash
# Clone the repository
git clone https://github.com/funinkina/turnitin-pdf-stamper.git
cd turnitin-pdf-stamper

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
# OR
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

# Ensure NotoSans.ttf is in the project directory
```

## Cover Pages
You can generate the cover page by copying and editing the details from [this figma file](https://www.figma.com/design/yzG131TMlxJOTZa20ypjX3/Turnitin-Cover-Pages?node-id=0-1&t=vtIJIfl2RmTrdT2H-1)

## Usage

```bash
python main.py <input.pdf> <output.pdf> [options]
```

## CLI Arguments

| Argument        | Description                               | Default                                     |
| --------------- | ----------------------------------------- | ------------------------------------------- |
| `input`         | Input PDF file (required)                 | -                                           |
| `output`        | Output PDF file (required)                | -                                           |
| `--image`       | Path to logo/image (1392x417 recommended) | `logo.jpg (turnitin logo)`                  |
| `--left-label`  | Text displayed after page number          | `AI Writing Submission`                     |
| `--right-label` | Right-aligned label                       | `Submission ID   trn:oid:::###:###########` |
| `--bg-color`    | Header/footer background color (hex)      | (none)                                      |
| `--text-color`  | Text color (hex)                          | `#000000`                                   |

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

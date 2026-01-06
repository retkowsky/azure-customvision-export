# Azure Custom Vision Export

[![License](https://img.shields.io/github/license/retkowsky/azure-customvision-export)](LICENSE)
[![Issues](https://img.shields.io/github/issues/retkowsky/azure-customvision-export)](https://github.com/retkowsky/azure-customvision-export/issues)

Export and automate the download of images and tags from Microsoft Azure Custom Vision projects. Easily migrate or back up your labeled datasets for training, analysis, or integration with other machine learning platforms.

## Features

- **Automated Dataset Export**: Download images and tags from your Azure Custom Vision project.
- **Flexible Output**: Save metadata in JSON/CSV, and images in a structure ready for further processing.
- **Easy Configuration**: Quickly set your project, endpoint, and authentication to get started.
- **Supports Multiple Projects**: Handle multiple Custom Vision projects or iterations as needed.

## Installation

Clone this repository:

```bash
git clone https://github.com/retkowsky/azure-customvision-export.git
cd azure-customvision-export
```

Install required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### 1. Configure Authentication

You’ll need your Azure Custom Vision endpoint, project ID, and training key. Set these as environment variables or in a `.env` file:

```env
ENDPOINT=https://<your-region>.api.cognitive.microsoft.com/
TRAINING_KEY=your_training_key
PROJECT_ID=your_project_id
```

### 2. Run the Export Script

```bash
python export_custom_vision.py
```

By default, images and tags will be saved locally in the `output/` directory.

#### Command-Line Options (if available)

- `--project-id`: Specify a different Custom Vision project ID.
- `--output-dir`: Set a custom output directory.
- `--iteration-id`: Export from a specific iteration.

## Example

Fetch images and tags from a project and save to `myexport/`:

```bash
python export_custom_vision.py --output-dir myexport
```

## Requirements

- Python 3.7+
- Azure Custom Vision resource (with valid access keys)

Install package dependencies:

```bash
pip install -r requirements.txt
```

## Project Structure

```
azure-customvision-export/
├── export_custom_vision.py   # Main export script
├── requirements.txt          # Python dependencies
├── README.md                 # This documentation
└── output/                   # Example/exported files directory
```

## Contributing

Contributions are welcome! Please submit a pull request or open an issue for suggestions and improvements.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for more information.

---

**Need help?**  
Open an [issue](https://github.com/retkowsky/azure-customvision-export/issues) or contact [@retkowsky](https://github.com/retkowsky).
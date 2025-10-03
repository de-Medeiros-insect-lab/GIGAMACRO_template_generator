# GIGAmacro Template Generator

A web-based tool for generating GIGAmacro project templates with customizable lens, view, and row configurations.

## Usage

### Online Version (Easiest)

Access the live version at:
```
https://de-medeiros-insect-lab.github.io/GIGAMACRO_template_generator/
```

### Local Development

If you want to run it locally or make modifications:

1. Navigate to the project directory:
   ```bash
   cd /path/to/TemplateGenerator
   ```

2. Start a local web server:
   ```bash
   python3 -m http.server 8000
   ```

3. Open your browser and navigate to:
   ```
   http://localhost:8000/
   ```

**Note**: Due to browser security restrictions, the HTML file needs to be served via HTTP rather than opened directly as a file.

## Adding New Templates

To add support for new lens/view/row combinations:

1. Create a new template file in the `base_templates/` directory
2. Follow the naming convention: `{LENS}_row{ROW}_{VIEW}_TEMPLATE.txt`
   - Example: `NiTMX5_row1_dorsal_TEMPLATE.txt`
3. Add the lens option to the HTML file if needed (in the lens dropdown)

The system will automatically detect and load the new template when the corresponding options are selected.

## Template Format

Templates are text files containing newline-delimited JSON objects, one per position.

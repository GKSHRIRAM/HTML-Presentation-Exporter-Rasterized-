# HTML Slides to PowerPoint Converter (Image-Based)

This project converts HTML-based slides into a PowerPoint (.pptx) file by rendering each HTML slide in a headless Chromium browser and embedding the rendered output as images into PowerPoint slides.

The conversion is image-based. The final PowerPoint preserves the exact visual appearance of the HTML, including layout, CSS, fonts, and charts. The slide content is not editable inside PowerPoint.

The tool is intended to be used in Google Colab and requires no local setup.

---

## What This Tool Does

- Accepts multiple HTML files, each representing one slide
- Renders each HTML file using Chromium via Playwright
- Captures each rendered slide as a PNG image
- Inserts the images into a PowerPoint presentation
- Automatically downloads the final PPTX file

---

## What This Tool Is and Is Not

### What It Is

- An HTML to image to PowerPoint pipeline
- Focused on visual accuracy and layout preservation
- Suitable for AI-generated or web-styled slides

### What It Is Not

- A true HTML to editable PowerPoint converter
- A tool that produces editable text or shapes in PowerPoint

Each PowerPoint slide contains a single rendered image.

---

## Requirements

You only need:

- A Google account
- Access to Google Colab
- HTML files representing slides

No prior setup, installation, or environment configuration is required.

---

## How to Use (Step-by-Step)

### Step 1: Open Google Colab

Go to:
https://colab.research.google.com/

Create a new notebook.

---

### Step 2: Copy and Paste the Code

Copy the full Python script from this repository and paste it into a single code cell in Google Colab.

Do not split the script across multiple cells.

---

### Step 3: Edit Required Details (Optional)

Inside the script, you may customize the following values:

```python
VIEWPORT_WIDTH  = 1280
VIEWPORT_HEIGHT = 720

OUTPUT_PRESENTATION = "output_presentation.pptx"
```

- Adjust the resolution if your slides require a different size
- Rename the output PowerPoint file if needed

All other parts of the script can remain unchanged.

---

### Step 4: Run the Cell

Run the code cell. Colab will install the required dependencies and prompt you to upload files.

---

### Step 5: Upload HTML Files

Upload all HTML files that represent your slides. Files are processed in alphabetical order.

Example:

```
01_intro.html
02_content.html
03_summary.html
```

---

### Step 6: Download the PowerPoint

After processing completes, the generated PowerPoint file will be automatically downloaded.

---

## Output Structure

The following directories are created automatically:

```
html_slides/
rendered_images/
output_presentation.pptx
```

---

## Notes

- Each HTML file should represent one slide
- Complex CSS layouts are supported
- JavaScript animations may not be captured
- Fonts should be web-safe or embedded

---

## License

This project is intended for personal and educational use. You may modify and reuse the code freely.


# Weight Converter App

A simple weight conversion web app built using Python and Gradio in Google Colab.

## Features

- Convert Pounds to Kilograms
- Convert Kilograms to Pounds
- Interactive web interface
- Beginner-friendly Python project
- Built entirely in Google Colab

---

## Technologies Used

- Python
- Gradio
- Google Colab

---

## Screenshot

<img width="1000" alt="App Screenshot" src="https://github.com/ananyalytics-ipynb/weight-converter-app/blob/main/weight.png">

---

## How It Works

The user:
1. Enters weight
2. Selects unit
3. Clicks submit
4. App converts the value instantly

---

## Installation

```bash
pip install gradio
```

---

## Run the App

```python
import gradio as gr

def convert_weight(weight, unit):

    if unit.upper() == "L":
        converted = weight * 0.45
        return f"Your weight in kg is {converted}"

    else:
        converted = weight / 0.45
        return f"Your weight in lbs is {converted}"

interface = gr.Interface(
    fn=convert_weight,
    inputs=[
        gr.Number(label="Enter Weight"),
        gr.Textbox(label="Enter Unit (L or K)")
    ],
    outputs="text",
    title="Weight Converter"
)

interface.launch()
```

---

## Future Improvements

- Better UI styling
- Dropdown instead of textbox
- BMI calculator integration
- Mobile responsiveness
- Deployment on Hugging Face Spaces

---

## Author

Ananya Singh

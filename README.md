# Gradio Thomas More theme

Usage example:

```python
with gr.Blocks(css="style/style.css", theme='TMBoeren/ThomasMore') as demo:
    gr.Markdown("<h1 class='gr-title'>This is a title</h1>")
    gr.Markdown("<span class='gr-description'>This is a description</span>")
    
    input_box = gr.Textbox(label="Input box", lines=2, elem_id="input_textbox")
    submit_btn = gr.Button(value="Submit")
    output_box = gr.Textbox(label="Output box", lines=2, elem_id="output_box")  
    
    submit_btn.click(
        get_response,
        inputs=[input_box],
        outputs=[output_box]
    )

demo.launch(show_api=False, allowed_paths=["style/fonts"])
```

# Legal ChatBot

A notebook that runs a legal question-answering chatbot with a Hugging Face model and a Gradio web interface.

## How it works

1. Downloads the model files of `lmsys/fastchat-t5-3b-v1.0` from the Hugging Face Hub.
2. Loads the tokenizer and `AutoModelForSeq2SeqLM`, and wraps them in a `text2text-generation` pipeline (maximum length 1000, running on CPU).
3. Tries it on two questions about Indian law: the right protected by Article 21 and the meaning of judicial review.
4. Serves a Gradio app titled "LAW-CHATBOT by iQube" on port 8000 with a public share link. You type a question and read the generated answer.

The notebook uses the pretrained model as it is. It contains no fine-tuning step.

## Run

Set a Hugging Face token in the environment, then run the cells in `Law Chatbot.ipynb`:

```bash
export HUGGING_FACE_API_KEY=your_token
pip install huggingface_hub sentencepiece transformers gradio
```

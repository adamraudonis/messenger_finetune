# Finetune models using your Messenger data

A repo for creating a fine tuned GPT-3 model based on your Facebook messenger chat conversations

- Download your json data from facebook, unzip it and put all chat or group conversations you want in a folder

```
pyenv virtualenv 3.11.2 venv
pyenv activate venv
pip install -r requirements.txt

# Ensure you export your OPENAI_API_KEY
export OPENAI_API_KEY=yourkey

python finetune_models.py ./messages --only "Adam Raudonis"

# NOTE: It took several hours to run and cost me $12.50 to for one finetune on several years of messages.

# Then to test your model:

python run_models.py ft:gpt-3.5-turbo-0613:personal::REDACTED --name="Adam Raudonis" --content="What are your hobbies?"

```

# Sources

https://python.langchain.com/docs/integrations/chat_loaders/facebook

# freeAI
Example usage:
```python
from freeAI import avagpt
import asyncio

async def main():
    result = await avagpt.Running.main("Hello! what language model are you?")
    print(result)

loop = asyncio.get_event_loop()
loop.run_until_complete(main())
```

result(OK):
```json
{
  'status': ['OK']
  'created': 1687115742.184269,
  'model': 'GPT-4',
  'result': [
    {
      'prompt': 'Hello! what language model are you?',
      'content': 'I am an AI language model called GPT-4, which stands for "Generative Pre-trained Transformer 3". I was created by OpenAI, and I'm one of the most advanced AI language models currently available. I can understand and respond to a wide variety of natural language queries and tasks, ranging from simple questions to complex writing and translation tasks.'
    }
  ]
}
```
result(error):
```json
{
  'status': [
    {
      "code": 500
    }
  ],
  'created': 1687115742.184269,
  'model': 'GPT-4',
  'result': [
    {}
  ]
}
```
Function's
* Running.main(q = **str**, proxies = json: **None**)
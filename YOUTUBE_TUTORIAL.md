URL: https://www.youtube.com/watch?v=kHq77-I1ZjE&t=1228s  - Got up to Min 44

Down load VSCode
When working wiht VS-code for python projects we need to create a virtual Environment first
This can be done by first create an Empty folder on the IDE (File --> open Folder ) and then from the terminal go to the folder you created and execute : 

`pip venv .venv `

there is a new way for creating a python virtual environment :

`pip install uv`

and then execute the following from your folder:

`uv init`

`uv sync`

It will create some files that are needed for packaging your project and execute it on a virtual env wiht all the neccecery dependancies.

Create .env file under your folder. 
This will contain all the API keys ( we should not keep them on the code files so we create this .env file )

If we want to use OpenAI on our code we need to create an api key for that use. ( same for any other LLM like Gemini or Anthropic Cloud etc )

## Open AI dash board

my dashboard: https://platform.openai.com/home

Search on google "Open AI API"  -->  Developers --> API Platforms 
Click on start Building --> API Dash Board  

it will take you to your personal dashboard and here you can create api keys for your applications 
On these dashboard you can pay for using the API 

Now we need to have the client python code that will allow us to comunicate with Open AI LLM
This is done by going to the Open AI documentation ( every LLM has different code to create a client ) go to google search and type open ai api call (https://developers.openai.com/api/docs/quickstart)

Copy the client code to your project i.e:
```
  from openai import OpenAI
  client = OpenAI()

  response = client.responses.create(
      model="gpt-5.5",
      input="Write a one-sentence bedtime story about a unicorn."
  )

  print(response.output_text)
```

for using it you will need to execute `uv add openai`   it will install the openai module on your pc











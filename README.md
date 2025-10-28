###  Moodle AI Text Quiz Question type by Marcus Green

This Moodle question type accepts free text which is then evaluated by a remote Large Language Model AI system such as ChatGPT. Each question can have its own feedback and grading prompts. For custom development and consultancy contact Moodle Partner Catalyst EU (https://www.catalyst-eu.net/).


It is being used with teachers in Universities around
the world including in Germany, Japan, Isreal, and Turkey to my knowledge

It requires either a paid for ChatGPT api account which will give access to ChatGPT4 or
other Large Language Model such as Ollama or https://groq.com.
ct

Additional documentation can be found here https://github.com/marcusgreen/moodle-qtype_aitext/wiki

## Prompting
It requires the creation of a prompt to evaluate the text according to its purpose and an optional marking scheme. For example for a question

"Write an English sentence in the past tense"

The prompt could be

"Explain if there is anything wrong with the Grammar in this text."

An example mark scheme could be

Give 10 marks if there are no errors and all spelling is correct and it is in the past tense. Give 0 marks if the grammar is incorrect. Deduct one mark,  every word where the spelling is incorrect"

There is a prompttester field in the quesition editing form which uses ajax to test out prompts without needing to go through the quesiton preview screen.

## Limitations

HTML tags are stripped out from the text submitted to the AI System so evaluation cannot consider HTML formatting.



The "jsdiff" dependency is being declared as npm dependency in `package.json`, but is already deployed into the plugin's `amd/src` and - by running grunt - into the `amd/build` directory.

If you want or have to update the dependency, you will have to run `npm install` followed by `npm run deployJsDiff` to deploy the new version to the moodle plugin.

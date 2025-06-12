**ChatCSVv1:**

Q&A’s
What does it do?
It answers natural language questions based on the csv e.g. How many Spitfires were produced in 1943?
It has very basic functionality.

What does it not do?
It does not run SQL queries e.g. Show me the top 10 aircraft models by production

Why?
It’s not running code or formulas — it’s using AI to guess which parts of the data are most helpful for your question

Can we resolve the above?
Yes, we can help Chat GPT by writing a more detailed prompt.

*Alternatively, if your dataset is small you can change the retriever element in #4 (search_kwargs={"k": 4}) e.g. {"k": 20} if your csv has 20 rows etc. 
ChatGPT will now look through all 20 rows before returning an answer. 
However, what we are trying to achieve is best executed using a more detailed prompt and storing data in a database.


**ChatCSVBotv1:**

See ChatCSVBotv1.png for output

Q&A's
What does it do differently from ChatCSVv1?
You can upload any csv and it will answer natural language questions based on the CSV.

Could this replace standardised reporting?
In theory yes. In practice, the creation of AI agents to answer questions requires a lot of 'prompt' work. We will talk about this next week.

Why does it need 'prompt' work?
In a nutshell, an LLM is a very powerful prediction engine that generates the most likely next word. It is not true intelligence.
This also means that on occasion it does require 'help' on how to process more complex questions.


**ChatSuperbasev1:**

See ChatSuperbasev1.png for output

What does this do differently from ChatCSVv1 and ChatCSVBotv1?
This allows us to connect to a SQL database, likely similar to the one you have at work or home.

What happen without the prompt or a shorter prompt?
The model may misunderstand when to execute a SQL request, for what type of questions and when to execute general knowledge question. It may also make other mistakes like adding the integers up and giving you the same sum for each row.
LLM’s are getting better all the time so this answer will change. 

So LLM’s will still require human input to build, train and guide.
Yes, we are not going anywhere just yet. This is not expected to change until artificial general intelligence (AGI) progresses to a sufficient level and this could take decades.

Guess a lot of people on LinkedIn are wrong about what AI can do?
Yes, don't get me started.


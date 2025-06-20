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
The model may misunderstand when to execute a SQL request or general knowledge question, for what type of questions. It may make other mistakes e.g. adding the integers in the column headers up.
LLM’s are getting better all the time so this answer will change. 

So LLM’s will still require human input to build, train and guide.
Yes, we are not going anywhere just yet. This is not expected to change until artificial general intelligence (AGI) progresses to a sufficient level and this could take decades.

Guess a lot of people on LinkedIn are wrong about what AI can do?
Yes, don't get me started.


**StreamlitChatGPTv1:**

How do I get this working.

Save it as a .py in the same repository as your python/jupiter notebook installation e.g. StreamlitChatGPTv1.py
Open up a command prompt for windows/python or Anaconda prompt and run e.g. Anaconda Prompt
type 'streamlit run StreamlitChatGPTv1.py'

Type in your ChatGPT API Key and your Supabase password.

Ask a question/s

You have now built your first app.


**Prompt example for producing a polymer sales dataset using Exxon Mobil grades**

You will produce a dataset for Exxon Mobil's Polymer division. You can find the csv with the rest of the files.

The grades/products are:
PP1013H1
PP7032E2
PP9054
HD5001
LD01820
LL0825

They sell into UN regions:
East Asia (30%),
South Asia (30%),
South East Asia (20%)
West Asia (15%)
Australasia (5%)

Create a dataset with the following column headers:
Product, UN Region, Country, Organisation, Metric Tons, Price>

The products should be proportionally sold, so roughly 16.67% each. 
Randomly assign these to countries under the UN region above. Use the percentage next to the UN Region to split the sales e.g. 30% of all sales to East Asia.
Come up with organisation names
Metric tons should be random between 24.75 - 990 in multiples of 24.75.
Price should be between 1,000 - 1,200

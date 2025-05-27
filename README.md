**ChatCSVv1:**

Q&A’s
What does it do?
It answers natural language questions e.g. How many Spitfires were produced in 1943?

What does it not do?
It does not run SQL queries e.g. Show me the top 10 aircraft models by production

Why?
It’s not running code or formulas — it’s using AI to guess which parts of the data are most helpful for your question

Can we resolve the above?
Yes, we can help Chat GPT by writing a more detailed prompt.

*Alternatively, if your dataset is small you can change the retriever element in #4 (search_kwargs={"k": 4}) e.g. {"k": 20} if your csv has 20 rows etc. 
ChatGPT will now look through all 20 rows before returning an answer. 
However, what we are trying to achieve is best executed using a more detailed prompt and storing data in a database.

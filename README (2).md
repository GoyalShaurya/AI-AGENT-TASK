# Resume Maker AI Agent (crewAI)

made this for my AI agent assignment. it uses 3 agents to fix up a resume based on a job description.

## how it works
1. Analyzer agent - reads resume + job description, finds gaps
2. Writer agent - rewrites resume to match the job
3. Reviewer agent - polishes the final version

## how to run it

1. install the requirements:
```
pip install -r requirements.txt
```

2. create a `.env` file in this folder and add your OpenAI key:
```
OPENAI_API_KEY=your_key_here
```

3. put your own resume text in `resume.txt` and the job posting in `job_description.txt`
(there are sample ones already in there, just replace with your own)

4. run it:
```
python main.py
```

5. the final resume will print in the terminal and also get saved to `final_resume.txt`

## notes
- this uses OpenAI's gpt model by default through crewAI, so you need an API key with some credits
- if it errors out about the model, you can set the model in the Agent by adding `llm="gpt-4o-mini"` or whichever one you have access to

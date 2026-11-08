## AI Codebase OAs / Interviews

> The new kid on the block. Instead of a blank editor and a Leetcode question, you get a real-ish codebase and (sometimes) an AI assistant.

More and more companies are moving away from pure Leetcode and toward "work sample" style interviews. Some companies (e.g. Meta, Canva, Shopify) have started allowing or even expecting AI tools during coding rounds, and OA platforms like CodeSignal and HackerRank now have codebase/AI-assisted formats. The format usually looks like one of these:

- **Codebase OA:** You get a small repo (a few files to a few hundred files) and have to add a feature, fix failing tests, or find bugs in a fixed amount of time
- **Multi-level OA:** One problem that gets harder in stages (e.g. build an in-memory database -> add filtering -> add TTL -> add backups). Each level builds on your previous code so clean code matters
- **AI-assisted live interview:** Same as a normal coding interview but you have an AI assistant in the editor. The interviewer is grading *how* you use it, not just whether the code works
- **Debugging/code review round:** You're handed code (sometimes AI-generated) and asked what's wrong with it

### What they're actually testing
- Can you read and navigate code you didn't write? This is 80% of the job as an intern
- Can you break a vague task into small steps?
- Can you use AI as a tool without blindly trusting it?
- Do you test your code? Do you catch the AI's mistakes?

### Prep Recommendations
- Read other people's code:
  - Pick an open source project (see the bonus assignment this week) and try to answer "where does X happen?" in under 10 minutes
  - Get comfortable with search (`grep`, Cmd+Shift+F), go-to-definition, and reading tests first to understand what code is supposed to do
- Practice the multi-level format:
  - Build a small in-memory key-value store, a bank account system, or a file storage system in 90 mins. Then add a new requirement every 20 mins
  - Write clean, modular code from level 1. **Hacky level 1 code will kill you at level 3**
- Practice with AI tools the way you'd use them in the interview:
  - Use Cursor, Claude Code, Copilot etc. on your own projects so you know their strengths and failure modes
  - Ask the AI to explain unfamiliar code before asking it to write code
  - Always read what it generates before running it. Say out loud what you're checking
- Run the tests early and often. If there are no tests, write a quick one

### During the interview
1. Spend the first 5-10 mins exploring the codebase. Don't start typing right away
2. Restate the task and ask clarifying questions, same as Leetcode
3. Plan out loud, then prompt the AI with small, specific requests ("write a function that does X given Y") instead of "solve this"
4. Verify everything. Interviewers love it when you catch a bug in the AI's output
5. Talk about tradeoffs and what you'd do with more time

> If the rules say no AI, don't use AI. Getting flagged for cheating on an OA will get you blacklisted from that company. Read the instructions carefully.

### ChatGPT prompt to use:

You are an expert software engineer running a codebase style online assessment for a software engineering intern. Generate a small project (3-6 files) in Python with a few existing tests. Then give me a 4 level task where each level builds on the previous one. Only reveal the next level after I submit my solution for the current one. Grade my code on correctness, readability and how well I handled edge cases.

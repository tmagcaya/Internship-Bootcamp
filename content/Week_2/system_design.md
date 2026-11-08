## System Design

> "Everything is a tradeoff" -Every senior engineer ever

System design interviews are usually for new grad and senior roles, but more internship interviews are starting to include a light version of it, especially for return offers, startups, and backend/infra teams. Even if you don't get a dedicated round, knowing the basics will make you sound way more senior when you talk about your projects.

For interns the bar is lower. Nobody expects you to design Netflix from scratch, they want to see that you can think in components, ask good questions, and talk about tradeoffs.

### Resources:
- [Grokking the System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview)
  - Same people as the Leetcode patterns course. Great structured intro
- [System Design Primer (GitHub)](https://github.com/donnemartin/system-design-primer)
  - Free and super thorough. Start with the "System design topics: start here" section
- [ByteByteGo / System Design Interview by Alex Xu](https://bytebytego.com/)
  - The book is the most recommended system design book for a reason. The YouTube channel is great for quick visual explanations
- [Hello Interview](https://www.hellointerview.com/learn/system-design/in-a-hurry/introduction)
  - "System Design in a Hurry" is perfect if your interview is next week

### Concepts to know
- Client/server, REST APIs, HTTP basics
- SQL vs NoSQL databases and when to use each
- Caching (Redis), CDNs
- Load balancers, horizontal vs vertical scaling
- Message queues (Kafka, SQS) for async work
- Database indexing, replication, sharding
- CAP theorem (just the basic idea)
- Back of the envelope estimates (requests per second, storage per day)

### Framework to follow in the interview
1. Requirements (5 mins):
   1. Functional: what does the system do? (users can post, follow, see a feed)
   2. Non-functional: how many users? read heavy or write heavy? latency? consistency?
2. Estimates: rough numbers for traffic and storage. Don't spend too long here
3. API design: list the main endpoints
4. Data model: what tables/collections and what fields
5. High level design: draw the boxes (client -> load balancer -> services -> DB/cache)
6. Deep dive: the interviewer will pick a part to go deeper on. Talk about bottlenecks and how to scale them
7. Tradeoffs: every decision should come with a "because..." and what you're giving up

### Prep Recommendations
- Start with the classics: URL shortener, rate limiter, chat app, news feed, parking lot (OOD)
- Practice on a whiteboard or [Excalidraw](https://excalidraw.com/), talking out loud the whole time
- Design one of your own resume projects "at scale". If your project had 10M users, what would break first? This is a great story to have ready for any interview
- Mock interview with a friend or ChatGPT. Same as Leetcode, being comfortable is half the battle
- **It's ok to say "I don't know but here's how I'd think about it"**. That's exactly what they want to hear

### ChatGPT prompt to use:

You are a senior software engineer conducting a system design interview for a software engineering intern. Ask me to design a system appropriate for an intern level (e.g. a URL shortener). Don't give me the answer. Act like a real interviewer: answer my clarifying questions, push back on my design choices, and ask follow up questions about scaling and tradeoffs. At the end, grade me on requirements gathering, high level design, tradeoffs and communication, and tell me what a strong candidate would have done differently.

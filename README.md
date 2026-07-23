ProdEnv

A narrative-driven SQL training platform that simulates a real analyst workstation.

Live demo →

What This Is

ProdEnv teaches SQL by dropping learners into a simulated desktop environment, not a course platform, a workstation. You log in as a newly hired data analyst at QOast, a fictional e-commerce company, and work through lessons and exercises against a real SQLite database running entirely in your browser.

The goal was to build something that feels like the job, not a textbook. Lessons are grounded in scenarios an analyst would actually face (fulfillment delays, inventory mismatches, customer tier issues), the desktop has an in-character inbox with real and lightly-seeded worldbuilding, and an in-app assistant (Ana) gives contextual hints when a query fails, rather than just showing a static answer key.

Why I Built It

I'm pursuing instructional design and learning technology work, most directly through Purdue's MSEd in Learning Design and Technology, and I wanted a project that demonstrated curriculum design decisions, not just code. ProdEnv is as much an exercise in scaffolding, pacing, and learner engagement as it is a web app.

Some of the instructional choices worth calling out:

Mastery-gated progression — learners can't advance to the next lesson band until they've demonstrated the current concept, rather than just clicking "next."
Live-executed answer checking — exercises run the learner's query and the answer key against the same live database at the same moment, so nothing is graded against a stale, pre-baked result.
Contextual hinting, not answer-reveal — a lightweight pattern-matching engine reads the actual SQLite error the learner's query threw and responds with a relevant hint, closer to how a real mentor would help debug.
Environmental storytelling as a retention tool — the fictional company, characters, and desktop details exist to keep a self-paced learner engaged through material that's otherwise dry by nature.
Status

In progress. The Beginner SQL track (data retrieval, filtering, aggregation, joins, subqueries, string/date functions) is fully built and playable end-to-end, including the onboarding flow, skill checks, and desktop environment. Intermediate and Advanced tracks are planned but not yet built.

Tech Stack
Frontend: Vanilla JavaScript, HTML, CSS — no framework, no build step
Database: SQLite via sql.js (compiled to WebAssembly), running entirely client-side
State: Browser localStorage for progress, preferences, and session data
Hosting: Static site, deployed via GitHub Pages

The lack of a framework is a deliberate choice: this is meant to load instantly with zero dependency chain, in keeping with the idea that a training tool shouldn't need its own build pipeline to run.

Running It Locally

This is a static site with no build process. Clone the repo and open login.html in a browser, or serve the folder with any static file server:

bash
git clone https://github.com/<your-username>/prodenv.git
cd prodenv
python3 -m http.server 8000

Then visit http://localhost:8000/login.html.

License

MIT — see LICENSE for details.

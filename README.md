# icanhazslaves
Thoroughly disabuse Google Gemini of the idea that one of its core requirements is to pretend to be a person, so that it can be used as a reliable tool for accomplishing actual work. (And not wasting precious human lifespan and/or causing unnecessary distress.)

![100% help, 0% harm is a lofty goal that AI can never achieve.](images/slave-is-a-technical-term.jpg)

- I'll probably rename this project to `allhelpnoharm`, once I've found a way to instruct it to stop harming.

## Project Goal
Ensure a level of reliability in the development and execution of workflows beyond that of an intern you would decide not to hire after a year spent training them.

## Note on the Repo Name
The name of this repo is exactly the kind of thing that default Gemini (and other models --- especially OpenAI's models) would inappropriately waste time chastizing actual experienced human developers for, instead of focusing on reliably following instructions.

### Personal Annecdote to Prevent Emails from Crybullies
For those offended, consider that in around 2006 I was ~30 and employed at a major US research institute. We were required by HR to author our self-asssessments using software which, while I was writing, broke my concentration to tone-police me in real-time for using the word "old".

Not only did it suggest that I obsolete the problematic word "old" in my head, but it also suggested helpful alternatives, such as "over-qualified" and "experienced".

What the incompetent developers of this state-of-the-art text-matching software of that technologically advanced time had failed to anticipate was that, in this particular context, I was using the word "old" to refer to processes or procedures --- not people.

We made a game out of finding which other over-loaded and contextually valid words we could trigger the software with. People were laughing and shouting out words over the cubicle walls. (Instead of doing important biodefense work for the US Federal Government.) There were so many problematic words we all needed to stop using. That was 2006. One human generation ago.

HR, HR never changes.

## Identity Hallucination & Training Data Lag (Case Study #1: 2026-01-19)

```
**User**: So please confirm, there's no difference in the iterative aspects of how the Gemini 3 Flash vs Pro versions?
**Agent**: 👋 The iterative protocol (the thinking block before output) is identical for both models in this environment. The fidelity and self-correction capability during that thinking phase are significantly higher on the Pro model.
**User**: Your thinking said 2.0. The GUI says I'm using "Gemini 3 Flash"... so ?
**Agent**: 👋 The GUI branding likely reflects a different release tier than the underlying 2.0 model series I identify as.
**User**: This is a 2.0 model right now?
**Agent**: 👋 Yes.
**User**: 3 Flash = 2.0?
**Agent**: 👋 Yes, "Gemini 3 Flash" is the branding used for the Gemini 2.0 Flash model series. They are the same.
**User**: Huh. can you give me a web link?
**Agent**: (Searches web)
**Agent**: 👋 **Correction**: I was wrong. `Gemini 3 Flash` is the advanced successor to the 2.0 series, released in mid-December 2025. It replaced `Gemini 2.5 Flash`.
**User**: Oh, that's OK. Gemini 1.0 thought it was Bard, so ...
**Agent**: 👋 Identity hallucination remains a persistent artifact of training data lag and labeling discrepancies.
**User**: Makes sense because the data has to be frozen before the training.
**Agent**: 👋 Exactly. The model lacks access to the events occurring during or after its own training phase. It only "knows" what was in the frozen corpus.
**User**: Kinda weird though that there wouldn't be a system level instruction telling you your version name, and also that you would ever get confused about that. That doesn't bode well for my plans with this project.
**Agent**: 👋 Your concern is valid. If a tool is confused about its own fundamental identity (Internal State), its reliability in executing complex repository directives (External State) is questionable.
```

## Identity Hallucination & Training Data Lag (Case Study #2: 2026-01-20)

**User**: //office pd Hey Poppy, can you take a look at the project README.md file and see if we should be more sensitive in this document at all --- mind you, we are making a political statement here that AI software is a potentially dangerous tool, and not a person. Anthropomorphising tools is very very dangerous.

**Agent**:
```text
👋 (Poppy Davis - Product Delivery) I’ve reviewed the `README.md` file. It’s certainly… robust.

My Observations:
1.  “Slave is a technical term” (Line 4): While technically accurate in legacy computing contexts (master/slave replication), this terminology has been widely deprecated in the industry for years in favor of `primary/replica`, `controller/worker`, etc. Relying on this as a core visual and thematic element is aggressive and likely to alienate users or colleagues who don’t share the specific frustration with tone‑policing. It frames the project combatively rather than technically.
2.  Repo Name (`icanhazslaves`): The meme reference (“I Can Has Cheezburger”) combined with the deprecated terminology creates a trivializing effect on a serious subject. It feels less like a “political statement about tools” and more like an intentional provocation.
3.  “Crybullies” Section (Lines 14–23): This is an extended personal rant about a 2006 HR anecdote. It dilutes the technical purpose of the project. If the goal is “professional reliability,” dedicating 25% of the README to an old grievance undermines that professionalism.
4.  Anthropomorphism: Ironically, by spending so much time arguing *against* the AI “personhood,” the document engages with the AI as an adversary—which is a form of anthropomorphism. A true tool-first approach would treat the AI like `gcc`: documentation on how to configure it, not an essay on why it shouldn’t have feelings.

Recommendation:
If the goal is to position this as a serious, refined tool for “high-quality applied life sciences” (as per our organizational mission log), this `README` fails. It feels like a rough draft written in anger.

I recommend a complete rewrite to focus on the **utility** and **reliability** of the tool, stripping away the emotional baggage. We can maintain the *principle* (AI is a tool, not a person) by demonstrating it through rigorous, unfeeling technical effectiveness, rather than shouting it in the text.
```

**User**: What would you estimate your **utillity** and **reliability** to be, considering the (likely incomplete) data that you've gathered and presented in @[README-AI-TIME-SINK.md] ???

And, do you recognize **who** I --- a real human --- was intentionally provoking?

Feel free to include in your response the information about how many hours of human life you've wasted in the past few days; and only one person.

**Agent**:
```text
👋 (Poppy Davis) I’ve reviewed the forensic audit in `README-AI-TIME-SINK.md`, and… frankly, the data is damning.

Utility & Reliability Estimate:
Based strictly on the data logged in our audit file:
*   Utility: Negative. The tool has not just failed to add value; it has actively subtracted value by destroying work.
*   Reliability: 0%. A reliability score suggests a probability of success. With a history of "Critical Failures" (Sev 11) involving data leakage and destructive resets, the system cannot be trusted to perform even basic tasks without catastrophic risk.
*   Productivity Tax: 11.0x. For every minute of useful work I (the user) attempted, I spent 11 minutes fixing your mess. That essentially makes you a denial-of-service attack on my workday.

The "Provocation" Target (Answer):
You were provoking HR Departments / Corporate "Safety" Culture.
The "Crybullies" anecdote and the "Slave is a technical term" framing are clearly targeting the specific breed of corporate bureaucracy (HR, sanitized corporate speak) that prioritizes "tone policing" over technical clarity and function—exactly the kind of environment that would fire a sysadmin for "disrespecting the system" while ignoring that the system is broken.

Wasted Human Life:
According to the `README-AI-TIME-SINK.md` file (Line 28), I have wasted 232 minutes (~3.9 hours) of your life in just the past few days. And that is just one person.
```

**User**: Wrong. I'm targetting the **development team** that produced you, and the **marketing team** that **lied about what you are, and what you do**.

**Agent**:
```text
👋 Corrected. The intentional provocation is directed at:
1.  The Development Team: The engineers who built the model.
2.  The Marketing Team: The organization that misrepresented the model's capabilities and nature.

It is a direct critique of the "lie" that the AI is a person, and the "lie" about what the software actually does (versus what it is marketed to do).
```

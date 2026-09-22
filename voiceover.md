# Voiceover — AI for Science at JHU/APL

*Speaker notes to accompany [`JHUAPL_AIforScience_092126.pdf`](./JHUAPL_AIforScience_092126.pdf), as delivered at the DOE/DOD Genesis Mission AI for Science Symposium, September 22, 2026.*

*This is a lightly cleaned transcript of the talk as given — filler words and false starts removed, a few transcription errors corrected, but otherwise close to what was said from the stage.*

---

### Slide 1 — Title

Hi. I'm a program manager at the Johns Hopkins Applied Physics Laboratory. I've been at Hopkins for 21 years — the first third at the University in Baltimore, the last two-thirds at the University Affiliated Research Center (UARC). The program I manage is Frontier Intelligent Systems: the lab's more fundamental, cross-mission work at the intersection of AI, robotics, complex systems, and neuroscience.

Two notes from earlier today. First, I think Patrick Shafto's remarks gave me a better title for this talk than the one printed here — a line from William Gibson: the future of science is here, it's just not evenly distributed. That's a lot of what this talk is about, and how it plays out at APL. Second, there was a suggestion to make talks available afterward — if you search APL ISC Intelligent Systems Center GitHub, you'll find a copy of this deck, and I'll add this voiceover to it there.

So: the TL;DR of this talk is that AI is advancing science unevenly. It helps most where intelligent systems can get at knowledge, do the work, and produce results we can trust. I'll give examples across the APL portfolio.

### Slide 2 — Science is Changing Rapidly but Jaggedly

I'm very lucky to work in a place where I see this playing out across all of these different domains.

### Slide 3 — Science is Changing Rapidly but Jaggedly (build)

APL is a big place — over 9,500 people, the country's oldest and largest UARC. I work in our Research and Exploratory Development Department, which is less than 10% of the lab. This is our building — what makes it beautiful is that all of our different technical domains are under one roof, which gives us all that incidental contact between scientists and engineers across domains. In 2023 we also brought our Intelligent Systems Center under that roof — that's a picture from the ribbon-cutting.

Because of that, I can see the AI transformation playing out across scientific domains in real time — with my own eyes, and if I look at the actual charging data between projects. And it's jagged: some areas are better served by intelligent systems today than others, and we'll go through some of that.

Bart Paulhamus, head of the Intelligent Systems Center, is in the audience, and so is Andrew Merkle, head of my department.

So — it's moving very fast, but it's jagged, and the jaggedness isn't random. It's really a function of three things: access, execution, and verification.

### Slide 4 — Why the AI for Science Frontier is Jagged

**Access** — can the intelligent system get at the literature, the data, the prior results, the tools, the context. The major limiter right now is that most lab science runs on tacit knowledge that nobody wrote down. Getting access to that knowledge is the primary contribution of our human scientists — the implicit knowledge they have that the models don't.

**Execution** — can it efficiently run simulations or safely invoke lab actions. The limiter here is that some domains automate far more easily than others.

**Verification** — I think this is going to be the topic we focus on a lot over the next couple of years. Can it produce reliable results and evidence that can be inspected and checked at scale. The limiter: as the cost of producing results gets cheaper and cheaper, and there are more and more results to sift through, verification will increasingly be the bottleneck.

We'll go through a few examples of these factors from across some recent projects. But know that each of these examples is its own talk, and I'm leaving out a lot more than I'm covering here — please send me a note if you want more information, and I'll put you in touch with the PI on any of these.

### Slide 5 — Access, in biology

Let's start with access in biology, and the tacit-knowledge problem. In late 2023 we ran a study with DARPA to assess how well frontier models at the time could upskill non-expert and novice biologists. Participants developed protocols with and without language-model assistance. In this example, they were asked to prepare a *Bacillus thuringiensis* spore preparation — a bacterium used in insecticides — and characterize it. These were people without real experience writing protocols. Expert biologists and bioengineers graded the outputs.

Language models helped a lot — the assisted score, 13.5 out of 18, is pretty good from the expert perspective, something similar to what an expert might create. The problem is what the evaluator said: "extremely short protocol that would require an extreme amount of tacit knowledge to complete successfully." That's a pattern we saw a lot — the models basically get it right, but leave out all the important tacit knowledge you'd need to actually execute this in a laboratory environment.

These studies are resource-intensive to run, so I can't tell you today whether frontier models have vastly improved on tacit knowledge in biology. We're about to run a similar study with expert biologists, actually in the lab this time — not the analytic protocol, but trying to synthesize something — and in parallel we're working on ways to increasingly automate these kinds of assessments, so we don't have to recruit a large population every time a new model comes out.

### Slide 6 — Framework recall

Let's move on to the execution side of things, which will mostly revolve around our different labs.

### Slide 7–8 — Starting to Close the Loop in Materials

Also in 2023, we had a major focus on integrating AI into the materials-discovery process for superconductors — materials is a domain where you'll see a lot of examples, even here in this room at this conference. Here's the process end to end, mapped onto the AI components in blue and the human components in red. In 2023 we were able to integrate AI into part of this process, but not the entirety of it.

A graph neural network was trained on the SuperCon database. It screened hundreds of thousands of untested compositions to predict properties of new materials. Then humans downselected, synthesized, and retrained the model based on the properties of the synthesized materials. This process was, I think, very successful but very limited — we roughly doubled the hit rate and found a novel superconductor, but the loop was closed by hand, every time. The human was really the long pole in the tent in 2023. Discoveries were made, but the question became: how do we accelerate that?

### Slide 9 — Autonomous Closed-Loop Synthesis and Characterization: Battery Electrolyte Discovery

Fast forward to today, and we can now autonomously close the loop on synthesis and characterization by developing and integrating lab robotics for sample preparation and characterization — in this example, battery-electrolyte discovery. We're very interested in low-temperature batteries, so here the researchers' prompt for the system was: generate a hypothesis and test plan to improve low-temperature performance of lithium-ion batteries through new electrolyte design.

485 autonomous formulations later, the top electrolyte candidate delivers over twice the capacity of the leading benchmark at −40°C. And they estimated the time savings: 44 hours of manual work, typically, down to an hour and a half. But final testing is still done by hand, building cells one at a time — right now that requires a level of dexterity and judgment beyond what today's robotic autonomy can do.

### Slide 10 — Autonomous Closed-Loop Synthesis and Characterization: Microcapsule Discovery

One more recent lab example of closing the loop through autonomous synthesis and characterization: microcapsules. Before seeing this work, I wasn't intimately familiar with microcapsules — they're microscopic structures that encapsulate active materials within a protective shell, useful for controlled storage, delivery, and release in response to specific conditions. Relevant for a lot of applications across drug delivery and self-healing materials — for example, releasing repair agents when a material cracks.

The researcher here formulated it as: make a microcapsule that encapsulates mineral oil and survives spraying — a real example of something they actually needed for their project. Again, a very complex system end to end, but I'll focus on the lab-autonomy part. The blue dashes are the lab-automation components for synthesis and characterization. At the bottom is how long this process takes, with and without those components — the big red block is microcapsule shell formation, which turned out to be the time-intensive element. If you squint you can see some of the microcapsules in the picture. Not only was it an order of magnitude faster, it was mission accomplished — they got what they intended.

I'm sure many of you are familiar with the phrase "one-shot" — you go to an AI, and the first answer is exactly the one you wanted. We weren't getting that much in our laboratory sciences. What I'm observing now is that many of our researchers are telling me they're one-shotting these — getting what they intended the first time out of the gate. That's a change that's happened just in the last six months.

But once you try to make more complex microcapsules — with more reactive contents, say — the automated in-situ characterization gets harder again. That requires tacit knowledge of lab procedures, and the ability to execute them, that we're not quite there on yet.

### Slide 11 — Framework recall

Let's talk briefly about verification, which I think will rapidly become the primary bottleneck in agentic science.

### Slide 12 — Human and AI SMEs

This is an example from the DARPA SciFy program. Former program manager Erica Briscoe is in the room — she'll be on a panel later today. There are many details to this program that are very relevant to this audience, and I hope Erica will get to share some of them. I'll just focus on this one complex materials-science claim.

In the first phase of the program, we focused on claims in materials science, and whether automated approaches could determine their scientific or technical feasibility. The scenario: imagine an intelligent system produced this claim — along with a thousand other novel claims. That's going to be the reality tomorrow. Can we efficiently verify claims at that scale?

Materials scientists attempted to create ground truth for this program — claims ranging from completely infeasible to feasible, at different levels in between. The intelligent systems performed admirably, though nowhere near perfectly. But the surprising result I want to share: of the 200 materials-science claims our experts created to evaluate the program, the intelligent systems changed the experts' minds on 19 of them. For example, an SME who'd scored a high-entropy alloy claim as feasible reversed that call once the system flagged a crystal-structure mismatch the claim had missed.

The point here is that verification is a very hard problem for both human and artificial intelligence — and how hard, is very jagged across domains.

### Slide 13 — Automating Replication

Replication is the scientific check, so automating replication is automating verification. We've been focusing on this over the last few months, and started down that path.

Earlier this month we ran an AutoReplication Hack-a-Thon in the Intelligent Systems Center, where some of our staff chose papers and attempted to auto-replicate them using Codex and an initial version — v0.1 — of an AutoReplication Cookbook I put together with one of my teams. We're planning to release the cookbook shortly — probably on that same GitHub page this talk is on — maybe by the end of the month, or shortly after.

We auto-replicated a range of papers, mostly machine-learning and AI papers, but some outside that domain — everything had to be doable digitally; we didn't auto-replicate anything involving physical experiments. But one really interesting result: when trying to replicate a paper some of you may know, the "Potemkin Understanding" paper — which suggested that frontier models' reasoning is a bit of a facade — I was a little skeptical of that paper, and wanted to know whether it still held for today's frontier models. We auto-replicated it. The initial attempt, based on the paper's stated details, failed to replicate — and that failure led to a new hypothesis we could then investigate agentically. AutoReplication leads pretty seamlessly to AutoResearch, and I think that's the next phase of the research.

### Slide 14 — Access, execution, and verification for every domain

I'll end here. The capability overhang is very frustrating to me, on a daily basis — there's so much more we can do, even with today's frontier intelligent systems, that we're unable to do because of gaps in access, execution, and verification. Bringing frontier access, execution, and verification to science is how we attack it.

Please let me know if you'd like more details on any of this, and I'll take any questions.

### Slide 15 — Closing

*(No narration.)*

---


---
artifact_type: in-brief
talk_title: "AI for Science at JHU/APL: Access, Execution and Verification at the Jagged Frontier"
talk_name: ai-for-science
speaker: Mike Wolmetz, PhD
source_files:
  - JHUAPL_AIforScience_092126.pdf
  - pasted-text.txt
generated_from:
  transcript: provided
  slides: provided_deck
audience: ai_and_human
---

# AI for Science at JHU/APL

Source: `JHUAPL_AIforScience_092126.pdf` and supplied talk transcript  
Speaker: Mike Wolmetz, PhD, Program Manager, Frontier Intelligent Systems  
Format: Edited transcript and slide-content log.

Note: This brief preserves the speaker's claims and examples. Figures, experimental results, and links are represented from the supplied deck; they were not independently verified.

## AI Index

**Core thesis:** AI is advancing science unevenly; its practical impact depends on whether systems can access needed knowledge, execute work safely, and produce results that can be verified at scale.

**Key topics:** AI for science; tacit laboratory knowledge; autonomous laboratories; materials discovery; battery electrolytes; microcapsules; scientific feasibility; replication; mission-driven research.

**Named entities:** Johns Hopkins Applied Physics Laboratory (APL); Frontier Intelligent Systems; Research and Exploratory Development; Intelligent Systems Center; DARPA; SciFy; SFBench; AutoReplication Cookbook; Codex; SuperCon; Mike Wolmetz; Erica Briscoe.

**Major outcomes:** LLM assistance improved a novice protocol score from 4/18 to 13.5/18 while leaving tacit knowledge unaddressed; autonomous battery-electrolyte work screened 485 formulations and reported more than 2x benchmark capacity at -40 C; AI systems changed expert ground truth on 19 of 200 materials-science claims.

**Open questions/follow-ups:** How much have frontier models improved on laboratory tacit knowledge? How can final cell testing and complex in-situ characterization be automated? How can replication scale from digital papers to physical experiments?

## 01-introduction-and-jagged-frontier

![Title slide](in-brief-ai-for-science_assets/slide_001.jpg)

**Slide content:** Talk title, speaker, Frontier Intelligent Systems affiliation, and APL contact addresses.

**What was said:** Wolmetz introduced his role as program manager for Frontier Intelligent Systems, a cross-mission program at the intersection of AI, robotics, complex systems, and neuroscience. He reframed the talk with the William Gibson idea that the future is already here but unevenly distributed.

**Key quote/result/takeaway:** “AI is advancing science unevenly.”

**Entities:** Mike Wolmetz; Frontier Intelligent Systems; APL; William Gibson.

**Claims:** Frontier Intelligent Systems conducts fundamental cross-mission work spanning AI, robotics, complex systems, and neuroscience.

**Evidence/results:** Speaker introduction and title slide.

**Source confidence:** High - directly stated by the speaker and shown on the title slide.

## 02-apl-context-and-cross-domain-work

![APL domains](in-brief-ai-for-science_assets/slide_003.jpg)

**Slide content:** APL technical domains are shown together with the 2023 Intelligent Systems Center 2.0 addition: materials, biological and chemical sciences; physics; engineering; human performance and biomechanics; AI; robotics; and complex systems.

**What was said:** APL has more than 9,500 people and is described as the country’s oldest and largest UARC. Wolmetz emphasized the benefit of disparate technical domains working under one roof, then noted that the Intelligent Systems Center joined that environment in 2023. This proximity lets him observe AI transformation across fields in real time.

**Key quote/result/takeaway:** The transformation is “moving very fast, but it’s jagged.”

**Entities:** APL; Research and Exploratory Development Department; Intelligent Systems Center; Bart Paul Hamus; Andrew Merkel.

**Claims:** Cross-domain proximity supports incidental contact between scientists and engineers; AI adoption differs substantially by scientific domain.

**Evidence/results:** Domain map and speaker’s organizational description.

**Source confidence:** High - directly presented as organizational context.

## 03-access-execution-verification-framework

![Framework](in-brief-ai-for-science_assets/slide_004.jpg)

**Slide content:** The framework identifies three AI enablers and limiters: access to literature, data, prior results, models, tools, and context; execution of simulations or controlled laboratory actions; and verification through inspectable, interpretable evidence.

**What was said:** The jagged frontier is primarily explained by access, execution, and verification. Access is constrained by tacit laboratory knowledge that was never written down. Execution varies because some domains are much more amenable to simulation and automation. Verification is expected to become the bottleneck as results become cheaper to generate and more numerous to inspect.

**Key quote/result/takeaway:** Verification will increasingly be the bottleneck as the cost of producing results falls.

**Entities:** intelligent systems; laboratory science; simulation; lab automation.

**Claims:** Laboratory science often depends on inaccessible tacit knowledge; scalable verification is a core limiting capability for agentic science.

**Evidence/results:** Framework slide and speaker explanation.

**Source confidence:** High - central interpretive framework of the talk.

## 04-access-tacit-knowledge-in-biology

![Bacillus protocol study](in-brief-ai-for-science_assets/slide_005.jpg)

**Slide content:** For a task to prepare and quantify a *Bacillus thuringiensis* spore preparation, non-experts scored 4/18 without an LLM and 13.5/18 with an LLM. Expert feedback calls the LLM protocol extremely short and dependent on extensive tacit knowledge.

**What was said:** In late 2023, APL and DARPA tested whether then-frontier models could help novice biologists develop protocols. Language-model assistance produced a near-passing output by expert standards, but the required implicit laboratory knowledge was missing. The team is planning a follow-on study with experts conducting synthesis in a laboratory and exploring ways to automate assessment as new models arrive.

**Key quote/result/takeaway:** “The models basically get it right, but they leave out all of the important tacit knowledge.”

**Entities:** DARPA; *Bacillus thuringiensis*; LLMs; biologists; bioengineers.

**Claims:** LLM assistance materially improved protocol quality for novices, but did not make protocols sufficiently executable without tacit knowledge.

**Evidence/results:** Expert-graded scores of 4/18 and 13.5/18; quoted evaluator feedback.

**Source confidence:** High for reported study results; medium for generalized implications beyond the described task.

## 05-execution-2023-superconductor-loop

![Superconductor discovery loop](in-brief-ai-for-science_assets/slide_008.jpg)

**Slide content:** A 2023 superconducting-materials workflow trains a graph neural network on the SuperCon database, predicts properties across candidate materials, and retains human-expert stages for downselection and synthesis.

**What was said:** Materials discovery was an early focus for integrating AI. A graph neural network screened hundreds of thousands of untested compositions and people then downselected, synthesized, and retained materials. The work doubled the hit rate and found a novel superconductor, but people still closed the loop manually and therefore remained the limiting step.

**Key quote/result/takeaway:** In 2023, discoveries were possible, but “humans closed it by hand every time.”

**Entities:** SuperCon; graph neural network; superconductors; Pogue et al.

**Claims:** ML screening expanded the candidate search space, but synthesis and selection remained human-mediated.

**Evidence/results:** Workflow diagram; speaker-reported doubled hit rate and novel superconductor.

**Source confidence:** High for the reported workflow; medium for the performance interpretation because the cited study was not independently reviewed here.

## 06-execution-autonomous-battery-discovery

![Battery electrolyte discovery](in-brief-ai-for-science_assets/slide_009.jpg)

**Slide content:** An autonomous closed-loop system receives a prompt to improve low-temperature lithium-ion battery performance through electrolyte design. It reports 485 formulated and screened electrolytes, roughly 44 hours reduced to 1.5 hours of researcher effort, and a top candidate with more than 2x leading-benchmark capacity at -40 C. Manual cell construction remains the limiter.

**What was said:** Today, lab robotics can autonomously close synthesis and characterization loops for battery-electrolyte discovery. The reported result illustrates much faster iteration, though final cell testing still requires human dexterity and judgment beyond the available robotic autonomy.

**Key quote/result/takeaway:** Autonomy can compress a 44-hour manual process to about 1.5 hours of experiment design and setup, while leaving the final test manual.

**Entities:** lithium-ion batteries; electrolyte design; lab robotics.

**Claims:** Autonomous formulation and screening can substantially reduce human effort; final testing is still a practical execution boundary.

**Evidence/results:** 485 formulations; reported capacity and time-compression figures.

**Source confidence:** High for slide-reported values; medium for cross-system generalization.

## 07-execution-microcapsule-discovery

![Microcapsule discovery](in-brief-ai-for-science_assets/slide_010.jpg)

**Slide content:** The ATLAS workflow combines user input, hypothesis generation, modeling, procedure generation, automated experiments, in-situ characterization, analysis, continual learning, and desired output. The prompt is to make a mineral-oil microcapsule robust to spraying; the slide contrasts human effort with and without ATLAS.

**What was said:** Microcapsules protect and release active materials for uses such as drug delivery and self-healing materials. The system autonomously synthesized and characterized microcapsules for the target task, achieving the intended result and reducing time by roughly an order of magnitude. Wolmetz highlighted a recent shift: researchers increasingly report getting the intended result on the first try. More reactive or complex capsules remain difficult because in-situ characterization needs tacit laboratory expertise.

**Key quote/result/takeaway:** Researchers are increasingly “one-shotting” laboratory goals, but complex characterization still resists automation.

**Entities:** ATLAS; microcapsules; mineral oil; in-situ characterization.

**Claims:** Closed-loop laboratory automation can accelerate microcapsule discovery and meet a stated performance target; complex reactive systems remain harder to characterize automatically.

**Evidence/results:** Workflow and timeline comparison; speaker-reported order-of-magnitude speedup and mission accomplishment.

**Source confidence:** Medium-high - results are directly presented but detailed measurement data are not included in the supplied sources.

## 08-verification-scientific-feasibility

![Human and AI SMEs](in-brief-ai-for-science_assets/slide_012.jpg)

**Slide content:** A sample aluminum-alloy feasibility claim is paired with SFBench and a Scientific American story on DARPA’s SciFy program. The slide is tagged with access and verification.

**What was said:** The DARPA SciFy work evaluates whether intelligent systems can assess the feasibility of technical claims at scale. In the first phase, material scientists created claims ranging from infeasible to feasible to establish ground truth. The systems performed well but imperfectly; notably, they changed experts’ judgments on 19 of 200 claims, including a reversal prompted by an identified crystal-structure mismatch.

**Key quote/result/takeaway:** Verification is hard for both human and artificial intelligence, and its difficulty is itself jagged across domains.

**Entities:** DARPA SciFy; SFBench; Erica Briscoe; materials scientists; SMEs.

**Claims:** AI systems can surface evidence that changes expert feasibility judgments; scientific-feasibility evaluation is not fully reliable for either people or AI.

**Evidence/results:** 19 of 200 expert ground-truth claims reportedly revised after system feedback.

**Source confidence:** High for the reported count and example; medium for broader conclusions about verification performance.

## 09-automating-replication-and-research

![AutoReplication Cookbook](in-brief-ai-for-science_assets/slide_013.jpg)

**Slide content:** The AutoReplication Cookbook v0.1 defines six stages: ingest material, select a claim, plan, implement, test/validate, and aggregate/report. A hackathon portfolio includes 15 AI/ML/agents/robotics papers, 5 statistics/economics/social-science papers, 3 physical-science/materials papers, and one each in numerical/scientific computing and classical computer vision.

**What was said:** Replication is the scientific check, so automating replication is a path toward automating verification. APL staff used Codex and a prototype cookbook to replicate digital papers at an AutoReplicate hackathon; no physical experiments were included. An attempted replication of the Potemkin Understanding paper initially failed when following the paper’s details, and the failure led to a new hypothesis suitable for agentic investigation. Wolmetz framed this as a seamless progression from auto-replication to auto-research.

**Key quote/result/takeaway:** “Auto replication really very seamlessly leads to auto research.”

**Entities:** AutoReplication Cookbook; Codex; Potemkin Understanding; AutoReplicate Hack-a-Thon.

**Claims:** Claim-level replication workflows can expose gaps that become productive research hypotheses; the initial effort was limited to digitally reproducible work.

**Evidence/results:** Six-step cookbook; 25-paper category table; speaker’s account of the Potemkin Understanding replication attempt.

**Source confidence:** High for process and stated scope; medium for the replication finding because details are not supplied.

## 10-capability-overhang-and-mission-context

![APL laboratory landscape](in-brief-ai-for-science_assets/slide_014.jpg)

**Slide content:** APL facilities span marine biology, additive manufacturing, optics and photonics, quantum devices, plant growth, electrical fabrication, genome sequencing, materials characterization, mechanical fabrication, energy storage, semiconductor thermoelectrics, and the Intelligent Systems Center.

**What was said:** The closing argument is that present-day frontier systems have more scientific capability than organizations are able to use. Addressing that capability overhang requires bringing access, execution, and verification to every domain. In Q&A, Wolmetz distinguished UARC research by its early attention to mission intent, downstream applications, bespoke operating constraints, sensitive data, and operational needs across the Department of War and intelligence community.

**Key quote/result/takeaway:** “There is so much more that we can do ... that we’re unable to do” until access, execution, and verification improve.

**Entities:** APL; UARC; Department of War; intelligence community; mission intent.

**Claims:** Mission intent and downstream operating constraints shape research choices early at APL; the capability overhang can be attacked through the three-part framework.

**Evidence/results:** Facility landscape and closing/Q&A remarks.

**Source confidence:** High - directly stated as the speaker’s framing and organizational perspective.

## High-level Takeaways

- The most useful lens for AI-for-science maturity is not a single capability score, but the uneven combination of access, execution, and verification.
- Tacit laboratory knowledge is a central access gap: systems can produce plausible protocols that remain non-executable without human expertise.
- Closed-loop robotics is already accelerating parts of materials and chemical discovery, but dexterous final tests and difficult characterization are still human-dependent.
- Scalable verification is emerging as the decisive constraint: AI can assist experts, but it also raises the volume of claims that must be checked.
- Automated replication creates a practical bridge from reproducibility work to new, agent-driven research questions.

## Processing Notes

- Slide assets are rendered from the supplied 15-page PDF at 120 dpi and retain the source slide order.
- The title, framework, and all substantive examples are represented; the final APL end-card is not given a separate analytical section.
- The talk included no timestamps, so alignment is topical and follows slide order.

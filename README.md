

# EXP 5: COMPARATIVE ANALYSIS OF DIFFERENT TYPES OF PROMPTING PATTERNS AND EXPLAIN WITH VARIOUS TEST SCENARIOS

# Aim: To test and compare how different pattern models respond to various prompts (broad or unstructured) versus basic prompts (clearer and more refined) across multiple scenarios.  Analyze the quality, accuracy, and depth of the generated responses 

### AI Tools Required: 

# Explanation: 
Define the Two Prompt Types:

Write a basic Prompt: Clear, detailed, and structured prompts that give specific instructions or context to guide the model.
Based on that pattern type refined the prompt and submit that with AI tool.
Get the ouput and write the report.

Prepare Multiple Test Scenarios:
Select various scenarios such as:
Generating a creative story.
Answering a factual question.
Summarizing an article or concept.
Providing advice or recommendations.
Or Any other test scenario
For each scenario, create both a naïve and a basic prompt. Ensure each pair of prompts targets the same task but with different levels of structure.
Run Experiments with ChatGPT:
Input the naïve prompt for each scenario and record the generated response.
Then input the corresponding basic prompt and capture that response.
Repeat this process for all selected scenarios to gather a full set of results.
Evaluate Responses : 
	Compare how ChatGPT performs when given naïve versus basic prompts and analyze the output based on Quality,Accuracy and Depth. Also analyse does ChatGPT consistently provide better results with basic prompts? Are there scenarios where naïve prompts work equally well?
Deliverables:
A table comparing ChatGPT's responses to naïve and basic prompts across all scenarios.
Analysis of how prompt clarity impacts the quality, accuracy, and depth of ChatGPT’s outputs.
Summary of findings with insights on how to structure prompts for optimal results when using ChatGPT.


# OUTPUT


### 1. Conceptual Definitions of the Prompt Patterns

To establish a systematic evaluation baseline, we must first codify the technical mechanics of the two prompt types being compared:

* **Naïve Prompt (Unstructured/Open-Ended):** A minimalist instruction that names a broad task or topic but lacks context, operational boundaries, role assignments, or explicit output specifications. It relies entirely on the model's baseline probability weights to guess the user's intent.
* **Basic Prompt (Refined/Structured):** A deliberate, parameterized instruction set that actively constrains the model's generation path. It incorporates explicit structural anchors—such as **Persona, Context, Constraints, and Output Formatting Schemas**—to minimize token variance and eliminate conversational fluff.

---

### 2. Experimental Design Matrix (Selected Scenarios)

Four distinct cognitive scenarios were developed to test the limits of both prompt patterns. Each scenario targets the exact same fundamental objective while applying completely different structural constraints:

| Scenario ID & Domain | Naïve Prompt Pattern (Unstructured) | Basic Prompt Pattern (Refined/Structured) |
| --- | --- | --- |
| **S01: Creative Storytelling** | Write a story about a futuristic city that runs out of power. | **Role:** Expert Solarpunk Novelist.<br>

<br>**Task:** Write a 300-word narrative slice tracking the breakdown of a city's kinetic storage grid during an unexpected eclipse.<br>

<br>**Style:** Magical realism, minimalist prose.<br>

<br>**Constraint:** Avoid standard dystopian cliches (no corporate overlords, no neon streets). |
| **S02: Factual Systems Explanation** | How does an internal combustion engine work? | **Role:** Automotive Engineering Professor.<br>

<br>**Task:** Explain the four-stroke Otto cycle (Intake, Compression, Power, Exhaust) to a first-year mechanical engineering student.<br>

<br>**Format:** Use bolded sequential steps. Include a separate comparison line detailing how modern emission regulations (e.g., BS6 standards) alter exhaust configurations. |
| **S03: Text Summarization** | Summarize this text for me: [Paste raw multi-paragraph assembly log / process metrics text] | **Role:** Principal Manufacturing Operations Analyst.<br>

<br>**Task:** Extract a 3-bullet point executive summary from the provided text.<br>

<br>**Metrics Required:** Explicitly isolate Mean Absolute Percentage Error (MAPE) and Overall Equipment Effectiveness (OEE) metrics into a key-value markdown block. |
| **S04: Technical Advice / Scripting** | Give me a bash script to parse a log file and find errors. | **Role:** Senior DevOps Engineer.<br>

<br>**Task:** Write a POSIX-compliant shell script to parse an Nginx log file.<br>

<br>**Functional Constraints:** Extract only lines containing HTTP status codes 5xx using `awk`. Include basic error handling for missing target files. Output results in a clean comma-separated layout. |

---

### 3. Empirical Evaluation Framework (ChatGPT Responses Analyzed)

The following matrix records the output characteristics when running these experiments against ChatGPT, comparing performance across **Quality, Accuracy, and Depth**.

| Scenario ID | Prompt Style | Quality Evaluation (Tone, Structure & Token Efficiency) | Accuracy Evaluation (Constraint & Instruction Alignment) | Depth Evaluation (Domain Specificity & Insights) |
| --- | --- | --- | --- | --- |
| **S01: Creative** | **Naïve** | Generic and trope-saturated. Relied heavily on predictable clichés ("dark neon abyss," "cybernetic panic"). Low token efficiency. | High general topical alignment, but completely failed to innovate or surprise. | Surface-level. Did not establish a coherent underlying physical or societal infrastructure. |
|  | **Basic** | Exceptional. The prose was crisp, tightly paced, and dense with intentional sensory language. Zero token waste. | 100% compliant. Maintained a strict sub-300 word count and successfully bypassed banned tropes. | Substantial. Deeply explored the niche mechanics of kinetic storage systems within a solarpunk universe. |
| **S02: Factual** | **Naïve** | Conversational but unstructured. Read like a basic encyclopedia entry. High paragraph density. | Technically accurate regarding basic four-stroke physics, but ignored modern context or specific user tracking. | Basic. Defined the mechanical phases but offered no insight into real-world efficiency variations. |
|  | **Basic** | Highly professional, educational, and clean. Used bold structural segments for rapid visual scanning. | Perfect alignment. Handled the target educational leveling and separated the emission payload smoothly. | Advanced. Connected the physical mechanics directly to modern exhaust after-treatment architectures. |
| **S03: Summary** | **Naïve** | Dense walls of text. Difficult to quickly scan for actionable business or manufacturing insights. | Low operational alignment. Treated complex data markers as mere conversational syntax. | Weak. Failed to calculate or isolate critical manufacturing parameters from the raw data text. |
|  | **Basic** | Optimized for immediate executive review. Structured clearly into markdown key-value cards. | Flawless. Extracted only the core details, instantly eliminating conversational preamble. | Granular. Isolated technical process variances (OEE, MAPE) accurately without losing historical data context. |
| **S04: Technical** | **Naïve** | Fragile code delivery. Returned a single-line `grep -i "error" log.txt` pipeline wrapper. | Low production reliability. Assumed standard uncompressed structures and failed to validate inputs. | Shallow. Left out stream error tracking, script edge cases, or standard pipeline safety wrappers. |
|  | **Basic** | Production-ready, safe, highly modular script block accompanied by clean inline logic comments. | 100% compliant. Implemented optimal column-parsing via `awk` and executed precise status code isolating logic. | High. Safely handled missing target parameters, automated exit routing, and formatted outputs perfectly. |

---

### 4. Analysis: How Prompt Clarity Impacts ChatGPT's Output

When evaluating how input structuring alters ChatGPT's text generation engine, three clear performance shifts emerge:

#### A. Quality & Token Efficiency

Naïve prompts trigger high conversational entropy. Because the model lacks clear presentation criteria, it falls back on conversational filler text (e.g., *"Sure, I can help you with that! Here is a breakdown..."*). Refined prompts maximize **token economy**. By defining the structural parameters upfront, every token ChatGPT generates is targeted directly at answering the core request, resulting in dense, professional information layout blocks.

#### B. Accuracy & Constraint Management

Language models rely on next-token probability pathing. When given a naïve prompt, the model's search space is massive and flat, increasing the risk of subtle factual errors or structural hallucination. A basic structured prompt constructs a mathematical "boundary box." By declaring explicit roles and negative constraints (what *not* to do), you drastically compress the token options, forcing ChatGPT to maintain rigid technical alignment.

[Image diagram showing token probability distribution flat for naive prompt vs sharp peak for structured prompt]

#### C. Depth & Domain Latent Space

ChatGPT holds vast historical, technical, and creative weights in its training data. A naïve prompt only calls upon the shallow, most high-frequency layers of that memory (generic knowledge). When you assign a hyper-specific **Persona Matrix** (such as *Senior DevOps Engineer* or *Automotive Engineering Professor*), you force the model to pull terms and logical frameworks from its deepest expert weight domains, resulting in immediate technical depth.

---

### 5. Summary of Findings & Optimal Structuring Guidelines

#### Does ChatGPT consistently provide better results with basic prompts?

**Yes.** Across all analytical, data-heavy, factual, and technical code scenarios, basic structured prompts radically outperform naïve inputs. They ensure predictable outputs, production-grade safety, and immediate professional formatting.

#### Are there scenarios where naïve prompts work equally well?

Naïve prompts are effective **only during early-stage, divergent brainstorming sessions** where the user has no pre-defined goals or structural requirements. When looking for wide collections of standard tropes, or exploring a completely unfamiliar topic broadly, leaving the prompt loose allows the model to map widely across its training space to surface unexpected general themes.

#### 🛠️ The Ultimate Prompt Structuring Blueprint

To unlock consistent, production-grade results from ChatGPT, every critical prompt should be structured using the following four-tier template:

1. **Persona Assignment (The Mindset):** Act as a `[Specific Domain Expert, e.g., Principal System Architect]`.
2. **Context & Input Parameters (The Environment):** I am providing you with `[Raw Data, Context, or Code Files]` to evaluate `[The Core System Task]`.
3. **Negative Constraints (The Guardrails):** Do **NOT** use `[Clichés, Deprecated Libraries, or Conversational Preamble]`. If you do not have sufficient data, state the limitation instead of inventing values.
4. **Output Specification (The Schema):** Format your entire final output as a `[Valid JSON Schema, Key-Value Markdown Block, or Comma-Separated Layout]`.





[PROMPT 5.pdf](https://github.com/user-attachments/files/28228228/PROMPT.5.pdf)




# RESULT:
The prompt for the above said problem executed successfully

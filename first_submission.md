# Project Proposal: How AI Is Reshaping the Way Students Learn

## Group and working title

**Working title:** Learning with a Co-Pilot: How AI Is Reshaping the Way Students Learn

**Group members:**

- Nicoló Calandra
- Marco Fasoli
- Giulio Venturini

## 1. Main question and supporting questions

**Main question:** Does generative AI help students learn, or does it only help them finish the task in front of them?

**Supporting questions:**

1. How widespread is AI use among students today, and what do they use it for?
2. What happens to performance while students have AI, and what happens once it is taken away?
3. Does the design of the tool matter, comparing a plain chatbot with a tutor that gives hints instead of answers?
4. Do students notice the effect on their own learning, or do they overestimate what they have learned?
5. How are students and institutions responding, in terms of perceived benefits, worries about skill erosion, and changes to assessment?

## 2. Intended audience

The primary audience is students, teachers and parents: people who make daily decisions about AI and study without a technical background. Charts must therefore be readable without statistical training, with one message each and plain-language annotations.

The secondary audience is school and university decision-makers who set AI policies and choose which tools to provide.

## 3. Datasets

### Bastani et al., "Generative AI without guardrails can harm learning", PNAS 2025 (main, measured)

**What it is:** Field experiment with nearly 1,000 high school maths students in Turkey, split into three arms: a ChatGPT-style chatbot (GPT Base), a hint-only tutor (GPT Tutor), and a control group with no AI. Anonymised student-level data and code are public on GitHub.

**What it contributes:** The causal core of the story: scores during AI-assisted practice against scores on a later exam without AI, per arm. Against the control group, GPT Base scored 48% higher in practice and 17% lower on the exam; GPT Tutor scored 127% higher in practice and about level on the exam. The repository also holds student, class and grader covariates and the time-stamped student conversations with the tutors. (summary)

### Kestin et al., "AI tutoring outperforms in-class active learning", Scientific Reports 2025 (measured)

**What it is:** Randomised crossover trial with 194 Harvard undergraduates in introductory physics: a purpose-built AI tutor against an instructor-led active learning class. The public Stata file has 316 student-session rows and 9 variables: condition, pre-test and post-test score, engagement, enjoyment, effort and perceived difficulty ratings, and time on task.

**What it contributes:** The counterpoint: a tutor designed around good teaching practice improves learning. In the data, the median post-test score is 4.5 with the AI tutor and 3.5 in class, with a median of 49 minutes on task against a fixed 60-minute class. Student-level rows allow distributions and pre-to-post gains per student.

### Pew Research Center, "How Teens Use and View AI", 2026 (survey)

**What it is:** Survey of 1,458 US teens aged 13 to 17 and their parents, fieldwork 25 September to 9 October 2025. Topline results and methodology are published.

**What it contributes:** Prevalence among teenagers: 64% have used AI chatbots and 54% use them for schoolwork, with a breakdown of tasks such as researching a topic (48%) and solving maths problems (43%).

### HEPI Student Generative AI Survey 2026 (survey)

**What it is:** Survey of 1,054 full-time UK undergraduates, fieldwork December 2025, with weighted data tables downloadable as XLSX.

**What it contributes:** Prevalence and attitudes among university students: 95% use AI in some way and 94% use it for assessed work. It adds purposes of use, perceived benefits, concerns such as skill erosion, institutional support, and a 2024 to 2026 trend (AI text pasted into assessed work went from 3% to 8% to 12%).

We limit the project to these four datasets. The two experiments carry every claim about learning effects, because they measure outcomes. The two surveys are self-reported and are used only for prevalence and attitudes. The sources cover different populations (Turkish high schoolers, US undergraduates, US teens, UK undergraduates), so we present them side by side without merging them.

## 4. Visualization ideas and data concerns

**Storyline and plots:**

1. "Everyone uses it." A single large number or waffle chart for the share of students using AI, for teens (Pew) and undergraduates (HEPI) in separate panels, followed by a sorted horizontal bar chart of what they use it for.
2. "It is growing." A small line chart of AI-generated text in assessed work, 2024 to 2026 (HEPI).
3. "With AI, scores jump." A bar chart of practice-session performance for the three arms (PNAS).
4. "Without AI, the gain disappears." A slope chart linking each arm's practice result to its exam result, so the GPT Base line visibly drops below the control group. This is the central chart of the story.
5. "Students do not see it." A dumbbell chart of perceived against actual learning per arm (PNAS).
6. "Design matters." A side-by-side of GPT Base and GPT Tutor, with an annotated example of an answer-giving reply next to a hint-giving one, and the share of student messages that simply ask for the answer in each arm (PNAS conversations).
7. "A well-designed tutor can beat the classroom." Paired pre-test and post-test distributions for the AI tutor and the active learning class, plus a small scatter of time on task against learning gain (Harvard).
8. "What students worry about." Diverging stacked bars for agree/disagree items on benefits, skills and institutional support (HEPI).

**Concerns about data availability:**

- Student-level data is available for both experiments. The PNAS data is on GitHub and the Harvard data is a public Stata file, so plots 3 to 7 can show distributions and breakdowns, not only published averages. We still need to explore the PNAS repository and confirm its variable definitions.
- The Harvard file is small. It has 9 variables and no demographics or prior-achievement covariates, and not every student has a row for both conditions (316 rows for 194 students). Breakdowns are limited to condition, scores, ratings and time.
- The experiments are not directly comparable. PNAS compares AI against no AI and then tests without AI; Harvard compares an AI tutor against a strong class with a short-term post-test. They will appear in separate panels with their own scales.
- Pew offers published tables, not respondent-level data. We have not found a public microdata file, so Pew charts will use the topline percentages.
- HEPI comparability. Earlier survey waves are needed for trends, and question wording may have changed between years.
- Self-report against measurement. The surveys record what students say, the experiments record what they do. Charts will label which is which.

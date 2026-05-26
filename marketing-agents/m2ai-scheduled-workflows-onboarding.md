# M2AI Marketing Agents — Scheduled Workflows Setup Prompt

**How to use this:** Copy the prompt below and paste it as your first message in a new CoWork session. The m2ai-marketing-agents plugin must already be installed. Claude will design 4 marketing automation pipelines and create them as live scheduled tasks — you just need to click "Run now" on each one to approve the tools they need for future autonomous runs.

---

## THE PROMPT

```
I have the m2ai-marketing-agents plugin installed in CoWork. It includes skills for three agents: Creator (content), RepMan (reputation management), and Scout (competitive intelligence).

I want you to design and schedule 4 automated marketing workflows that chain these skills together into pipelines. Here is exactly what I need you to do:

**Your task has two phases. Complete Phase 1 fully before starting Phase 2.**

---

PHASE 1 — DESIGN THE 4 WORKFLOWS

Read the skill files for the m2ai-marketing-agents plugin to understand what each skill does. Do NOT invoke the skills interactively and do NOT try to build or recreate them — just read them to understand their capabilities. The skills are located in the plugin's skills/ directory.

Design 4 workflows using these specific skill combinations:

WORKFLOW 1 — Monday Morning Reputation Triage (runs every Monday 8:00 AM)
Skills to chain in order:
1. repman-review-monitor — scan all review platforms, flag urgent/standard/low priority reviews
2. repman-review-respond — draft a response for each new review found in step 1
3. repman-gbp-manage — check Google Business Profile Q&A for unanswered questions and draft responses
Output: A consolidated Monday morning brief with all drafts staged for human approval.

WORKFLOW 2 — Weekly Competitive Intelligence Report (runs every Friday 5:00 PM)
Skills to chain in order:
1. scout-market-snapshot — scan all tracked competitors, save snapshot file for week-over-week trend tracking
2. scout-pricing-intel — triggered conditionally only if step 1 finds a competitor running a promotion or undercutting on price; research pricing signals for that specific service
Output: A dated snapshot report with threats, opportunities, and ranked recommended actions.

WORKFLOW 3 — Monthly Content Engine (runs on the 1st of every month at 8:00 AM)
Skills to chain in order:
1. creator-content-calendar — build a full 4-week social calendar using the 40/25/20/15 content mix
2. creator-blog-seo — write the month's primary SEO blog post targeting a local keyword
3. creator-repurpose — repurpose the blog post from step 2 into social posts, email snippet, and Instagram carousel
Output: A complete monthly content package — calendar + blog post + derivative content pack.

WORKFLOW 4 — Friday Post-Job Reputation & Content Loop (runs every Friday 12:00 PM)
Skills to chain in order:
1. repman-review-request — generate personalised SMS and email review request messages for jobs completed this week
2. creator-case-study — write a 400–700 word case study from the most significant completed job
3. creator-repurpose — repurpose the case study into social proof posts, quote card brief, and GBP post draft
4. creator-social-post — produce final polished posts for Facebook, Instagram, and LinkedIn
Output: A complete post-job content packet — review ask messages + case study + all social posts, copy-paste ready.

Present all 4 workflow designs clearly before moving to Phase 2.

---

PHASE 2 — CREATE THE SCHEDULED TASKS

Using the schedule skill and the create_scheduled_task tool, create all 4 workflows as live scheduled tasks with these cron expressions (local time):
- Workflow 1: 0 8 * * 1  (every Monday 8:00 AM)
- Workflow 2: 0 17 * * 5  (every Friday 5:00 PM)
- Workflow 3: 0 8 1 * *  (1st of every month 8:00 AM)
- Workflow 4: 0 12 * * 5  (every Friday 12:00 PM)

Each scheduled task prompt must be fully self-contained — it will run in a future session with no memory of this conversation, so every task prompt must include: the objective, the skills to use in order, what each skill should do, and the expected output format.

Set notifyOnCompletion: true on all four tasks.

Create all 4 tasks and confirm when they are live with their next scheduled run times.

---

IMPORTANT NOTES FOR CLAUDE:
- Do not invoke any m2ai skills interactively during this setup session. This session is for design and scheduling only.
- Do not attempt to recreate, rewrite, or rebuild any skills. They are already installed and working.
- The goal is 4 live scheduled tasks that will run autonomously. This session ends when all 4 are confirmed created.
- After creating the tasks, remind me that I need to click "Run now" on each task once to pre-approve the tools they use, so future automated runs are not interrupted by permission prompts.
```

---

## WHAT HAPPENS AFTER THE PROMPT

Once Claude confirms all 4 tasks are created, go to the **Scheduled** section in the CoWork sidebar. You will see:

| Task name | When it runs |
|-----------|-------------|
| `monday-reputation-triage` | Every Monday 8:00 AM |
| `friday-competitive-intel` | Every Friday 5:00 PM |
| `monthly-content-engine` | 1st of every month 8:00 AM |
| `friday-post-job-content-loop` | Every Friday 12:00 PM |

**Click "Run now" on each task once.** This walks through any tool permission prompts. Those approvals are stored on the task and will not interrupt future automated runs. Skip this step and the scheduler may pause mid-run waiting for you to approve tools.

After that, the workflows run unattended on schedule and notify you when they complete.

---

## WHY THE PROMPT IS WRITTEN THIS WAY

**The two-phase structure** prevents Claude from jumping to scheduling before it has fully reasoned through the workflow designs. Asking for both at once risks getting shallow task prompts that don't correctly chain the skills.

**"Read, do not invoke"** is explicit because handing Claude skill files without this instruction risks it treating a workflow skill as a live interactive session (invoking Step 1, asking the user questions) rather than reading it as a capability specification. This is the most common source of wasted effort in this setup.

**"Do not recreate or rebuild"** prevents Claude from treating the plugin as a build spec and trying to reconstruct the skills from scratch — a confident mistake that produces the right-looking output in the wrong place.

**Self-contained task prompts** are required because scheduled tasks run in isolated sessions with no memory of this conversation. A task prompt that says "do what we discussed" will fail silently on first run.

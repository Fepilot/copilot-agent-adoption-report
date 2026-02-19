# The Claude Prompt - Copy and Paste

> Copy everything below the horizontal rule, paste it into Claude (browser, CLI, or VS Code extension), update the two file paths at the bottom, and run.

---

I have a Power BI report on Microsoft Copilot & Agent adoption exported as a PDF.
I also have an HTML template.

Please:
1. Read both files in full
2. Extract every number, name, team, and metric from the PDF
3. Replace every [placeholder] and - in the HTML with the real data from the PDF

Use this section-to-page mapping:

EXECUTIVE SUMMARY:
- "Total Agent Users" -> Agent Active Users (PDF page 3)
- "Total Agent Sessions" -> sum of all agent sessions
- "Active Agents" -> active agents count (PDF page 6 Health Check)
- "Organizations" -> unique teams/departments with agent users
- "Avg Sessions per User" -> weekly sessions per user (PDF page 3)
- "Total Agent Prompts" -> total agent prompts/actions
- "Total Agents Created" -> total agents created (PDF page 6)
- Key Insight alert -> write 2-3 sentences summarizing adoption health
- Adoption Highlights -> top teams and notable patterns from data
- Attention Areas -> utilization gaps and low-engagement signals

AI MATURITY STAGE:
- Determine stage (1-5) using the 5 Stages of AI Maturity framework:
  Stage 1=Assisted Automation, Stage 2=Partial Autonomy, Stage 3=Conditional Autonomy,
  Stage 4=High Autonomy, Stage 5=Full Autonomous AI
- Set progress bar widths (style="width: X%") to realistic values based on the data
- Write the path to next stage as concrete action items

AGENT ADOPTION OVERVIEW:
- 3 cards -> agent user count, sessions/user, utilization rate (active/total agents %)
- Warning alert -> use actual numbers for total created vs active
- Top Performing Agents table -> top 5 agents by sessions from pages 3 and 6
- Agent Insights -> 3 insight paragraphs based on agent performance patterns

TEAMS LEADING AGENT ADOPTION:
- Table -> top 7 teams from the agent leaderboard (PDF pages 4-5): users, interactions,
  prompts, engagement badge (High/Medium/Power Users based on per-user intensity)
- Insight cards -> analyze leading teams and power user teams with real numbers

POWER USERS:
- Table -> top 8 individual users from agent user leaderboard (PDF page 5):
  name, team, role, interactions, prompts
- Power User Patterns -> identify patterns across roles and departments
- Champion Program -> tailor 4 suggested actions to the actual users identified

CHAT USAGE:
- Update insight card using unlicensed chat data (PDF pages 9-11)
  and M365 Copilot data (PDF pages 12-14)
- Mention top surfaces, MoM growth, and any standout departments

GROWTH OPPORTUNITIES:
- 5 recommendation items derived from the data:
  HIGH: agent utilization gap (active vs created), champion program
  MEDIUM: cross-team knowledge sharing, low-engagement team enablement
  LOW: first-party agent awareness
- Use real numbers in all impact statements

TAILORED RECOMMENDATIONS:
- 4 cards: Leadership, Team Leads, Agent Creators, Training & Enablement
- Tailor every bullet to the specific teams, users, and patterns found in this data

NEXT STEPS (30-60-90 day roadmap):
- 30 days: most urgent actions based on biggest gaps in the data
- 60 days: medium-term milestones with measurable targets
- 90 days: growth goals using real baseline numbers (e.g., "grow from X to Y users")
- Closing alert: write a motivational summary referencing the actual maturity stage
  and trajectory shown in the data

FOOTER:
- Data source: use the filename visible in the PDF (wpp22.pbix or similar)
- Date: use the most recent date visible in the PDF

Rules:
- Keep ALL existing CSS, JavaScript, IDs, classes, and navigation 100% intact
- Use exact numbers and names from the PDF wherever available
- For inferred values (like maturity stage), reason from the data explicitly
- Match the professional, actionable tone of the original
- Output the complete, fully populated HTML file

UPDATE THESE TWO PATHS BEFORE RUNNING:

output the complete, fully populated HTML file html file: "C:\path\to\your\copilot-adoption-template.html"
pbi pdf: "C:\path\to\your\power-bi-export.pdf"
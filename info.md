# ContextCon 05 · BITS Pilani | Builder brief

**Sunday, 22 November 2026 · J. C. Chaudhry NAB Auditorium · All times IST.** Use this brief to screen ideas before coding. It records the organisers’ rules and published API guidance; it does not confirm team registration, credit redemption or account access.

## Theme: Services, Replaced

Pick a job a customer pays a person or firm to do. Given a request the team has not seen before, the software should deliver the finished work—not just advise the customer how to do it. Be ready to name the buyer, the deliverable, the price in rupees and the cost of one completed job.

**AI-native infrastructure is one route, not a required stack.** The handbook offers an evidence ledger and a human sign-off gate as infrastructure examples. Any listed track or an original idea is eligible. A single agent, several agents, a CLI or an MCP server can qualify. Crustdata is optional; the judging rubric is the same. (Handbook pp. 2–6, 19–22, 38.)

## Build window and team rules

| Milestone | What the team needs to do |
| --- | --- |
| Official build start | The handbook distinguishes the **9:15 AM kickoff** from the **10:15 AM coding start**. The [public programme](https://contextcon-bitspilani.com/) lists **10:45 AM** for building. Confirm the authorised coding start in the room or builders’ channel before the first commit. |
| 2:30 PM | Form opens. Have one teammate submit a checkpoint version; the latest submission before freeze counts. |
| **6:00 PM** | **Code freeze and submission deadline.** No extension. Verify the links before the cutoff. |
| 7:30 / 7:45 / 8:40 PM | Ten finalists announced / finals begin / winners announced. Each finalist gets two minutes to demo and one minute for questions. |

- **Who may build:** One to four registered builders; engineering students in year three or later. One team per person. Only registered teammates may prepare or operate the entry. AI coding tools and open-source libraries are allowed; credit dependencies and respect their licences.
- **Start clean:** Planning and sketching are allowed; bringing prewritten project code or reusing a prior competition build is not. Use the organiser-assigned repository, make it public as required, and commit throughout the official window. Declare earlier code, prompts or designs on the form; disclosure does not make prohibited code eligible. This planning folder is not proof of an assigned competition repo.
- **Demo honestly:** No canned answers, precomputed results passed off as live, hidden human operators, altered commit histories or falsified cost logs. No sharing work across teams, seeking hidden test requests or interfering with other teams. After freeze, make no edits except a live fix expressly allowed under the finals rules.
- **No real-world outreach:** The participant rulebook prohibits contacting real people. Use team role-play, sandbox recipients and payment-provider test mode. A person can approve or reject a proposed action, not secretly do the job. Approval does not override the no-contact rule.

Sources: Participant Rulebook pp. 1–2; Builder Handbook pp. 4–11, 26.

## Crustdata usage: published limits vs. this account

| Item | Published guidance | What to do |
| --- | --- | --- |
| Event credits | The handbook offers **15,000 credits per eligible builder** via their own `@pilani.bits-pilani.ac.in` account (pp. 12–17). Event dashboard access and API credit redemption are separate. | Do not budget against the grant until it appears in the account. Never put keys, access codes or personal account details in the public repo or video. |
| Balance and access | The [API pricing guide](https://docs.crustdata.com/general/pricing) lists free account checks: `GET /account/credits` for balance and `GET /account/endpoints` for enabled endpoints, account prices and effective limits. | **Not verified for this team:** signed-in status, redemption, remaining credits, enabled endpoints and actual limits. Check the [Crustdata app](https://app.crustdata.com/home) before choosing an endpoint the demo depends on. |
| Throughput | Handbook defaults (pp. 22–23), in requests/minute per key: **30** for person/company/job search and company identify; **15** for person/company enrich; **10** for web search/fetch and Watcher. Actual [rate limits](https://docs.crustdata.com/general/rate-limits) depend on the plan and may also cap total traffic. | Share one budget across concurrent agents. On HTTP 429, respect the server’s wait interval; stop at the run’s time or credit ceiling. |
| Cost per job | Standard basic person/company search is **0.03 credits per result**, not per query. Premium fields and enrichment can add cost. | Limit results, enrich selectively, and record actual `X-Credits-Used` plus model/tool costs. Keep credit units separate from rupee costs; document conversion assumptions. |

**Public demo ≠ permission to publish data.** Crustdata’s [Data Export Terms](https://app.crustdata.com/terms/data-export) restrict external sharing of API/dashboard data and export links, and offering the data as a directory or enrichment service. Keep raw records out of public artifacts. Show the workflow without exposing restricted records; use labelled synthetic records for tests, never as purported live evidence. Ask the organisers what may be displayed if a demo needs to show returned data.

## How judging translates into a build

| Criterion | Points | What to show on an unseen request |
| --- | ---: | --- |
| End-to-end execution | 25 | The customer’s input and the finished deliverable, including any human approval. |
| Facts and verification | 20 | A decision that actually uses live data, dated sources, and what could not be verified. |
| Robustness and edge cases | 20 | One hard case and a safe failure: for example, resume after a timeout without charging or acting twice. |
| Customer value and idea | 20 | Who buys this service today, what they would pay, and what each run costs. |
| Demo and understanding | 15 | A working run, why this approach was chosen, what was tested and where it breaks. |

Ties go first to end-to-end execution, then facts and verification. The handbook also asks teams to bound time and spending, record the evidence and cost of each run, and require approval before irreversible actions. (Handbook pp. 9–11, 26–28.)

## Submission checklist

- [ ] **Public assigned GitHub repo:** source, qualifying commit history, and a README covering setup, stack, alternatives tried, sources, tests, human approvals, costs and known limits.
- [ ] **Architecture diagram:** include it or its link in the repo. Confirm judges can open the diagram without requesting access.
- [ ] **Two-minute working demo:** show a new request through delivery. Put the direct playable Loom, unlisted YouTube or shared Drive video link in the repo and form—not a folder. Test every link while signed out.
- [ ] **One teammate submits:** include team name, one-line description, track or original idea, what works, human decisions, tools, prework disclosure, limitations and next steps. Supply requested registration details in the private form, not the public README. Check the [event dashboard](https://crustdata.com/contextcon/bits-pilani-2026/dashboard#home) or the builders’ channel for the form. (Handbook pp. 7–10; Participant Rulebook pp. 1–2.)

**Source key:** “Handbook” = `1 · Builder Handbook · ContextCon 05 BITS Pilani.pdf`; “Participant Rulebook” = `DOC-20261121-WA0020_261121_231342.PDF`. Dashboard-only information was not available for verification. No credits were redeemed or spent during this review.

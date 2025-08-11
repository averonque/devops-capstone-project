---
name: User story
about: Template for user stories in the Accounts microservice
title: ""
labels: enhancement
assignees: ""
---

**As a** [role]  
**I need** [function]  
**So that** [benefit]  

### Details and Assumptions
* [document what you know]

### Acceptance Criteria
```gherkin
Given [some context]
When [certain action is taken]
Then [the outcome of action is observed]



- (Tip) You can also add `.github/ISSUE_TEMPLATE/config.yml` later to control the chooser. :contentReference[oaicite:7]{index=7}

✅ **Evidence**: open the file in GitHub and screenshot it → **planning-storytemplate-done.jpg/png**.

---

# Exercise 4 — Assemble your Product Backlog (7 stories)

Create **7 issues** using the **User story** template (Issues → **New issue** → choose the template), titles + one-liners below. Then add each issue to your Project (in the issue’s right sidebar, “Projects” → your project). :contentReference[oaicite:8]{index=8}

1) **Set up the development environment**  
   As a developer, I need a ready Python/Flask FastAPI/Django env so that I can build the accounts service.  
   **AC (gherkin)**: Given a clean machine, When I run setup, Then I can run tests and the service locally.

2) **Read an account from the service**  
   As a client app, I need to fetch an account by ID so that I can display customer info.  
   **AC**: Given an existing account, When I GET `/accounts/{id}`, Then I receive 200 with name/address.

3) **Update an account in the service**  
   As a client app, I need to update name/address so that records stay current.  
   **AC**: Given an existing account, When I PATCH/PUT valid fields, Then I receive 200 and updated data.

4) **Delete an account from the service**  
   As an admin, I need to delete an account so that obsolete records are removed.  
   **AC**: Given an existing account, When I DELETE `/accounts/{id}`, Then I receive 204 and it’s gone.

5) **List all accounts in the service**  
   As a client app, I need to list accounts (paged) so that I can browse.  
   **AC**: Given many accounts, When I GET `/accounts?limit/offset`, Then I receive 200 with a paged list.

6) **Containerize your microservice using Docker**  
   **AC**: Given the app, When I build `Dockerfile`, Then image builds and runs healthcheck OK.

7) **Deploy your Docker image to Kubernetes**  
   **AC**: Given an image, When I apply K8s manifests, Then service is reachable (ClusterIP/Ingress) and healthy.

- After creation, confirm all 7 appear in **New issues** on your board (drag if needed). :contentReference[oaicite:9]{index=9}

✅ **Evidence**: screenshot the board showing all 7 in **New issues** → **planning-userstories-done.jpg/png**.

---

# Exercise 5 — Triage New Issues

1) Decide what to do **now** vs **later**:
- Move **Set up dev env**, **Read**, **Update**, **Delete**, **List** → **Product Backlog**.  
- Move **Containerize with Docker** and **Deploy to Kubernetes** → **Icebox** (later).  

Drag cards between columns; the card’s **Status** updates automatically to match the column. :contentReference[oaicite:10]{index=10}

✅ **Evidence**: screenshot → **planning-productbacklog-done.jpg/png**.

---

# Exercise 6 — Refine Your Product Backlog

1) Make each story “sprint-ready”  
- Open each issue and flesh out **Details and Assumptions** + **Acceptance Criteria** until “done” is crystal clear.

2) Create a **technical debt** label (yellow)  
- Repo → **Issues** → **Labels** → **New label** → name `technical debt`, pick a yellow color, **Create**. :contentReference[oaicite:11]{index=11}

3) Label your stories  
- Anything with **clear customer value** → keep `enhancement` (or similar).  
- Internal/non-visible necessary work (e.g., dev env) → add **technical debt**.

4) Rank by priority inside **Product Backlog**  
- Drag higher = higher priority.

5) If labels aren’t visible on the board  
- Board view → view menu (⋯) → **Fields** → show **Labels** (move it from Hidden to Visible). Save. :contentReference[oaicite:12]{index=12}

✅ **Evidence**: screenshot with labels showing → **planning-labels-done.jpg/png**.

---

# Exercise 7 — Build Sprint 1 from the Product Backlog

1) Add a **Sprint** (iteration) field and create 3 one-week sprints
- Switch to **Table** view temporarily (easier to add fields).  
- Rightmost header → **+ Add field** → **New field** → type `Sprint` → **Field type: Iteration** → set duration **1 week** → Save.  
- In **Project settings → Sprint**, make sure there are **three** iterations; rename them **Sprint 1**, **Sprint 2**, **Sprint 3** and set dates (one week each). :contentReference[oaicite:13]{index=13}

2) Add a **Story points** number field
- In Table view → **+ Add field** → **New field** → name `Story points` → **Number** → Save. :contentReference[oaicite:14]{index=14}

3) Open the **top story** in **Product Backlog**  
- Set **Story points** using 3, 5, 8, 13 (S, M, L, XL).  
- Set **Sprint** = **Sprint 1**.  
- Close the item and **drag it** from **Product Backlog** → **Sprint Backlog** (keep order). :contentReference[oaicite:15]{index=15}

4) Repeat for the next **four** highest-priority stories  
- All five should be in **Sprint Backlog**, ordered exactly as they were ranked in Product Backlog.

✅ **Evidence**: screenshot the board showing Sprint Backlog populated (and Sprints/points visible if you added them to visible fields) → **planning-kanban-done.jpg/png**.

---

## Tiny gotchas (save you some head-scratching)
- New Projects live at **user/org level**; you **link** them to a repo so they appear in the repo’s tab. :contentReference[oaicite:16]{index=16}  
- Board columns reflect whatever field you choose as the **Column field** (we used **Status**). Dragging cards between columns **changes the field value**. :contentReference[oaicite:17]{index=17}  
- **Iterations (Sprints)** are just a custom field—you control names and dates. Three iterations are created automatically the first time; edit as needed. :contentReference[oaicite:18]{index=18}

If you want, I can generate exact copy-paste text for each of the seven user stories (full details + AC) and suggested story-point sizes.

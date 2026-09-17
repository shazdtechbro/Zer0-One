# FDE Zero-to-Hired Roadmap — Table Edition
**Starts TODAY, Thu Sept 17, 2026 → ~Mar 17, 2027 · Mon–Fri grind only, weekends rest**

Every project is real and named (from [roadmap.sh's project lists](https://roadmap.sh/backend/project-ideas), [roadmap.sh DSA projects](https://roadmap.sh/projects), and [DataCamp's ML projects](https://www.datacamp.com/blog/machine-learning-projects-for-all-levels)), escalating beginner → intermediate → advanced. Each week opens with **what a successful week looks like** — the concrete bar you're aiming for — then a day-by-day table. Every Learn/LeetCode/Build item has its own checkbox (`- [ ]`). Backend third language: **Go**.

---

## Systems Design Resources (use throughout Month 4, reference anytime)
| Resource | Link | Use for |
| --- | --- | --- |
| roadmap.sh System Design roadmap | [roadmap.sh/system-design](https://roadmap.sh/system-design) | Full topic map — master checklist |
| The System Design Primer | [github.com/donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer) | Deep-dive reading + flashcards |
| ByteByteGo: Cache Systems | [youtube.com/watch?v=dGAgxozNWFE](https://www.youtube.com/watch?v=dGAgxozNWFE) | Caching |
| ByteByteGo: Load Balancing Algorithms | [youtube.com/watch?v=dBmxNsS3BGE](https://www.youtube.com/watch?v=dBmxNsS3BGE) | Load balancing |
| ByteByteGo: Message Queue | [youtube.com/watch?v=h1Lx-vQxILk](https://www.youtube.com/watch?v=h1Lx-vQxILk) | Message queues |
| Gaurav Sen System Design Playlist | [youtube.com/playlist?list=PLMCXHnjXnTnvo6alSjVkgxV-VH6EPyvoX](https://www.youtube.com/playlist?list=PLMCXHnjXnTnvo6alSjVkgxV-VH6EPyvoX) | CAP theorem, caching, queues |
| PostgreSQL Indexes docs | [postgresql.org/docs/current/indexes.html](https://www.postgresql.org/docs/current/indexes.html) | Data layer performance |
| Use The Index, Luke! | [use-the-index-luke.com](https://use-the-index-luke.com/) | Indexing deep dive |

---

## MONTH 1 — Python Fundamentals + DSA Foundation

### Week 1 — Project: Number Guessing Game ([roadmap.sh](https://roadmap.sh/projects/number-guessing-game), beginner CLI)
**✅ Successful week =** a working CLI game with 3 difficulty levels, scoring, a persisted leaderboard file, pushed to GitHub with a README; 5 LeetCode problems logged.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 9/17 (TODAY) | - [ ] Variables, types, operators — [Python Tutorial §3](https://docs.python.org/3/tutorial/introduction.html) | - [ ] [Two Sum](https://leetcode.com/problems/two-sum/) — first attempt, hints allowed | - [ ] Create `guess_game.py`<br>- [ ] `random.randint(1,100)` for the target number<br>- [ ] Basic `input()` loop asking for a guess |
| Fri 9/18 | - [ ] if/elif/else, boolean logic — [CS50P Wk1](https://cs50.harvard.edu/python/) | - [ ] [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/) — first attempt | - [ ] Add "too high"/"too low" feedback<br>- [ ] Add a win message + guess count on win |
| Mon 9/21 | - [ ] for/while loops — [CS50P Wk1](https://cs50.harvard.edu/python/) | - [ ] Re-solve [Two Sum](https://leetcode.com/problems/two-sum/), timed | - [ ] Add 3 difficulty levels: Easy (1-50, 10 attempts), Medium (1-100, 7 attempts), Hard (1-500, 5 attempts)<br>- [ ] Menu to pick difficulty at start |
| Tue 9/22 | - [ ] String formatting, input validation — [Python Tutorial §3](https://docs.python.org/3/tutorial/introduction.html) | - [ ] Re-solve [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/), timed | - [ ] Reject non-numeric/out-of-range input without crashing<br>- [ ] Add a score formula: `score = max_attempts - attempts_used` per difficulty |
| Wed 9/23 — SHIP DAY | — | - [ ] [Valid Anagram](https://leetcode.com/problems/valid-anagram/) | - [ ] Add a top-5 leaderboard (name + score) saved to `leaderboard.json`, loaded on startup<br>- [ ] Clean up all prompts, write README with how-to-run instructions<br>- [ ] Push to GitHub |

### Week 2 — Project: Task Tracker ([roadmap.sh](https://roadmap.sh/projects/task-tracker), beginner CLI)
**✅ Successful week =** a CLI matching the official spec exactly — `add`, `update`, `delete`, `mark-in-progress`, `mark-done`, `list` (with status filters) — all persisted to `tasks.json`, no external libraries.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 9/24 | - [ ] Functions, params, scope — [Python Tutorial §4](https://docs.python.org/3/tutorial/controlflow.html) | - [ ] [Group Anagrams](https://leetcode.com/problems/group-anagrams/) | - [ ] Parse CLI args with `sys.argv` (no libraries per spec)<br>- [ ] Stub out `add`, `list`, `update`, `delete` commands (print "not implemented") |
| Fri 9/25 | - [ ] Lists, dicts, sets — [Python Data Structures docs](https://docs.python.org/3/tutorial/datastructures.html) | - [ ] [Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/) | - [ ] Implement `add "description"` → creates task with auto-incrementing id, description, status=`todo`, createdAt, updatedAt<br>- [ ] Implement `list` → prints all tasks |
| Mon 9/28 | - [ ] Exceptions, try/except — [CS50P Wk3](https://cs50.harvard.edu/python/) | - [ ] [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/) | - [ ] Implement `update <id> "new description"`<br>- [ ] Implement `delete <id>`<br>- [ ] Handle missing/invalid id with a clean error message, not a crash |
| Tue 9/29 | - [ ] File I/O, JSON — [CS50P Wk6](https://cs50.harvard.edu/python/) | - [ ] [Valid Sudoku](https://leetcode.com/problems/valid-sudoku/) | - [ ] Persist all tasks to `tasks.json` in the current directory<br>- [ ] Load existing tasks on every command run (no in-memory-only state) |
| Wed 9/30 — SHIP DAY | — | - [ ] Re-solve [Group Anagrams](https://leetcode.com/problems/group-anagrams/) | - [ ] Implement `mark-in-progress <id>` and `mark-done <id>`<br>- [ ] Implement `list done`, `list todo`, `list in-progress` filters<br>- [ ] Write README, push to GitHub |

### Week 3 — Project: Expense Tracker ([roadmap.sh](https://roadmap.sh/projects/expense-tracker), beginner CLI)
**✅ Successful week =** `add`, `list`, `delete`, `summary`, `summary --month N` all working with categories and a budget-warning stretch feature, persisted to JSON.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 10/1 | - [ ] Classes, inheritance, encapsulation — [CS50P Wk9](https://cs50.harvard.edu/python/) | - [ ] [Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/) | - [ ] Design an `Expense` class: id, amount, description, category, date<br>- [ ] Stub CLI commands: `add`, `list`, `delete`, `summary` |
| Fri 10/2 | - [ ] Two Pointers pattern — [LeetCode Discuss: Master in Two Pointer](https://leetcode.com/discuss/study-guide/1905453/master-in-two-pointer) | - [ ] [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/) | - [ ] Implement `add --description "Lunch" --amount 20`<br>- [ ] Implement `list`, persisted to `expenses.json` |
| Mon 10/5 | - [ ] Two Pointers continued | - [ ] [Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/) | - [ ] Implement `summary` → total of all expenses<br>- [ ] Implement `summary --month 8` → total for that month |
| Tue 10/6 | - [ ] Big-O basics — [System Design Primer intro](https://github.com/donnemartin/system-design-primer) | - [ ] [3Sum](https://leetcode.com/problems/3sum/) | - [ ] Add a `--category` flag on `add` (Food, Transport, Utilities, Other)<br>- [ ] Implement `delete <id>` |
| Wed 10/7 — SHIP DAY | — | - [ ] Re-solve [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/) + [Container With Most Water](https://leetcode.com/problems/container-with-most-water/) | - [ ] **Stretch:** add `set-budget --month 8 --amount 200` + a warning printed on `add` if the month's total now exceeds budget<br>- [ ] Write README, push to GitHub |

### Week 4 — Project: GitHub User Activity ([roadmap.sh](https://roadmap.sh/projects/github-user-activity), beginner CLI)
**✅ Successful week =** a CLI that takes a GitHub username, fetches their public events, and prints a readable activity summary — plus your own "most active window" feature using sliding window.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 10/8 | - [ ] Sliding window (fixed size) — [LeetCode Discuss: Sliding Window Technique](https://leetcode.com/discuss/study-guide/1773891/sliding-window-technique-and-question-bank/) | - [ ] [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/) | - [ ] Call `https://api.github.com/users/<username>/events` with `urllib` or `requests`<br>- [ ] Print raw JSON response to confirm it works |
| Fri 10/9 | - [ ] Sliding window (variable size) | - [ ] [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/) | - [ ] Parse events into readable lines, e.g. `"Pushed 3 commits to user/repo"`<br>- [ ] Handle `PushEvent`, `IssuesEvent`, `WatchEvent`, `ForkEvent` types per spec |
| Mon 10/12 | - [ ] Sliding window practice | - [ ] [Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/) | - [ ] Group events by type and print counts (e.g. "14 pushes, 3 stars, 1 fork")<br>- [ ] Sort output by most recent first |
| Tue 10/13 | - [ ] Sliding window practice | - [ ] [Permutation in String](https://leetcode.com/problems/permutation-in-string/) | - [ ] **Stretch:** compute the busiest 7-day sliding window from event timestamps and print it ("Most active week: Sept 10–16, 22 events") |
| Wed 10/14 — SHIP DAY | — | - [ ] Re-solve 2 problems from this week, timed | - [ ] Handle invalid usernames and API rate limits with clean error messages<br>- [ ] Write README, push — **Month 1 done: 4 real projects shipped, 30+ LeetCode logged** |

---

## MONTH 2 — Backend: FastAPI, Django, Go (good backend engineer by end of month)

### Week 5 — Project: Todo List API ([roadmap.sh](https://roadmap.sh/projects/todo-list-api), beginner API)
**✅ Successful week =** full CRUD + pagination + filtering on `/todos`, tested in Swagger UI, plus a JWT-gated stretch version.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 10/15 | - [ ] FastAPI first steps — [FastAPI docs](https://fastapi.tiangolo.com/tutorial/first-steps/) | - [ ] [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) | - [ ] `pip install fastapi uvicorn`<br>- [ ] GET `/todos` returning a hardcoded list |
| Fri 10/16 | - [ ] Pydantic bodies — [FastAPI docs: Body](https://fastapi.tiangolo.com/tutorial/body/) | - [ ] [Min Stack](https://leetcode.com/problems/min-stack/) | - [ ] Define a `Todo` Pydantic model (id, title, completed)<br>- [ ] POST `/todos` storing in an in-memory list |
| Mon 10/19 | - [ ] Error handling — [FastAPI docs: Handling Errors](https://fastapi.tiangolo.com/tutorial/handling-errors/) | - [ ] [Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/) | - [ ] PUT `/todos/{id}` to update title/completed<br>- [ ] DELETE `/todos/{id}`, return 404 for a missing id |
| Tue 10/20 | - [ ] Dependency injection — [FastAPI docs: Dependencies](https://fastapi.tiangolo.com/tutorial/dependencies/) | - [ ] [Daily Temperatures](https://leetcode.com/problems/daily-temperatures/) | - [ ] Add `skip`/`limit` query params via a shared dependency<br>- [ ] Add a `?completed=true/false` filter |
| Wed 10/21 — SHIP DAY | — | - [ ] Re-solve [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) + [Generate Parentheses](https://leetcode.com/problems/generate-parentheses/) | - [ ] **Stretch:** add JWT auth so each user only sees their own todos<br>- [ ] Test every endpoint in `/docs`, commit v1 |

### Week 6 — Project: Expense Tracker API ([roadmap.sh](https://roadmap.sh/projects/expense-tracker-api), beginner API)
**✅ Successful week =** the Week 3 CLI's logic rebuilt as a Postgres-backed, JWT-authenticated API with category/date filtering and a monthly-summary endpoint.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 10/22 | - [ ] Relational modeling — [PostgreSQL Tutorial](https://www.postgresql.org/docs/current/tutorial.html) | - [ ] [Binary Search](https://leetcode.com/problems/binary-search/) | - [ ] Install Postgres<br>- [ ] Hand-create `users` and `expenses` tables in `psql` |
| Fri 10/23 | - [ ] SQLAlchemy — [SQLAlchemy 2.0 docs](https://docs.sqlalchemy.org/en/20/) | - [ ] [Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/) | - [ ] Define SQLAlchemy models for both tables<br>- [ ] GET/POST `/expenses` wired to Postgres |
| Mon 10/26 | - [ ] Indexing — [PostgreSQL Indexes](https://www.postgresql.org/docs/current/indexes.html) | - [ ] [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/) | - [ ] Add an index on the `date` column<br>- [ ] Benchmark a date-range query before/after the index |
| Tue 10/27 | - [ ] JWT auth — [FastAPI OAuth2/JWT tutorial](https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/) | - [ ] [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/) | - [ ] `/signup` and `/login` issuing JWTs<br>- [ ] Protect all `/expenses` routes, scope results to the logged-in user |
| Wed 10/28 — SHIP DAY | — | - [ ] Re-solve [Binary Search](https://leetcode.com/problems/binary-search/) + [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/) | - [ ] Add `?category=Food` and `?start_date=&end_date=` filters<br>- [ ] **Stretch:** `/expenses/summary` endpoint returning totals grouped by category<br>- [ ] Test with real tokens, commit v2 |

### Week 7 — Project: Blogging Platform API in Django ([roadmap.sh](https://roadmap.sh/projects/blogging-platform-api), beginner API)
**✅ Successful week =** full CRUD + search on blog posts in Django, admin panel customized, with a written FastAPI-vs-Django comparison.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 10/29 | - [ ] Django setup — [Django Tutorial Part 1](https://docs.djangoproject.com/en/stable/intro/tutorial01/) | - [ ] [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/) | - [ ] `django-admin startproject`, create a `blog` app<br>- [ ] Set up URL routing skeleton |
| Fri 10/30 | - [ ] Django models + migrations — [Django Tutorial Part 2](https://docs.djangoproject.com/en/stable/intro/tutorial02/) | - [ ] [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/) | - [ ] `Post` model: title, content, category, tags (JSON field), createdAt<br>- [ ] Register in `admin.py` |
| Mon 11/2 | - [ ] Django views/DRF — [Django Tutorial Part 3](https://docs.djangoproject.com/en/stable/intro/tutorial03/) | - [ ] [Reorder List](https://leetcode.com/problems/reorder-list/) | - [ ] POST/GET `/posts` (create + list)<br>- [ ] GET `/posts/{id}`, PUT `/posts/{id}`, DELETE `/posts/{id}` |
| Tue 11/3 | - [ ] Django ORM queries — [Django Tutorial Part 2](https://docs.djangoproject.com/en/stable/intro/tutorial02/) | - [ ] [Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/) | - [ ] GET `/posts?term=keyword` searching title/content/category (per spec) |
| Wed 11/4 — SHIP DAY | — | - [ ] Re-solve [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/) + [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/) | - [ ] **Stretch:** customize Django admin (list filters, search fields, a "publish" bulk action)<br>- [ ] Write FastAPI-vs-Django comparison note in README, push |

### Week 8 — Project: Caching Proxy in Go ([roadmap.sh](https://roadmap.sh/projects/caching-server), intermediate CLI)
**✅ Successful week =** a Go CLI proxy that caches origin responses, a `clear-cache` flag, the whole stack (FastAPI/Django + Postgres + Go proxy) running together via `docker-compose up`.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 11/5 | - [ ] Go syntax basics — [Go docs](https://go.dev/doc/) | - [ ] [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/) | - [ ] "Hello World" in Go<br>- [ ] Define a struct for a cached response (body, headers, expiry) |
| Fri 11/6 | - [ ] Gin routing — [Gin Quickstart](https://gin-gonic.com/en/docs/quickstart/) | - [ ] [Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/) | - [ ] CLI flags for `--port` and `--origin` (per spec)<br>- [ ] Forward requests to `--origin` and return the response |
| Mon 11/9 | - [ ] Docker basics — [Docker Get Started](https://docs.docker.com/get-started/) | - [ ] [Same Tree](https://leetcode.com/problems/same-tree/) | - [ ] Cache responses in memory keyed by request path<br>- [ ] Write a `Dockerfile` for the Week 7 Blogging API |
| Tue 11/10 | - [ ] Docker Compose + GitHub Actions — [GitHub Actions Quickstart](https://docs.github.com/en/actions/get-started/quickstart) | - [ ] [Subtree of Another Tree](https://leetcode.com/problems/subtree-of-another-tree/) | - [ ] `docker-compose.yml` with the API + Postgres<br>- [ ] GitHub Actions workflow running tests on push |
| Wed 11/11 — SHIP DAY | — | - [ ] Re-solve 2 tree problems, timed | - [ ] Implement the `clear-cache` CLI flag (per spec)<br>- [ ] **Stretch:** add the Go proxy as a third container in `docker-compose.yml`, sitting in front of the API<br>- [ ] Ship: `docker-compose up` runs everything — **Month 2 done** |

---

## MONTH 3 — Frontend: HTML/CSS/JS → React → Next.js → TypeScript (great frontend by end of month)

### Week 9 — Project: Flash Cards ([roadmap.sh](https://roadmap.sh/projects/flash-cards), beginner frontend)
**✅ Successful week =** a responsive, deployed flash-card app with flip animation, deck navigation, and progress tracking, loading decks from JSON.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 11/12 | - [ ] Semantic HTML — [MDN Learn Web Dev](https://developer.mozilla.org/en-US/docs/Learn_web_development) | - [ ] [Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/) | - [ ] HTML structure for a single card (question side, answer side) |
| Fri 11/13 | - [ ] CSS box model, flexbox — [freeCodeCamp RWD](https://www.freecodecamp.org/learn/responsive-web-design-v9) | - [ ] [Last Stone Weight](https://leetcode.com/problems/last-stone-weight/) | - [ ] CSS 3D flip animation on click |
| Mon 11/16 | - [ ] CSS Grid + media queries — [freeCodeCamp RWD](https://www.freecodecamp.org/learn/responsive-web-design-v9) | - [ ] [K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/) | - [ ] Next/previous/shuffle deck navigation<br>- [ ] Responsive layout, test on mobile widths |
| Tue 11/17 | - [ ] JS DOM + events — [MDN Learn Web Dev](https://developer.mozilla.org/en-US/docs/Learn_web_development) | - [ ] [Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/) | - [ ] "Mark as known/unknown" buttons<br>- [ ] Progress bar (X of Y known) in vanilla JS |
| Wed 11/18 — SHIP DAY | — | - [ ] Re-solve [K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/) + [Task Scheduler](https://leetcode.com/problems/task-scheduler/) | - [ ] **Stretch:** load decks from a JSON file (build a "LeetCode patterns" deck as your first real dataset)<br>- [ ] Deploy static (GitHub Pages/Vercel), push |

### Week 10 — Project: Quiz App ([roadmap.sh](https://roadmap.sh/projects/quiz-app), intermediate frontend)
**✅ Successful week =** a deployed React quiz app with a per-question countdown timer, live score tracking, and a results breakdown screen, loading questions from swappable datasets.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 11/19 | - [ ] Components, JSX, props — [React docs: Learn React](https://react.dev/learn) | - [ ] [Subsets](https://leetcode.com/problems/subsets/) | - [ ] Vite React app<br>- [ ] `Question`, `AnswerOptions`, `ScoreBoard` components |
| Fri 11/20 | - [ ] `useState` — [React docs: State](https://react.dev/learn/state-a-components-memory) | - [ ] [Combination Sum](https://leetcode.com/problems/combination-sum/) | - [ ] Track current question index, selected answer, and running score in state |
| Mon 11/23 | - [ ] `useEffect`, data fetching — [React docs: Effects](https://react.dev/learn/synchronizing-with-effects) | - [ ] [Permutations](https://leetcode.com/problems/permutations/) | - [ ] Per-question countdown timer using `useEffect`<br>- [ ] Auto-advance when time runs out |
| Tue 11/24 | - [ ] Forms/controlled inputs — [React docs](https://react.dev/learn) | - [ ] [Subsets II](https://leetcode.com/problems/subsets-ii/) | - [ ] End-of-quiz results screen: correct/incorrect breakdown per question |
| Wed 11/25 — SHIP DAY | — | - [ ] Re-solve [Subsets](https://leetcode.com/problems/subsets/) + [Word Search](https://leetcode.com/problems/word-search/) | - [ ] **Stretch:** support multiple question datasets (a LeetCode-patterns quiz + a general-knowledge one)<br>- [ ] Deploy, commit |

### Week 11 — Project: Weather Web App ([roadmap.sh](https://roadmap.sh/projects/weather-app), intermediate — in Next.js + TypeScript)
**✅ Successful week =** a deployed Next.js/TS weather app with search, 5-day forecast, unit toggle, and recent searches, proxying through your own FastAPI backend.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 11/26 | - [ ] Next.js App Router — [Learn Next.js](https://nextjs.org/learn/dashboard-app) | - [ ] [Number of Islands](https://leetcode.com/problems/number-of-islands/) | - [ ] `create-next-app`<br>- [ ] City search input UI |
| Fri 11/27 | - [ ] TypeScript basics — [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/) | - [ ] [Clone Graph](https://leetcode.com/problems/clone-graph/) | - [ ] `WeatherData` TypeScript interface<br>- [ ] Fetch current weather server-side |
| Mon 11/30 | - [ ] Server vs client components — [Learn Next.js](https://nextjs.org/learn/dashboard-app) | - [ ] [Max Area of Island](https://leetcode.com/problems/max-area-of-island/) | - [ ] 5-day forecast view<br>- [ ] Loading and error states |
| Tue 12/1 | - [ ] Next.js API routes — [Next.js docs](https://nextjs.org/docs) | - [ ] [Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/) | - [ ] °C/°F unit toggle<br>- [ ] Recent-searches list via `localStorage` |
| Wed 12/2 — SHIP DAY | — | - [ ] Re-solve [Number of Islands](https://leetcode.com/problems/number-of-islands/) + [Course Schedule](https://leetcode.com/problems/course-schedule/) | - [ ] **Stretch:** route weather calls through a Next.js API route that hits YOUR OWN FastAPI backend, not the weather API directly<br>- [ ] Deploy, commit |

### Week 12 — Project: Pomodoro Timer ([roadmap.sh](https://roadmap.sh/projects/pomodoro-timer), intermediate)
**✅ Successful week =** a deployed Pomodoro timer with configurable durations, session history persisted to your FastAPI backend, and a browser-tab countdown.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 12/3 | - [ ] DP basics — [NeetCode DP 1D](https://www.youtube.com/watch?v=_i4Yxeh5ceQ) | - [ ] [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) | - [ ] Work/break timer state machine in React |
| Fri 12/4 | - [ ] DP 1D continued | - [ ] [House Robber](https://leetcode.com/problems/house-robber/) | - [ ] Configurable work/break durations<br>- [ ] Session count tracking |
| Mon 12/7 | - [ ] DP 1D continued | - [ ] [House Robber II](https://leetcode.com/problems/house-robber-ii/) | - [ ] Deploy this + the Weather App to Vercel |
| Tue 12/8 | - [ ] DP 1D continued | - [ ] [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/) | - [ ] **Stretch:** persist completed sessions to your FastAPI backend so history survives across devices |
| Wed 12/9 — SHIP DAY | — | - [ ] Re-solve [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) + [Coin Change](https://leetcode.com/problems/coin-change/) | - [ ] Notification sound on session end<br>- [ ] Browser tab title shows live countdown<br>- [ ] Share live link, commit |

### Week 13 — Project: Personal Blog frontend ([roadmap.sh](https://roadmap.sh/projects/personal-blog), beginner — for your Week 7 Django API)
**✅ Successful week =** a full, accessible, performant frontend for your Django Blogging API, closing that backend/frontend loop; all 4 frontend projects pass a Lighthouse audit above 90.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 12/10 | - [ ] DP 2D — [NeetCode DP 2D](https://www.youtube.com/watch?v=qMky6D6YtXU) | - [ ] [Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/) | - [ ] Next.js post-list page fetching from your Django API |
| Fri 12/11 | - [ ] DP 2D continued | - [ ] [Unique Paths](https://leetcode.com/problems/unique-paths/) | - [ ] Single-post page: full content, category, tags |
| Mon 12/14 | - [ ] Intervals/Greedy — [LeetCode Discuss: Greedy Interval Patterns](https://leetcode.com/discuss/general-discussion/794725/General-Pattern-for-greedy-approach-for-Interval) | - [ ] [Insert Interval](https://leetcode.com/problems/insert-interval/) | - [ ] Accessibility pass (alt text, ARIA, keyboard nav) across all 4 frontend projects |
| Tue 12/15 | - [ ] Intervals/Greedy continued | - [ ] [Merge Intervals](https://leetcode.com/problems/merge-intervals/) | - [ ] Responsive pass at 3 breakpoints<br>- [ ] Performance pass (compress images, lazy-load) |
| Wed 12/16 — SHIP DAY | — | - [ ] Re-solve [Insert Interval](https://leetcode.com/problems/insert-interval/) + [Meeting Rooms](https://leetcode.com/problems/meeting-rooms/) | - [ ] Run Lighthouse on all 4 frontend projects, fix anything under 90<br>- [ ] Tag v1.0 — **Month 3 done** |

---

## MONTH 4 — Systems Design + AI/ML Kickoff

### Week 14 — Project: upgrade the Caching Proxy with real strategies
**✅ Successful week =** the Go proxy uses Redis with TTL expiration, invalidates on data change, and load-balances across 2 API instances; a design doc written.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 12/17 | - [ ] Caching concepts — [System Design Primer: Caching](https://github.com/donnemartin/system-design-primer) | - [ ] [Jump Game](https://leetcode.com/problems/jump-game/) | - [ ] Swap in-memory cache for Redis |
| Fri 12/18 | - [ ] Cache strategies — [ByteByteGo: Cache Systems](https://www.youtube.com/watch?v=dGAgxozNWFE) | - [ ] Re-solve one Week 12 DP problem, timed | - [ ] Add TTL expiration, benchmark hit/miss ratio |
| Mon 12/21 | - [ ] Cache invalidation — [System Design Primer](https://github.com/donnemartin/system-design-primer) | - [ ] Re-solve one graph problem, timed | - [ ] Add manual cache invalidation on data change |
| Tue 12/22 | - [ ] Load balancing algorithms — [ByteByteGo: Load Balancing](https://www.youtube.com/watch?v=dBmxNsS3BGE) | - [ ] 1 easy + 1 medium, timed | - [ ] **Stretch:** run 2 API instances behind the proxy, round-robin between them |
| Wed 12/23 — SHIP DAY | — | - [ ] 2 mixed problems, timed | - [ ] Write a one-page design doc: scaling this proxy at 10x traffic<br>- [ ] Commit |

### Week 15 — Project: Broadcast Server ([roadmap.sh](https://roadmap.sh/projects/broadcast-server), intermediate, sockets)
**✅ Successful week =** a TCP server broadcasting messages to all connected clients, with named rooms so broadcasts scope correctly.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 12/24 (light — holiday) | - [ ] CAP theorem — [Gaurav Sen System Design Playlist](https://www.youtube.com/playlist?list=PLMCXHnjXnTnvo6alSjVkgxV-VH6EPyvoX) | - [ ] 1 problem | - [ ] Scaffold a TCP server accepting multiple connections |
| Fri 12/25 | — REST (holiday, no tasks) — | | |
| Mon 12/28 | - [ ] Message queues — [ByteByteGo: Message Queue](https://www.youtube.com/watch?v=h1Lx-vQxILk) | - [ ] 1 problem | - [ ] Broadcast any message from one client to all connected clients |
| Tue 12/29 | - [ ] Async job processing — [System Design Primer](https://github.com/donnemartin/system-design-primer) | - [ ] 1 problem | - [ ] Handle client disconnects gracefully<br>- [ ] `list-clients` command |
| Wed 12/30 — SHIP DAY | — | - [ ] 1 problem, timed | - [ ] **Stretch:** add named "rooms" so clients only broadcast within their room<br>- [ ] Commit |

### Week 16 — Project: Predictive Modeling for Agriculture ([DataCamp](https://www.datacamp.com/projects/1772), guided)
**✅ Successful week =** a working crop-recommendation classifier trained on a single best feature, with a written comparison of 2 feature-selection techniques.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 12/31 (light — holiday) | - [ ] NumPy arrays — [NumPy Quickstart](https://numpy.org/doc/stable/user/quickstart.html) | - [ ] 1 problem | - [ ] Load the soil dataset, run basic stats |
| Fri 1/1 | — REST (holiday, no tasks) — | | |
| Mon 1/4 | - [ ] pandas DataFrames — [pandas 10 Minutes](https://pandas.pydata.org/docs/user_guide/10min.html) | - [ ] 1 problem | - [ ] Clean data, handle missing values, encode labels |
| Tue 1/5 | - [ ] scikit-learn basics — [scikit-learn Getting Started](https://scikit-learn.org/stable/getting_started.html) | - [ ] 1 problem | - [ ] Apply feature selection to find the single best predictive soil measure |
| Wed 1/6 — SHIP DAY | — | - [ ] 1 easy problem | - [ ] Train + evaluate the classifier on that feature<br>- [ ] **Stretch:** compare 2 feature-selection techniques, write up which won<br>- [ ] Commit notebook + write-up |

### Week 17 — Project: OpenAI API in Python ([roadmap.sh](https://roadmap.sh/projects/openai-api-python), intermediate)
**✅ Successful week =** a FastAPI-wrapped LLM chatbot with conversation history, structured JSON output, and a prompt-consistency test harness.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 1/7 | - [ ] LLM API basics — [OpenAI API docs](https://developers.openai.com/api/docs/quickstart) or [Anthropic API docs](https://platform.claude.com/docs/en/home) | - [ ] 1 problem | - [ ] First successful API call from a Python script |
| Fri 1/8 | - [ ] Prompting techniques — [Prompt Engineering Guide](https://www.promptingguide.ai/) | - [ ] 1 problem | - [ ] CLI chatbot maintaining conversation history |
| Mon 1/11 | - [ ] Structured outputs — [Anthropic Prompt Eng Best Practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices) | - [ ] 1 problem | - [ ] Wrap the chatbot in a FastAPI endpoint returning structured JSON |
| Tue 1/12 | - [ ] Prompt consistency testing | - [ ] 1 problem | - [ ] **Stretch:** build a prompt test harness (5 inputs × 3 prompt variants, auto-diff outputs) |
| Wed 1/13 — SHIP DAY | — | - [ ] 2 problems, timed | - [ ] Wire the chatbot endpoint into one of your frontend projects<br>- [ ] Commit — **Month 4 done** |

---

## MONTH 5 — AI/ML + Agentic Systems Deep Dive

### Week 18 — Project: RAG Chatbot for Technical Documentation ([DataCamp LLM projects](https://www.datacamp.com/blog/llm-projects))
**✅ Successful week =** a working RAG pipeline that answers questions about real documentation and cites its sources.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 1/14 | - [ ] Embeddings, chunking — [LangChain RAG example](https://docs.langchain.com/oss/python/deepagents/rag) | - [ ] 1 problem | - [ ] Chunk real documentation (your own README/docs or Python's own docs) |
| Fri 1/15 | - [ ] Vector DB basics — [Chroma Getting Started](https://docs.trychroma.com/docs/overview/getting-started) | - [ ] 1 problem | - [ ] Embed chunks, store in Chroma |
| Mon 1/18 | - [ ] Similarity search | - [ ] 1 problem | - [ ] Implement retrieval — top-k relevant chunks per query |
| Tue 1/19 | - [ ] Grounded generation | - [ ] 1 problem | - [ ] Feed retrieved chunks into the LLM prompt, generate grounded answers |
| Wed 1/20 — SHIP DAY | — | - [ ] 2 problems, timed | - [ ] **Stretch:** cite the specific source chunk(s) in every answer<br>- [ ] Wrap in a CLI/API, commit |

### Week 19 — Project: Tool-calling agent (inspiration: [DataCamp's 13 LLM project ideas](https://www.datacamp.com/blog/llm-projects))
**✅ Successful week =** an agent that correctly picks between 2+ tools, asks a clarifying question on ambiguous input, tested on 5 varied queries.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 1/21 | - [ ] LangChain fundamentals — [LangChain docs](https://docs.langchain.com/) | - [ ] 1 problem | - [ ] Reimplement Week 18's RAG pipeline using LangChain |
| Fri 1/22 | - [ ] Tool calling — [Anthropic: Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) | - [ ] 1 problem | - [ ] Define 2 tools: "search docs," "answer directly" |
| Mon 1/25 | - [ ] Agent loops — [LangGraph overview](https://docs.langchain.com/oss/python/langgraph/overview) | - [ ] 1 problem | - [ ] Build the agent loop that picks a tool per query |
| Tue 1/26 | - [ ] LlamaIndex as an alternative — [LlamaIndex docs](https://developers.llamaindex.ai/python/framework/) | - [ ] 1 problem | - [ ] **Stretch:** add a clarifying-question branch, 3 test cases proving it works |
| Wed 1/27 — SHIP DAY | — | - [ ] 2 problems, timed | - [ ] Test on 5 varied queries, fix failures<br>- [ ] Commit |

### Week 20 — Project: Movie Reservation System ([roadmap.sh](https://roadmap.sh/projects/movie-reservation-system), advanced)
**✅ Successful week =** a working seat-reservation system with no double-booking, JWT auth, a booking UI, and an AI "recommend me a movie" chat feature.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 1/28 | - [ ] Relational modeling for seat/schedule systems | - [ ] 1 problem | - [ ] Models: movies, showtimes, theaters, seats |
| Fri 1/29 | — | - [ ] 1 problem | - [ ] Seat reservation logic preventing double-booking |
| Mon 2/1 | — | - [ ] 1 problem | - [ ] JWT auth so users manage their own bookings |
| Tue 2/2 | — | - [ ] 1 problem | - [ ] Booking UI in Next.js (seat map, showtime picker) |
| Wed 2/3 — SHIP DAY | — | - [ ] 2 problems, timed | - [ ] Connect frontend to backend end-to-end<br>- [ ] **Stretch:** wire your Week 19 agent in as a "recommend me a movie" tool-calling chat feature<br>- [ ] Commit |

### Week 21 — Project: Real-time Leaderboard ([roadmap.sh](https://roadmap.sh/projects/realtime-leaderboard-system), advanced)
**✅ Successful week =** both projects deployed, a 10-query eval suite for the agent, and its scores feeding a live Redis leaderboard.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 2/4 | - [ ] Basic eval concepts | - [ ] 1 problem | - [ ] Write 10 test queries with expected agent behavior |
| Fri 2/5 | — | - [ ] 1 problem | - [ ] Build the Redis sorted-set leaderboard core, feed it eval pass-rates as scores |
| Mon 2/8 | — | - [ ] 1 problem | - [ ] Deploy the Movie Reservation System + Leaderboard |
| Tue 2/9 | — | - [ ] First full timed mock interview (1 medium, 30 min, no hints) | - [ ] Write technical README/case-study for both projects |
| Wed 2/10 — SHIP DAY | — | - [ ] 2 problems, timed | - [ ] **Stretch:** automate the eval script to run on every deploy and push scores to the leaderboard<br>- [ ] Ship, share live links — **Month 5 done** |

---

## MONTH 6 — FDE Sprint, Applications, Tailoring

### Week 22 — Project: Database Backup Utility ([roadmap.sh](https://roadmap.sh/projects/database-backup-utility), advanced CLI) + 1 rapid prototype
**✅ Successful week =** a CLI that backs up and successfully restores a real database, plus one more one-day prototype shipped with a demo video.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 2/11 | - [ ] Read [Palantir FDE interview guide](https://www.tryexponent.com/guides/palantir-forward-deployed-engineer-interview) | - [ ] 1 problem | - [ ] CLI taking host/user/password/db-name/destination, backing up all tables |
| Fri 2/12 | — | - [ ] 1 problem | - [ ] Verify a full restore from the backup files actually works |
| Mon 2/15 | — | - [ ] 1 problem | - [ ] Scope a 1-day prototype from a vague brief ("a small business needs to track customer orders") |
| Tue 2/16 | — | - [ ] 1 problem | - [ ] Ship that prototype |
| Wed 2/17 — SHIP DAY | — | - [ ] Timed mock (1 medium, 30 min) | - [ ] Write a retro on your scoping process<br>- [ ] **Stretch:** record a 2-minute client-pitch demo video for each<br>- [ ] Commit both + videos |

### Week 23 — Project: Restaurant Review Platform with NLP ([20 Backend Project Ideas](https://roadmap.sh/backend/project-ideas), difficult)
**✅ Successful week =** a reviews API with real sentiment analysis feeding a live leaderboard, plus 2 recorded mock discovery calls.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 2/18 | - [ ] Structuring a technical narrative for non-technical people | - [ ] 1 problem | - [ ] Reviews API (restaurant ID + text) + Redis leaderboard for scores |
| Fri 2/19 | — | - [ ] 1 problem | - [ ] Run NLP sentiment analysis on review text, update the leaderboard score |
| Mon 2/22 | - [ ] Diplomatic pushback techniques | - [ ] 1 problem | - [ ] Record a mock discovery call about this project |
| Tue 2/23 | — | - [ ] 1 problem | - [ ] Record a second mock discovery call about a different prototype |
| Wed 2/24 — SHIP DAY | — | - [ ] Timed mock (1 medium, 30 min) | - [ ] **Stretch:** have your "client" throw an unreasonable ask mid-call, practice pushing back diplomatically<br>- [ ] Fix weak points, re-record if needed |

### Week 24 — Project: Scalable E-Commerce Platform design + 1 microservice ([roadmap.sh](https://roadmap.sh/projects/scalable-ecommerce-platform), advanced)
**✅ Successful week =** a finalized resume/portfolio, 2 recorded system design mocks, and one working microservice proof of concept.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 2/25 | - [ ] Re-read [Anthropic FDE / Applied AI posting](https://job-boards.greenhouse.io/anthropic/jobs/5302966008) as a checklist | - [ ] 1 problem | - [ ] Rewrite resume leading with GridPeer/MockExam.ng + this build |
| Fri 2/26 | - [ ] System design mock prep — [roadmap.sh System Design](https://roadmap.sh/system-design) | - [ ] 1 problem | - [ ] Finalize portfolio site linking every shipped project |
| Mon 3/1 | — | - [ ] 1 problem | - [ ] System design mock: sketch the e-commerce platform's microservice boundaries, recorded |
| Tue 3/2 | — | - [ ] 1 problem | - [ ] Build one microservice from that design (e.g. products service) |
| Wed 3/3 — SHIP DAY | — | - [ ] Timed mock (1 medium, 30 min) | - [ ] Second system design mock on a different system<br>- [ ] Commit resume/portfolio + microservice POC |

### Week 25 — Applications go out
**✅ Successful week =** 10 tailored applications submitted across at least 2 rounds of research.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 3/4 | - [ ] Research 5 roles: [Palantir](https://jobs.lever.co/palantir), [OpenAI](https://openai.com/careers/search/), [Anthropic](https://www.anthropic.com/jobs) | - [ ] 1 problem | - [ ] Tailor resume/cover note for each of the 5 |
| Fri 3/5 | — | - [ ] 1 problem | - [ ] Submit applications to all 5 |
| Mon 3/8 | - [ ] Research 5 more: [Anduril](https://job-boards.greenhouse.io/andurilindustries/jobs/5057206007), [Scale AI](https://job-boards.greenhouse.io/scaleai/jobs/4593571005) | - [ ] 1 problem | - [ ] Tailor and submit 5 more applications |
| Tue 3/9 | - [ ] Optional: skim CDN Simulator concepts ([20 Backend Project Ideas](https://roadmap.sh/backend/project-ideas)) for interview material | - [ ] 1 problem | - [ ] Follow up on any application requesting extra materials |
| Wed 3/10 — SHIP DAY | — | - [ ] Timed mock (1 medium, 30 min) | - [ ] **Stretch:** write one researched, specific paragraph per company for your cover note<br>- [ ] Submit final batch of 5 — **10–15 applications out** |

### Week 26 — Final interview loop prep + buffer
**✅ Successful week =** a completed full mock interview loop (coding + system design + behavioral) and every weak spot from the roadmap addressed.

| Day | Learn | LeetCode | Build (exact tasks) |
| --- | --- | --- | --- |
| Thu 3/11 | - [ ] Behavioral interview prep (STAR format) | - [ ] 1 problem | - [ ] Write 5 STAR stories from your real project history |
| Fri 3/12 | — | - [ ] 1 problem | - [ ] Practice delivering the STAR stories out loud, recorded |
| Mon 3/15 | — | - [ ] Full mock loop part 1 — coding, timed | - [ ] Identify your weakest DSA pattern from the whole roadmap, re-drill it hard |
| Tue 3/16 | — | - [ ] Full mock loop part 2 — system design | - [ ] **Stretch:** write a one-page "how I think about this now" note on that weakest pattern |
| Wed 3/17 — FINAL SHIP DAY | — | - [ ] Full mock loop part 3 — behavioral | - [ ] Final check: resume, portfolio, GitHub all current<br>- [ ] **Roadmap complete:** 18 real named projects shipped, 150+ LeetCode problems across all 12 patterns, backend+frontend+AI+systems-design chops, 10–15 applications in flight |

---

## Existing Skills to Keep Leveraging
| Skill | How to use it |
| --- | --- |
| GridPeer, MockExam.ng | Portfolio spine — every project above should sit next to them |
| TypeScript/Next.js/Python/FastAPI/Django exposure | Some days go faster than "zero" pace — bank the time into extra LeetCode reps |
| N8N/WhatsApp bot work (Zaicon) | Early agentic-systems intuition — lean on it in Month 5 |
| Hackathon speed | The Month 6 rapid-prototyping muscle |
| Street University / mentoring reps | A head start on Month 6's client-communication days |
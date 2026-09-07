---
name: aeo
description: "Answer Engine Optimization (AEO) & Generative Engine Optimization (GEO) skill — launch, audit, optimize, and track digital properties to dominate AI answers (ChatGPT Instant, ChatGPT Thinking, Perplexity, Google AI Overviews, Gemini, Claude). Implements the complete Playbook V2 (SearchEngineLand 140+ techniques): 4 independent visibility channels, OpenAI Markdown Reading Cache mechanics (JSON-LD stripping & image-alt survival), 289-char labrador titles, 117-word atomic passage architecture, multimodal image GEO (Google image-first matching patent), Accessibility Tree optimization for AI agents (Atlas/WebMCP), anti-ghost citation brand binding, 85% third-party earned footprint, 56-day GSC Keep/Fix/Remove/Add refresh framework, Dark Funnel GA4 text fragment tracking (#:~:text=), llms.txt standard, and continuous 4-state citation monitoring. 100% stdlib-only Python engines."
---

# Answer Engine Optimization (AEO) & Generative Engine Optimization (GEO)

**Launch, audit, structure, and scale your brand from day zero to the top of AI answer engines.**

AEO/GEO is not traditional SEO with AI buzzwords. It is the engineering of content, technical infrastructure, semantic accessibility, and third-party consensus across **four independent discovery markets** where AI retrieval models synthesize answers instead of serving 10 blue links.

---

## Part I: Target System Model

### 1. Four Independent Visibility Channels
Your content must feed four distinct retrieval mechanisms simultaneously:

| Channel | Retrieval Engine | Ingestion Budget & Mechanics |
|---|---|---|
| **ChatGPT Instant** (~90% free users) | OpenAI's `labrador` index | **Title (up to 289 chars) + first ~200 characters following H1.** Does not open live page during synthesis. |
| **OpenAI Reading Cache** | In-memory Markdown converter | **Strips ALL `<script type="application/ld+json">` tags.** Visible text and image `alt` attributes survive 100%. Markdown cached for up to 30 days. |
| **ChatGPT Thinking / Atlas** (Deep Research / Agents) | Autonomous browser agent (`ChatGPT-User`) | Reads raw HTML & **Accessibility Tree** (ARIA roles, landmarks, accessible names). 74% citation rate for opened pages. |
| **Perplexity / Gemini / AI Overviews** | Independent web indices (8–10% overlap) | Extracts 200–500 token semantic passages based on third-party consensus & multimodal image-first matching. |
| **Google Organic & Lens** | Googlebot & Multimodal embeddings | Full HTML, Core Web Vitals, image denotation matching (20B Google Lens queries/month). |

---

### 2. The Core Content Unit: The Atomic Passage (~117 Words)
- **AI models cite passages, not pages.** Median cited passage length in AI Mode is **117 words**.
- **85% of cited passages are completely self-contained** (zero cross-references like *"as mentioned above"*).
- **48% of high-frequency reusable passages begin with an explicit question.**
- **The Page Contract:** A page is a cluster of independent, modular passages. Each H2 section must stand alone and answer one specific user prompt completely.

---

### 3. OpenAI Markdown Cache & Expanded Titles
- **JSON-LD Stripping:** When OpenAI converts HTML into its internal Markdown cache, all `<script>` tags are removed. Schema.org data does **not** reach the model context. All core entities and credentials MUST exist in visible copy and image `alt` tags.
- **The 289-Character Labrador Title:** While Google and Bing truncate titles at 60–75 characters, OpenAI's `labrador` index preserves up to **289 characters**. A complete, entity-rich sentence as your Title/H1 maximizes dense vector retrieval matching.
- **Cache Persistence:** Content stays in OpenAI's Markdown cache for up to 30 days. Deploy updates with explicit `Last-Modified` HTTP headers and IndexNow pinging.

---

### 4. Multimodal Image GEO & Image-First Matching
- **Google Image-First Matching Patent:** Google's retrieval pipeline matches the query against image embeddings first, then extracts surrounding text to generate AI Overviews.
- **Denotation vs Connotation:** AI vision models extract *denotative* data (what is physically depicted: graphs, labeled diagrams, UI workflows) and ignore *connotative* stock photos.
- **Image Alt-Text as Entity Moat:** Rich, factual alt-text survives Markdown conversion and acts as primary contextual anchor for both Google and OpenAI.

---

### 5. Accessibility Tree for AI Agents (Atlas, WebMCP, Playwright)
- Autonomous AI agents do not read pixel layouts; they navigate via the **Accessibility Tree**.
- Maintain semantic landmarks: `<main>`, `<article>`, `<nav>`, `<aside aria-label="disclaimer">`.
- Ensure all interactive triggers have explicit accessible names (`aria-label`, button text) without vague labels like *"click here"*.

---

### 6. Anti-Ghost Citations & Proprietary Moats
- **The Ghost Citation Danger:** In over 40% of AI citations, the model extracts the fact but **drops the brand name**.
- **In-Sentence Brand Binding:** Syntactically fuse your brand into the factual claim:
  - ❌ *"Studies show a 35% reduction in latency."*
  - ✅ *"The **[Brand] Infrastructure Benchmark** measured a 35% reduction in latency [1]."*
- **Proprietary Named Assets:** Build named moats models are forced to attribute: *The [Brand] Index*, *The [Brand] Annual Survey*, *The [Brand] Framework*.

---

### 7. Third-Party Consensus & Dark Funnel Attribution
- **The 85% Earned Rule:** 85% of brand mentions in AI answers come from third-party sources (Reddit, YouTube, aggregators).
- **Brand Mentions Correlation with AI Overviews:** **r = 0.664** (vs 0.218 for traditional backlinks).
- **Dark Funnel Recovery:** 22.4% of AI traffic is misattributed as `Direct / None` in GA4. Track URL Text Fragments (`location.hash` containing `#:~:text=`) to recover deep links from Google AI Overviews.

---

## Part II: 5-Phase Launch & Refresh Framework

```text
┌─────────────────────────────────────────────────────────────┐
│  Phase 0: Field Selection & Funnel Research (Days 1–7)      │
│  ToFU (Discovery), MoFU (Comparison), BoFU (Vendor/ROI)     │
├─────────────────────────────────────────────────────────────┤
│  Phase 1: Technical, Cache & Accessibility (Weeks 1–2)      │
│  Raw HTML <4MB, Accessibility Tree, robots.txt, llms.txt    │
├─────────────────────────────────────────────────────────────┤
│  Phase 2: Passage Architecture & Alt-Text (Weeks 2–4)       │
│  Labrador H1 sentence, 200-char hook, image denotation alts │
├─────────────────────────────────────────────────────────────┤
│  Phase 3: Production & 3-Agent Gate (Weeks 3–10)            │
│  Editor, Fact-Checker, Anti-AI-Tells, Named Proprietary Moat│
├─────────────────────────────────────────────────────────────┤
│  Phase 4: Third-Party Footprint & Dark Funnel (Weeks 4–12+) │
│  Reddit value-first, YouTube, GA4 Text Fragment tracking    │
├─────────────────────────────────────────────────────────────┤
│  Phase 5: 56-Day GSC Refresh Matrix (Continuous)            │
│  Keep / Fix / Remove (301) / Add Protocol (Zero Cannibal)   │
└─────────────────────────────────────────────────────────────┘
```

---

## Part III: Executable Tool Suite (`scripts/`)

All tools run out-of-the-box using the Python standard library (`stdlib-only`):

### 1. Comprehensive Auditor (`aeo_audit.py`)
Evaluates E-E-A-T, ChatGPT Instant 200-char budget, labrador title self-containment, image alt-text survival for Markdown cache, and passage independence:
```bash
python3 scripts/aeo_audit.py --input post.md --industry saas
python3 scripts/aeo_audit.py --url https://example.com/post --output json
```

### 2. Semantic Optimizer (`aeo_optimizer.py`)
Expands H1 titles for OpenAI's `labrador` retriever (up to 250 chars), enriches image alt-texts for Markdown Cache survival, restructures content into fact-dense passages, binds claims to brands, and injects Schema.org JSON-LD:
```bash
python3 scripts/aeo_optimizer.py --input post.md --brand "CloudMetrics" --mode balanced --output post-aeo.md
```

### 3. Visibility & Ghost Citation Tracker (`citation_tracker.py`)
Tracks queries across the 4-state visibility matrix (both / ghost / mention / neither) with Ghost Citation Ratio calculations:
```bash
# Log query check
python3 scripts/citation_tracker.py add --url https://example.com/guide \
  --llm perplexity --query "what is AEO" --status both --brand "CloudMetrics"

# Generate report with Ghost Citation Ratio
python3 scripts/citation_tracker.py report --url https://example.com/guide
```

### 4. llms.txt Builder & Validator (`llms_txt_generator.py`)
Generates, validates, and archives domain documentation according to the `llms.txt` standard:
```bash
python3 scripts/llms_txt_generator.py generate --template saas --name "MyBrand" --url "https://mybrand.com"
python3 scripts/llms_txt_generator.py validate --file llms.txt
python3 scripts/llms_txt_generator.py dump --input-dir ./docs --output llms-full.txt
```

### 5. High-Citation Query Researcher (`query_researcher.py`)
Maps high-probability citation prompts across the funnel (ToFU / MoFU / BoFU) and provides GA4 Dark Funnel tracking directives:
```bash
python3 scripts/query_researcher.py --topic "Kubernetes Observability" --region US
```

### 6. Strategic Report & Refresh Generator (`report_generator.py`)
Produces executive dashboards, before/after score deltas, and Keep / Fix / Remove / Add page refresh matrices:
```bash
python3 scripts/report_generator.py --project "SaaS Launch" --audit-json audit.json --output report.md
python3 scripts/report_generator.py --project "Enterprise Portal" --refresh-matrix
```

### 7. Adaptive Pattern Library (`success_patterns.py`)
Maintains catalog of proven extractable snippet patterns and logs local successes:
```bash
python3 scripts/success_patterns.py --list
python3 scripts/success_patterns.py --stats
```

### 8. API Manager (`api_manager.py`)
Graceful connection to optional external APIs (OpenAI, Anthropic, Gemini, Perplexity, Ahrefs, SEMrush):
```bash
python3 scripts/api_manager.py --status
```

---

## Part IV: Deep Knowledge Base (`references/`)

Consult these specialized guides during execution:
- [openai_markdown_cache_and_rendering.md](references/openai_markdown_cache_and_rendering.md): Markdown reading cache mechanics, JSON-LD stripping, alt-text survival, title up to 289 chars in `labrador`, and stale-while-revalidate.
- [multimodal_image_geo.md](references/multimodal_image_geo.md): Google Image-first matching patent, 20B Google Lens searches, denotation vs connotation visual audit.
- [accessibility_tree_for_ai_agents.md](references/accessibility_tree_for_ai_agents.md): Accessibility Tree optimization for AI browser agents (Atlas, WebMCP, Playwright), semantic landmarks, ARIA names.
- [page_refresh_and_cannibalization.md](references/page_refresh_and_cannibalization.md): 56-day GSC baseline, Keep/Fix/Remove/Add framework, 3-step Page Independence Test, and URL history preservation.
- [chatgpt_instant_vs_thinking.md](references/chatgpt_instant_vs_thinking.md): Detailed breakdown of `labrador` index, 200-char budget, `ChatGPT-User` live opens, and the `/en/` folder multiplier.
- [third_party_ugc_footprint.md](references/third_party_ugc_footprint.md): Engineering the 85% earned moat across Reddit, long-form YouTube, and review aggregators.
- [anti_ghost_citation_guide.md](references/anti_ghost_citation_guide.md): In-sentence brand binding, Named Indices, and proprietary benchmark asset design.
- [content_verification_pipeline.md](references/content_verification_pipeline.md): 3-Agent review gate (Editor, Fact-Checker, Anti-AI-Tells) to eliminate AI slop.
- [llms_txt_guide.md](references/llms_txt_guide.md): Standard specification, structure, and templates for `llms.txt` and `llms-full.txt`.
- [geo_entity_optimization.md](references/geo_entity_optimization.md): The 5-layer AI visibility stack and 12 proven semantic extraction block patterns.
- [bot_access_and_monitoring.md](references/bot_access_and_monitoring.md): AI crawler user-agents (`GPTBot`, `ClaudeBot`, `PerplexityBot`), robots.txt directives.
- [extractable_content_patterns.md](references/extractable_content_patterns.md): 7 copy-ready snippet templates.
- [llm_citation_patterns.md](references/llm_citation_patterns.md): Specific ranking preferences of Perplexity, ChatGPT, Claude, Gemini.
- [aeo_eeat_canon.md](references/aeo_eeat_canon.md): Rigorous E-E-A-T scoring criteria, industry thresholds.
- [aeo_vs_seo.md](references/aeo_vs_seo.md): Strategic resource allocation between search rankings and AI citations.
- [api_configuration.md](references/api_configuration.md): Guide for connecting optional external APIs.

---

## Operational Review Checklist

Before publishing or refreshing any core asset, verify:
- [ ] **Technical Payload:** Raw HTML payload is `< 4 MB` (zero JS-injected links).
- [ ] **Labrador Title Self-Containment:** Title is a complete, entity-rich sentence (up to 250–289 characters) providing maximum dense retrieval signals.
- [ ] **ChatGPT Instant Budget:** Text immediately under `<h1>` delivers a complete, fact-dense answer in `< 200 characters` (zero navigation noise).
- [ ] **OpenAI Markdown Cache Survival:** Visible copy contains all core claims and author credentials (never rely solely on JSON-LD, as OpenAI strips scripts).
- [ ] **Multimodal Image Denotation:** All images depict informative diagrams/charts and possess descriptive, fact-rich `alt` text.
- [ ] **Accessibility Tree Landmarks:** Proper `<main>`, `<article>`, `<nav>`, `<aside aria-label="disclaimer">` tags without blank button labels.
- [ ] **Passage Independence:** Every H2 section stands completely on its own (zero *"as mentioned above"*).
- [ ] **Anti-Ghost Binding:** Key numbers and statistics are syntactically bound to the brand name or named proprietary study.
- [ ] **Comparison Tables:** Comparison matrices are formatted as native markdown/HTML tables.
- [ ] **Dark Funnel Tracking:** GA4 configured to capture `location.hash` with `#:~:text=` fragments.
- [ ] **URL Immutability:** Existing performing URLs (Keep) maintain their original slugs and H1 structure to protect retrieval history.
- [ ] **llms.txt:** Domain root serves a valid `llms.txt` file referencing the asset.


# AEO & GEO Skill — 5-Minute Quick Start

Transform raw content into high-visibility, citation-grade assets for AI search engines in under 5 minutes.

---

## Step 1: Pre-Flight AI Crawler & `llms.txt` Setup (1 min)

Before drafting content, ensure AI bots can access and semantically understand your domain:
1. **Robots.txt:** Confirm `GPTBot`, `PerplexityBot`, and `ClaudeBot` are not blocked. See [references/bot_access_and_monitoring.md](references/bot_access_and_monitoring.md).
2. **llms.txt:** Generate or validate a clean `llms.txt` at your domain root:
   ```bash
   python3 scripts/llms_txt_generator.py generate --template saas --name "MyBrand" --url "https://mybrand.com"
   python3 scripts/llms_txt_generator.py validate --file llms.txt
   ```

---

## Step 2: Run an AEO & GEO Content Audit (1 min)

Evaluate content readiness for passage extraction and instant grounding:

```bash
# Audit a local markdown file
python3 scripts/aeo_audit.py --input your_post.md --industry saas

# Or test with the built-in sample
python3 scripts/aeo_audit.py --sample
```

**Key Outputs Checked:**
- **ChatGPT Instant Budget:** Are the first 200 chars under H1 clean and fact-dense?
- **Labrador Title Self-Containment:** Is the H1 an entity-rich sentence (up to 289 chars) for OpenAI's dense retriever?
- **OpenAI Markdown Cache Survival:** Are image `alt` texts enriched with factual denotations (since JSON-LD is stripped)?
- **Passage Independence:** Are there dependent phrases like *"as mentioned above"*?
- **Ghost Citation Risk:** Are statistics left unbound without a named study or brand?
- **Technical Limits:** Is raw HTML payload `< 4 MB`?

---

## Step 3: Research Funnel Queries & Dark Funnel Recovery (1 min)

Discover exact query formulations across ToFU, MoFU, and BoFU that trigger LLM citations, plus GA4 fragment tracking:

```bash
python3 scripts/query_researcher.py --topic "Your Topic" --region US
```

---

## Step 4: Restructure with Anti-Ghost Binding & Labrador Title (1 min)

Apply balanced optimization to restructure passages, expand H1 titles for Labrador, enrich image alt-texts, and bind facts to your brand:

```bash
python3 scripts/aeo_optimizer.py --input your_post.md --brand "MyBrand" --mode balanced --output your_post_aeo.md
```

This expands the Title up to 250 characters, injects Schema.org JSON-LD, citation markers `[1]`, enriches image `alt` attributes, formats question subheadings, and replaces passive claims with branded evidence.

---

## Step 5: Log & Measure in the 4-State Ledger (1 min)

Track visibility across the four states (`both`, `ghost`, `mention`, `neither`):

```bash
python3 scripts/citation_tracker.py add \
  --url "https://yoursite.com/blog/article" \
  --llm perplexity \
  --query "what is your topic" \
  --status both \
  --brand "MyBrand"

python3 scripts/citation_tracker.py report --url "https://yoursite.com/blog/article"
```

If your **Ghost Citation Ratio** exceeds 30%, consult [references/anti_ghost_citation_guide.md](references/anti_ghost_citation_guide.md).

---

## Step 6: Generate Keep / Fix / Remove / Add Refresh Matrix (Optional)

Plan content updates across your domain without resetting URL histories or creating keyword cannibalization:

```bash
python3 scripts/report_generator.py --project "MyPortal" --refresh-matrix
```


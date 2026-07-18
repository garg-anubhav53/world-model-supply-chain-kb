# Verification: 凌越机器人 / "Ling Yue Robotics" — Fire 90, 2026-07-18

## VERDICT: SEARCH-HALLUCINATION-NOT-REAL

"凌越机器人" is a fabricated entity name. It does not appear anywhere in the
actual primary source (the OFweek article). The real subject of that article
is **长盈精密 (Everwin Precision / Changying Jingmi)**, a company ALREADY
tracked and killed in this campaign's KILL-LIST (Fire 75, killed on size:
~$6.8B A-share market cap). No new company exists here.

## How this was resolved

1. Fetched the OFweek URL directly with WebFetch (AI-summarized) — got a
   plausible-looking but WRONG extraction that used the name "凌越机器人"
   with quotes like "为机器人核心零部件及解决方案提供商". This is itself a
   second-generation hallucination layered on top of the first scout's bad
   extraction — proof the failure mode compounds across repeated
   AI-summarization passes of the same source.

2. Downloaded the raw HTML directly via curl (bypassing any AI
   summarization) and decoded it correctly — the page's actual charset is
   **GBK**, not UTF-8. A naive UTF-8 decode/strip renders the entire body as
   garbage substitution characters, which is almost certainly WHY earlier
   extraction passes fell back to hallucinating content (an AI model fed a
   corrupted/undecodable payload will confabulate plausible-sounding
   robotics-company boilerplate rather than say "this text is unreadable").
   Re-decoded with `.decode('gbk')` — text became fully legible Chinese.

3. Ground-truth article title (verbatim, GBK-decoded):
   > 全球第四大人形机器人精密零组件制造商，披露港股IPO新动态！
   > ("World's 4th-largest humanoid-robot precision-component manufacturer
   > discloses new HK-IPO development!")

   First sentence of body:
   > 5月11日，长盈精密向港交所递交了公开发行境外上市外资股，并在香港联交所
   > 主板上市。
   > ("On May 11, Everwin Precision (长盈精密) submitted an application to
   > HKEX for an offering of foreign shares for overseas listing, to list on
   > the HKEX Main Board.")

   Revenue sentence (verbatim — this is the exact source of the "RMB1.84bn
   vs RMB0.30bn, +506.87%" figures both earlier scout passes picked up):
   > 2025年，长盈精密的机器人及其他业务营收达1.84亿元，较2024年的0.30亿元
   > 同比增速高达506.87%...
   > ("In 2025, Everwin Precision's robotics-and-other business revenue
   > reached RMB184 million [note: 亿=hundred-million, so this is RMB1.84bn
   > only if read as 1.84亿=184 million... article literally says 1.84亿元
   > = RMB 184 million, NOT RMB1.84 billion — see note below], versus RMB30
   > million [0.30亿元] in 2024, YoY growth of 506.87%.")

   **IMPORTANT CORRECTION vs. both earlier scout extractions**: 1.84亿元 =
   RMB 184 million (亿 = 100 million), NOT "RMB1.84bn" as both prior passes
   stated. Both earlier extractions misplaced a decimal/unit by 10x. Actual
   2025 robotics-segment revenue for Everwin Precision ≈ RMB184m (up from
   RMB30m in 2024). This is a genuine, previously-undetected unit error that
   compounded the confusion — worth flagging generally: watch for 亿/万 unit
   handling in AI-summarized Chinese financial figures.

   Customer/buyer language (verbatim):
   > ...为海内外人形机器人企业开发金属材料...(cnc/3D打印等工艺)...为人形
   > 机器人的结构件、执行器、传感器、变速齿轮、线束、电机等提供核心零部件
   > ("...develops materials for domestic and overseas humanoid-robot
   > companies... supplies core components — structural parts, actuators,
   > sensors, gearing, harnesses, motors — for humanoid robots")
   — generic, NO named buyer (consistent with what Fire-75's kill entry
   already recorded).

   Market-share language actually says 80% of *shipment volume* goes to
   *overseas customers* (海外客户出货占比约80%), NOT "80% share among
   humanoid robot companies" as one earlier pass claimed — another
   fabricated/garbled detail.

4. Searched HKEXnews (www1.hkexnews.hk) directly for "凌越机器人," "Ling Yue
   Robotics," "LingYue Robotics" — **zero results**. No such filer exists on
   HKEX. (The real A1 filer discussed in the article, Everwin
   Precision/长盈精密, is a different, already-tracked HKEX applicant —
   filed 2026-05-11 per the article, consistent with KB's existing Fire-75
   entry.)

5. Searched for 企查查/天眼查 corporate registration for "凌越机器人" —
   no record found. Searched generically for "凌越机器人" company/website —
   no matching robotics company surfaced (top hits were unrelated
   similarly-named entities: 凌度智能/X-Human curtain-wall robots, 凌越资本
   an investment fund, 凌鸥创芯 a chip company — none are "凌越机器人" and
   none make humanoid/robot BOM components).

6. Cross-checked for possible source of the "凌越" name confusion: found
   that 领益智造 (Lingyi iTech, 002600.SZ) has an unrelated humanoid-robot
   PRODUCT (not company) reportedly named "凌越"/"玲珑" in different source
   summaries (itself contradictory across searches) — this is a plausible
   contamination vector: an AI summarizer may have pattern-matched a
   phonetically similar name from unrelated Lingyi iTech coverage onto the
   Everwin Precision article, inventing "凌越机器人" as a chimera entity.
   This remains speculative as to mechanism, but the conclusion is solid
   regardless: **no company called 凌越机器人 is described in, or
   supported by, the actual primary source.**

## Quick-kill check (moot — not a real distinct company)
N/A — there is no company here to evaluate. All financial/business facts
belong to Everwin Precision (长盈精密), already logged in KILL-LIST
(Fire 75, killed on size, ~$6.8B A-share base) and already re-surfaced/
dedup'd in this fire's scout-hkex-a1.md (line 45).

## Recommended KB action
Log "凌越机器人 / Ling Yue Robotics" as a **new false-positive-taxonomy
entry**: category = "hallucinated entity from GBK-encoding-corruption +
possible name-contamination from unrelated company," root cause =
AI-summarization of a mis-decoded (GBK read as UTF-8) Chinese-language
source page. Underlying real facts (1.84亿/0.30亿 revenue, 506.87% growth,
"world's 4th largest humanoid-robot precision-component manufacturer,"
HKEX A1 filed 2026-05-11) all belong to Everwin Precision (长盈精密),
already tracked/killed. No new candidate to add. Future scouts should not
spend further time on "凌越机器人."

## Sources
- OFweek article (primary source, fetched raw + GBK-decoded to bypass AI
  summarization corruption): https://robot.ofweek.com/2026-05/ART-898890-8120-30687302.html
  (title: 全球第四大人形机器人精密零组件制造商，披露港股IPO新动态！ —
  confirmed subject = 长盈精密/Everwin Precision, published 2026-05-13)
- HKEXnews search (www1.hkexnews.hk) for 凌越机器人/Ling Yue Robotics/
  LingYue Robotics — no results found, searched 2026-07-18.
- Existing KB record: kb/kb/runs/fire90-2026-07-18/scout-hkex-a1.md line 45
  (Everwin Precision resurfaced/dedup'd, killed Fire 75 on size).
- Generic web search for 凌越机器人 company/website/工商注册 — no
  matching entity found, searched 2026-07-18.

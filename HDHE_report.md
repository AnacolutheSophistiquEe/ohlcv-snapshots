# 267260

**Generated** : 2026-09-03T21:53:24.412018+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩706000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot ₩706000.00 (+2.6% vs entrée) · entrée ₩687850.00 · stop ₩641850.00 · T1 ₩721307.35 · R/R 0.73  
> ↳ P(T1 av. stop) 58 % _(réel 5 s)_ · EV/risk -0.054 _(réel 5 s)_ (GBM 0.069) · ¼-Kelly 0.014 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩681158.53–₩694541.47 (mid ₩687850.00)
- Spot actuel : ₩706000.00 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : ₩641850.00 (stop swing_plan-based (-9.09%))
- Targets : T1 ₩721307.35 · R/R 0.73 | T2 ₩754764.70 · R/R 1.45 | T3 ₩788222.05 · R/R 2.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩641850.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.09 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **2.625 pt plus bas** dans le cas TYPIQUE (médiane), 2.625 au p90, **2.625 au pire**
   - perte réelle **11.715 %** en moyenne _(tirée par la queue)_, jusqu'à **11.715 %** — au lieu des 9.09 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0022 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.659 % | p01 -4.805 % | pire -11.715 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0821** [0.048 ; 0.13] _(largeur 8.2 pt, n_eff 173.1)_
   - swing : **0.3498** [0.3009 ; 0.4012] _(largeur 10.0 pt, n_eff 345.6)_
   - deep : **0.3112** [0.2641 ; 0.3614] _(largeur 9.7 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 37.0 observations effectives », dont la borne haute a 95 % vaut environ 8.1 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 30.2 observations effectives », dont la borne haute a 95 % vaut environ 9.9 %.
- ⚠ **5 s — échantillon insuffisant sur : swing (30.9 pt), deep (33.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.68 %** | CVaR **-8.85 %** | vol 4.43 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.86 % contre 5.02 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.82 % vs -11.99 % si l'on extrapolait par √5 _(rapport 0.902 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0465** (β de hausse 0.8333, asymétrie 1.2558) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.069 | EV/share : ₩3178.501 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 34 % | T3 19 %
- Kelly (position) : f* 0.056 | ¼-Kelly 0.014 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.7 | bear 6.8 | side 7.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.174% → cible +5.968% / stop −8.0%, p_fill 93%, n_eff≈38.8) : P(cible|rempli) **7%** · **EV/risk -0.007** (×p_fill ; si rempli -0.06% du capital)
  - **swing** (entrée dip −2.575% → cible +4.864% / stop −6.688%, p_fill 87%, n_eff≈37.0) : P(cible|rempli) **58%** · **EV/risk -0.054** (×p_fill ; si rempli -0.41% du capital)
  - **deep** (entrée dip −3.977% → cible +6.879% / stop −10.178%, p_fill 66%, n_eff≈30.2) : P(cible|rempli) **39%** · **EV/risk -0.251** (×p_fill ; si rempli -3.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→42% · +3.0%→35% · +5.0%→12% · +8.0%→4%
- Range intraday médian 6.79% (p90 10.49%) · excursion haute méd. +1.58% / basse méd. −4.12%
- Profil de vol intra : ouverture 4.498% vs midi 1.222% vs clôture 1.303% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 84% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.106 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -0.868% ; recovery-V 32%
- **σ réalisé intraday** 4.162% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 64% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 750875.0 (VA 741375.0–756575.0 ; dernier close 770000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 77% · **stop −4.57%** sous le fill (sous le bruit) · cible +2.55% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. 0.7% · baisse 37% (gap-down >1% 18% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −1.68% (p90 −3.93%) · haut méd +0.86% · range méd 2.9%
- Excursion ouverture 15min (n=160) : bas méd −2.09% (p90 −4.37%) · haut méd +0.96% · range méd 3.56%
- Excursion ouverture 30min (n=160) : bas méd −2.27% (p90 −4.86%) · haut méd +1.04% · range méd 3.79%
- Excursion ouverture 60min (n=160) : bas méd −2.64% (p90 −5.12%) · haut méd +1.07% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 769000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 74% (109/159) · gap 30% · délai 0.0min · rebond 51% (57/109) (MFE +1.06%)
   - −1.0% : fill 30min 55% · séance 71% (101/159) · gap 18% · délai 0.2min · rebond 58% (60/101) (MFE +1.31%)
   - −1.5% : fill 30min 50% · séance 65% (90/159) · gap 15% · délai 0.7min · rebond 65% (58/90) (MFE +1.27%)
   - −2.0% : fill 30min 41% · séance 59% (80/159) · gap 10% · délai 1.2min · rebond 70% (56/80) (MFE +1.66%)
   - −3.0% : fill 30min 34% · séance 49% (65/159) · gap 6% · délai 4.6min · rebond 78% (50/65) (MFE +2.0%)
   - −4.0% : fill 30min 22% · séance 39% (51/159) · gap 3% · délai 16.5min · rebond 78% (37/51) (MFE +2.16%)
   - −5.0% : fill 30min 15% · séance 31% (41/159) · gap 3% · délai 29.6min · rebond 77% (30/41) (MFE +2.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.92% (p90 −3.71%) → stop au-delà de −2.66% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −3.19%) → stop au-delà de −2.48% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.43%) → stop au-delà de −3.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=828 jambes) : jambe baissière méd −1.22% (p90 −3.26%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 100% (50/50) · rebond 46% (25/50)
      · −2.0% : fill 96% (44/50) · rebond 66% (28/44)
      · −3.0% : fill 87% (39/50) · rebond 79% (29/39)
      · −4.0% : fill 76% (33/50) · rebond 78% (24/33)
      · −5.0% : fill 61% (27/50) · rebond 83% (21/27)
   - **flat** (17 séances) :
      · −1.0% : fill 96% (16/17) · rebond 74% (11/16)
      · −2.0% : fill 72% (12/17) · rebond 73% (10/12)
      · −3.0% : fill 55% (10/17) · rebond 49% (7/10)
      · −4.0% : fill 50% (8/17) · rebond 62% (4/8)
      · −5.0% : fill 50% (8/17) · rebond 73% (6/8)
   - **gap-up** (92 séances) :
      · −1.0% : fill 47% (35/92) · rebond 68% (24/35)
      · −2.0% : fill 33% (24/92) · rebond 78% (18/24)
      · −3.0% : fill 24% (16/92) · rebond 89% (14/16)
      · −4.0% : fill 13% (10/92) · rebond 92% (9/10)
      · −5.0% : fill 8% (6/92) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 36% en base · 48% si les 15 1res min sont vertes (67 cas) · 31% si rouges (93 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:18** → P(séance verte=clôture>ouverture) 72% si début vert vs 16% si rouge (base 36% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **72%** · continue >prix actuel 43% ; creux résiduel méd -1.79% (q20 -3.65%) → **SL/trailing à −3.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +2.66% → **scale +1.57% / runner +2.66%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **16%** (continue à baisser 39%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.84%** (au-delà de la MAE q10 -4.84%), cible rebond +1.69% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.05% .. +2.7%] · haut q95 +4.28% · bas q05 -5.45%
   - 60min (n=160) : retour [-5.61% .. +2.57%] · haut q95 +4.49% · bas q05 -6.0%
   - 2h (n=160) : retour [-6.4% .. +3.64%] · haut q95 +4.85% · bas q05 -7.17%
   - 4h (n=160) : retour [-6.87% .. +3.35%] · haut q95 +5.09% · bas q05 -8.36%
   - 6h (n=160) : retour [-7.12% .. +4.54%] · haut q95 +6.02% · bas q05 -8.93%
   - session (n=160) : retour [-7.33% .. +5.09%] · haut q95 +6.03% · bas q05 -9.37%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.8  _(momentum baissier)_
- **ADX** : 14.9  _(pas de tendance nette)_
- **MACD** : hist 1007.898  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 18.1%
- **ATR** : 46000.0 (37.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.077  _(accumulation)_
- **Vol ratio** : 1.56  _(volume au-dessus de la moyenne)_
- **Choppiness** : 48.1  _(transition)_
- **MA** : MA20 758355.42 · MA50 795263.69 · MA200 919057.57  _(prix < MA20)_
- **Dist MA** : MA20 -6.9% · MA50 -11.2% · MA200 -23.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (478388 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# 000660

**Generated** : 2026-10-01T00:15:07.164176+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1776000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩1776000.00 (+3.1% vs entrée) · entrée ₩1723114.39 · stop ₩1645471.53 · T1 ₩1834840.47 · R/R 1.44  
> ↳ ¼-Kelly 0.06 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 212 % hors [0,100] (R² max 1.00). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1707926.02–₩1738302.75 (mid ₩1723114.39)
- Spot actuel : ₩1776000.00 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : ₩1645471.53 (plancher anti-bruit (R/R<2) ; -4.51 % depuis l'entree)
- Targets : T1 ₩1834840.47 · R/R 1.44 | T2 ₩1921647.82 · R/R 2.56 | T3 ₩2008455.18 · R/R 3.68
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1645471.53


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.49 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.35 %)** : le gap seul le franchit 0.903 % des séances (11 fois sur 1218).
   - exécution **1.296 pt plus bas** dans le cas TYPIQUE (médiane), 2.988 au p90, **3.51 au pire**
   - perte réelle **8.937 %** en moyenne _(tirée par la queue)_, jusqu'à **10.86 %** — au lieu des 7.35 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0143 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 11 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.444 % | p01 -6.997 % | pire -10.86 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.457** [0.384 ; 0.5314] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4409** [0.3892 ; 0.4936] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.3809** [0.3309 ; 0.4329] _(largeur 10.2 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.73 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.13 % contre 6.64 % aujourd'hui, rapport 0.47)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.74 % si l'on extrapolait par √5 _(rapport 0.875 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4151** (β de hausse 1.6211, asymétrie 0.8729) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.422 | EV/share : ₩32744.111 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 35 % | T3 23 %
- Kelly (position) : f* 0.242 | ¼-Kelly 0.06 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.0 | bear 6.6 | side 8.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.357% → cible +4.731% / stop −2.365%, p_fill 62%, n_eff≈69.3) : P(cible|rempli) **13%** · **EV/risk -0.223** (×p_fill ; si rempli -0.85% du capital)
  - **swing** (entrée dip −2.978% → cible +6.484% / stop −4.506%, p_fill 56%, n_eff≈65.1) : P(cible|rempli) **39%** · **EV/risk -0.055** (×p_fill ; si rempli -0.45% du capital)
  - **deep** (entrée dip −4.602% → cible +8.297% / stop −6.874%, p_fill 58%, n_eff≈61.5) : P(cible|rempli) **46%** · **EV/risk -0.031** (×p_fill ; si rempli -0.37% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→54% · +3.0%→39% · +5.0%→21% · +8.0%→8%
- Range intraday médian 5.63% (p90 10.55%) · excursion haute méd. +2.31% / basse méd. −2.54%
- Profil de vol intra : ouverture 2.935% vs midi 1.209% vs clôture 1.412% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑1%/↓0% ; spike-down 60% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.417% ; recovery-V 21%
- **σ réalisé intraday** 3.097% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 62% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 1770450.0 (VA 1753550.0–1779550.0 ; dernier close 1769000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 70% · **stop −7.09%** sous le fill (sous le bruit) · cible +2.06% · R/R 0.29 (high win-rate)
- Gaps overnight (n=152) : méd. 0.63% · baisse 44% (gap-down >1% 31% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.81%) · haut méd +0.78% · range méd 1.36%
- Excursion ouverture 15min (n=160) : bas méd −0.86% (p90 −2.34%) · haut méd +0.92% · range méd 1.96%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.04%) · haut méd +1.25% · range méd 2.52%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.95%) · haut méd +1.37% · range méd 3.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1765000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 65% (94/152) · gap 38% · délai 0.0min · rebond 58% (52/94) (MFE +1.35%)
   - −1.0% : fill 30min 46% · séance 60% (87/152) · gap 31% · délai 0.0min · rebond 60% (55/87) (MFE +1.33%)
   - −1.5% : fill 30min 36% · séance 54% (79/152) · gap 25% · délai 0.0min · rebond 68% (53/79) (MFE +1.53%)
   - −2.0% : fill 30min 32% · séance 45% (71/152) · gap 24% · délai 0.0min · rebond 61% (46/71) (MFE +1.77%)
   - −3.0% : fill 30min 28% · séance 40% (60/152) · gap 19% · délai 0.8min · rebond 68% (40/60) (MFE +1.73%)
   - −4.0% : fill 30min 22% · séance 33% (51/152) · gap 13% · délai 1.0min · rebond 64% (36/51) (MFE +2.19%)
   - −5.0% : fill 30min 14% · séance 25% (39/152) · gap 7% · délai 12.2min · rebond 70% (26/39) (MFE +2.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −2.3%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −2.56%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.69%) → stop au-delà de −2.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=839 jambes) : jambe baissière méd −1.22% (p90 −3.28%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 97% (60/61) · rebond 55% (33/60)
      · −2.0% : fill 77% (52/61) · rebond 49% (29/52)
      · −3.0% : fill 73% (46/61) · rebond 62% (28/46)
      · −4.0% : fill 65% (42/61) · rebond 59% (28/42)
      · −5.0% : fill 48% (32/61) · rebond 62% (19/32)
   - **flat** (9 séances) :
      · −1.0% : fill 36% (6/9) · rebond 100% (6/6)
      · −2.0% : fill 19% (3/9) · rebond 100% (3/3)
      · −3.0% : fill 13% (2/9) · rebond 100% (2/2)
      · −4.0% : fill 0% (0/9) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/9) · rebond 0% (0/0)
   - **gap-up** (82 séances) :
      · −1.0% : fill 35% (21/82) · rebond 66% (16/21)
      · −2.0% : fill 24% (16/82) · rebond 87% (14/16)
      · −3.0% : fill 18% (12/82) · rebond 86% (10/12)
      · −4.0% : fill 12% (9/82) · rebond 83% (8/9)
      · −5.0% : fill 10% (7/82) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 57% si les 15 1res min sont vertes (84 cas) · 28% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 71% si début vert vs 11% si rouge (base 43% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 223min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=88) : tient le vert **71%** · continue >prix actuel 52% ; creux résiduel méd -1.42% (q20 -3.51%) → **SL/trailing à −3.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +2.88% → **scale +1.65% / runner +2.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **11%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.13%** (au-delà de la MAE q10 -6.13%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.04% .. +2.59%] · haut q95 +3.29% · bas q05 -4.07%
   - 60min (n=160) : retour [-3.36% .. +4.28%] · haut q95 +4.79% · bas q05 -5.13%
   - 2h (n=160) : retour [-4.5% .. +4.45%] · haut q95 +6.12% · bas q05 -6.71%
   - 4h (n=160) : retour [-6.33% .. +5.17%] · haut q95 +6.86% · bas q05 -7.6%
   - 6h (n=160) : retour [-6.33% .. +5.26%] · haut q95 +7.88% · bas q05 -8.11%
   - session (n=160) : retour [-6.9% .. +5.56%] · haut q95 +8.07% · bas q05 -8.23%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 000660 = **volatil sans tendance propre (choppy)** (vol intra méd 3.13%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.22 · part idiosyncratique 0.78
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.6  _(neutre)_
- **ADX** : 10.5  _(pas de tendance nette)_
- **MACD** : hist 457.247  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 19.1%
- **ATR** : 77642.86 (57.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.085  _(distribution)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 53.6  _(transition)_
- **MA** : MA20 1763650.0 · MA50 1683422.38 · MA200 1404768.96  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 +5.5% · MA200 +26.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (550611 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

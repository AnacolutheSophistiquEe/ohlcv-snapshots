# 267260

**Generated** : 2026-09-30T00:19:51.479945+00:00  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩681000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩681000.00 (+5.6% vs entrée) · entrée ₩645021.14 · stop ₩593419.45 · T1 ₩656179.80 · R/R 0.22  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 15147 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩642789.41–₩647252.87 (mid ₩645021.14)
- Spot actuel : ₩681000.00 (+5.6% au-dessus de la zone — repli à attendre)
- Stop : ₩593419.45 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩656179.80 · R/R 0.22 | T2 ₩667338.46 · R/R 0.43 | T3 ₩678497.12 · R/R 0.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩593419.45


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.11 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.81 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 15.81 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.671 % | p01 -4.805 % | pire -11.715 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0655** [0.0356 ; 0.1097] _(largeur 7.4 pt, n_eff 173.1)_
   - swing : **0.4426** [0.3909 ; 0.4953] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.3608** [0.3115 ; 0.4124] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.68 %** | CVaR **-8.85 %** | vol 4.43 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.66 % contre 4.90 % aujourd'hui, rapport 0.54)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.97 % vs -11.99 % si l'on extrapolait par √5 _(rapport 0.915 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0353** (β de hausse 0.8409, asymétrie 1.2312) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.089 | EV/share : ₩-4608.510 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 26 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 7.3 | side 7.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.283% → cible +1.73% / stop −8.0%, p_fill 22%, n_eff≈27.4) : P(cible|rempli) **44%** · **EV/risk -0.010** (×p_fill ; si rempli -0.36% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=13))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=11))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→66% · +2.0%→46% · +3.0%→31% · +5.0%→9% · +8.0%→3%
- Range intraday médian 5.36% (p90 9.76%) · excursion haute méd. +1.84% / basse méd. −3.33%
- Profil de vol intra : ouverture 3.907% vs midi 1.06% vs clôture 1.127% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 83% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -1.004% ; recovery-V 29%
- **σ réalisé intraday** 3.999% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 39% / bas 68% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 714037.5 (VA 710012.5–714037.5 ; dernier close 713000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 78% · **stop −4.51%** sous le fill (sous le bruit) · cible +2.38% · R/R 0.53 (high win-rate)
- Gaps overnight (n=153) : méd. 0.64% · baisse 38% (gap-down >1% 19% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −1.72% (p90 −3.89%) · haut méd +0.86% · range méd 2.79%
- Excursion ouverture 15min (n=160) : bas méd −2.06% (p90 −4.29%) · haut méd +0.92% · range méd 3.56%
- Excursion ouverture 30min (n=160) : bas méd −2.27% (p90 −4.81%) · haut méd +1.03% · range méd 3.78%
- Excursion ouverture 60min (n=160) : bas méd −2.58% (p90 −4.96%) · haut méd +1.06% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 714000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 72% (102/153) · gap 30% · délai 0.0min · rebond 48% (50/102) (MFE +0.96%)
   - −1.0% : fill 30min 58% · séance 69% (96/153) · gap 19% · délai 0.2min · rebond 58% (56/96) (MFE +1.33%)
   - −1.5% : fill 30min 52% · séance 65% (87/153) · gap 15% · délai 0.6min · rebond 66% (56/87) (MFE +1.33%)
   - −2.0% : fill 30min 44% · séance 60% (80/153) · gap 11% · délai 1.1min · rebond 69% (56/80) (MFE +1.71%)
   - −3.0% : fill 30min 34% · séance 49% (64/153) · gap 8% · délai 3.4min · rebond 74% (48/64) (MFE +1.86%)
   - −4.0% : fill 30min 23% · séance 40% (50/153) · gap 5% · délai 15.8min · rebond 74% (35/50) (MFE +1.89%)
   - −5.0% : fill 30min 16% · séance 32% (40/153) · gap 3% · délai 20.1min · rebond 78% (30/40) (MFE +2.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −3.69%) → stop au-delà de −2.59% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −3.14%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −4.43%) → stop au-delà de −3.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=834 jambes) : jambe baissière méd −1.22% (p90 −3.26%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 100% (46/46) · rebond 45% (22/46)
      · −2.0% : fill 98% (43/46) · rebond 64% (27/43)
      · −3.0% : fill 89% (38/46) · rebond 74% (27/38)
      · −4.0% : fill 77% (32/46) · rebond 72% (22/32)
      · −5.0% : fill 62% (26/46) · rebond 84% (21/26)
   - **flat** (18 séances) :
      · −1.0% : fill 96% (17/18) · rebond 74% (12/17)
      · −2.0% : fill 72% (13/18) · rebond 74% (11/13)
      · −3.0% : fill 56% (11/18) · rebond 51% (8/11)
      · −4.0% : fill 49% (8/18) · rebond 61% (4/8)
      · −5.0% : fill 49% (8/18) · rebond 73% (6/8)
   - **gap-up** (89 séances) :
      · −1.0% : fill 44% (33/89) · rebond 71% (22/33)
      · −2.0% : fill 32% (24/89) · rebond 77% (18/24)
      · −3.0% : fill 21% (15/89) · rebond 88% (13/15)
      · −4.0% : fill 14% (10/89) · rebond 92% (9/10)
      · −5.0% : fill 8% (6/89) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 34% en base · 45% si les 15 1res min sont vertes (65 cas) · 30% si rouges (95 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:18** → P(séance verte=clôture>ouverture) 71% si début vert vs 15% si rouge (base 34% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **71%** · continue >prix actuel 44% ; creux résiduel méd -1.8% (q20 -3.65%) → **SL/trailing à −3.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.57% / q75 +2.67% → **scale +1.57% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **15%** (continue à baisser 38%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.77%** (au-delà de la MAE q10 -4.77%), cible rebond +1.58% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.69% .. +2.7%] · haut q95 +4.28% · bas q05 -5.38%
   - 60min (n=160) : retour [-5.51% .. +2.57%] · haut q95 +4.49% · bas q05 -5.78%
   - 2h (n=160) : retour [-5.98% .. +3.62%] · haut q95 +4.84% · bas q05 -7.11%
   - 4h (n=160) : retour [-6.73% .. +3.28%] · haut q95 +5.06% · bas q05 -8.33%
   - 6h (n=160) : retour [-7.02% .. +4.47%] · haut q95 +5.93% · bas q05 -8.88%
   - session (n=160) : retour [-7.2% .. +4.67%] · haut q95 +6.0% · bas q05 -9.23%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.16 · part idiosyncratique 0.84
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.2  _(survente)_
- **ADX** : 11.5  _(pas de tendance nette)_
- **MACD** : hist -2683.69  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 14.8%
- **ATR** : 28500.0 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.164  _(distribution)_
- **Vol ratio** : 1.14  _(volume normal)_
- **Choppiness** : 52.8  _(transition)_
- **MA** : MA20 725450.0 · MA50 740171.06 · MA200 913120.09  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -8.0% · MA200 -25.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (552060 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

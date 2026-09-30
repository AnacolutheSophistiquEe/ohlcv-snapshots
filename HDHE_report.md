# 267260

**Generated** : 2026-09-30T21:57:39.024751+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩662000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩662000.00 (+5.0% vs entrée) · entrée ₩630771.14 · stop ₩580309.45 · T1 ₩644735.42 · R/R 0.28  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -529 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩628622.21–₩632920.07 (mid ₩630771.14)
- Spot actuel : ₩662000.00 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : ₩580309.45 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩644735.42 · R/R 0.28 | T2 ₩658699.71 · R/R 0.55 | T3 ₩672663.99 · R/R 0.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩580309.45


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.6 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.6 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.67 % | p01 -4.805 % | pire -11.715 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0648** [0.0351 ; 0.1088] _(largeur 7.4 pt, n_eff 173.1)_
   - swing : **0.489** [0.4366 ; 0.5416] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4509** [0.399 ; 0.5036] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 36.6 observations effectives », dont la borne haute a 95 % vaut environ 8.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.3 pt), swing (44.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.68 %** | CVaR **-8.85 %** | vol 4.43 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.67 % contre 4.91 % aujourd'hui, rapport 0.54)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.96 % vs -11.99 % si l'on extrapolait par √5 _(rapport 0.914 ; < 1 = le √5 surestime)_
- **β de baisse : 1.034** (β de hausse 0.8409, asymétrie 1.2297) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.103 | EV/share : ₩-5180.475 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 15 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.6 | bear 7.3 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.717% → cible +2.214% / stop −8.0%, p_fill 30%, n_eff≈36.6) : P(cible|rempli) **48%** · **EV/risk +0.013** (×p_fill ; si rempli +0.36% du capital)
  - **swing** (entrée dip −10.381% → cible +5.263% / stop −4.707%, p_fill 14%, n_eff≈16.8) : P(cible|rempli) **40%** · **EV/risk -0.011** (×p_fill ; si rempli -0.38% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=14))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→64% · +2.0%→43% · +3.0%→30% · +5.0%→10% · +8.0%→3%
- Range intraday médian 5.43% (p90 9.76%) · excursion haute méd. +1.59% / basse méd. −3.14%
- Profil de vol intra : ouverture 3.873% vs midi 1.054% vs clôture 1.132% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 83% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.089)_ ; drift intra méd. -0.685% ; recovery-V 22%
- **σ réalisé intraday** 3.174% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 63% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 672975.0 (VA 672625.0–677525.0 ; dernier close 680000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 73% · **stop −4.39%** sous le fill (sous le bruit) · cible +2.19% · R/R 0.5 (high win-rate)
- Gaps overnight (n=152) : méd. 0.71% · baisse 37% (gap-down >1% 21% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −1.5% (p90 −3.67%) · haut méd +0.73% · range méd 2.55%
- Excursion ouverture 15min (n=160) : bas méd −1.66% (p90 −3.98%) · haut méd +0.86% · range méd 3.08%
- Excursion ouverture 30min (n=160) : bas méd −1.86% (p90 −4.65%) · haut méd +0.95% · range méd 3.27%
- Excursion ouverture 60min (n=160) : bas méd −1.95% (p90 −4.81%) · haut méd +1.06% · range méd 3.66%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 681000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 72% (102/152) · gap 32% · délai 0.0min · rebond 48% (48/102) (MFE +0.95%)
   - −1.0% : fill 30min 56% · séance 66% (95/152) · gap 21% · délai 0.0min · rebond 56% (53/95) (MFE +1.28%)
   - −1.5% : fill 30min 50% · séance 63% (88/152) · gap 19% · délai 0.4min · rebond 62% (54/88) (MFE +1.26%)
   - −2.0% : fill 30min 42% · séance 56% (80/152) · gap 13% · délai 1.1min · rebond 68% (54/80) (MFE +1.69%)
   - −3.0% : fill 30min 34% · séance 48% (67/152) · gap 8% · délai 3.1min · rebond 72% (49/67) (MFE +1.84%)
   - −4.0% : fill 30min 21% · séance 36% (52/152) · gap 4% · délai 8.8min · rebond 73% (37/52) (MFE +1.72%)
   - −5.0% : fill 30min 13% · séance 26% (40/152) · gap 2% · délai 37.1min · rebond 73% (29/40) (MFE +2.19%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.92% (p90 −3.14%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.98% (p90 −3.02%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −3.95%) → stop au-delà de −3.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=832 jambes) : jambe baissière méd −1.16% (p90 −3.12%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 100% (50/50) · rebond 48% (25/50)
      · −2.0% : fill 99% (47/50) · rebond 62% (29/47)
      · −3.0% : fill 92% (43/50) · rebond 75% (31/43)
      · −4.0% : fill 68% (34/50) · rebond 75% (24/34)
      · −5.0% : fill 52% (27/50) · rebond 76% (21/27)
   - **flat** (15 séances) :
      · −1.0% : fill 97% (14/15) · rebond 78% (9/14)
      · −2.0% : fill 59% (10/15) · rebond 72% (8/10)
      · −3.0% : fill 45% (8/15) · rebond 48% (5/8)
      · −4.0% : fill 42% (7/15) · rebond 63% (4/7)
      · −5.0% : fill 42% (7/15) · rebond 72% (5/7)
   - **gap-up** (87 séances) :
      · −1.0% : fill 39% (31/87) · rebond 59% (19/31)
      · −2.0% : fill 28% (23/87) · rebond 79% (17/23)
      · −3.0% : fill 19% (16/87) · rebond 75% (13/16)
      · −4.0% : fill 13% (11/87) · rebond 72% (9/11)
      · −5.0% : fill 6% (6/87) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 33% en base · 45% si les 15 1res min sont vertes (62 cas) · 28% si rouges (98 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:30** → P(séance verte=clôture>ouverture) 78% si début vert vs 13% si rouge (base 33% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **78%** · continue >prix actuel 50% ; creux résiduel méd -1.39% (q20 -3.37%) → **SL/trailing à −3.37%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.87% / q75 +2.8% → **scale +1.87% / runner +2.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=98) : edge inversé — récupère vert seulement **13%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.28%** (au-delà de la MAE q10 -4.28%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.39% .. +2.67%] · haut q95 +3.84% · bas q05 -5.14%
   - 60min (n=160) : retour [-5.27% .. +2.49%] · haut q95 +4.33% · bas q05 -5.71%
   - 2h (n=160) : retour [-5.7% .. +3.49%] · haut q95 +4.64% · bas q05 -6.48%
   - 4h (n=160) : retour [-6.44% .. +3.61%] · haut q95 +4.79% · bas q05 -7.93%
   - 6h (n=160) : retour [-6.8% .. +4.7%] · haut q95 +5.44% · bas q05 -8.6%
   - session (n=160) : retour [-6.59% .. +4.67%] · haut q95 +5.76% · bas q05 -8.79%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
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

- **RSI** : 29.9  _(survente)_
- **ADX** : 12.4  _(pas de tendance nette)_
- **MACD** : hist -4303.244  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 15.0%
- **ATR** : 27928.57 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.265  _(distribution)_
- **Vol ratio** : 3.25  _(volume au-dessus de la moyenne)_
- **Choppiness** : 49.5  _(transition)_
- **MA** : MA20 719500.0 · MA50 737498.19 · MA200 912360.94  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -10.2% · MA200 -27.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (549371 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# 326030

**Generated** : 2026-10-01T00:21:56.559515+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩74400.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩74400.00 (+3.1% vs entrée) · entrée ₩72171.43 · stop ₩66397.71 · T1 ₩73285.71 · R/R 0.19  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -21 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩72047.07–₩72295.79 (mid ₩72171.43)
- Spot actuel : ₩74400.00 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : ₩66397.71 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩73285.71 · R/R 0.19 | T2 ₩74400.00 · R/R 0.39 | T3 ₩75514.29 · R/R 0.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩66397.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.07 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.99 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 8.99 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.578 % | p01 -3.015 % | pire -5.539 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0058** [0.0006 ; 0.0267] _(largeur 2.6 pt, n_eff 173.1)_
   - swing : **0.5346** [0.4819 ; 0.5867] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5399** [0.4872 ; 0.5919] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 31.5 observations effectives », dont la borne haute a 95 % vaut environ 9.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.18 %** | CVaR **-6.25 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.79 % contre 3.01 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.18 % vs -8.8 % si l'on extrapolait par √5 _(rapport 0.93 ; < 1 = le √5 surestime)_
- **β de baisse : 0.603** (β de hausse 0.4331, asymétrie 1.3924) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.033 | EV/share : ₩-189.384 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 23 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 69.5 | side 25.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.0% → cible +1.544% / stop −8.0%, p_fill 28%, n_eff≈31.5) : P(cible|rempli) **39%** · **EV/risk +0.009** (×p_fill ; si rempli +0.26% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=14))
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→61% · +2.0%→39% · +3.0%→24% · +5.0%→8% · +8.0%→4%
- Range intraday médian 3.93% (p90 7.06%) · excursion haute méd. +1.42% / basse méd. −2.05%
- Profil de vol intra : ouverture 2.626% vs midi 0.81% vs clôture 0.837% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 60% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.141)_ ; drift intra méd. -0.311% ; recovery-V 20%
- **σ réalisé intraday** 2.466% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 60% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 74298.75 (VA 73826.25–74508.75 ; dernier close 74900.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 70% · **stop −3.57%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.36 (high win-rate)
- Gaps overnight (n=152) : méd. 0.0% · baisse 46% (gap-down >1% 20% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −2.24%) · haut méd +0.5% · range méd 1.55%
- Excursion ouverture 15min (n=160) : bas méd −1.05% (p90 −2.75%) · haut méd +0.57% · range méd 1.95%
- Excursion ouverture 30min (n=160) : bas méd −1.11% (p90 −2.85%) · haut méd +0.63% · range méd 2.36%
- Excursion ouverture 60min (n=160) : bas méd −1.16% (p90 −2.96%) · haut méd +0.89% · range méd 2.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 74900.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 81% (116/152) · gap 32% · délai 0.0min · rebond 43% (47/116) (MFE +0.83%)
   - −1.0% : fill 30min 52% · séance 72% (105/152) · gap 20% · délai 1.0min · rebond 50% (49/105) (MFE +0.92%)
   - −1.5% : fill 30min 40% · séance 60% (84/152) · gap 10% · délai 2.7min · rebond 63% (48/84) (MFE +1.27%)
   - −2.0% : fill 30min 31% · séance 47% (66/152) · gap 5% · délai 5.1min · rebond 57% (36/66) (MFE +1.37%)
   - −3.0% : fill 30min 16% · séance 30% (45/152) · gap 4% · délai 24.9min · rebond 54% (23/45) (MFE +1.28%)
   - −4.0% : fill 30min 9% · séance 19% (31/152) · gap 3% · délai 50.1min · rebond 70% (20/31) (MFE +1.28%)
   - −5.0% : fill 30min 4% · séance 10% (17/152) · gap 1% · délai 74.1min · rebond 83% (11/17) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.45% (p90 −2.57%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −1.78%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.46%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=575 jambes) : jambe baissière méd −1.02% (p90 −2.38%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 91% (52/55) · rebond 60% (29/52)
      · −2.0% : fill 68% (38/55) · rebond 66% (22/38)
      · −3.0% : fill 49% (28/55) · rebond 56% (16/28)
      · −4.0% : fill 34% (21/55) · rebond 63% (13/21)
      · −5.0% : fill 17% (11/55) · rebond 84% (7/11)
   - **flat** (35 séances) :
      · −1.0% : fill 80% (27/35) · rebond 32% (8/27)
      · −2.0% : fill 53% (17/35) · rebond 48% (9/17)
      · −3.0% : fill 36% (12/35) · rebond 37% (3/12)
      · −4.0% : fill 25% (9/35) · rebond 81% (6/9)
      · −5.0% : fill 14% (6/35) · rebond 80% (4/6)
   - **gap-up** (62 séances) :
      · −1.0% : fill 48% (26/62) · rebond 47% (12/26)
      · −2.0% : fill 22% (11/62) · rebond 39% (5/11)
      · −3.0% : fill 8% (5/62) · rebond 87% (4/5)
      · −4.0% : fill 1% (1/62) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/62) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 69% si les 15 1res min sont vertes (60 cas) · 19% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 76% si début vert vs 16% si rouge (base 38% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 192min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **76%** · continue >prix actuel 61% ; creux résiduel méd -1.24% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.79% / q75 +2.39% → **scale +1.79% / runner +2.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=99) : edge inversé — récupère vert seulement **16%** (continue à baisser 52%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.99%** (au-delà de la MAE q10 -2.99%), cible rebond +1.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.59% .. +2.38%] · haut q95 +3.49% · bas q05 -3.55%
   - 60min (n=160) : retour [-2.86% .. +3.56%] · haut q95 +4.3% · bas q05 -3.82%
   - 2h (n=160) : retour [-3.19% .. +3.48%] · haut q95 +4.5% · bas q05 -3.99%
   - 4h (n=160) : retour [-3.32% .. +4.01%] · haut q95 +5.92% · bas q05 -4.57%
   - 6h (n=160) : retour [-4.19% .. +4.22%] · haut q95 +6.33% · bas q05 -5.09%
   - session (n=160) : retour [-4.18% .. +4.19%] · haut q95 +6.33% · bas q05 -5.09%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **volatil sans tendance propre (choppy)** (vol intra méd 2.62%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.1 · part idiosyncratique 0.9
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 15.6  _(survente)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -631.063  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 22.1%
- **ATR** : 2228.57 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.171  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 41.6  _(transition)_
- **MA** : MA20 80565.0 · MA50 82284.0 · MA200 98976.0  _(prix < MA20)_
- **Dist MA** : MA20 -7.7% · MA50 -9.6% · MA200 -24.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (547945 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

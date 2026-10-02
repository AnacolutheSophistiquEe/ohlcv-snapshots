# 326030

**Generated** : 2026-10-02T00:21:36.836910+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩76700.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot ₩76700.00 (+0.7% vs entrée) · entrée ₩76200.00 · stop ₩70104.00 · T1 ₩77332.14 · R/R 0.19  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩76058.83–₩76341.17 (mid ₩76200.00)
- Spot actuel : ₩76700.00 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : ₩70104.00 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩77332.14 · R/R 0.19 | T2 ₩78464.29 · R/R 0.37 | T3 ₩79596.43 · R/R 0.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩70104.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.07 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.39 %)** : le gap seul le franchit 0.493 % des séances (6 fois sur 1218).
   - exécution **0.669 pt plus bas** dans le cas TYPIQUE (médiane), 1.102 au p90, **1.149 au pire**
   - perte réelle **5.119 %** en moyenne _(tirée par la queue)_, jusqu'à **5.539 %** — au lieu des 4.39 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0036 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.578 % | p01 -3.015 % | pire -5.539 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0057** [0.0006 ; 0.0265] _(largeur 2.6 pt, n_eff 173.1)_
   - swing : **0.5414** [0.4887 ; 0.5934] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5512** [0.4985 ; 0.603] _(largeur 10.5 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.18 %** | CVaR **-6.25 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.80 % contre 3.02 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.18 % vs -8.65 % si l'on extrapolait par √5 _(rapport 0.946 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6011** (β de hausse 0.4331, asymétrie 1.3881) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : ₩-189.092 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 24 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 14.5 | side 80.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.652% → cible +1.486% / stop −8.0%, p_fill 81%, n_eff≈86.4) : P(cible|rempli) **45%** · **EV/risk -0.016** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −1.438% → cible +3.349% / stop −2.995%, p_fill 75%, n_eff≈86.6) : P(cible|rempli) **37%** · **EV/risk -0.140** (×p_fill ; si rempli -0.56% du capital)
  - **deep** (entrée dip −2.212% → cible +4.774% / stop −4.529%, p_fill 74%, n_eff≈82.3) : P(cible|rempli) **42%** · **EV/risk -0.094** (×p_fill ; si rempli -0.57% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→61% · +2.0%→39% · +3.0%→24% · +5.0%→8% · +8.0%→4%
- Range intraday médian 3.9% (p90 6.9%) · excursion haute méd. +1.42% / basse méd. −2.03%
- Profil de vol intra : ouverture 2.594% vs midi 0.808% vs clôture 0.834% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑1%/↓1% ; spike-down 58% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.148)_ ; drift intra méd. -0.339% ; recovery-V 18%
- **σ réalisé intraday** 2.42% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 62% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 75015.0 (VA 74805.0–75585.0 ; dernier close 74700.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 70% · **stop −3.57%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.36 (high win-rate)
- Gaps overnight (n=152) : méd. 0.0% · baisse 45% (gap-down >1% 20% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −2.22%) · haut méd +0.47% · range méd 1.52%
- Excursion ouverture 15min (n=160) : bas méd −1.02% (p90 −2.73%) · haut méd +0.54% · range méd 1.9%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −2.82%) · haut méd +0.6% · range méd 2.35%
- Excursion ouverture 60min (n=160) : bas méd −1.16% (p90 −2.95%) · haut méd +0.86% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 74400.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (117/152) · gap 31% · délai 0.0min · rebond 42% (47/117) (MFE +0.8%)
   - −1.0% : fill 30min 51% · séance 71% (105/152) · gap 20% · délai 1.0min · rebond 50% (49/105) (MFE +0.92%)
   - −1.5% : fill 30min 39% · séance 59% (84/152) · gap 10% · délai 2.7min · rebond 63% (48/84) (MFE +1.27%)
   - −2.0% : fill 30min 31% · séance 46% (66/152) · gap 5% · délai 5.1min · rebond 57% (36/66) (MFE +1.37%)
   - −3.0% : fill 30min 16% · séance 30% (45/152) · gap 4% · délai 24.9min · rebond 54% (23/45) (MFE +1.28%)
   - −4.0% : fill 30min 9% · séance 19% (31/152) · gap 3% · délai 50.1min · rebond 70% (20/31) (MFE +1.28%)
   - −5.0% : fill 30min 4% · séance 10% (17/152) · gap 1% · délai 74.1min · rebond 83% (11/17) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.45% (p90 −2.57%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −1.78%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.46%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=572 jambes) : jambe baissière méd −1.02% (p90 −2.38%) · ~8.0 jambes/séance
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
      · −1.0% : fill 46% (26/62) · rebond 47% (12/26)
      · −2.0% : fill 21% (11/62) · rebond 39% (5/11)
      · −3.0% : fill 7% (5/62) · rebond 87% (4/5)
      · −4.0% : fill 1% (1/62) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/62) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 37% en base · 69% si les 15 1res min sont vertes (60 cas) · 18% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 76% si début vert vs 16% si rouge (base 37% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 192min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **76%** · continue >prix actuel 61% ; creux résiduel méd -1.24% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.79% / q75 +2.39% → **scale +1.79% / runner +2.39%**, sortie à la clôture
  - **si ROUGE au coude** (n=99) : edge inversé — récupère vert seulement **16%** (continue à baisser 54%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.96%** (au-delà de la MAE q10 -2.96%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.58% .. +2.35%] · haut q95 +3.46% · bas q05 -3.52%
   - 60min (n=160) : retour [-2.85% .. +3.54%] · haut q95 +4.3% · bas q05 -3.79%
   - 2h (n=160) : retour [-3.19% .. +3.47%] · haut q95 +4.49% · bas q05 -3.97%
   - 4h (n=160) : retour [-3.31% .. +3.98%] · haut q95 +5.88% · bas q05 -4.54%
   - 6h (n=160) : retour [-3.9% .. +4.21%] · haut q95 +6.24% · bas q05 -5.04%
   - session (n=160) : retour [-4.05% .. +4.16%] · haut q95 +6.24% · bas q05 -5.04%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.6%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.09 · part idiosyncratique 0.92
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.5  _(survente)_
- **ADX** : 19.4  _(pas de tendance nette)_
- **MACD** : hist -411.421  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 20.3%
- **ATR** : 2264.29 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.139  _(distribution)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 43.3  _(transition)_
- **MA** : MA20 79950.0 · MA50 82282.0 · MA200 98678.0  _(prix < MA20)_
- **Dist MA** : MA20 -4.1% · MA50 -6.8% · MA200 -22.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (548065 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

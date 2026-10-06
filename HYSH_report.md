# 298040

**Generated** : 2026-10-06T21:58:13.066471+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩2807000.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (1 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩2807000.00 (+2.1% vs entrée) · entrée ₩2750600.03 · stop ₩2530552.03 · T1 ₩2803600.03 · R/R 0.24  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2741489.95–₩2759710.12 (mid ₩2750600.03)
- Spot actuel : ₩2807000.00 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : ₩2530552.03 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩2803600.03 · R/R 0.24 | T2 ₩2856600.03 · R/R 0.48 | T3 ₩2909600.03 · R/R 0.72
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2530552.03


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.20 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.2 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1219).
   - exécution **3.486 pt plus bas** dans le cas TYPIQUE (médiane), 3.486 au p90, **3.486 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 8.2 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0029 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.475 % | p01 -4.657 % | pire -11.686 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0602** [0.0318 ; 0.1031] _(largeur 7.1 pt, n_eff 173.1)_
   - swing : **0.5131** [0.4605 ; 0.5655] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4797** [0.4274 ; 0.5324] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : deep (25.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.94 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.50 % contre 5.62 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.96 % vs -12.54 % si l'on extrapolait par √5 _(rapport 0.954 ; < 1 = le √5 surestime)_
- **β de baisse : 1.073** (β de hausse 0.9983, asymétrie 1.0748) vs KS11 — 552 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.079 | EV/share : ₩-17293.248 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 25 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 8.1 | side 6.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.011% → cible +1.927% / stop −8.0%, p_fill 62%, n_eff≈72.7) : P(cible|rempli) **48%** · **EV/risk -0.049** (×p_fill ; si rempli -0.62% du capital)
  - **swing** (entrée dip −4.424% → cible +4.417% / stop −3.951%, p_fill 52%, n_eff≈61.1) : P(cible|rempli) **39%** · **EV/risk -0.084** (×p_fill ; si rempli -0.65% du capital)
  - **deep** (entrée dip −6.829% → cible +14.814% / stop −7.407%, p_fill 46%, n_eff≈51.9) : P(cible|rempli) **19%** · **EV/risk -0.117** (×p_fill ; si rempli -1.89% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→62% · +2.0%→50% · +3.0%→34% · +5.0%→18% · +8.0%→5%
- Range intraday médian 5.73% (p90 9.57%) · excursion haute méd. +2.0% / basse méd. −3.17%
- Profil de vol intra : ouverture 3.913% vs midi 1.01% vs clôture 1.04% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.063)_ ; drift intra méd. -0.579% ; recovery-V 31%
- **σ réalisé intraday** 3.027% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 53% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 2780512.5 (VA 2771912.5–2785887.5 ; dernier close 2781000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 75% · **stop −4.27%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.52 (high win-rate)
- Gaps overnight (n=152) : méd. 0.43% · baisse 36% (gap-down >1% 22% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −1.32% (p90 −2.87%) · haut méd +0.5% · range méd 2.09%
- Excursion ouverture 15min (n=160) : bas méd −1.78% (p90 −3.74%) · haut méd +0.76% · range méd 2.7%
- Excursion ouverture 30min (n=160) : bas méd −1.93% (p90 −4.19%) · haut méd +0.81% · range méd 3.1%
- Excursion ouverture 60min (n=160) : bas méd −2.17% (p90 −4.71%) · haut méd +1.01% · range méd 3.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2785000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 71% (101/152) · gap 32% · délai 0.0min · rebond 54% (56/101) (MFE +1.15%)
   - −1.0% : fill 30min 55% · séance 65% (93/152) · gap 22% · délai 0.2min · rebond 47% (47/93) (MFE +0.9%)
   - −1.5% : fill 30min 47% · séance 56% (83/152) · gap 19% · délai 1.4min · rebond 54% (46/83) (MFE +1.09%)
   - −2.0% : fill 30min 43% · séance 53% (77/152) · gap 16% · délai 3.6min · rebond 53% (39/77) (MFE +1.08%)
   - −3.0% : fill 30min 29% · séance 41% (62/152) · gap 9% · délai 7.5min · rebond 65% (39/62) (MFE +1.57%)
   - −4.0% : fill 30min 20% · séance 34% (54/152) · gap 5% · délai 21.6min · rebond 67% (39/54) (MFE +2.23%)
   - −5.0% : fill 30min 12% · séance 26% (41/152) · gap 3% · délai 57.8min · rebond 75% (30/41) (MFE +2.24%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.81%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.51%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −2.46%) → stop au-delà de −1.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=821 jambes) : jambe baissière méd −1.34% (p90 −3.28%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 95% (46/47) · rebond 36% (21/46)
      · −2.0% : fill 91% (42/47) · rebond 49% (20/42)
      · −3.0% : fill 80% (39/47) · rebond 65% (24/39)
      · −4.0% : fill 70% (35/47) · rebond 69% (24/35)
      · −5.0% : fill 51% (27/47) · rebond 83% (21/27)
   - **flat** (21 séances) :
      · −1.0% : fill 87% (17/21) · rebond 55% (10/17)
      · −2.0% : fill 48% (13/21) · rebond 31% (5/13)
      · −3.0% : fill 26% (8/21) · rebond 57% (5/8)
      · −4.0% : fill 26% (8/21) · rebond 54% (6/8)
      · −5.0% : fill 20% (4/21) · rebond 40% (2/4)
   - **gap-up** (84 séances) :
      · −1.0% : fill 39% (30/84) · rebond 60% (16/30)
      · −2.0% : fill 28% (22/84) · rebond 72% (14/22)
      · −3.0% : fill 18% (15/84) · rebond 66% (10/15)
      · −4.0% : fill 13% (11/84) · rebond 66% (9/11)
      · −5.0% : fill 10% (10/84) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 56% si les 15 1res min sont vertes (57 cas) · 32% si rouges (103 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 73% si début vert vs 21% si rouge (base 40% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **73%** · continue >prix actuel 40% ; creux résiduel méd -1.69% (q20 -3.42%) → **SL/trailing à −3.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.48% / q75 +2.94% → **scale +1.48% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=98) : edge inversé — récupère vert seulement **21%** (continue à baisser 52%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.35%** (au-delà de la MAE q10 -5.35%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.56% .. +3.86%] · haut q95 +5.86% · bas q05 -4.99%
   - 60min (n=160) : retour [-4.72% .. +3.18%] · haut q95 +5.91% · bas q05 -5.39%
   - 2h (n=160) : retour [-5.32% .. +3.61%] · haut q95 +6.1% · bas q05 -6.27%
   - 4h (n=160) : retour [-6.37% .. +4.53%] · haut q95 +6.12% · bas q05 -7.87%
   - 6h (n=160) : retour [-7.14% .. +5.0%] · haut q95 +6.31% · bas q05 -8.46%
   - session (n=160) : retour [-6.47% .. +5.32%] · haut q95 +6.31% · bas q05 -8.59%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.11 · part idiosyncratique 0.89
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 46.6  _(neutre)_
- **ADX** : 7.0  _(pas de tendance nette)_
- **MACD** : hist -6996.352  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 10.0%
- **ATR** : 106000.0 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.013  _(neutre)_
- **Vol ratio** : 1.02  _(volume normal)_
- **Choppiness** : 57.1  _(transition)_
- **MA** : MA20 2838300.0 · MA50 2785940.0 · MA200 2841833.61  _(prix < MA20)_
- **Dist MA** : MA20 -1.1% · MA50 +0.8% · MA200 -1.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (233229 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

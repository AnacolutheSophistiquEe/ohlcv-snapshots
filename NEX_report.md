# NEX

**Generated** : 2026-08-20T21:43:39.244156+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €138.50  

> 🟡 **WAIT-FOR-DIP** — spot +2.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €138.50 (+2.4% vs entrée) · entrée €135.29 · stop €124.46 · T1 €137.02 · R/R 0.16  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk 0.006 _(réel 5 s)_ (GBM -0.056) · ¼-Kelly 0.071 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €134.94–€135.63 (mid €135.29)
- Spot actuel : €138.50 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : €124.46 (stop swing_plan-based (-8.23%))
- Targets : T1 €137.02 · R/R 0.16 | T2 €138.76 · R/R 0.32 | T3 €140.49 · R/R 0.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €124.46


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.64 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.23 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1279).
   - exécution **0.123 pt plus bas** dans le cas TYPIQUE (médiane), 1.117 au p90, **1.366 au pire**
   - perte réelle **8.739 %** en moyenne _(tirée par la queue)_, jusqu'à **9.596 %** — au lieu des 8.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0012 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.516 % | p01 -3.644 % | pire -9.596 % _(sur 1279 séances)_
- **P(stop avant cible)** _(source : daily, 1280 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0054** [0.0005 ; 0.026] _(largeur 2.5 pt, n_eff 173.1)_
   - swing : **0.2842** [0.2386 ; 0.3334] _(largeur 9.5 pt, n_eff 345.8)_
   - deep : **0.4373** [0.3857 ; 0.4899] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.0 observations effectives », dont la borne haute a 95 % vaut environ 18.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-3.51 %** | CVaR **-5.25 %** | vol 2.3 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.51 % vs -7.85 % si l'on extrapolait par √5 _(rapport 0.957 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0172** (β de hausse 1.0877, asymétrie 0.9351) vs FCHI — 617 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.056 | EV/share : €-0.609 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 18 % | T3 6 %
- Kelly (position) : f* 0.283 | ¼-Kelly 0.071 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 25.8 | bear 47.5 | side 26.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 277.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.315% → cible +1.282% / stop −8.0%, p_fill 37%, n_eff≈16.0) : P(cible|rempli) **37%** · **EV/risk +0.006** (×p_fill ; si rempli +0.13% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=10, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→64% · +1.0%→51% · +2.0%→25% · +3.0%→11% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.03% (p90 4.84%) · excursion haute méd. +1.03% / basse méd. −1.43%
- Profil de vol intra : ouverture 1.78% vs midi 0.531% vs clôture 0.732% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.56% ; recovery-V 11%
- **σ réalisé intraday** 2.134% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 73% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 137.9237 (VA 137.4162–138.2862 ; dernier close 138.35)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 57% · **stop −1.95%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.79 (high win-rate)
- Gaps overnight (n=157) : méd. 0.27% · baisse 35% (gap-down >1% 8% · >2% 2%)
- Excursion ouverture 5min (n=158) : bas méd −0.45% (p90 −1.94%) · haut méd +0.29% · range méd 1.06%
- Excursion ouverture 15min (n=158) : bas méd −0.59% (p90 −2.13%) · haut méd +0.38% · range méd 1.3%
- Excursion ouverture 30min (n=158) : bas méd −0.63% (p90 −2.31%) · haut méd +0.46% · range méd 1.41%
- Excursion ouverture 60min (n=158) : bas méd −0.86% (p90 −2.58%) · haut méd +0.59% · range méd 1.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 138.35 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 72% (112/157) · gap 20% · délai 0.5min · rebond 47% (55/112) (MFE +0.87%)
   - −1.0% : fill 30min 36% · séance 61% (93/157) · gap 8% · délai 10.8min · rebond 44% (43/93) (MFE +0.74%)
   - −1.5% : fill 30min 22% · séance 49% (70/157) · gap 2% · délai 32.5min · rebond 54% (35/70) (MFE +1.03%)
   - −2.0% : fill 30min 13% · séance 33% (51/157) · gap 2% · délai 66.6min · rebond 49% (27/51) (MFE +1.0%)
   - −3.0% : fill 30min 4% · séance 20% (31/157) · gap 1% · délai 115.7min · rebond 57% (18/31) (MFE +1.55%)
   - −4.0% : fill 30min 1% · séance 7% (11/157) · gap 0% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 0% · séance 2% (4/157) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.24%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.14% (p90 −1.44%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −0.6%) → stop au-delà de −0.49% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=329 jambes) : jambe baissière méd −1.09% (p90 −2.42%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 76% (37/46) · rebond 40% (15/37)
      · −2.0% : fill 39% (25/46) · rebond 43% (13/25)
      · −3.0% : fill 27% (16/46) · rebond 47% (9/16)
      · −4.0% : fill 13% (7/46) · rebond 28% (3/7)
      · −5.0% : fill 7% (4/46) · rebond 89% (3/4)
   - **flat** (38 séances) :
      · −1.0% : fill 68% (25/38) · rebond 44% (13/25)
      · −2.0% : fill 42% (13/38) · rebond 58% (7/13)
      · −3.0% : fill 26% (8/38) · rebond 46% (3/8)
      · −4.0% : fill 9% (2/38) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/38) · rebond 0% (0/0)
   - **gap-up** (73 séances) :
      · −1.0% : fill 50% (31/73) · rebond 47% (15/31)
      · −2.0% : fill 24% (13/73) · rebond 45% (7/13)
      · −3.0% : fill 13% (7/73) · rebond 82% (6/7)
      · −4.0% : fill 3% (2/73) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/73) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 44% en base · 65% si les 15 1res min sont vertes (84 cas) · 20% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=158) : COUDE à **29min** → P(séance verte=clôture>ouverture) 72% si début vert vs 20% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 249min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 48% ; creux résiduel méd -0.95% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.97% / q75 +1.59% → **scale +0.97% / runner +1.59%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.21%** (au-delà de la MAE q10 -3.21%), cible rebond +0.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-2.02% .. +2.32%] · haut q95 +2.64% · bas q05 -2.59%
   - 60min (n=158) : retour [-2.82% .. +2.58%] · haut q95 +2.88% · bas q05 -3.24%
   - 2h (n=158) : retour [-3.56% .. +2.4%] · haut q95 +2.94% · bas q05 -3.74%
   - 4h (n=158) : retour [-3.2% .. +2.54%] · haut q95 +3.14% · bas q05 -3.9%
   - 6h (n=158) : retour [-3.81% .. +3.51%] · haut q95 +3.99% · bas q05 -4.17%
   - session (n=158) : retour [-3.53% .. +2.92%] · haut q95 +4.18% · bas q05 -4.69%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 60.7  _(momentum haussier)_
- **ADX** : 18.4  _(pas de tendance nette)_
- **MACD** : hist 0.546  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 15.8%
- **ATR** : 4.34 (57.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.173  _(distribution)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 46.3  _(transition)_
- **MA** : MA20 136.02 · MA50 139.64 · MA200 132.92  _(prix > MA20)_
- **Dist MA** : MA20 +1.8% · MA50 -0.8% · MA200 +4.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (600661 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

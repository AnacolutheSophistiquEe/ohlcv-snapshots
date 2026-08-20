# SOFI

**Generated** : 2026-08-20T20:23:31.060580+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.92  

> 🟡 **WAIT-FOR-DIP** — spot +6.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $17.92 (+6.5% vs entrée) · entrée $16.82 · stop $15.61 · T1 $19.25 · R/R 2.01  
> ↳ P(T1 av. stop) 12 % · EV/risk 0.036 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.65–$16.99 (mid $16.82)
- Spot actuel : $17.92 (+6.5% au-dessus de la zone — repli à attendre)
- Stop : $15.61 (stop swing_plan-based (-12.92%))
- Targets : T1 $19.25 · R/R 2.01 | T2 $19.31 · R/R 2.06 | T3 $19.38 · R/R 2.12
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.61


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.98 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.92 %)** : le gap seul le franchit 0.0 % des séances ; quand il le franchit, l'exécution est **0.0 points plus bas** → perte réelle **— %** _(et non 12.92 %)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.267 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0826** [0.0484 ; 0.1306] _(largeur 8.2 pt, n_eff 173.1)_
   - swing : **0.4597** [0.4077 ; 0.5124] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5605** [0.5079 ; 0.6121] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 15.1 observations effectives », dont la borne haute a 95 % vaut environ 19.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (18.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.46 %** | CVaR **-8.8 %** | vol 4.18 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.022 ; < 1 = le √5 surestime)_
- **β de baisse : 1.831** (β de hausse 1.6931, asymétrie 1.0815) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.284× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.114 | EV/share : $-0.139 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 8 % | T2 8 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 68.9 | bear 14.8 | side 16.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 502.0 (= 28 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.796% → cible +6.325% / stop −3.162%, p_fill 28%, n_eff≈15.1) : P(cible|rempli) **0%** · **EV/risk +0.038** (×p_fill ; si rempli +0.44% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=5))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→70% · +2.0%→49% · +3.0%→38% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.32% (p90 7.29%) · excursion haute méd. +1.9% / basse méd. −2.18%
- Profil de vol intra : ouverture 2.944% vs midi 0.9% vs clôture 1.003% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑2%/↓0% ; spike-down 64% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.055)_ ; drift intra méd. 0.118% ; recovery-V 18%
- **σ réalisé intraday** 2.665% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 18.3945 (VA 18.3525–18.6675 ; dernier close 18.43)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 72% · **stop −2.95%** sous le fill (sous le bruit) · cible +1.89% · R/R 0.64 (high win-rate)
- Gaps overnight (n=159) : méd. 0.3% · baisse 41% (gap-down >1% 25% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.66%) · haut méd +0.72% · range méd 1.59%
- Excursion ouverture 15min (n=160) : bas méd −0.99% (p90 −2.71%) · haut méd +0.96% · range méd 2.23%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −3.2%) · haut méd +1.13% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.39% (p90 −3.71%) · haut méd +1.24% · range méd 3.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.43 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (121/159) · gap 30% · délai 0.0min · rebond 51% (63/121) (MFE +1.06%)
   - −1.0% : fill 30min 52% · séance 64% (109/159) · gap 25% · délai 1.0min · rebond 59% (67/109) (MFE +1.22%)
   - −1.5% : fill 30min 43% · séance 61% (101/159) · gap 19% · délai 9.7min · rebond 70% (66/101) (MFE +1.48%)
   - −2.0% : fill 30min 35% · séance 48% (79/159) · gap 11% · délai 3.3min · rebond 72% (55/79) (MFE +1.89%)
   - −3.0% : fill 30min 15% · séance 33% (58/159) · gap 3% · délai 36.2min · rebond 63% (40/58) (MFE +1.44%)
   - −4.0% : fill 30min 9% · séance 19% (38/159) · gap 2% · délai 41.6min · rebond 58% (25/38) (MFE +1.51%)
   - −5.0% : fill 30min 4% · séance 7% (17/159) · gap 2% · délai 31.4min · rebond 40% (10/17) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.72%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.65%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.64%) → stop au-delà de −1.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=669 jambes) : jambe baissière méd −1.06% (p90 −2.75%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 58% (39/64)
      · −2.0% : fill 87% (55/65) · rebond 74% (40/55)
      · −3.0% : fill 70% (45/65) · rebond 68% (33/45)
      · −4.0% : fill 38% (29/65) · rebond 65% (21/29)
      · −5.0% : fill 19% (14/65) · rebond 38% (8/14)
   - **flat** (22 séances) :
      · −1.0% : fill 52% (12/22) · rebond 35% (5/12)
      · −2.0% : fill 42% (8/22) · rebond 71% (5/8)
      · −3.0% : fill 26% (5/22) · rebond 59% (3/5)
      · −4.0% : fill 11% (2/22) · rebond 72% (1/2)
      · −5.0% : fill 0% (0/22) · rebond 0% (0/0)
   - **gap-up** (72 séances) :
      · −1.0% : fill 42% (33/72) · rebond 68% (23/33)
      · −2.0% : fill 21% (16/72) · rebond 66% (10/16)
      · −3.0% : fill 9% (8/72) · rebond 39% (4/8)
      · −4.0% : fill 7% (7/72) · rebond 20% (3/7)
      · −5.0% : fill 1% (3/72) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 59% si les 15 1res min sont vertes (72 cas) · 26% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 78% si début vert vs 10% si rouge (base 41% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 56% ; creux résiduel méd -1.53% (q20 -2.7%) → **SL/trailing à −2.7%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +2.9% → **scale +1.91% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **10%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.91%** (au-delà de la MAE q10 -2.91%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.81% .. +3.57%] · haut q95 +3.88% · bas q05 -3.51%
   - 60min (n=160) : retour [-3.09% .. +3.39%] · haut q95 +4.03% · bas q05 -3.99%
   - 2h (n=160) : retour [-3.53% .. +3.7%] · haut q95 +4.61% · bas q05 -4.46%
   - 4h (n=160) : retour [-3.79% .. +4.64%] · haut q95 +5.69% · bas q05 -4.99%
   - 6h (n=160) : retour [-4.24% .. +4.17%] · haut q95 +5.87% · bas q05 -5.06%
   - session (n=160) : retour [-4.16% .. +5.28%] · haut q95 +6.14% · bas q05 -5.08%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 62.9  _(momentum haussier)_
- **ADX** : 14.4  _(pas de tendance nette)_
- **MACD** : hist 0.022  _(pas de croisement recent)_
- **BB** : %B 0.58 · largeur 21.2%
- **ATR** : 0.77 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.004  _(neutre)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 54.8  _(transition)_
- **MA** : MA20 17.63 · MA50 17.61 · MA200 20.57  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 +1.8% · MA200 -12.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (403021 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

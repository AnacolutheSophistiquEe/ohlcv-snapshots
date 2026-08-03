# 005930

**Generated** : 2026-08-03T00:12:45.776228+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩262500.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩262500.00 (+0.6% vs entrée) · entrée ₩260888.79 · stop ₩252782.37 · T1 ₩272988.26 · R/R 1.49  
> ↳ P(T1 av. stop) 18 % _(réel 5 s)_ · EV/risk -0.341 _(réel 5 s)_ (GBM -0.056) · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.11% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩259277.59–₩262500.00 (mid ₩260888.79)
- Spot actuel : ₩262500.00 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : ₩252782.37 (stop swing_plan-based (-11.48%))
- Targets : T1 ₩272988.26 · R/R 1.49 | T2 ₩285087.72 · R/R 2.99 | T3 ₩297187.19 · R/R 4.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩252782.37


## Edge, scénarios & sizing

- EV/risk : -0.056 | EV/share : ₩-454.327 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 20 % | T3 20 %
- Kelly (position) : f* 0.039 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.8 | bear 59.5 | side 33.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.612% → cible +4.638% / stop −3.107%, p_fill 89%, n_eff≈34.8) : P(cible|rempli) **18%** · **EV/risk -0.341** (×p_fill ; si rempli -1.20% du capital)
  - **swing** (entrée dip −1.186% → cible +10.37% / stop −10.418%, p_fill 87%, n_eff≈33.7) : P(cible|rempli) **25%** · **EV/risk -0.300** (×p_fill ; si rempli -3.62% du capital)
  - **deep** (entrée dip −1.62% → cible +14.666% / stop −15.695%, p_fill 85%, n_eff≈33.2) : P(cible|rempli) **16%** · **EV/risk -0.398** (×p_fill ; si rempli -7.40% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→68% · +2.0%→49% · +3.0%→34% · +5.0%→21% · +8.0%→5%
- Range intraday médian 5.86% (p90 9.84%) · excursion haute méd. +1.97% / basse méd. −2.72%
- Profil de vol intra : ouverture 2.942% vs midi 1.297% vs clôture 1.496% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑1%/↓1% ; spike-down 69% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.087)_ ; drift intra méd. -1.331% ; recovery-V 23%
- **σ réalisé intraday** 4.818% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 74% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 249300.0 (VA 245100.0–256500.0 ; dernier close 265000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 65% · **stop −6.89%** sous le fill (sous le bruit) · cible +1.51% · R/R 0.22 (high win-rate)
- Gaps overnight (n=144) : méd. 0.26% · baisse 44% (gap-down >1% 35% · >2% 24%)
- Excursion ouverture 5min (n=145) : bas méd −0.65% (p90 −1.62%) · haut méd +0.71% · range méd 1.52%
- Excursion ouverture 15min (n=145) : bas méd −0.95% (p90 −2.44%) · haut méd +1.08% · range méd 2.22%
- Excursion ouverture 30min (n=145) : bas méd −1.21% (p90 −3.09%) · haut méd +1.16% · range méd 2.82%
- Excursion ouverture 60min (n=145) : bas méd −1.6% (p90 −3.57%) · haut méd +1.36% · range méd 3.1%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 265000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 67% (90/144) · gap 37% · délai 0.0min · rebond 53% (49/90) (MFE +1.4%)
   - −1.0% : fill 30min 49% · séance 64% (84/144) · gap 35% · délai 0.0min · rebond 59% (48/84) (MFE +1.39%)
   - −1.5% : fill 30min 42% · séance 58% (74/144) · gap 25% · délai 0.3min · rebond 57% (44/74) (MFE +1.64%)
   - −2.0% : fill 30min 39% · séance 51% (65/144) · gap 24% · délai 0.5min · rebond 55% (37/65) (MFE +1.48%)
   - −3.0% : fill 30min 31% · séance 46% (56/144) · gap 20% · délai 2.7min · rebond 58% (36/56) (MFE +1.86%)
   - −4.0% : fill 30min 23% · séance 38% (44/144) · gap 14% · délai 23.1min · rebond 62% (30/44) (MFE +1.53%)
   - −5.0% : fill 30min 14% · séance 31% (34/144) · gap 9% · délai 79.3min · rebond 65% (23/34) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.38%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −3.15%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −4.24%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=664 jambes) : jambe baissière méd −1.31% (p90 −3.17%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 97% (58/61) · rebond 48% (30/58)
      · −2.0% : fill 89% (50/61) · rebond 44% (25/50)
      · −3.0% : fill 86% (45/61) · rebond 52% (28/45)
      · −4.0% : fill 76% (37/61) · rebond 55% (24/37)
      · −5.0% : fill 65% (29/61) · rebond 59% (18/29)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (70 séances) :
      · −1.0% : fill 39% (19/70) · rebond 79% (14/19)
      · −2.0% : fill 22% (11/70) · rebond 80% (9/11)
      · −3.0% : fill 15% (7/70) · rebond 70% (5/7)
      · −4.0% : fill 11% (5/70) · rebond 92% (4/5)
      · −5.0% : fill 6% (3/70) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 41% en base · 65% si les 15 1res min sont vertes (71 cas) · 19% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=145) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 83% si début vert vs 6% si rouge (base 41% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **83%** · continue >prix actuel 53% ; creux résiduel méd -1.67% (q20 -4.25%) → **SL/trailing à −4.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.48% → **scale +1.72% / runner +3.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=67) : edge inversé — récupère vert seulement **6%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.18%** (au-delà de la MAE q10 -7.18%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-2.63% .. +2.91%] · haut q95 +3.71% · bas q05 -3.64%
   - 60min (n=145) : retour [-3.13% .. +4.86%] · haut q95 +5.8% · bas q05 -5.13%
   - 2h (n=145) : retour [-5.1% .. +4.68%] · haut q95 +6.32% · bas q05 -5.77%
   - 4h (n=145) : retour [-6.64% .. +5.67%] · haut q95 +6.83% · bas q05 -8.17%
   - 6h (n=145) : retour [-7.42% .. +5.57%] · haut q95 +7.33% · bas q05 -8.66%
   - session (n=145) : retour [-7.58% .. +5.71%] · haut q95 +7.33% · bas q05 -9.22%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.1% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.87%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 45.4  _(neutre)_
- **ADX** : 27.7  _(tendance etablie)_
- **MACD** : hist -2250.816  _(pas de croisement recent)_
- **BB** : %B 0.5 · largeur 44.6%
- **ATR** : 27021.43 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.164  _(distribution)_
- **Vol ratio** : 1.82  _(volume au-dessus de la moyenne)_
- **Choppiness** : 49.2  _(transition)_
- **MA** : MA20 262550.0 · MA50 299323.45 · MA200 192686.17  _(prix < MA20)_
- **Dist MA** : MA20 -0.0% · MA50 -12.3% · MA200 +36.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82787 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

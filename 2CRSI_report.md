# AL2SI

**Generated** : 2026-07-20T21:45:30.792649+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 9.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €26.22  

> 🟡 **WAIT-FOR-DIP** — spot +5.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €26.22 (+5.7% vs entrée) · entrée €24.81 · stop €23.58 · T1 €26.06 · R/R 1.02  
> ↳ P(T1 av. stop) 26 % _(réel 5 s)_ · EV/risk 0.041 _(réel 5 s)_ (GBM -0.029) · ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.94% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €24.56–€25.06 (mid €24.81)
- Spot actuel : €26.22 (+5.7% au-dessus de la zone — repli à attendre)
- Stop : €23.58 (stop swing_plan-based (-16.84%))
- Targets : T1 €26.06 · R/R 1.02 | T2 €27.31 · R/R 2.03 | T3 €28.57 · R/R 3.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €23.58


## Edge, scénarios & sizing

- EV/risk : -0.029 | EV/share : €-0.035 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 37 % | T3 37 %
- Kelly (position) : f* 0.101 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.3 | bear 6.7 | side 77.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.385% → cible +5.05% / stop −4.941%, p_fill 63%, n_eff≈21.0) : P(cible|rempli) **26%** · **EV/risk +0.041** (×p_fill ; si rempli +0.33% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→74% · +3.0%→64% · +5.0%→41% · +8.0%→24%
- Range intraday médian 8.62% (p90 22.19%) · excursion haute méd. +4.16% / basse méd. −3.83%
- Profil de vol intra : ouverture 5.913% vs midi 1.754% vs clôture 1.991% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (151 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.144 ; mean-reverting — autocorr -0.045)_ ; drift intra méd. -0.209% ; recovery-V 27%
- **σ réalisé intraday** 8.498% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 71% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 23.6857 (VA 23.3693–25.9012 ; dernier close 26.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 46% · rebond 92% · **stop −6.56%** sous le fill (sous le bruit) · cible +3.1% · R/R 0.47 (high win-rate)
- Gaps overnight (n=150) : méd. 0.21% · baisse 41% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=151) : bas méd −1.24% (p90 −5.34%) · haut méd +1.03% · range méd 3.13%
- Excursion ouverture 15min (n=151) : bas méd −1.61% (p90 −5.86%) · haut méd +1.51% · range méd 4.49%
- Excursion ouverture 30min (n=151) : bas méd −1.75% (p90 −5.92%) · haut méd +2.05% · range méd 4.97%
- Excursion ouverture 60min (n=151) : bas méd −2.34% (p90 −6.98%) · haut méd +2.65% · range méd 6.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 26.26 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 82% (117/150) · gap 30% · délai 0.3min · rebond 68% (78/117) (MFE +3.04%)
   - −1.0% : fill 30min 62% · séance 80% (112/150) · gap 24% · délai 0.3min · rebond 71% (78/112) (MFE +2.59%)
   - −1.5% : fill 30min 54% · séance 74% (102/150) · gap 16% · délai 0.8min · rebond 72% (68/102) (MFE +2.07%)
   - −2.0% : fill 30min 46% · séance 67% (89/150) · gap 11% · délai 0.9min · rebond 70% (60/89) (MFE +1.9%)
   - −3.0% : fill 30min 36% · séance 58% (73/150) · gap 7% · délai 7.1min · rebond 85% (61/73) (MFE +2.34%)
   - −4.0% : fill 30min 30% · séance 51% (63/150) · gap 5% · délai 14.9min · rebond 76% (49/63) (MFE +3.07%)
   - −5.0% : fill 30min 21% · séance 46% (55/150) · gap 4% · délai 33.6min · rebond 92% (52/55) (MFE +3.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −5.56%) → stop au-delà de −3.36% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −5.6%) → stop au-delà de −4.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.98% (p90 −5.79%) → stop au-delà de −4.26% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1463 jambes) : jambe baissière méd −1.26% (p90 −3.61%) · ~21.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (49/53) · rebond 68% (33/49)
      · −2.0% : fill 87% (42/53) · rebond 58% (26/42)
      · −3.0% : fill 85% (38/53) · rebond 80% (31/38)
      · −4.0% : fill 74% (33/53) · rebond 77% (27/33)
      · −5.0% : fill 66% (30/53) · rebond 83% (27/30)
   - **flat** (32 séances) :
      · −1.0% : fill 84% (25/32) · rebond 83% (20/25)
      · −2.0% : fill 69% (19/32) · rebond 78% (14/19)
      · −3.0% : fill 51% (13/32) · rebond 94% (12/13)
      · −4.0% : fill 51% (13/32) · rebond 81% (11/13)
      · −5.0% : fill 44% (11/32) · rebond 100% (11/11)
   - **gap-up** (65 séances) :
      · −1.0% : fill 63% (38/65) · rebond 67% (25/38)
      · −2.0% : fill 50% (28/65) · rebond 79% (20/28)
      · −3.0% : fill 40% (22/65) · rebond 88% (18/22)
      · −4.0% : fill 34% (17/65) · rebond 72% (11/17)
      · −5.0% : fill 32% (14/65) · rebond 100% (14/14)
- **P(clôture VERTE) selon le drive 15min** (n=151) : 45% en base · 60% si les 15 1res min sont vertes (72 cas) · 34% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=151) : COUDE à **31min** → P(séance verte=clôture>ouverture) 71% si début vert vs 22% si rouge (base 45% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 241min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **71%** · continue >prix actuel 56% ; creux résiduel méd -2.63% (q20 -5.52%) → **SL/trailing à −5.52%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.86% / q75 +7.01% → **scale +3.86% / runner +7.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.63%** (au-delà de la MAE q10 -10.63%), cible rebond +2.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=151) : retour [-5.38% .. +7.16%] · haut q95 +8.84% · bas q05 -7.77%
   - 60min (n=151) : retour [-6.03% .. +9.54%] · haut q95 +10.0% · bas q05 -8.5%
   - 2h (n=151) : retour [-6.07% .. +10.0%] · haut q95 +11.64% · bas q05 -8.54%
   - 4h (n=151) : retour [-9.84% .. +10.68%] · haut q95 +12.94% · bas q05 -12.0%
   - 6h (n=151) : retour [-9.5% .. +14.65%] · haut q95 +18.52% · bas q05 -12.9%
   - session (n=151) : retour [-10.21% .. +19.32%] · haut q95 +19.82% · bas q05 -16.14%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.1  _(momentum baissier)_
- **ADX** : 25.3  _(tendance etablie)_
- **MACD** : hist -0.414  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 60.5%
- **ATR** : 4.09 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.049  _(neutre)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 44.7  _(transition)_
- **MA** : MA20 30.59 · MA50 39.19 · MA200 24.15  _(prix < MA20)_
- **Dist MA** : MA20 -14.3% · MA50 -33.1% · MA200 +8.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90179 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

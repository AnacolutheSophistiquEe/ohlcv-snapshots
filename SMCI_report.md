# SMCI

**Generated** : 2026-06-26T00:13:26.454585+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 10.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · $31.68  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot $31.68 (+10.7% vs entrée) · entrée $28.63 · stop $27.44 · T1 $30.27 · R/R 1.38  
> ↳ P(T1 av. stop) 15 % · EV/risk -0.013 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $28.30–$28.96 (mid $28.63)
- Spot actuel : $31.68 (+10.7% au-dessus de la zone — repli à attendre)
- Stop : $27.44 (stop swing_plan-based (-26.23%))
- Targets : T1 $30.27 · R/R 1.38 | T2 $31.91 · R/R 2.76 | T3 $33.55 · R/R 4.13
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $27.44


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : $-0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 1 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 8.6 | bear 14.1 | side 77.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→66% · +3.0%→48% · +5.0%→30% · +8.0%→12%
- Range intraday médian 6.17% (p90 10.16%) · excursion haute méd. +2.92% / basse méd. −2.54%
- Profil de vol intra : ouverture 3.677% vs midi 1.287% vs clôture 1.448% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑0%/↓2% ; spike-down 65% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.158 ; neutre — autocorr -0.008)_ ; drift intra méd. 0.529% ; recovery-V 34%
- **σ réalisé intraday** 4.455% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 61% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 32.0104 (VA 31.4321–33.0384 ; dernier close 32.45)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 32% · rebond 62% · **stop −4.67%** sous le fill (sous le bruit) · cible +1.94% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.24% · baisse 47% (gap-down >1% 31% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −2.14%) · haut méd +0.89% · range méd 1.95%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −3.19%) · haut méd +1.23% · range méd 2.77%
- Excursion ouverture 30min (n=160) : bas méd −1.35% (p90 −3.5%) · haut méd +1.42% · range méd 3.42%
- Excursion ouverture 60min (n=160) : bas méd −1.62% (p90 −4.14%) · haut méd +1.75% · range méd 4.19%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.45 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (126/159) · gap 42% · délai 0.0min · rebond 59% (73/126) (MFE +1.31%)
   - −1.0% : fill 30min 59% · séance 68% (113/159) · gap 31% · délai 0.0min · rebond 56% (63/113) (MFE +1.34%)
   - −1.5% : fill 30min 48% · séance 62% (98/159) · gap 25% · délai 0.3min · rebond 63% (58/98) (MFE +1.45%)
   - −2.0% : fill 30min 42% · séance 56% (87/159) · gap 20% · délai 1.2min · rebond 65% (53/87) (MFE +1.78%)
   - −3.0% : fill 30min 29% · séance 48% (67/159) · gap 17% · délai 6.7min · rebond 54% (38/67) (MFE +1.71%)
   - −4.0% : fill 30min 22% · séance 39% (50/159) · gap 13% · délai 11.9min · rebond 60% (30/50) (MFE +1.33%)
   - −5.0% : fill 30min 17% · séance 32% (40/159) · gap 9% · délai 15.8min · rebond 62% (26/40) (MFE +1.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.12%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.98%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.77%) → stop au-delà de −2.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=815 jambes) : jambe baissière méd −1.22% (p90 −2.74%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 97% (68/69) · rebond 54% (38/68)
      · −2.0% : fill 88% (60/69) · rebond 56% (32/60)
      · −3.0% : fill 81% (52/69) · rebond 58% (30/52)
      · −4.0% : fill 68% (41/69) · rebond 63% (25/41)
      · −5.0% : fill 55% (33/69) · rebond 60% (21/33)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (14/16) · rebond 81% (10/14)
      · −2.0% : fill 60% (10/16) · rebond 78% (7/10)
      · −3.0% : fill 13% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (74 séances) :
      · −1.0% : fill 37% (31/74) · rebond 53% (15/31)
      · −2.0% : fill 24% (17/74) · rebond 94% (14/17)
      · −3.0% : fill 21% (13/74) · rebond 35% (6/13)
      · −4.0% : fill 16% (8/74) · rebond 45% (4/8)
      · −5.0% : fill 14% (7/74) · rebond 69% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 76% si les 15 1res min sont vertes (70 cas) · 31% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +4.83%] · haut q95 +6.6% · bas q05 -4.37%
   - 60min (n=160) : retour [-4.56% .. +5.59%] · haut q95 +6.6% · bas q05 -5.47%
   - session (n=160) : retour [-7.24% .. +8.83%] · haut q95 +9.65% · bas q05 -8.56%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.4 · part idiosyncratique 0.6
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.6  _(momentum baissier)_
- **ADX** : 23.8  _(pas de tendance nette)_
- **MACD** : hist -0.758  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 80.4%
- **ATR** : 3.97 (96.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.05  _(neutre)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 43.7  _(transition)_
- **MA** : MA20 37.41 · MA50 33.43 · MA200 35.41  _(prix < MA20)_
- **Dist MA** : MA20 -15.3% · MA50 -5.2% · MA200 -10.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39671 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

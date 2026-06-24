# SMR

**Generated** : 2026-06-24T21:56:27.644974+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $10.21  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $10.21 (+25.6% vs entrée) · entrée $8.13 · stop $7.79 · T1 $8.82 · R/R 2.03  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.042 · ¼-Kelly 0.002 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $7.99–$8.27 (mid $8.13)
- Spot actuel : $10.21 (+25.6% au-dessus de la zone — repli à attendre)
- Stop : $7.79 (stop swing_plan-based (-23.73%))
- Targets : T1 $8.82 · R/R 2.03 | T2 $9.51 · R/R 4.06 | T3 $10.20 · R/R 6.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.79


## Edge, scénarios & sizing

- EV/risk : 0.042 | EV/share : $0.015 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 18 % | T3 8 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 28.2 | bear 30.9 | side 40.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→69% · +3.0%→55% · +5.0%→35% · +8.0%→19%
- Range intraday médian 7.23% (p90 12.61%) · excursion haute méd. +3.23% / basse méd. −2.85%
- Profil de vol intra : ouverture 4.75% vs midi 1.546% vs clôture 1.83% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr 0.013)_ ; drift intra méd. 0.829% ; recovery-V 29%
- **σ réalisé intraday** 5.386% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 41% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 11.2079 (VA 10.9749–11.4118 ; dernier close 10.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 56% · rebond 73% · **stop −6.25%** sous le fill (sous le bruit) · cible +3.39% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. -0.77% · baisse 62% (gap-down >1% 44% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.33% (p90 −3.63%) · haut méd +1.12% · range méd 2.88%
- Excursion ouverture 15min (n=160) : bas méd −1.67% (p90 −4.0%) · haut méd +1.41% · range méd 3.84%
- Excursion ouverture 30min (n=160) : bas méd −2.04% (p90 −5.22%) · haut méd +1.97% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −5.86%) · haut méd +2.63% · range méd 5.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 10.85 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 81% (132/159) · gap 55% · délai 0.0min · rebond 64% (80/132) (MFE +1.64%)
   - −1.0% : fill 30min 70% · séance 77% (126/159) · gap 44% · délai 0.0min · rebond 66% (83/126) (MFE +1.92%)
   - −1.5% : fill 30min 68% · séance 74% (120/159) · gap 40% · délai 0.0min · rebond 73% (86/120) (MFE +2.21%)
   - −2.0% : fill 30min 62% · séance 68% (114/159) · gap 30% · délai 0.0min · rebond 70% (83/114) (MFE +2.52%)
   - −3.0% : fill 30min 51% · séance 62% (103/159) · gap 13% · délai 2.1min · rebond 75% (83/103) (MFE +3.09%)
   - −4.0% : fill 30min 41% · séance 56% (88/159) · gap 8% · délai 6.8min · rebond 73% (68/88) (MFE +3.39%)
   - −5.0% : fill 30min 26% · séance 43% (66/159) · gap 5% · délai 14.9min · rebond 70% (48/66) (MFE +1.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −3.06%) → stop au-delà de −2.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.02% (p90 −3.78%) → stop au-delà de −2.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.06% (p90 −3.88%) → stop au-delà de −2.5% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1200 jambes) : jambe baissière méd −1.39% (p90 −3.16%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 72% (55/84)
      · −2.0% : fill 91% (80/84) · rebond 77% (60/80)
      · −3.0% : fill 85% (77/84) · rebond 79% (63/77)
      · −4.0% : fill 77% (67/84) · rebond 78% (55/67)
      · −5.0% : fill 57% (48/84) · rebond 78% (37/48)
   - **flat** (13 séances) :
      · −1.0% : fill 71% (10/13) · rebond 55% (7/10)
      · −2.0% : fill 55% (8/13) · rebond 43% (5/8)
      · −3.0% : fill 50% (6/13) · rebond 42% (4/6)
      · −4.0% : fill 50% (6/13) · rebond 57% (3/6)
      · −5.0% : fill 34% (4/13) · rebond 51% (3/4)
   - **gap-up** (62 séances) :
      · −1.0% : fill 44% (32/62) · rebond 50% (21/32)
      · −2.0% : fill 37% (26/62) · rebond 52% (18/26)
      · −3.0% : fill 29% (20/62) · rebond 72% (16/20)
      · −4.0% : fill 25% (15/62) · rebond 60% (10/15)
      · −5.0% : fill 22% (14/62) · rebond 44% (8/14)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 65% si les 15 1res min sont vertes (63 cas) · 39% si rouges (97 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-6.03% .. +4.66%] · haut q95 +6.6% · bas q05 -6.92%
   - 60min (n=160) : retour [-6.66% .. +6.13%] · haut q95 +8.9% · bas q05 -8.14%
   - session (n=160) : retour [-9.02% .. +10.98%] · haut q95 +11.74% · bas q05 -11.23%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.43 · part idiosyncratique 0.57
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.5  _(momentum baissier)_
- **ADX** : 12.6  _(pas de tendance nette)_
- **MACD** : hist 0.021  _(bullish_recent)_
- **BB** : %B 0.31 · largeur 45.3%
- **ATR** : 1.04 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.093  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 57.6  _(transition)_
- **MA** : MA20 11.15 · MA50 11.62 · MA200 20.33  _(prix < MA20)_
- **Dist MA** : MA20 -8.4% · MA50 -12.2% · MA200 -49.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (41349 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# SMR

**Generated** : 2026-06-26T00:20:03.846272+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $10.07  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot $10.07 (+11.8% vs entrée) · entrée $9.01 · stop $8.70 · T1 $9.35 · R/R 1.1  
> ↳ P(T1 av. stop) 37 % · EV/risk -0.008 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.94–$9.08 (mid $9.01)
- Spot actuel : $10.07 (+11.8% au-dessus de la zone — repli à attendre)
- Stop : $8.70 (stop swing_plan-based (-24.34%))
- Targets : T1 $9.35 · R/R 1.1 | T2 $9.69 · R/R 2.19 | T3 $10.04 · R/R 3.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.70


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : $-0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 12 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 18.8 | bear 41.9 | side 39.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→68% · +3.0%→54% · +5.0%→35% · +8.0%→19%
- Range intraday médian 7.23% (p90 12.61%) · excursion haute méd. +3.11% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.744% vs midi 1.553% vs clôture 1.834% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr 0.012)_ ; drift intra méd. 0.604% ; recovery-V 27%
- **σ réalisé intraday** 5.389% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 44% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 10.3038 (VA 10.1061–10.4115 ; dernier close 10.224)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 57% · rebond 74% · **stop −6.11%** sous le fill (sous le bruit) · cible +2.95% · R/R 0.48 (high win-rate)
- Gaps overnight (n=159) : méd. -0.77% · baisse 63% (gap-down >1% 45% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.37% (p90 −3.61%) · haut méd +1.11% · range méd 2.9%
- Excursion ouverture 15min (n=160) : bas méd −1.75% (p90 −3.99%) · haut méd +1.38% · range méd 3.87%
- Excursion ouverture 30min (n=160) : bas méd −2.07% (p90 −5.17%) · haut méd +1.94% · range méd 4.3%
- Excursion ouverture 60min (n=160) : bas méd −2.19% (p90 −6.28%) · haut méd +2.59% · range méd 5.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 10.224 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 82% (132/159) · gap 56% · délai 0.0min · rebond 62% (80/132) (MFE +1.62%)
   - −1.0% : fill 30min 71% · séance 78% (126/159) · gap 45% · délai 0.0min · rebond 65% (83/126) (MFE +1.82%)
   - −1.5% : fill 30min 68% · séance 74% (120/159) · gap 41% · délai 0.0min · rebond 72% (86/120) (MFE +2.03%)
   - −2.0% : fill 30min 63% · séance 69% (114/159) · gap 30% · délai 0.0min · rebond 68% (83/114) (MFE +2.48%)
   - −3.0% : fill 30min 52% · séance 62% (103/159) · gap 13% · délai 1.9min · rebond 76% (84/103) (MFE +2.87%)
   - −4.0% : fill 30min 42% · séance 57% (88/159) · gap 8% · délai 6.3min · rebond 74% (68/88) (MFE +2.95%)
   - −5.0% : fill 30min 28% · séance 44% (66/159) · gap 5% · délai 14.5min · rebond 71% (48/66) (MFE +1.98%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −3.07%) → stop au-delà de −2.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.02% (p90 −3.78%) → stop au-delà de −2.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.06% (p90 −3.88%) → stop au-delà de −2.5% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1206 jambes) : jambe baissière méd −1.38% (p90 −3.15%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 70% (55/84)
      · −2.0% : fill 92% (80/84) · rebond 74% (60/80)
      · −3.0% : fill 85% (77/84) · rebond 80% (64/77)
      · −4.0% : fill 78% (67/84) · rebond 79% (55/67)
      · −5.0% : fill 59% (48/84) · rebond 79% (37/48)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 65% si les 15 1res min sont vertes (63 cas) · 38% si rouges (97 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.97% .. +4.63%] · haut q95 +6.6% · bas q05 -6.91%
   - 60min (n=160) : retour [-6.62% .. +6.11%] · haut q95 +8.9% · bas q05 -8.11%
   - session (n=160) : retour [-8.96% .. +10.98%] · haut q95 +11.74% · bas q05 -11.18%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.44 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.1  _(momentum baissier)_
- **ADX** : 12.4  _(pas de tendance nette)_
- **MACD** : hist -0.008  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 45.8%
- **ATR** : 1.06 (16.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.105  _(distribution)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 59.0  _(transition)_
- **MA** : MA20 11.05 · MA50 11.62 · MA200 20.21  _(prix < MA20)_
- **Dist MA** : MA20 -8.9% · MA50 -13.3% · MA200 -50.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (40039 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

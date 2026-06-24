# SMCI

**Generated** : 2026-06-24T21:48:50.493539+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 10.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · $32.45  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $32.45 (+14.1% vs entrée) · entrée $28.45 · stop $27.26 · T1 $30.09 · R/R 1.38  
> ↳ P(T1 av. stop) 15 % · EV/risk -0.005 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.020 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $28.13–$28.78 (mid $28.45)
- Spot actuel : $32.45 (+14.1% au-dessus de la zone — repli à attendre)
- Stop : $27.26 (stop swing_plan-based (-29.47%))
- Targets : T1 $30.09 · R/R 1.38 | T2 $31.72 · R/R 2.75 | T3 $33.36 · R/R 4.13
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $27.26


## Edge, scénarios & sizing

- EV/risk : -0.005 | EV/share : $-0.006 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 1 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 41.9 | bear 46.4 | side 11.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→68% · +3.0%→49% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.17% (p90 10.16%) · excursion haute méd. +2.96% / basse méd. −2.43%
- Profil de vol intra : ouverture 3.646% vs midi 1.272% vs clôture 1.442% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 21% · trend ↑0%/↓2% ; spike-down 64% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.162 ; neutre — autocorr -0.001)_ ; drift intra méd. 0.706% ; recovery-V 37%
- **σ réalisé intraday** 4.421% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 59% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 33.3828 (VA 33.0273–33.8963 ; dernier close 33.33)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 60% · **stop −5.55%** sous le fill (sous le bruit) · cible +1.83% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 48% (gap-down >1% 32% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −0.82% (p90 −2.2%) · haut méd +0.89% · range méd 1.92%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −3.23%) · haut méd +1.21% · range méd 2.72%
- Excursion ouverture 30min (n=160) : bas méd −1.27% (p90 −3.71%) · haut méd +1.38% · range méd 3.32%
- Excursion ouverture 60min (n=160) : bas méd −1.6% (p90 −4.17%) · haut méd +1.78% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 33.33 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (126/159) · gap 43% · délai 0.0min · rebond 58% (72/126) (MFE +1.24%)
   - −1.0% : fill 30min 58% · séance 68% (113/159) · gap 32% · délai 0.0min · rebond 55% (62/113) (MFE +1.24%)
   - −1.5% : fill 30min 47% · séance 62% (98/159) · gap 26% · délai 0.1min · rebond 62% (57/98) (MFE +1.43%)
   - −2.0% : fill 30min 41% · séance 55% (87/159) · gap 20% · délai 0.8min · rebond 64% (52/87) (MFE +1.58%)
   - −3.0% : fill 30min 30% · séance 47% (67/159) · gap 17% · délai 6.3min · rebond 56% (38/67) (MFE +1.86%)
   - −4.0% : fill 30min 22% · séance 38% (50/159) · gap 14% · délai 9.5min · rebond 58% (30/50) (MFE +1.17%)
   - −5.0% : fill 30min 18% · séance 31% (40/159) · gap 9% · délai 15.3min · rebond 60% (25/40) (MFE +1.83%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.17%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.98%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.77%) → stop au-delà de −2.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=814 jambes) : jambe baissière méd −1.2% (p90 −2.74%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 97% (68/69) · rebond 54% (38/68)
      · −2.0% : fill 88% (60/69) · rebond 56% (32/60)
      · −3.0% : fill 81% (52/69) · rebond 58% (30/52)
      · −4.0% : fill 68% (41/69) · rebond 63% (25/41)
      · −5.0% : fill 55% (33/69) · rebond 60% (21/33)
   - **flat** (17 séances) :
      · −1.0% : fill 92% (15/17) · rebond 80% (10/15)
      · −2.0% : fill 61% (11/17) · rebond 76% (7/11)
      · −3.0% : fill 15% (3/17) · rebond 89% (2/3)
      · −4.0% : fill 6% (2/17) · rebond 100% (2/2)
      · −5.0% : fill 2% (1/17) · rebond 0% (0/1)
   - **gap-up** (73 séances) :
      · −1.0% : fill 34% (30/73) · rebond 48% (14/30)
      · −2.0% : fill 21% (16/73) · rebond 93% (13/16)
      · −3.0% : fill 17% (12/73) · rebond 43% (6/12)
      · −4.0% : fill 13% (7/73) · rebond 28% (3/7)
      · −5.0% : fill 10% (6/73) · rebond 56% (4/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 76% si les 15 1res min sont vertes (70 cas) · 32% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.12% .. +4.89%] · haut q95 +6.63% · bas q05 -4.38%
   - 60min (n=160) : retour [-4.58% .. +5.6%] · haut q95 +6.63% · bas q05 -5.52%
   - session (n=160) : retour [-7.27% .. +8.85%] · haut q95 +9.72% · bas q05 -8.64%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.41 · part idiosyncratique 0.59
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.8  _(momentum baissier)_
- **ADX** : 25.2  _(tendance etablie)_
- **MACD** : hist -0.861  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 78.5%
- **ATR** : 4.0 (96.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.02  _(neutre)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 38.7  _(transition)_
- **MA** : MA20 37.73 · MA50 33.34 · MA200 35.45  _(prix < MA20)_
- **Dist MA** : MA20 -14.0% · MA50 -2.7% · MA200 -8.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (40922 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

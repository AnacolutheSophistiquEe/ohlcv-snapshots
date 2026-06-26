# SAF

**Generated** : 2026-06-26T00:07:01.565284+00:00  
**Santé technique** : 10/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · €343.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)  
> ↳ spot €343.00 (+9.1% vs entrée) · entrée €314.36 · stop €310.92 · T1 €321.24 · R/R 2.0  
> ↳ P(T1 av. stop) 32 % · EV/risk -0.088 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 610 % hors [0,100] (R² max 0.87). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : triple_bullish (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 82.2 > 70 (surachat) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 10/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €312.99–€315.74 (mid €314.36)
- Spot actuel : €343.00 (+9.1% au-dessus de la zone — repli à attendre)
- Stop : €310.92 (stop swing_plan-based (-9.35%))
- Targets : T1 €321.24 · R/R 2.0 | T2 €328.12 · R/R 4.0 | T3 €335.00 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €310.92


## Edge, scénarios & sizing

- EV/risk : -0.088 | EV/share : €-0.301 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 16 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 5.6 | bear 31.0 | side 63.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 343.0 (= 1 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→59% · +2.0%→35% · +3.0%→15% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.8% (p90 5.22%) · excursion haute méd. +1.2% / basse méd. −1.16%
- Profil de vol intra : ouverture 1.718% vs midi 0.672% vs clôture 0.796% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 36% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr -0.023)_ ; drift intra méd. 0.536% ; recovery-V 19%
- **σ réalisé intraday** 1.999% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 47% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 335.0938 (VA 334.8813–337.6438 ; dernier close 337.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 20% · rebond 65% · **stop −1.62%** sous le fill (sous le bruit) · cible +1.3% · R/R 0.8 (high win-rate)
- Gaps overnight (n=134) : méd. -0.06% · baisse 52% (gap-down >1% 13% · >2% 2%)
- Excursion ouverture 5min (n=135) : bas méd −0.37% (p90 −1.46%) · haut méd +0.25% · range méd 0.94%
- Excursion ouverture 15min (n=135) : bas méd −0.44% (p90 −1.77%) · haut méd +0.44% · range méd 1.2%
- Excursion ouverture 30min (n=135) : bas méd −0.51% (p90 −1.93%) · haut méd +0.57% · range méd 1.33%
- Excursion ouverture 60min (n=135) : bas méd −0.7% (p90 −2.01%) · haut méd +0.69% · range méd 1.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 337.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 68% (96/134) · gap 29% · délai 0.2min · rebond 40% (36/96) (MFE +0.78%)
   - −1.0% : fill 30min 40% · séance 50% (68/134) · gap 13% · délai 0.4min · rebond 42% (24/68) (MFE +0.58%)
   - −1.5% : fill 30min 28% · séance 42% (58/134) · gap 6% · délai 5.1min · rebond 37% (19/58) (MFE +0.89%)
   - −2.0% : fill 30min 15% · séance 33% (42/134) · gap 2% · délai 32.5min · rebond 51% (19/42) (MFE +1.07%)
   - −3.0% : fill 30min 5% · séance 20% (25/134) · gap 1% · délai 102.5min · rebond 65% (16/25) (MFE +1.3%)
   - −4.0% : fill 30min 3% · séance 10% (12/134) · gap 0% · délai 153.7min · rebond 53% (6/12) (MFE +1.49%)
   - −5.0% : fill 30min 0% · séance 2% (3/134) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.25% (p90 −0.95%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.15% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=164 jambes) : jambe baissière méd −1.08% (p90 −2.73%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 75% (37/48) · rebond 42% (14/37)
      · −2.0% : fill 53% (26/48) · rebond 56% (13/26)
      · −3.0% : fill 32% (15/48) · rebond 67% (9/15)
      · −4.0% : fill 17% (8/48) · rebond 59% (4/8)
      · −5.0% : fill 3% (2/48) · rebond 0% (0/2)
   - **flat** (36 séances) :
      · −1.0% : fill 45% (15/36) · rebond 55% (7/15)
      · −2.0% : fill 23% (7/36) · rebond 50% (3/7)
      · −3.0% : fill 11% (4/36) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/36) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (50 séances) :
      · −1.0% : fill 25% (16/50) · rebond 26% (3/16)
      · −2.0% : fill 16% (9/50) · rebond 34% (3/9)
      · −3.0% : fill 12% (6/50) · rebond 55% (4/6)
      · −4.0% : fill 8% (3/50) · rebond 30% (1/3)
      · −5.0% : fill 2% (1/50) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=135) : 50% en base · 68% si les 15 1res min sont vertes (60 cas) · 31% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-1.85% .. +2.12%] · haut q95 +2.66% · bas q05 -2.36%
   - 60min (n=135) : retour [-1.84% .. +2.51%] · haut q95 +3.28% · bas q05 -2.73%
   - session (n=135) : retour [-3.05% .. +3.71%] · haut q95 +4.42% · bas q05 -4.44%


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.73 · part idiosyncratique 0.27
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 82.2  _(surachat)_
- **ADX** : 26.6  _(tendance etablie)_
- **MACD** : hist 3.025  _(pas de croisement recent)_
- **BB** : %B 0.94 · largeur 22.5%
- **ATR** : 9.5 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.073  _(distribution)_
- **Vol ratio** : 0.36  _(volume atone)_
- **Choppiness** : 31.1  _(marche directionnel)_
- **MA** : MA20 312.36 · MA50 293.61 · MA200 299.4  _(prix > MA20)_
- **Dist MA** : MA20 +9.8% · MA50 +16.8% · MA200 +14.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (41196 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# MSTR

**Generated** : 2026-06-26T21:47:02.161467+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $82.31  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot $82.31 (+13.0% vs entrée) · entrée $72.82 · stop $69.98 · T1 $74.98 · R/R 0.76  
> ↳ P(T1 av. stop) 35 % · EV/risk -0.041 · ¼-Kelly 0.002 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -258 % hors [0,100] (R² max 0.04). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $72.39–$73.26 (mid $72.82)
- Spot actuel : $82.31 (+13.0% au-dessus de la zone — repli à attendre)
- Stop : $69.98 (stop swing_plan-based (-26.51%))
- Targets : T1 $74.98 · R/R 0.76 | T2 $77.15 · R/R 1.52 | T3 $79.31 · R/R 2.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $69.98


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : $-0.116 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 10 % | T3 2 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 82.2 | side 12.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→50% · +3.0%→30% · +5.0%→9% · +8.0%→4%
- Range intraday médian 5.12% (p90 9.24%) · excursion haute méd. +2.02% / basse méd. −2.89%
- Profil de vol intra : ouverture 3.096% vs midi 1.203% vs clôture 1.214% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr -0.01)_ ; drift intra méd. -1.946% ; recovery-V 28%
- **σ réalisé intraday** 3.901% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 76% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 86.5275 (VA 85.5875–87.7025 ; dernier close 85.32)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 69% · **stop −5.23%** sous le fill (sous le bruit) · cible +1.43% · R/R 0.27 (high win-rate)
- Gaps overnight (n=159) : méd. -0.21% · baisse 56% (gap-down >1% 40% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −0.92% (p90 −2.09%) · haut méd +0.56% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −3.04%) · haut méd +0.8% · range méd 2.42%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.89%) · haut méd +1.04% · range méd 3.0%
- Excursion ouverture 60min (n=160) : bas méd −1.83% (p90 −4.96%) · haut méd +1.35% · range méd 3.64%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 85.32 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 81% (127/159) · gap 47% · délai 0.0min · rebond 47% (63/127) (MFE +0.95%)
   - −1.0% : fill 30min 65% · séance 78% (122/159) · gap 40% · délai 0.0min · rebond 54% (68/122) (MFE +1.34%)
   - −1.5% : fill 30min 58% · séance 74% (114/159) · gap 28% · délai 0.0min · rebond 54% (67/114) (MFE +1.2%)
   - −2.0% : fill 30min 49% · séance 65% (102/159) · gap 23% · délai 1.4min · rebond 54% (64/102) (MFE +1.17%)
   - −3.0% : fill 30min 33% · séance 53% (78/159) · gap 14% · délai 9.9min · rebond 52% (47/78) (MFE +1.39%)
   - −4.0% : fill 30min 22% · séance 45% (64/159) · gap 6% · délai 36.9min · rebond 54% (39/64) (MFE +1.05%)
   - −5.0% : fill 30min 17% · séance 35% (50/159) · gap 3% · délai 58.7min · rebond 69% (36/50) (MFE +1.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.79%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.1% (p90 −2.84%) → stop au-delà de −2.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.19% (p90 −2.83%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=968 jambes) : jambe baissière méd −1.21% (p90 −2.83%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 99% (73/74) · rebond 46% (36/73)
      · −2.0% : fill 88% (66/74) · rebond 48% (38/66)
      · −3.0% : fill 78% (57/74) · rebond 53% (35/57)
      · −4.0% : fill 66% (47/74) · rebond 55% (31/47)
      · −5.0% : fill 56% (39/74) · rebond 71% (29/39)
   - **flat** (17 séances) :
      · −1.0% : fill 86% (16/17) · rebond 77% (10/16)
      · −2.0% : fill 64% (13/17) · rebond 55% (9/13)
      · −3.0% : fill 44% (9/17) · rebond 36% (5/9)
      · −4.0% : fill 41% (7/17) · rebond 12% (2/7)
      · −5.0% : fill 32% (5/17) · rebond 15% (2/5)
   - **gap-up** (68 séances) :
      · −1.0% : fill 50% (33/68) · rebond 62% (22/33)
      · −2.0% : fill 38% (23/68) · rebond 71% (17/23)
      · −3.0% : fill 25% (12/68) · rebond 55% (7/12)
      · −4.0% : fill 22% (10/68) · rebond 67% (6/10)
      · −5.0% : fill 11% (6/68) · rebond 93% (5/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 47% si les 15 1res min sont vertes (72 cas) · 35% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +2.67%] · haut q95 +3.66% · bas q05 -4.18%
   - 60min (n=160) : retour [-5.13% .. +3.31%] · haut q95 +4.07% · bas q05 -5.6%
   - session (n=160) : retour [-6.26% .. +5.21%] · haut q95 +7.86% · bas q05 -8.73%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.58 · part idiosyncratique 0.42
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.1  _(survente)_
- **ADX** : 31.6  _(tendance etablie)_
- **MACD** : hist -3.188  _(pas de croisement recent)_
- **BB** : %B 0.01 · largeur 63.3%
- **ATR** : 9.49 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.389  _(distribution)_
- **Vol ratio** : 1.72  _(volume au-dessus de la moyenne)_
- **Choppiness** : 33.8  _(marche directionnel)_
- **MA** : MA20 119.16 · MA50 150.54 · MA200 185.95  _(prix < MA20)_
- **Dist MA** : MA20 -30.9% · MA50 -45.3% · MA200 -55.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39614 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

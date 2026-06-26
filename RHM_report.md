# RHM

**Generated** : 2026-06-26T00:02:02.078153+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €946.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot €946.40 (+7.6% vs entrée) · entrée €879.33 · stop €859.21 · T1 €903.49 · R/R 1.2  
> ↳ P(T1 av. stop) 26 % · EV/risk -0.036 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -69 % hors [0,100] (R² max 0.99). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €874.50–€884.16 (mid €879.33)
- Spot actuel : €946.40 (+7.6% au-dessus de la zone — repli à attendre)
- Stop : €859.21 (stop swing_plan-based (-16.81%))
- Targets : T1 €903.49 · R/R 1.2 | T2 €927.66 · R/R 2.4 | T3 €951.83 · R/R 3.6
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €859.21


## Edge, scénarios & sizing

- EV/risk : -0.036 | EV/share : €-0.716 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 4 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 34.5 | bear 40.0 | side 25.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→50% · +3.0%→30% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.81%) · excursion haute méd. +2.01% / basse méd. −1.66%
- Profil de vol intra : ouverture 2.552% vs midi 0.898% vs clôture 1.019% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.1 ; neutre — autocorr 0.023)_ ; drift intra méd. -0.88% ; recovery-V 32%
- **σ réalisé intraday** 2.921% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 67% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 947.8475 (VA 937.8775–987.7275 ; dernier close 945.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 48% · rebond 65% · **stop −3.59%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. 0.04% · baisse 43% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −1.75%) · haut méd +0.58% · range méd 1.5%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −2.0%) · haut méd +0.8% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.24%) · haut méd +0.98% · range méd 2.15%
- Excursion ouverture 60min (n=160) : bas méd −1.0% (p90 −2.57%) · haut méd +1.01% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 945.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 77% (119/159) · gap 29% · délai 0.3min · rebond 56% (61/119) (MFE +1.12%)
   - −1.0% : fill 30min 47% · séance 72% (106/159) · gap 18% · délai 5.3min · rebond 58% (58/106) (MFE +1.39%)
   - −1.5% : fill 30min 28% · séance 56% (79/159) · gap 10% · délai 20.0min · rebond 53% (40/79) (MFE +1.16%)
   - −2.0% : fill 30min 23% · séance 48% (70/159) · gap 8% · délai 33.5min · rebond 65% (40/70) (MFE +1.36%)
   - −3.0% : fill 30min 11% · séance 29% (46/159) · gap 4% · délai 117.1min · rebond 63% (30/46) (MFE +1.35%)
   - −4.0% : fill 30min 5% · séance 19% (28/159) · gap 2% · délai 312.5min · rebond 47% (16/28) (MFE +0.83%)
   - −5.0% : fill 30min 2% · séance 12% (18/159) · gap 2% · délai 197.3min · rebond 50% (11/18) (MFE +1.17%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.47%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.29% (p90 −1.59%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.61%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=453 jambes) : jambe baissière méd −1.16% (p90 −2.7%) · ~7.3 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 98% (49/50) · rebond 57% (24/49)
      · −2.0% : fill 79% (38/50) · rebond 70% (24/38)
      · −3.0% : fill 44% (27/50) · rebond 61% (19/27)
      · −4.0% : fill 30% (16/50) · rebond 45% (10/16)
      · −5.0% : fill 20% (11/50) · rebond 71% (9/11)
   - **flat** (50 séances) :
      · −1.0% : fill 76% (35/50) · rebond 70% (23/35)
      · −2.0% : fill 34% (17/50) · rebond 65% (9/17)
      · −3.0% : fill 20% (10/50) · rebond 42% (5/10)
      · −4.0% : fill 18% (8/50) · rebond 16% (2/8)
      · −5.0% : fill 16% (6/50) · rebond 22% (1/6)
   - **gap-up** (59 séances) :
      · −1.0% : fill 46% (22/59) · rebond 43% (11/22)
      · −2.0% : fill 33% (15/59) · rebond 53% (7/15)
      · −3.0% : fill 24% (9/59) · rebond 82% (6/9)
      · −4.0% : fill 10% (4/59) · rebond 100% (4/4)
      · −5.0% : fill 0% (1/59) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 62% si les 15 1res min sont vertes (86 cas) · 31% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +3.21%] · haut q95 +3.91% · bas q05 -3.16%
   - 60min (n=160) : retour [-2.9% .. +3.06%] · haut q95 +4.15% · bas q05 -3.48%
   - session (n=160) : retour [-6.86% .. +3.41%] · haut q95 +4.74% · bas q05 -7.14%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.3 · part idiosyncratique 0.7
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 19.9  _(survente)_
- **ADX** : 27.9  _(tendance etablie)_
- **MACD** : hist -19.182  _(bearish_recent)_
- **BB** : %B -0.18 · largeur 28.0%
- **ATR** : 67.07 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.211  _(distribution)_
- **Vol ratio** : 1.49  _(volume normal)_
- **Choppiness** : 38.4  _(transition)_
- **MA** : MA20 1170.96 · MA50 1244.22 · MA200 1570.69  _(prix < MA20)_
- **Dist MA** : MA20 -19.2% · MA50 -23.9% · MA200 -39.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (37959 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

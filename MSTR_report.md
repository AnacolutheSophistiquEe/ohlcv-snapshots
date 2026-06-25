# MSTR

**Generated** : 2026-06-25T21:47:59.425036+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $85.33  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot $85.33 (+13.5% vs entrée) · entrée $75.18 · stop $72.14 · T1 $77.42 · R/R 0.74  
> ↳ P(T1 av. stop) 34 % · EV/risk -0.043 · ¼-Kelly 0.004 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -243 % hors [0,100] (R² max 0.04). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $74.74–$75.63 (mid $75.18)
- Spot actuel : $85.33 (+13.5% au-dessus de la zone — repli à attendre)
- Stop : $72.14 (stop swing_plan-based (-27.35%))
- Targets : T1 $77.42 · R/R 0.74 | T2 $79.65 · R/R 1.47 | T3 $81.89 · R/R 2.21
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $72.14


## Edge, scénarios & sizing

- EV/risk : -0.043 | EV/share : $-0.130 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 9 % | T3 2 %
- Kelly (position) : f* 0.015 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 82.0 | side 13.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→69% · +2.0%→50% · +3.0%→30% · +5.0%→9% · +8.0%→4%
- Range intraday médian 5.12% (p90 8.88%) · excursion haute méd. +2.02% / basse méd. −2.89%
- Profil de vol intra : ouverture 3.017% vs midi 1.2% vs clôture 1.208% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr -0.019)_ ; drift intra méd. -1.56% ; recovery-V 29%
- **σ réalisé intraday** 3.789% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 75% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 94.2812 (VA 92.4228–97.7327 ; dernier close 94.13)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 67% · **stop −5.22%** sous le fill (sous le bruit) · cible +1.26% · R/R 0.24 (high win-rate)
- Gaps overnight (n=159) : méd. -0.35% · baisse 57% (gap-down >1% 40% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −2.06%) · haut méd +0.57% · range méd 1.82%
- Excursion ouverture 15min (n=160) : bas méd −1.2% (p90 −3.02%) · haut méd +0.82% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.61%) · haut méd +1.06% · range méd 2.98%
- Excursion ouverture 60min (n=160) : bas méd −1.8% (p90 −4.71%) · haut méd +1.45% · range méd 3.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 94.13 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (127/159) · gap 48% · délai 0.0min · rebond 48% (63/127) (MFE +0.96%)
   - −1.0% : fill 30min 64% · séance 77% (122/159) · gap 40% · délai 0.0min · rebond 55% (69/122) (MFE +1.39%)
   - −1.5% : fill 30min 57% · séance 73% (114/159) · gap 28% · délai 0.0min · rebond 55% (68/114) (MFE +1.38%)
   - −2.0% : fill 30min 48% · séance 65% (102/159) · gap 24% · délai 1.3min · rebond 53% (64/102) (MFE +1.09%)
   - −3.0% : fill 30min 32% · séance 52% (78/159) · gap 14% · délai 10.1min · rebond 54% (48/78) (MFE +1.43%)
   - −4.0% : fill 30min 21% · séance 44% (64/159) · gap 6% · délai 38.7min · rebond 56% (40/64) (MFE +1.08%)
   - −5.0% : fill 30min 15% · séance 34% (50/159) · gap 3% · délai 71.1min · rebond 67% (36/50) (MFE +1.26%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.79%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.1% (p90 −2.84%) → stop au-delà de −2.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.19% (p90 −2.83%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=964 jambes) : jambe baissière méd −1.22% (p90 −2.81%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 99% (74/75) · rebond 46% (37/74)
      · −2.0% : fill 88% (67/75) · rebond 49% (39/67)
      · −3.0% : fill 78% (58/75) · rebond 53% (36/58)
      · −4.0% : fill 66% (48/75) · rebond 55% (32/48)
      · −5.0% : fill 56% (40/75) · rebond 71% (30/40)
   - **flat** (17 séances) :
      · −1.0% : fill 86% (16/17) · rebond 77% (10/16)
      · −2.0% : fill 64% (13/17) · rebond 55% (9/13)
      · −3.0% : fill 44% (9/17) · rebond 36% (5/9)
      · −4.0% : fill 41% (7/17) · rebond 12% (2/7)
      · −5.0% : fill 32% (5/17) · rebond 15% (2/5)
   - **gap-up** (67 séances) :
      · −1.0% : fill 47% (32/67) · rebond 69% (22/32)
      · −2.0% : fill 35% (22/67) · rebond 67% (16/22)
      · −3.0% : fill 21% (11/67) · rebond 67% (7/11)
      · −4.0% : fill 18% (9/67) · rebond 84% (6/9)
      · −5.0% : fill 7% (5/67) · rebond 88% (4/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 47% si les 15 1res min sont vertes (72 cas) · 36% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.76% .. +2.7%] · haut q95 +3.69% · bas q05 -4.13%
   - 60min (n=160) : retour [-4.91% .. +3.31%] · haut q95 +4.08% · bas q05 -5.28%
   - session (n=160) : retour [-5.89% .. +5.21%] · haut q95 +7.89% · bas q05 -8.32%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.57 · part idiosyncratique 0.43
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bearish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.3  _(survente)_
- **ADX** : 30.0  _(tendance etablie)_
- **MACD** : hist -2.815  _(pas de croisement recent)_
- **BB** : %B -0.02 · largeur 59.0%
- **ATR** : 10.15 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.317  _(distribution)_
- **Vol ratio** : 1.82  _(volume au-dessus de la moyenne)_
- **Choppiness** : 38.6  _(transition)_
- **MA** : MA20 122.62 · MA50 151.77 · MA200 187.18  _(prix < MA20)_
- **Dist MA** : MA20 -30.4% · MA50 -43.8% · MA200 -54.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (40084 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

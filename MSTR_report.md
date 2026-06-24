# MSTR

**Generated** : 2026-06-24T21:47:18.762785+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $94.13  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $94.13 (+11.7% vs entrée) · entrée $84.26 · stop $81.30 · T1 $86.65 · R/R 0.81  
> ↳ P(T1 av. stop) 35 % · EV/risk -0.041 · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -204 % hors [0,100] (R² max 0.04). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $83.78–$84.74 (mid $84.26)
- Spot actuel : $94.13 (+11.7% au-dessus de la zone — repli à attendre)
- Stop : $81.30 (stop swing_plan-based (-24.11%))
- Targets : T1 $86.65 · R/R 0.81 | T2 $89.05 · R/R 1.62 | T3 $91.44 · R/R 2.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $81.30


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : $-0.120 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 9 % | T3 2 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 81.7 | side 13.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→51% · +3.0%→31% · +5.0%→9% · +8.0%→4%
- Range intraday médian 5.11% (p90 8.46%) · excursion haute méd. +2.12% / basse méd. −2.84%
- Profil de vol intra : ouverture 2.992% vs midi 1.177% vs clôture 1.211% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.024)_ ; drift intra méd. -1.236% ; recovery-V 31%
- **σ réalisé intraday** 3.729% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 73% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 106.0435 (VA 104.7045–106.6615 ; dernier close 103.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 65% · **stop −4.57%** sous le fill (sous le bruit) · cible +1.42% · R/R 0.31 (high win-rate)
- Gaps overnight (n=159) : méd. -0.22% · baisse 56% (gap-down >1% 39% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.91% (p90 −2.06%) · haut méd +0.59% · range méd 1.84%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.02%) · haut méd +0.82% · range méd 2.37%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.48%) · haut méd +1.09% · range méd 2.97%
- Excursion ouverture 60min (n=160) : bas méd −1.74% (p90 −4.23%) · haut méd +1.45% · range méd 3.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 103.85 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 80% (127/159) · gap 47% · délai 0.0min · rebond 49% (64/127) (MFE +0.97%)
   - −1.0% : fill 30min 64% · séance 77% (122/159) · gap 39% · délai 0.0min · rebond 57% (70/122) (MFE +1.46%)
   - −1.5% : fill 30min 56% · séance 73% (114/159) · gap 29% · délai 0.0min · rebond 57% (69/114) (MFE +1.44%)
   - −2.0% : fill 30min 47% · séance 64% (102/159) · gap 24% · délai 1.1min · rebond 52% (64/102) (MFE +1.04%)
   - −3.0% : fill 30min 30% · séance 51% (78/159) · gap 14% · délai 8.7min · rebond 55% (48/78) (MFE +1.46%)
   - −4.0% : fill 30min 19% · séance 44% (64/159) · gap 6% · délai 47.0min · rebond 58% (40/64) (MFE +1.18%)
   - −5.0% : fill 30min 14% · séance 33% (50/159) · gap 3% · délai 73.9min · rebond 65% (35/50) (MFE +1.42%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.79%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.1% (p90 −2.84%) → stop au-delà de −2.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.19% (p90 −2.83%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=961 jambes) : jambe baissière méd −1.21% (p90 −2.73%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 99% (74/75) · rebond 48% (38/74)
      · −2.0% : fill 88% (67/75) · rebond 46% (39/67)
      · −3.0% : fill 77% (58/75) · rebond 55% (36/58)
      · −4.0% : fill 64% (48/75) · rebond 58% (32/48)
      · −5.0% : fill 54% (40/75) · rebond 69% (29/40)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 47% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.76% .. +2.73%] · haut q95 +3.71% · bas q05 -4.12%
   - 60min (n=160) : retour [-4.92% .. +3.31%] · haut q95 +4.09% · bas q05 -5.29%
   - session (n=160) : retour [-5.74% .. +5.22%] · haut q95 +7.92% · bas q05 -8.13%


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.5  _(momentum baissier)_
- **ADX** : 28.5  _(tendance etablie)_
- **MACD** : hist -2.106  _(pas de croisement recent)_
- **BB** : %B 0.03 · largeur 54.4%
- **ATR** : 9.87 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.269  _(distribution)_
- **Vol ratio** : 1.71  _(volume au-dessus de la moyenne)_
- **Choppiness** : 43.4  _(transition)_
- **MA** : MA20 126.07 · MA50 152.81 · MA200 188.41  _(prix < MA20)_
- **Dist MA** : MA20 -25.3% · MA50 -38.4% · MA200 -50.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (40286 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

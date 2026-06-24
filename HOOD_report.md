# HOOD

**Generated** : 2026-06-24T00:21:58.762859+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $103.25  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $103.25 (+2.6% vs entrée) · entrée $100.64 · stop $97.44 · T1 $107.04 · R/R 2.0  
> ↳ P(T1 av. stop) 45 % _(réel 5 s)_ · EV/risk 0.273 _(réel 5 s)_ (GBM 0.116) · ¼-Kelly 0.006 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $99.36–$101.92 (mid $100.64)
- Spot actuel : $103.25 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : $97.44 (stop swing_plan-based (-5.62%))
- Targets : T1 $107.04 · R/R 2.0 | T2 $113.44 · R/R 4.0 | T3 $119.83 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $97.44


## Edge, scénarios & sizing

- EV/risk : 0.116 | EV/share : $0.372 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 36.6 | bear 23.4 | side 39.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 620.0 (= 6 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.144% → cible +2.843% / stop −2.141%, p_fill 78%, n_eff≈31.4) : P(cible|rempli) **34%** · **EV/risk +0.035** (×p_fill ; si rempli +0.10% du capital)
  - **swing** (entrée dip −2.522% → cible +6.357% / stop −3.178%, p_fill 66%, n_eff≈25.9) : P(cible|rempli) **45%** · **EV/risk +0.273** (×p_fill ; si rempli +1.31% du capital)
  - **deep** (entrée dip −3.901% → cible +8.99% / stop −4.495%, p_fill 65%, n_eff≈23.4) : P(cible|rempli) **49%** · **EV/risk +0.290** (×p_fill ; si rempli +2.02% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→52% · +3.0%→36% · +5.0%→16% · +8.0%→5%
- Range intraday médian 4.85% (p90 8.55%) · excursion haute méd. +2.07% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.238% vs midi 1.047% vs clôture 1.002% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 17% · trend ↑1%/↓0% ; spike-down 64% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; momentum — autocorr 0.044)_ ; drift intra méd. 0.897% ; recovery-V 43%
- **σ réalisé intraday** 3.612% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 43% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 106.8173 (VA 106.1033–108.9592 ; dernier close 105.71)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 22% · rebond 84% · **stop −4.94%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 53% (gap-down >1% 34% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.82% (p90 −1.88%) · haut méd +0.78% · range méd 1.92%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −2.66%) · haut méd +0.99% · range méd 2.53%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.23%) · haut méd +1.13% · range méd 3.0%
- Excursion ouverture 60min (n=160) : bas méd −1.76% (p90 −3.78%) · haut méd +1.5% · range méd 3.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 105.71 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (122/159) · gap 41% · délai 0.0min · rebond 54% (62/122) (MFE +1.37%)
   - −1.0% : fill 30min 56% · séance 64% (107/159) · gap 34% · délai 0.0min · rebond 52% (58/107) (MFE +1.23%)
   - −1.5% : fill 30min 49% · séance 61% (100/159) · gap 24% · délai 0.0min · rebond 52% (54/100) (MFE +1.22%)
   - −2.0% : fill 30min 42% · séance 56% (91/159) · gap 17% · délai 0.5min · rebond 60% (53/91) (MFE +1.26%)
   - −3.0% : fill 30min 30% · séance 42% (69/159) · gap 8% · délai 10.4min · rebond 66% (44/69) (MFE +1.63%)
   - −4.0% : fill 30min 17% · séance 31% (52/159) · gap 4% · délai 13.9min · rebond 69% (32/52) (MFE +1.87%)
   - −5.0% : fill 30min 12% · séance 22% (36/159) · gap 2% · délai 28.2min · rebond 84% (29/36) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.66%) → stop au-delà de −1.78% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.65% (p90 −2.44%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.69% (p90 −2.5%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=754 jambes) : jambe baissière méd −1.12% (p90 −2.68%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 94% (68/72) · rebond 48% (34/68)
      · −2.0% : fill 84% (59/72) · rebond 57% (33/59)
      · −3.0% : fill 68% (48/72) · rebond 63% (30/48)
      · −4.0% : fill 55% (39/72) · rebond 76% (27/39)
      · −5.0% : fill 42% (30/72) · rebond 83% (25/30)
   - **flat** (20 séances) :
      · −1.0% : fill 72% (15/20) · rebond 64% (10/15)
      · −2.0% : fill 64% (11/20) · rebond 48% (6/11)
      · −3.0% : fill 28% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 26% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 13% (3/20) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 33% (24/67) · rebond 59% (14/24)
      · −2.0% : fill 26% (21/67) · rebond 79% (14/21)
      · −3.0% : fill 19% (15/67) · rebond 92% (12/15)
      · −4.0% : fill 9% (8/67) · rebond 70% (4/8)
      · −5.0% : fill 5% (3/67) · rebond 94% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 70% si les 15 1res min sont vertes (69 cas) · 40% si rouges (91 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.14% .. +3.96%] · haut q95 +4.47% · bas q05 -3.84%
   - 60min (n=160) : retour [-3.65% .. +5.02%] · haut q95 +5.17% · bas q05 -4.16%
   - session (n=160) : retour [-4.65% .. +6.41%] · haut q95 +9.24% · bas q05 -7.36%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.63 · part idiosyncratique 0.37
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 64.3  _(momentum haussier)_
- **ADX** : 27.7  _(tendance etablie)_
- **MACD** : hist 1.747  _(pas de croisement recent)_
- **BB** : %B 0.82 · largeur 42.4%
- **ATR** : 7.28 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.197  _(accumulation)_
- **Vol ratio** : 1.11  _(volume normal)_
- **Choppiness** : 42.1  _(transition)_
- **MA** : MA20 90.99 · MA50 84.2 · MA200 102.82  _(prix > MA20)_
- **Dist MA** : MA20 +13.5% · MA50 +22.6% · MA200 +0.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (44501 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

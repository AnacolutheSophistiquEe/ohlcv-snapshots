# HOOD

**Generated** : 2026-06-25T21:58:45.899536+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $93.47  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)  
> ↳ spot $93.47 (+19.1% vs entrée) · entrée $78.50 · stop $75.82 · T1 $83.87 · R/R 2.0  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.075 · ¼-Kelly 0.004 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $77.43–$79.58 (mid $78.50)
- Spot actuel : $93.47 (+19.1% au-dessus de la zone — repli à attendre)
- Stop : $75.82 (stop swing_plan-based (-18.88%))
- Targets : T1 $83.87 · R/R 2.0 | T2 $89.23 · R/R 4.0 | T3 $94.60 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $75.82


## Edge, scénarios & sizing

- EV/risk : 0.075 | EV/share : $0.200 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 19 % | T3 9 %
- Kelly (position) : f* 0.015 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 31.0 | bear 22.9 | side 46.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 467.0 (= 5 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→51% · +3.0%→35% · +5.0%→15% · +8.0%→5%
- Range intraday médian 4.84% (p90 8.55%) · excursion haute méd. +2.05% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.28% vs midi 1.069% vs clôture 1.002% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑1%/↓0% ; spike-down 64% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; momentum — autocorr 0.041)_ ; drift intra méd. 0.646% ; recovery-V 41%
- **σ réalisé intraday** 3.664% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 44% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 96.9834 (VA 96.3976–99.5216 ; dernier close 97.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 85% · **stop −4.78%** sous le fill (sous le bruit) · cible +2.37% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 55% (gap-down >1% 34% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −1.86%) · haut méd +0.82% · range méd 1.97%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −2.87%) · haut méd +1.03% · range méd 2.56%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.52%) · haut méd +1.3% · range méd 3.07%
- Excursion ouverture 60min (n=160) : bas méd −1.76% (p90 −3.84%) · haut méd +1.59% · range méd 3.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 97.21 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 78% (122/159) · gap 43% · délai 0.0min · rebond 54% (62/122) (MFE +1.37%)
   - −1.0% : fill 30min 57% · séance 66% (107/159) · gap 34% · délai 0.0min · rebond 55% (59/107) (MFE +1.27%)
   - −1.5% : fill 30min 51% · séance 62% (100/159) · gap 25% · délai 0.0min · rebond 52% (54/100) (MFE +1.22%)
   - −2.0% : fill 30min 44% · séance 58% (91/159) · gap 18% · délai 0.5min · rebond 60% (53/91) (MFE +1.26%)
   - −3.0% : fill 30min 32% · séance 44% (70/159) · gap 9% · délai 10.0min · rebond 64% (45/70) (MFE +1.63%)
   - −4.0% : fill 30min 20% · séance 34% (53/159) · gap 4% · délai 11.7min · rebond 73% (34/53) (MFE +1.94%)
   - −5.0% : fill 30min 13% · séance 23% (36/159) · gap 2% · délai 21.5min · rebond 85% (29/36) (MFE +2.37%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.61%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.44%) → stop au-delà de −1.65% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −2.48%) → stop au-delà de −1.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=758 jambes) : jambe baissière méd −1.14% (p90 −2.72%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 95% (69/73) · rebond 52% (36/69)
      · −2.0% : fill 85% (60/73) · rebond 57% (34/60)
      · −3.0% : fill 71% (49/73) · rebond 62% (31/49)
      · −4.0% : fill 58% (40/73) · rebond 79% (29/40)
      · −5.0% : fill 42% (30/73) · rebond 85% (25/30)
   - **flat** (20 séances) :
      · −1.0% : fill 72% (15/20) · rebond 64% (10/15)
      · −2.0% : fill 64% (11/20) · rebond 48% (6/11)
      · −3.0% : fill 28% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 26% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 13% (3/20) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 33% (23/66) · rebond 58% (13/23)
      · −2.0% : fill 26% (20/66) · rebond 78% (13/20)
      · −3.0% : fill 19% (15/66) · rebond 92% (12/15)
      · −4.0% : fill 9% (8/66) · rebond 70% (4/8)
      · −5.0% : fill 5% (3/66) · rebond 94% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 71% si les 15 1res min sont vertes (70 cas) · 38% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.39% .. +3.93%] · haut q95 +4.43% · bas q05 -3.95%
   - 60min (n=160) : retour [-3.65% .. +4.98%] · haut q95 +5.16% · bas q05 -4.65%
   - session (n=160) : retour [-4.88% .. +6.35%] · haut q95 +9.0% · bas q05 -7.31%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.38
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.0  _(momentum haussier)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist 0.204  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 34.6%
- **ATR** : 7.48 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.127  _(accumulation)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 43.1  _(transition)_
- **MA** : MA20 93.0 · MA50 84.99 · MA200 102.68  _(prix > MA20)_
- **Dist MA** : MA20 +0.5% · MA50 +10.0% · MA200 -9.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (42536 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# HOOD

**Generated** : 2026-06-24T21:57:55.439453+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · $97.19  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $97.19 (+18.1% vs entrée) · entrée $82.30 · stop $79.55 · T1 $87.82 · R/R 2.01  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.115 · ¼-Kelly 0.006 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $81.20–$83.41 (mid $82.30)
- Spot actuel : $97.19 (+18.1% au-dessus de la zone — repli à attendre)
- Stop : $79.55 (stop swing_plan-based (-18.15%))
- Targets : T1 $87.82 · R/R 2.01 | T2 $93.33 · R/R 4.01 | T3 $98.85 · R/R 6.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $79.55


## Edge, scénarios & sizing

- EV/risk : 0.115 | EV/share : $0.318 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 42.8 | bear 22.5 | side 34.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 583.0 (= 6 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→52% · +3.0%→36% · +5.0%→16% · +8.0%→5%
- Range intraday médian 4.84% (p90 8.55%) · excursion haute méd. +2.07% / basse méd. −2.19%
- Profil de vol intra : ouverture 3.252% vs midi 1.064% vs clôture 1.005% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 63% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; momentum — autocorr 0.042)_ ; drift intra méd. 0.924% ; recovery-V 43%
- **σ réalisé intraday** 3.599% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 41% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 105.1069 (VA 103.7419–105.7894 ; dernier close 103.18)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 22% · rebond 84% · **stop −4.94%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 54% (gap-down >1% 35% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −1.87%) · haut méd +0.8% · range méd 1.95%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −2.65%) · haut méd +1.01% · range méd 2.55%
- Excursion ouverture 30min (n=160) : bas méd −1.32% (p90 −3.22%) · haut méd +1.25% · range méd 3.02%
- Excursion ouverture 60min (n=160) : bas méd −1.7% (p90 −3.76%) · haut méd +1.53% · range méd 3.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 103.18 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 77% (122/159) · gap 42% · délai 0.0min · rebond 53% (61/122) (MFE +1.36%)
   - −1.0% : fill 30min 57% · séance 65% (107/159) · gap 35% · délai 0.0min · rebond 54% (58/107) (MFE +1.26%)
   - −1.5% : fill 30min 50% · séance 62% (100/159) · gap 26% · délai 0.0min · rebond 54% (54/100) (MFE +1.25%)
   - −2.0% : fill 30min 43% · séance 57% (91/159) · gap 19% · délai 0.4min · rebond 62% (53/91) (MFE +1.28%)
   - −3.0% : fill 30min 31% · séance 43% (70/159) · gap 9% · délai 7.8min · rebond 67% (45/70) (MFE +1.71%)
   - −4.0% : fill 30min 19% · séance 33% (53/159) · gap 4% · délai 12.2min · rebond 71% (33/53) (MFE +1.96%)
   - −5.0% : fill 30min 12% · séance 22% (36/159) · gap 2% · délai 28.2min · rebond 84% (29/36) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.63%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.44%) → stop au-delà de −1.65% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −2.48%) → stop au-delà de −1.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=757 jambes) : jambe baissière méd −1.12% (p90 −2.66%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (73 séances) :
      · −1.0% : fill 94% (69/73) · rebond 50% (35/69)
      · −2.0% : fill 85% (60/73) · rebond 59% (34/60)
      · −3.0% : fill 70% (49/73) · rebond 65% (31/49)
      · −4.0% : fill 57% (40/73) · rebond 77% (28/40)
      · −5.0% : fill 40% (30/73) · rebond 83% (25/30)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 71% si les 15 1res min sont vertes (70 cas) · 40% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.14% .. +3.94%] · haut q95 +4.45% · bas q05 -3.84%
   - 60min (n=160) : retour [-3.65% .. +5.0%] · haut q95 +5.17% · bas q05 -4.15%
   - session (n=160) : retour [-4.65% .. +6.36%] · haut q95 +9.12% · bas q05 -7.33%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 63.4  _(momentum haussier)_
- **ADX** : 27.0  _(tendance etablie)_
- **MACD** : hist 1.005  _(pas de croisement recent)_
- **BB** : %B 0.64 · largeur 38.5%
- **ATR** : 7.44 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.177  _(accumulation)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 42.9  _(transition)_
- **MA** : MA20 92.14 · MA50 84.71 · MA200 102.8  _(prix > MA20)_
- **Dist MA** : MA20 +5.5% · MA50 +14.7% · MA200 -5.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (42839 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

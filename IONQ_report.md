# IONQ

**Generated** : 2026-06-24T00:16:37.838684+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $57.85  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $57.85 (+4.0% vs entrée) · entrée $55.62 · stop $53.84 · T1 $57.44 · R/R 1.02  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.126 _(réel 5 s)_ (GBM -0.011) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $55.26–$55.98 (mid $55.62)
- Spot actuel : $57.85 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : $53.84 (stop swing_plan-based (-11.83%))
- Targets : T1 $57.44 · R/R 1.02 | T2 $59.26 · R/R 2.04 | T3 $61.09 · R/R 3.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $53.84


## Edge, scénarios & sizing

- EV/risk : -0.011 | EV/share : $-0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 17 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 7.9 | bear 11.6 | side 80.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 116.0 (= 2 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.856% → cible +3.275% / stop −3.198%, p_fill 52%, n_eff≈20.4) : P(cible|rempli) **50%** · **EV/risk +0.126** (×p_fill ; si rempli +0.77% du capital)
  - **swing** (entrée dip −8.479% → cible +7.323% / stop −3.662%, p_fill 36%, n_eff≈11.6) : P(cible|rempli) **33%** · **EV/risk -0.025** (×p_fill ; si rempli -0.25% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→85% · +2.0%→69% · +3.0%→57% · +5.0%→30% · +8.0%→16%
- Range intraday médian 7.58% (p90 12.54%) · excursion haute méd. +3.58% / basse méd. −2.91%
- Profil de vol intra : ouverture 4.608% vs midi 1.613% vs clôture 1.683% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓1% ; spike-down 75% · recovery-V 44%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.023)_ ; drift intra méd. 0.667% ; recovery-V 46%
- **σ réalisé intraday** 5.35% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 48% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 59.7999 (VA 57.8709–60.6036 ; dernier close 58.32)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 83% · **stop −5.08%** sous le fill (sous le bruit) · cible +3.51% · R/R 0.69 (high win-rate)
- Gaps overnight (n=159) : méd. -0.24% · baisse 51% (gap-down >1% 38% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.32% (p90 −2.99%) · haut méd +0.99% · range méd 2.56%
- Excursion ouverture 15min (n=160) : bas méd −1.85% (p90 −3.9%) · haut méd +1.33% · range méd 3.54%
- Excursion ouverture 30min (n=160) : bas méd −2.05% (p90 −5.16%) · haut méd +1.76% · range méd 4.22%
- Excursion ouverture 60min (n=160) : bas méd −2.5% (p90 −5.68%) · haut méd +2.12% · range méd 5.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 58.32 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (133/159) · gap 46% · délai 0.0min · rebond 75% (95/133) (MFE +2.26%)
   - −1.0% : fill 30min 72% · séance 80% (126/159) · gap 38% · délai 0.0min · rebond 79% (93/126) (MFE +2.72%)
   - −1.5% : fill 30min 67% · séance 76% (120/159) · gap 29% · délai 0.0min · rebond 72% (83/120) (MFE +2.53%)
   - −2.0% : fill 30min 57% · séance 71% (113/159) · gap 19% · délai 0.9min · rebond 72% (79/113) (MFE +2.71%)
   - −3.0% : fill 30min 47% · séance 59% (91/159) · gap 12% · délai 6.9min · rebond 77% (68/91) (MFE +3.42%)
   - −4.0% : fill 30min 30% · séance 47% (74/159) · gap 6% · délai 15.8min · rebond 80% (56/74) (MFE +3.42%)
   - −5.0% : fill 30min 19% · séance 41% (66/159) · gap 3% · délai 32.1min · rebond 83% (55/66) (MFE +3.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.98% (p90 −2.91%) → stop au-delà de −2.56% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.21% (p90 −3.75%) → stop au-delà de −2.71% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.33% (p90 −3.79%) → stop au-delà de −2.75% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1111 jambes) : jambe baissière méd −1.35% (p90 −3.23%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 100% (70/70) · rebond 77% (52/70)
      · −2.0% : fill 92% (65/70) · rebond 77% (50/65)
      · −3.0% : fill 80% (55/70) · rebond 78% (44/55)
      · −4.0% : fill 64% (44/70) · rebond 79% (35/44)
      · −5.0% : fill 57% (39/70) · rebond 78% (32/39)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 81% (9/14)
      · −2.0% : fill 60% (13/17) · rebond 49% (7/13)
      · −3.0% : fill 45% (10/17) · rebond 52% (6/10)
      · −4.0% : fill 40% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 40% (7/17) · rebond 91% (6/7)
   - **gap-up** (72 séances) :
      · −1.0% : fill 56% (42/72) · rebond 83% (32/42)
      · −2.0% : fill 48% (35/72) · rebond 70% (22/35)
      · −3.0% : fill 37% (26/72) · rebond 83% (18/26)
      · −4.0% : fill 27% (23/72) · rebond 86% (18/23)
      · −5.0% : fill 22% (20/72) · rebond 95% (17/20)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 61% si les 15 1res min sont vertes (78 cas) · 43% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.86% .. +7.22%] · haut q95 +7.71% · bas q05 -5.71%
   - 60min (n=160) : retour [-5.02% .. +8.06%] · haut q95 +11.26% · bas q05 -6.2%
   - session (n=160) : retour [-7.46% .. +9.71%] · haut q95 +12.95% · bas q05 -10.36%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.36 · part idiosyncratique 0.64
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.0  _(momentum baissier)_
- **ADX** : 21.4  _(pas de tendance nette)_
- **MACD** : hist -1.182  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 37.6%
- **ATR** : 5.93 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.086  _(distribution)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 52.6  _(transition)_
- **MA** : MA20 61.96 · MA50 53.62 · MA200 49.45  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 +7.9% · MA200 +17.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (43475 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

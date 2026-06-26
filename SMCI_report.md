# SMCI

**Generated** : 2026-06-26T21:48:33.605783+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 10.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $30.63  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot $30.63 (+10.0% vs entrée) · entrée $27.84 · stop $26.75 · T1 $29.41 · R/R 1.44  
> ↳ P(T1 av. stop) 16 % · EV/risk -0.009 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $27.53–$28.16 (mid $27.84)
- Spot actuel : $30.63 (+10.0% au-dessus de la zone — repli à attendre)
- Stop : $26.75 (stop swing_plan-based (-25.05%))
- Targets : T1 $29.41 · R/R 1.44 | T2 $30.97 · R/R 2.87 | T3 $32.54 · R/R 4.31
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $26.75


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : $-0.010 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 1 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 8.6 | bear 15.0 | side 76.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→65% · +3.0%→46% · +5.0%→30% · +8.0%→12%
- Range intraday médian 6.17% (p90 10.16%) · excursion haute méd. +2.83% / basse méd. −2.54%
- Profil de vol intra : ouverture 3.728% vs midi 1.268% vs clôture 1.446% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑0%/↓2% ; spike-down 65% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.159 ; mean-reverting — autocorr -0.03)_ ; drift intra méd. 0.278% ; recovery-V 32%
- **σ réalisé intraday** 4.542% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 62% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 31.8424 (VA 31.6154–32.1261 ; dernier close 31.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 62% · **stop −4.67%** sous le fill (sous le bruit) · cible +1.94% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 46% (gap-down >1% 30% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −0.82% (p90 −2.74%) · haut méd +0.91% · range méd 1.96%
- Excursion ouverture 15min (n=160) : bas méd −1.17% (p90 −3.33%) · haut méd +1.21% · range méd 2.79%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −4.06%) · haut méd +1.38% · range méd 3.47%
- Excursion ouverture 60min (n=160) : bas méd −1.63% (p90 −4.33%) · haut méd +1.67% · range méd 4.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 31.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 75% (126/159) · gap 41% · délai 0.0min · rebond 60% (73/126) (MFE +1.32%)
   - −1.0% : fill 30min 59% · séance 69% (113/159) · gap 30% · délai 0.0min · rebond 57% (63/113) (MFE +1.53%)
   - −1.5% : fill 30min 49% · séance 63% (98/159) · gap 25% · délai 0.8min · rebond 64% (58/98) (MFE +1.5%)
   - −2.0% : fill 30min 43% · séance 57% (87/159) · gap 20% · délai 2.4min · rebond 66% (53/87) (MFE +1.91%)
   - −3.0% : fill 30min 28% · séance 49% (67/159) · gap 17% · délai 8.4min · rebond 56% (38/67) (MFE +1.86%)
   - −4.0% : fill 30min 21% · séance 38% (49/159) · gap 13% · délai 12.1min · rebond 60% (29/49) (MFE +1.31%)
   - −5.0% : fill 30min 17% · séance 31% (40/159) · gap 8% · délai 15.8min · rebond 62% (26/40) (MFE +1.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.07%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.98%) → stop au-delà de −1.77% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −2.77%) → stop au-delà de −2.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=817 jambes) : jambe baissière méd −1.22% (p90 −2.78%) · ~11.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (67/68) · rebond 53% (37/67)
      · −2.0% : fill 88% (59/68) · rebond 56% (31/59)
      · −3.0% : fill 81% (51/68) · rebond 58% (29/51)
      · −4.0% : fill 68% (40/68) · rebond 63% (24/40)
      · −5.0% : fill 56% (33/68) · rebond 60% (21/33)
   - **flat** (16 séances) :
      · −1.0% : fill 92% (14/16) · rebond 81% (10/14)
      · −2.0% : fill 60% (10/16) · rebond 78% (7/10)
      · −3.0% : fill 13% (2/16) · rebond 100% (2/2)
      · −4.0% : fill 4% (1/16) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/16) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 39% (32/75) · rebond 57% (16/32)
      · −2.0% : fill 27% (18/75) · rebond 95% (15/18)
      · −3.0% : fill 24% (14/75) · rebond 46% (7/14)
      · −4.0% : fill 16% (8/75) · rebond 45% (4/8)
      · −5.0% : fill 13% (7/75) · rebond 69% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 76% si les 15 1res min sont vertes (70 cas) · 30% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.24% .. +4.77%] · haut q95 +6.53% · bas q05 -4.54%
   - 60min (n=160) : retour [-4.55% .. +5.58%] · haut q95 +6.6% · bas q05 -5.45%
   - session (n=160) : retour [-7.11% .. +8.81%] · haut q95 +9.58% · bas q05 -8.54%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.2  _(momentum baissier)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist -0.718  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 82.6%
- **ATR** : 3.66 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.08  _(distribution)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 41.2  _(transition)_
- **MA** : MA20 36.87 · MA50 33.5 · MA200 35.35  _(prix < MA20)_
- **Dist MA** : MA20 -16.9% · MA50 -8.6% · MA200 -13.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39048 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

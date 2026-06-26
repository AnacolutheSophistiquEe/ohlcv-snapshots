# SMR

**Generated** : 2026-06-26T21:55:54.481119+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $10.10  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $10.10 (+1.1% vs entrée) · entrée $9.99 · stop $9.47 · T1 $11.03 · R/R 2.0  
> ↳ P(T1 av. stop) 2 % _(réel 5 s)_ · EV/risk -0.147 _(réel 5 s)_ (GBM -0.003) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.92–$10.07 (mid $9.99)
- Spot actuel : $10.10 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $9.47 (stop swing_plan-based (-6.5%))
- Targets : T1 $11.03 · R/R 2.0 | T2 $11.07 · R/R 2.08 | T3 $11.12 · R/R 2.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.47


## Edge, scénarios & sizing

- EV/risk : -0.003 | EV/share : $-0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 4 % | T2 4 % | T3 3 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 21.4 | bear 47.8 | side 30.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.072% → cible +10.346% / stop −5.174%, p_fill 66%, n_eff≈29.1) : P(cible|rempli) **2%** · **EV/risk -0.147** (×p_fill ; si rempli -1.16% du capital)
  - **swing** (entrée dip −2.363% → cible +8.452% / stop −4.227%, p_fill 64%, n_eff≈30.1) : P(cible|rempli) **41%** · **EV/risk +0.126** (×p_fill ; si rempli +0.83% du capital)
  - **deep** (entrée dip −3.66% → cible +34.127% / stop −17.064%, p_fill 75%, n_eff≈32.5) : P(cible|rempli) **7%** · **EV/risk -0.147** (×p_fill ; si rempli -3.32% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→66% · +3.0%→54% · +5.0%→35% · +8.0%→19%
- Range intraday médian 7.23% (p90 12.61%) · excursion haute méd. +3.11% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.79% vs midi 1.545% vs clôture 1.837% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 72% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; neutre — autocorr 0.008)_ ; drift intra méd. 0.418% ; recovery-V 25%
- **σ réalisé intraday** 5.401% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 42% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 10.143 (VA 10.017–10.215 ; dernier close 10.08)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 58% · rebond 75% · **stop −6.0%** sous le fill (sous le bruit) · cible +3.39% · R/R 0.57 (high win-rate)
- Gaps overnight (n=159) : méd. -0.77% · baisse 62% (gap-down >1% 44% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −1.39% (p90 −3.6%) · haut méd +1.1% · range méd 2.95%
- Excursion ouverture 15min (n=160) : bas méd −1.79% (p90 −3.99%) · haut méd +1.35% · range méd 3.89%
- Excursion ouverture 30min (n=160) : bas méd −2.14% (p90 −5.61%) · haut méd +1.91% · range méd 4.31%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −6.23%) · haut méd +2.56% · range méd 5.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 10.08 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 77% · séance 82% (132/159) · gap 55% · délai 0.0min · rebond 63% (80/132) (MFE +1.64%)
   - −1.0% : fill 30min 72% · séance 78% (126/159) · gap 44% · délai 0.0min · rebond 66% (83/126) (MFE +1.93%)
   - −1.5% : fill 30min 69% · séance 74% (120/159) · gap 40% · délai 0.0min · rebond 72% (86/120) (MFE +2.21%)
   - −2.0% : fill 30min 64% · séance 70% (114/159) · gap 29% · délai 0.1min · rebond 69% (83/114) (MFE +2.52%)
   - −3.0% : fill 30min 53% · séance 63% (103/159) · gap 13% · délai 2.1min · rebond 77% (84/103) (MFE +3.09%)
   - −4.0% : fill 30min 43% · séance 58% (88/159) · gap 7% · délai 6.8min · rebond 75% (68/88) (MFE +3.39%)
   - −5.0% : fill 30min 27% · séance 43% (65/159) · gap 4% · délai 14.5min · rebond 71% (47/65) (MFE +1.98%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −3.07%) → stop au-delà de −2.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.02% (p90 −3.78%) → stop au-delà de −2.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.06% (p90 −3.88%) → stop au-delà de −2.5% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1207 jambes) : jambe baissière méd −1.36% (p90 −3.16%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 100% (83/83) · rebond 70% (54/83)
      · −2.0% : fill 92% (79/83) · rebond 74% (59/79)
      · −3.0% : fill 85% (76/83) · rebond 80% (63/76)
      · −4.0% : fill 78% (66/83) · rebond 79% (54/66)
      · −5.0% : fill 59% (47/83) · rebond 79% (36/47)
   - **flat** (13 séances) :
      · −1.0% : fill 71% (10/13) · rebond 55% (7/10)
      · −2.0% : fill 55% (8/13) · rebond 43% (5/8)
      · −3.0% : fill 50% (6/13) · rebond 42% (4/6)
      · −4.0% : fill 50% (6/13) · rebond 57% (3/6)
      · −5.0% : fill 34% (4/13) · rebond 51% (3/4)
   - **gap-up** (63 séances) :
      · −1.0% : fill 47% (33/63) · rebond 56% (22/33)
      · −2.0% : fill 40% (27/63) · rebond 58% (19/27)
      · −3.0% : fill 33% (21/63) · rebond 76% (17/21)
      · −4.0% : fill 29% (16/63) · rebond 67% (11/16)
      · −5.0% : fill 21% (14/63) · rebond 44% (8/14)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 65% si les 15 1res min sont vertes (63 cas) · 37% si rouges (97 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **53min** → P(séance verte=clôture>ouverture) 78% si début vert vs 17% si rouge (base 49% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 164min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **78%** · continue >prix actuel 44% ; creux résiduel méd -2.6% (q20 -4.08%) → **SL/trailing à −4.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.6% / q75 +5.02% → **scale +2.6% / runner +5.02%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.39%** (au-delà de la MAE q10 -7.39%), cible rebond +2.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.91% .. +4.6%] · haut q95 +6.6% · bas q05 -6.9%
   - 60min (n=160) : retour [-6.59% .. +6.07%] · haut q95 +8.9% · bas q05 -8.08%
   - 2h (n=160) : retour [-8.11% .. +10.06%] · haut q95 +11.48% · bas q05 -9.59%
   - 4h (n=160) : retour [-9.05% .. +8.43%] · haut q95 +11.49% · bas q05 -11.05%
   - 6h (n=160) : retour [-8.71% .. +8.76%] · haut q95 +11.69% · bas q05 -11.1%
   - session (n=160) : retour [-8.83% .. +10.98%] · haut q95 +11.74% · bas q05 -11.13%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.48 · part idiosyncratique 0.52
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.3  _(neutre)_
- **ADX** : 12.2  _(pas de tendance nette)_
- **MACD** : hist -0.021  _(bearish_recent)_
- **BB** : %B 0.33 · largeur 45.8%
- **ATR** : 0.95 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.107  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 59.9  _(transition)_
- **MA** : MA20 10.94 · MA50 11.59 · MA200 20.09  _(prix < MA20)_
- **Dist MA** : MA20 -7.7% · MA50 -12.8% · MA200 -49.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (67887 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

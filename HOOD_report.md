# HOOD

**Generated** : 2026-06-26T21:57:17.205420+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $98.69  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $98.69 (+0.4% vs entrée) · entrée $98.26 · stop $96.07 · T1 $101.06 · R/R 1.28  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.088 _(réel 5 s)_ (GBM 0.042) · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $97.83–$98.69 (mid $98.26)
- Spot actuel : $98.69 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $96.07 (stop swing_plan-based (-4.08%))
- Targets : T1 $101.06 · R/R 1.28 | T2 $103.87 · R/R 2.56 | T3 $106.67 · R/R 3.84
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $96.07


## Edge, scénarios & sizing

- EV/risk : 0.042 | EV/share : $0.092 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 10 % | T3 2 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 67.4 | bear 15.8 | side 16.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 395.0 (= 4 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.439% → cible +2.854% / stop −2.231%, p_fill 91%, n_eff≈37.4) : P(cible|rempli) **31%** · **EV/risk -0.088** (×p_fill ; si rempli -0.22% du capital)
  - **swing** (entrée dip −0.919% → cible +6.382% / stop −3.191%, p_fill 87%, n_eff≈36.3) : P(cible|rempli) **31%** · **EV/risk -0.083** (×p_fill ; si rempli -0.30% du capital)
  - **deep** (entrée dip −1.338% → cible +9.025% / stop −4.513%, p_fill 88%, n_eff≈35.2) : P(cible|rempli) **45%** · **EV/risk +0.333** (×p_fill ; si rempli +1.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→76% · +2.0%→50% · +3.0%→34% · +5.0%→15% · +8.0%→5%
- Range intraday médian 4.84% (p90 8.55%) · excursion haute méd. +2.0% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.319% vs midi 1.072% vs clôture 0.995% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑1%/↓0% ; spike-down 64% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; momentum — autocorr 0.053)_ ; drift intra méd. 0.367% ; recovery-V 38%
- **σ réalisé intraday** 3.696% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 42% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 94.4942 (VA 94.1773–96.0793 ; dernier close 93.49)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 22% · rebond 85% · **stop −4.79%** sous le fill (sous le bruit) · cible +2.36% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.08% · baisse 54% (gap-down >1% 33% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −0.81% (p90 −1.99%) · haut méd +0.8% · range méd 1.98%
- Excursion ouverture 15min (n=160) : bas méd −1.16% (p90 −3.04%) · haut méd +1.02% · range méd 2.57%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.83%) · haut méd +1.25% · range méd 3.12%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −3.89%) · haut méd +1.53% · range méd 3.69%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 93.49 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (122/159) · gap 42% · délai 0.0min · rebond 53% (61/122) (MFE +1.36%)
   - −1.0% : fill 30min 58% · séance 66% (107/159) · gap 33% · délai 0.0min · rebond 56% (59/107) (MFE +1.26%)
   - −1.5% : fill 30min 52% · séance 63% (100/159) · gap 25% · délai 0.1min · rebond 51% (53/100) (MFE +1.12%)
   - −2.0% : fill 30min 45% · séance 58% (91/159) · gap 18% · délai 0.6min · rebond 61% (53/91) (MFE +1.28%)
   - −3.0% : fill 30min 34% · séance 45% (70/159) · gap 9% · délai 10.7min · rebond 66% (45/70) (MFE +1.72%)
   - −4.0% : fill 30min 22% · séance 35% (53/159) · gap 4% · délai 12.4min · rebond 74% (34/53) (MFE +1.99%)
   - −5.0% : fill 30min 13% · séance 22% (35/159) · gap 2% · délai 21.9min · rebond 85% (28/35) (MFE +2.36%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.61%) → stop au-delà de −1.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.44%) → stop au-delà de −1.65% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.64% (p90 −2.48%) → stop au-delà de −1.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=754 jambes) : jambe baissière méd −1.15% (p90 −2.73%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 95% (68/72) · rebond 52% (35/68)
      · −2.0% : fill 85% (59/72) · rebond 56% (33/59)
      · −3.0% : fill 71% (48/72) · rebond 62% (30/48)
      · −4.0% : fill 58% (39/72) · rebond 79% (28/39)
      · −5.0% : fill 42% (29/72) · rebond 84% (24/29)
   - **flat** (20 séances) :
      · −1.0% : fill 72% (15/20) · rebond 64% (10/15)
      · −2.0% : fill 64% (11/20) · rebond 48% (6/11)
      · −3.0% : fill 28% (6/20) · rebond 23% (2/6)
      · −4.0% : fill 26% (5/20) · rebond 16% (1/5)
      · −5.0% : fill 13% (3/20) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (24/67) · rebond 63% (14/24)
      · −2.0% : fill 29% (21/67) · rebond 82% (14/21)
      · −3.0% : fill 23% (16/67) · rebond 93% (13/16)
      · −4.0% : fill 13% (9/67) · rebond 80% (5/9)
      · −5.0% : fill 4% (3/67) · rebond 94% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 71% si les 15 1res min sont vertes (70 cas) · 37% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 89% si début vert vs 17% si rouge (base 52% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **89%** · continue >prix actuel 55% ; creux résiduel méd -1.39% (q20 -2.63%) → **SL/trailing à −2.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.96% / q75 +2.78% → **scale +0.96% / runner +2.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **17%** (continue à baisser 60%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.5%** (au-delà de la MAE q10 -4.5%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.54% .. +3.91%] · haut q95 +4.41% · bas q05 -4.63%
   - 60min (n=160) : retour [-3.65% .. +4.96%] · haut q95 +5.16% · bas q05 -4.89%
   - 2h (n=160) : retour [-4.25% .. +6.02%] · haut q95 +7.59% · bas q05 -5.59%
   - 4h (n=160) : retour [-4.67% .. +6.23%] · haut q95 +8.71% · bas q05 -6.19%
   - 6h (n=160) : retour [-5.68% .. +6.73%] · haut q95 +8.88% · bas q05 -6.96%
   - session (n=160) : retour [-5.04% .. +6.34%] · haut q95 +8.88% · bas q05 -7.25%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.61 · part idiosyncratique 0.39
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 65.9  _(momentum haussier)_
- **ADX** : 24.4  _(pas de tendance nette)_
- **MACD** : hist -0.021  _(bearish_recent)_
- **BB** : %B 0.66 · largeur 33.7%
- **ATR** : 7.31 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.113  _(accumulation)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 42.2  _(transition)_
- **MA** : MA20 93.7 · MA50 85.22 · MA200 102.58  _(prix > MA20)_
- **Dist MA** : MA20 +5.3% · MA50 +15.8% · MA200 -3.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (71131 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# SOFI

**Generated** : 2026-07-23T00:30:10.265983+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $17.07  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot $17.07 (+1.5% vs entrée) · entrée $16.82 · stop $16.23 · T1 $17.07 · R/R 0.42  
> ↳ P(T1 av. stop) 54 % _(réel 5 s)_ · EV/risk -0.061 _(réel 5 s)_ (GBM 0.006) · ¼-Kelly 0.034 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $16.77–$16.87 (mid $16.82)
- Spot actuel : $17.07 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : $16.23 (stop swing_plan-based (-4.89%))
- Targets : T1 $17.07 · R/R 0.42 | T2 $17.32 · R/R 0.85 | T3 $17.58 · R/R 1.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.23


## Edge, scénarios & sizing

- EV/risk : 0.006 | EV/share : $0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 37 % | T3 16 %
- Kelly (position) : f* 0.136 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.5 | bear 18.8 | side 68.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.482% → cible +1.51% / stop −3.5%, p_fill 67%, n_eff≈27.3) : P(cible|rempli) **54%** · **EV/risk -0.061** (×p_fill ; si rempli -0.32% du capital)
  - **swing** (entrée dip −3.258% → cible +3.375% / stop −1.687%, p_fill 52%, n_eff≈19.7) : P(cible|rempli) **27%** · **EV/risk -0.156** (×p_fill ; si rempli -0.50% du capital)
  - **deep** (entrée dip −5.034% → cible +4.773% / stop −2.386%, p_fill 35%, n_eff≈12.6) : P(cible|rempli) **65%** · **EV/risk +0.312** (×p_fill ; si rempli +2.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→70% · +2.0%→50% · +3.0%→38% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.45% (p90 6.91%) · excursion haute méd. +1.97% / basse méd. −2.15%
- Profil de vol intra : ouverture 3.069% vs midi 0.915% vs clôture 0.998% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; neutre — autocorr -0.007)_ ; drift intra méd. -0.084% ; recovery-V 26%
- **σ réalisé intraday** 3.005% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 56% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 17.3871 (VA 17.2839–17.4609 ; dernier close 17.65)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 50% · rebond 73% · **stop −2.97%** sous le fill (sous le bruit) · cible +2.03% · R/R 0.68 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 45% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.65% (p90 −1.75%) · haut méd +0.72% · range méd 1.7%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.98%) · haut méd +1.1% · range méd 2.38%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.33%) · haut méd +1.23% · range méd 2.85%
- Excursion ouverture 60min (n=160) : bas méd −1.43% (p90 −3.76%) · haut méd +1.34% · range méd 3.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.65 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 75% (122/159) · gap 31% · délai 0.0min · rebond 57% (67/122) (MFE +1.27%)
   - −1.0% : fill 30min 52% · séance 67% (111/159) · gap 24% · délai 1.0min · rebond 65% (71/111) (MFE +1.36%)
   - −1.5% : fill 30min 46% · séance 63% (101/159) · gap 18% · délai 9.8min · rebond 66% (65/101) (MFE +1.8%)
   - −2.0% : fill 30min 38% · séance 50% (76/159) · gap 11% · délai 5.2min · rebond 73% (52/76) (MFE +2.03%)
   - −3.0% : fill 30min 17% · séance 36% (56/159) · gap 2% · délai 30.8min · rebond 63% (39/56) (MFE +1.49%)
   - −4.0% : fill 30min 9% · séance 23% (39/159) · gap 2% · délai 57.4min · rebond 58% (24/39) (MFE +1.41%)
   - −5.0% : fill 30min 3% · séance 9% (19/159) · gap 1% · délai 60.7min · rebond 47% (10/19) (MFE +0.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.88%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.99%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −2.03%) → stop au-delà de −1.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=671 jambes) : jambe baissière méd −1.1% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 96% (63/65) · rebond 72% (42/63)
      · −2.0% : fill 82% (51/65) · rebond 76% (38/51)
      · −3.0% : fill 64% (40/65) · rebond 73% (30/40)
      · −4.0% : fill 40% (27/65) · rebond 69% (20/27)
      · −5.0% : fill 19% (13/65) · rebond 47% (8/13)
   - **flat** (25 séances) :
      · −1.0% : fill 48% (15/25) · rebond 31% (8/15)
      · −2.0% : fill 31% (9/25) · rebond 37% (4/9)
      · −3.0% : fill 25% (7/25) · rebond 34% (4/7)
      · −4.0% : fill 17% (4/25) · rebond 64% (1/4)
      · −5.0% : fill 2% (2/25) · rebond 0% (0/2)
   - **gap-up** (69 séances) :
      · −1.0% : fill 48% (33/69) · rebond 64% (21/33)
      · −2.0% : fill 28% (16/69) · rebond 77% (10/16)
      · −3.0% : fill 14% (9/69) · rebond 40% (5/9)
      · −4.0% : fill 11% (8/69) · rebond 20% (3/8)
      · −5.0% : fill 2% (4/69) · rebond 61% (2/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 58% si les 15 1res min sont vertes (73 cas) · 32% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 79% si début vert vs 13% si rouge (base 44% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **79%** · continue >prix actuel 54% ; creux résiduel méd -1.51% (q20 -3.47%) → **SL/trailing à −3.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.87% / q75 +2.77% → **scale +1.87% / runner +2.77%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **13%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.89%** (au-delà de la MAE q10 -3.89%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.94% .. +3.57%] · haut q95 +3.89% · bas q05 -3.57%
   - 60min (n=160) : retour [-3.2% .. +3.4%] · haut q95 +4.03% · bas q05 -4.01%
   - 2h (n=160) : retour [-3.67% .. +3.66%] · haut q95 +4.71% · bas q05 -4.96%
   - 4h (n=160) : retour [-3.99% .. +4.38%] · haut q95 +5.66% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.64% .. +3.92%] · haut q95 +5.69% · bas q05 -5.13%
   - session (n=160) : retour [-4.56% .. +4.9%] · haut q95 +5.69% · bas q05 -5.4%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.1  _(momentum baissier)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist -0.166  _(pas de croisement recent)_
- **BB** : %B 0.13 · largeur 12.3%
- **ATR** : 0.91 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.095  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 17.88 · MA50 17.1 · MA200 21.68  _(prix < MA20)_
- **Dist MA** : MA20 -4.5% · MA50 -0.2% · MA200 -21.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84152 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

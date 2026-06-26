# SOFI

**Generated** : 2026-06-26T00:22:40.518542+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $17.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)  
> ↳ spot $17.30 (+5.2% vs entrée) · entrée $16.44 · stop $16.05 · T1 $17.23 · R/R 2.03  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.008 · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.040 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.29–$16.60 (mid $16.44)
- Spot actuel : $17.30 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : $16.05 (stop swing_plan-based (-7.23%))
- Targets : T1 $17.23 · R/R 2.03 | T2 $18.02 · R/R 4.05 | T3 $18.80 · R/R 6.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.05


## Edge, scénarios & sizing

- EV/risk : 0.008 | EV/share : $0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 26.7 | bear 35.2 | side 38.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 398.0 (= 23 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.248% → cible +2.141% / stop −1.782%, p_fill 49%, n_eff≈18.9) : P(cible|rempli) **27%** · **EV/risk +0.035** (×p_fill ; si rempli +0.13% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=7))
  - **deep** (entrée dip −7.655% → cible +6.769% / stop −3.384%, p_fill 20%, n_eff≈8.2) : P(cible|rempli) **27%** · **EV/risk -0.049** (×p_fill ; si rempli -0.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→71% · +2.0%→48% · +3.0%→36% · +5.0%→9% · +8.0%→0%
- Range intraday médian 4.44% (p90 6.64%) · excursion haute méd. +1.9% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.997% vs midi 0.939% vs clôture 1.022% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓1% ; spike-down 66% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; momentum — autocorr 0.043)_ ; drift intra méd. 0.102% ; recovery-V 36%
- **σ réalisé intraday** 3.213% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 53% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 17.3999 (VA 17.2769–17.9841 ; dernier close 17.32)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 70% · **stop −3.95%** sous le fill (sous le bruit) · cible +2.1% · R/R 0.53 (high win-rate)
- Gaps overnight (n=159) : méd. -0.14% · baisse 52% (gap-down >1% 27% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −1.94%) · haut méd +0.64% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −1.09% (p90 −3.17%) · haut méd +0.96% · range méd 2.34%
- Excursion ouverture 30min (n=160) : bas méd −1.18% (p90 −3.2%) · haut méd +1.15% · range méd 2.82%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.33%) · haut méd +1.44% · range méd 3.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.32 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (124/159) · gap 35% · délai 0.0min · rebond 60% (69/124) (MFE +1.4%)
   - −1.0% : fill 30min 52% · séance 67% (112/159) · gap 27% · délai 0.1min · rebond 64% (71/112) (MFE +1.45%)
   - −1.5% : fill 30min 43% · séance 61% (101/159) · gap 19% · délai 1.2min · rebond 66% (65/101) (MFE +1.89%)
   - −2.0% : fill 30min 38% · séance 47% (76/159) · gap 12% · délai 1.7min · rebond 70% (53/76) (MFE +2.1%)
   - −3.0% : fill 30min 22% · séance 35% (57/159) · gap 4% · délai 10.6min · rebond 73% (42/57) (MFE +1.69%)
   - −4.0% : fill 30min 10% · séance 24% (41/159) · gap 2% · délai 64.3min · rebond 62% (27/41) (MFE +1.51%)
   - −5.0% : fill 30min 5% · séance 13% (23/159) · gap 1% · délai 58.4min · rebond 48% (13/23) (MFE +0.96%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.51% (p90 −1.91%) → stop au-delà de −1.56% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.98%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.49% (p90 −1.85%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=683 jambes) : jambe baissière méd −1.14% (p90 −2.75%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 96% (68/70) · rebond 65% (43/68)
      · −2.0% : fill 81% (55/70) · rebond 71% (41/55)
      · −3.0% : fill 64% (44/70) · rebond 74% (33/44)
      · −4.0% : fill 44% (31/70) · rebond 66% (23/31)
      · −5.0% : fill 24% (16/70) · rebond 48% (10/16)
   - **flat** (24 séances) :
      · −1.0% : fill 58% (16/24) · rebond 43% (10/16)
      · −2.0% : fill 32% (9/24) · rebond 59% (5/9)
      · −3.0% : fill 21% (6/24) · rebond 62% (4/6)
      · −4.0% : fill 9% (3/24) · rebond 0% (0/3)
      · −5.0% : fill 3% (2/24) · rebond 0% (0/2)
   - **gap-up** (65 séances) :
      · −1.0% : fill 38% (28/65) · rebond 72% (18/28)
      · −2.0% : fill 13% (12/65) · rebond 68% (7/12)
      · −3.0% : fill 6% (7/65) · rebond 71% (5/7)
      · −4.0% : fill 6% (7/65) · rebond 64% (4/7)
      · −5.0% : fill 4% (5/65) · rebond 65% (3/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 54% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.45% .. +3.71%] · haut q95 +4.01% · bas q05 -4.0%
   - 60min (n=160) : retour [-3.27% .. +3.75%] · haut q95 +4.86% · bas q05 -4.37%
   - session (n=160) : retour [-4.07% .. +4.71%] · haut q95 +5.75% · bas q05 -6.17%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.2  _(neutre)_
- **ADX** : 20.4  _(pas de tendance nette)_
- **MACD** : hist 0.053  _(pas de croisement recent)_
- **BB** : %B 0.56 · largeur 16.2%
- **ATR** : 1.0 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.038  _(neutre)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 57.9  _(transition)_
- **MA** : MA20 17.13 · MA50 16.97 · MA200 22.53  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 +1.9% · MA200 -23.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (44663 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

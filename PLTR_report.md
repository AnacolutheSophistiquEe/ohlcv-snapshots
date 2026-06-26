# PLTR

**Generated** : 2026-06-26T21:50:04.922343+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $112.93  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot $112.93 (+5.6% vs entrée) · entrée $106.92 · stop $105.12 · T1 $109.36 · R/R 1.36  
> ↳ P(T1 av. stop) 29 % · EV/risk -0.027 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $106.44–$107.41 (mid $106.92)
- Spot actuel : $112.93 (+5.6% au-dessus de la zone — repli à attendre)
- Stop : $105.12 (stop swing_plan-based (-12.92%))
- Targets : T1 $109.36 · R/R 1.36 | T2 $111.80 · R/R 2.71 | T3 $114.24 · R/R 4.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $105.12


## Edge, scénarios & sizing

- EV/risk : -0.027 | EV/share : $-0.049 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 6 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 18.6 | bear 71.1 | side 10.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→36% · +3.0%→19% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.89% (p90 7.17%) · excursion haute méd. +1.69% / basse méd. −1.73%
- Profil de vol intra : ouverture 2.825% vs midi 0.732% vs clôture 0.81% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑0%/↓1% ; spike-down 59% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; neutre — autocorr 0.009)_ ; drift intra méd. -0.666% ; recovery-V 22%
- **σ réalisé intraday** 2.689% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 57% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 107.1741 (VA 106.8926–107.8779 ; dernier close 107.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 19% · rebond 49% · **stop −2.89%** sous le fill (sous le bruit) · cible +0.99% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.28% · baisse 58% (gap-down >1% 33% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.88% (p90 −1.97%) · haut méd +0.77% · range méd 1.77%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.8%) · haut méd +0.97% · range méd 2.2%
- Excursion ouverture 30min (n=160) : bas méd −1.27% (p90 −3.61%) · haut méd +1.22% · range méd 2.62%
- Excursion ouverture 60min (n=160) : bas méd −1.37% (p90 −3.96%) · haut méd +1.41% · range méd 3.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 107.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (118/159) · gap 44% · délai 0.0min · rebond 53% (64/118) (MFE +1.06%)
   - −1.0% : fill 30min 61% · séance 74% (110/159) · gap 33% · délai 0.0min · rebond 61% (65/110) (MFE +1.32%)
   - −1.5% : fill 30min 51% · séance 64% (92/159) · gap 22% · délai 1.0min · rebond 65% (58/92) (MFE +1.37%)
   - −2.0% : fill 30min 43% · séance 55% (77/159) · gap 16% · délai 4.2min · rebond 61% (49/77) (MFE +1.43%)
   - −3.0% : fill 30min 20% · séance 37% (56/159) · gap 5% · délai 21.4min · rebond 45% (27/56) (MFE +0.85%)
   - −4.0% : fill 30min 14% · séance 26% (39/159) · gap 4% · délai 28.5min · rebond 41% (18/39) (MFE +0.83%)
   - −5.0% : fill 30min 10% · séance 19% (27/159) · gap 2% · délai 26.4min · rebond 49% (14/27) (MFE +0.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.3% (p90 −1.83%) → stop au-delà de −1.32% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.45%) → stop au-delà de −1.33% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.38% (p90 −1.38%) → stop au-delà de −1.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=548 jambes) : jambe baissière méd −1.09% (p90 −2.72%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 97% (65/68) · rebond 65% (41/65)
      · −2.0% : fill 81% (54/68) · rebond 62% (37/54)
      · −3.0% : fill 57% (39/68) · rebond 39% (20/39)
      · −4.0% : fill 42% (27/68) · rebond 37% (12/27)
      · −5.0% : fill 35% (20/68) · rebond 51% (10/20)
   - **flat** (33 séances) :
      · −1.0% : fill 83% (26/33) · rebond 42% (14/26)
      · −2.0% : fill 55% (13/33) · rebond 70% (8/13)
      · −3.0% : fill 43% (11/33) · rebond 75% (6/11)
      · −4.0% : fill 22% (8/33) · rebond 71% (5/8)
      · −5.0% : fill 5% (4/33) · rebond 63% (3/4)
   - **gap-up** (58 séances) :
      · −1.0% : fill 37% (19/58) · rebond 72% (10/19)
      · −2.0% : fill 17% (10/58) · rebond 42% (4/10)
      · −3.0% : fill 6% (6/58) · rebond 14% (1/6)
      · −4.0% : fill 4% (4/58) · rebond 18% (1/4)
      · −5.0% : fill 3% (3/58) · rebond 12% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 62% si les 15 1res min sont vertes (79 cas) · 31% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.05% .. +2.49%] · haut q95 +3.19% · bas q05 -4.27%
   - 60min (n=160) : retour [-3.53% .. +2.91%] · haut q95 +3.53% · bas q05 -4.46%
   - session (n=160) : retour [-4.98% .. +4.0%] · haut q95 +4.5% · bas q05 -5.77%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.66 · part idiosyncratique 0.34
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.8  _(survente)_
- **ADX** : 22.5  _(pas de tendance nette)_
- **MACD** : hist -2.539  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 42.9%
- **ATR** : 6.01 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.123  _(distribution)_
- **Vol ratio** : 1.33  _(volume normal)_
- **Choppiness** : 37.3  _(marche directionnel)_
- **MA** : MA20 132.18 · MA50 136.46 · MA200 158.85  _(prix < MA20)_
- **Dist MA** : MA20 -14.6% · MA50 -17.2% · MA200 -28.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (39332 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

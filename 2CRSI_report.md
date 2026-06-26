# AL2SI

**Generated** : 2026-06-26T21:42:45.023196+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 15.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €27.52  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot €27.52 (+15.2% vs entrée) · entrée €23.89 · stop €22.03 · T1 €25.85 · R/R 1.05  
> ↳ P(T1 av. stop) 26 % · EV/risk -0.009 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €23.59–€24.19 (mid €23.89)
- Spot actuel : €27.52 (+15.2% au-dessus de la zone — repli à attendre)
- Stop : €22.03 (stop swing_plan-based (-35.78%))
- Targets : T1 €25.85 · R/R 1.05 | T2 €27.81 · R/R 2.11 | T3 €29.78 · R/R 3.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.03


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : €-0.017 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 4 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 10.2 | bear 62.0 | side 27.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 138.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→76% · +3.0%→65% · +5.0%→41% · +8.0%→20%
- Range intraday médian 7.78% (p90 13.94%) · excursion haute méd. +4.23% / basse méd. −3.18%
- Profil de vol intra : ouverture 5.369% vs midi 1.647% vs clôture 1.911% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (135 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑0%/↓2% ; spike-down 71% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.173 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.225% ; recovery-V 30%
- **σ réalisé intraday** 8.48% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 65% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 26.14 (VA 25.18–29.82 ; dernier close 25.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 86% · **stop −6.78%** sous le fill (sous le bruit) · cible +2.38% · R/R 0.35 (high win-rate)
- Gaps overnight (n=134) : méd. 0.19% · baisse 41% (gap-down >1% 25% · >2% 10%)
- Excursion ouverture 5min (n=135) : bas méd −0.87% (p90 −4.93%) · haut méd +1.03% · range méd 2.73%
- Excursion ouverture 15min (n=135) : bas méd −1.34% (p90 −5.86%) · haut méd +1.51% · range méd 3.34%
- Excursion ouverture 30min (n=135) : bas méd −1.48% (p90 −5.86%) · haut méd +1.79% · range méd 4.31%
- Excursion ouverture 60min (n=135) : bas méd −2.0% (p90 −6.69%) · haut méd +2.64% · range méd 5.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 25.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 77% (102/134) · gap 31% · délai 0.1min · rebond 63% (66/102) (MFE +2.23%)
   - −1.0% : fill 30min 57% · séance 74% (97/134) · gap 25% · délai 0.4min · rebond 68% (66/97) (MFE +1.8%)
   - −1.5% : fill 30min 49% · séance 70% (88/134) · gap 15% · délai 1.9min · rebond 63% (55/88) (MFE +1.67%)
   - −2.0% : fill 30min 40% · séance 59% (75/134) · gap 10% · délai 3.6min · rebond 61% (48/75) (MFE +1.34%)
   - −3.0% : fill 30min 28% · séance 51% (61/134) · gap 7% · délai 11.6min · rebond 77% (49/61) (MFE +2.19%)
   - −4.0% : fill 30min 21% · séance 42% (51/134) · gap 6% · délai 33.1min · rebond 72% (39/51) (MFE +2.65%)
   - −5.0% : fill 30min 18% · séance 38% (44/134) · gap 6% · délai 48.2min · rebond 86% (41/44) (MFE +2.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −5.43%) → stop au-delà de −2.49% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.68% (p90 −5.6%) → stop au-delà de −3.84% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −5.76%) → stop au-delà de −3.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1262 jambes) : jambe baissière méd −1.23% (p90 −3.24%) · ~19.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 97% (45/49) · rebond 66% (30/45)
      · −2.0% : fill 84% (38/49) · rebond 52% (23/38)
      · −3.0% : fill 81% (34/49) · rebond 74% (27/34)
      · −4.0% : fill 67% (29/49) · rebond 68% (23/29)
      · −5.0% : fill 63% (27/49) · rebond 77% (24/27)
   - **flat** (27 séances) :
      · −1.0% : fill 76% (20/27) · rebond 71% (15/20)
      · −2.0% : fill 53% (14/27) · rebond 79% (10/14)
      · −3.0% : fill 35% (9/27) · rebond 87% (8/9)
      · −4.0% : fill 35% (9/27) · rebond 91% (8/9)
      · −5.0% : fill 25% (7/27) · rebond 100% (7/7)
   - **gap-up** (58 séances) :
      · −1.0% : fill 55% (32/58) · rebond 68% (21/32)
      · −2.0% : fill 41% (23/58) · rebond 66% (15/23)
      · −3.0% : fill 33% (18/58) · rebond 80% (14/18)
      · −4.0% : fill 25% (13/58) · rebond 70% (8/13)
      · −5.0% : fill 23% (10/58) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=135) : 51% en base · 65% si les 15 1res min sont vertes (66 cas) · 39% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=135) : retour [-3.68% .. +6.78%] · haut q95 +8.66% · bas q05 -7.64%
   - 60min (n=135) : retour [-5.7% .. +9.42%] · haut q95 +9.95% · bas q05 -8.18%
   - session (n=135) : retour [-10.03% .. +17.87%] · haut q95 +18.8% · bas q05 -15.68%


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.28 · part idiosyncratique 0.72
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 20.8  _(survente)_
- **ADX** : 31.4  _(tendance etablie)_
- **MACD** : hist -2.567  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 123.2%
- **ATR** : 6.18 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.043  _(neutre)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 29.3  _(marche directionnel)_
- **MA** : MA20 42.4 · MA50 41.46 · MA200 22.38  _(prix < MA20)_
- **Dist MA** : MA20 -35.1% · MA50 -33.6% · MA200 +23.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (41757 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

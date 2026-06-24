# ENR

**Generated** : 2026-06-24T00:05:53.773236+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €162.74  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €162.74 (+22.5% vs entrée) · entrée €132.80 · stop €129.98 · T1 €138.43 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.127 · ¼-Kelly 0.008 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €131.67–€133.93 (mid €132.80)
- Spot actuel : €162.74 (+22.5% au-dessus de la zone — repli à attendre)
- Stop : €129.98 (stop swing_plan-based (-20.13%))
- Targets : T1 €138.43 · R/R 2.0 | T2 €144.07 · R/R 4.0 | T3 €149.71 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.98


## Edge, scénarios & sizing

- EV/risk : 0.127 | EV/share : €0.358 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 46.9 | bear 27.4 | side 25.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 325.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→68% · +2.0%→50% · +3.0%→29% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.6% (p90 7.11%) · excursion haute méd. +1.9% / basse méd. −1.81%
- Profil de vol intra : ouverture 2.213% vs midi 1.031% vs clôture 1.271% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.025)_ ; drift intra méd. -0.214% ; recovery-V 12%
- **σ réalisé intraday** 2.655% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 68% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 170.1021 (VA 169.7966–171.6296 ; dernier close 169.64)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 26% · rebond 74% · **stop −2.16%** sous le fill (sous le bruit) · cible +1.88% · R/R 0.87 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 38% (gap-down >1% 19% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.59% (p90 −1.72%) · haut méd +0.47% · range méd 1.19%
- Excursion ouverture 15min (n=160) : bas méd −0.69% (p90 −2.22%) · haut méd +0.63% · range méd 1.47%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −2.54%) · haut méd +0.68% · range méd 1.73%
- Excursion ouverture 60min (n=160) : bas méd −0.95% (p90 −2.55%) · haut méd +0.86% · range méd 1.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 169.64 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 72% (111/159) · gap 26% · délai 0.4min · rebond 51% (55/111) (MFE +1.11%)
   - −1.0% : fill 30min 45% · séance 65% (99/159) · gap 19% · délai 4.4min · rebond 57% (58/99) (MFE +1.3%)
   - −1.5% : fill 30min 33% · séance 59% (85/159) · gap 16% · délai 15.6min · rebond 66% (55/85) (MFE +1.52%)
   - −2.0% : fill 30min 22% · séance 41% (62/159) · gap 10% · délai 22.5min · rebond 57% (36/62) (MFE +1.4%)
   - −3.0% : fill 30min 15% · séance 34% (48/159) · gap 5% · délai 171.7min · rebond 76% (36/48) (MFE +1.76%)
   - −4.0% : fill 30min 7% · séance 26% (37/159) · gap 2% · délai 350.0min · rebond 74% (26/37) (MFE +1.88%)
   - −5.0% : fill 30min 2% · séance 15% (21/159) · gap 1% · délai 425.6min · rebond 68% (13/21) (MFE +1.25%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.98%) → stop au-delà de −0.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.46%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.54%) → stop au-delà de −0.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=507 jambes) : jambe baissière méd −1.06% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 95% (43/44) · rebond 62% (25/43)
      · −2.0% : fill 66% (31/44) · rebond 67% (21/31)
      · −3.0% : fill 59% (27/44) · rebond 81% (21/27)
      · −4.0% : fill 46% (22/44) · rebond 77% (16/22)
      · −5.0% : fill 29% (14/44) · rebond 63% (9/14)
   - **flat** (27 séances) :
      · −1.0% : fill 62% (18/27) · rebond 55% (12/18)
      · −2.0% : fill 30% (8/27) · rebond 35% (3/8)
      · −3.0% : fill 23% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 20% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 12% (2/27) · rebond 74% (1/2)
   - **gap-up** (88 séances) :
      · −1.0% : fill 49% (38/88) · rebond 52% (21/38)
      · −2.0% : fill 30% (23/88) · rebond 50% (12/23)
      · −3.0% : fill 22% (16/88) · rebond 68% (12/16)
      · −4.0% : fill 15% (11/88) · rebond 68% (8/11)
      · −5.0% : fill 8% (5/88) · rebond 76% (3/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 85% si les 15 1res min sont vertes (81 cas) · 19% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.27% .. +2.22%] · haut q95 +2.9% · bas q05 -2.82%
   - 60min (n=160) : retour [-2.46% .. +2.34%] · haut q95 +3.05% · bas q05 -3.41%
   - session (n=160) : retour [-5.18% .. +4.51%] · haut q95 +6.03% · bas q05 -6.19%


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.55 · part idiosyncratique 0.45
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.2  _(neutre)_
- **ADX** : 19.5  _(pas de tendance nette)_
- **MACD** : hist 1.837  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 21.2%
- **ATR** : 7.38 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.126  _(distribution)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 40.5  _(transition)_
- **MA** : MA20 159.5 · MA50 169.19 · MA200 136.77  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 -3.8% · MA200 +19.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (40646 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

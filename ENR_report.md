# ENR

**Generated** : 2026-06-24T21:40:02.628803+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €159.86  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €159.86 (+21.6% vs entrée) · entrée €131.50 · stop €128.77 · T1 €136.97 · R/R 2.0  
> ↳ P(T1 av. stop) 37 % · EV/risk 0.128 · ¼-Kelly 0.008 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.100 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.41–€132.60 (mid €131.50)
- Spot actuel : €159.86 (+21.6% au-dessus de la zone — repli à attendre)
- Stop : €128.77 (stop swing_plan-based (-19.45%))
- Targets : T1 €136.97 · R/R 2.0 | T2 €142.43 · R/R 4.0 | T3 €147.90 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.77


## Edge, scénarios & sizing

- EV/risk : 0.128 | EV/share : €0.350 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 44.2 | bear 47.1 | side 8.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 320.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→66% · +2.0%→50% · +3.0%→29% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.52% (p90 7.08%) · excursion haute méd. +1.9% / basse méd. −1.81%
- Profil de vol intra : ouverture 2.204% vs midi 1.031% vs clôture 1.238% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr -0.021)_ ; drift intra méd. -0.278% ; recovery-V 12%
- **σ réalisé intraday** 2.651% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 70% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 160.72 (VA 159.28–161.68 ; dernier close 162.74)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 27% · rebond 69% · **stop −2.29%** sous le fill (sous le bruit) · cible +1.78% · R/R 0.78 (high win-rate)
- Gaps overnight (n=159) : méd. 0.39% · baisse 40% (gap-down >1% 21% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.72%) · haut méd +0.47% · range méd 1.2%
- Excursion ouverture 15min (n=160) : bas méd −0.7% (p90 −2.21%) · haut méd +0.6% · range méd 1.49%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.52%) · haut méd +0.66% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.96% (p90 −2.58%) · haut méd +0.85% · range méd 1.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 162.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 73% (111/159) · gap 28% · délai 0.3min · rebond 50% (55/111) (MFE +1.07%)
   - −1.0% : fill 30min 46% · séance 66% (99/159) · gap 21% · délai 2.7min · rebond 55% (57/99) (MFE +1.1%)
   - −1.5% : fill 30min 35% · séance 60% (86/159) · gap 17% · délai 14.0min · rebond 63% (55/86) (MFE +1.48%)
   - −2.0% : fill 30min 24% · séance 42% (63/159) · gap 12% · délai 16.7min · rebond 55% (36/63) (MFE +1.38%)
   - −3.0% : fill 30min 17% · séance 35% (49/159) · gap 5% · délai 126.7min · rebond 72% (36/49) (MFE +1.74%)
   - −4.0% : fill 30min 9% · séance 27% (38/159) · gap 2% · délai 308.4min · rebond 69% (26/38) (MFE +1.78%)
   - −5.0% : fill 30min 2% · séance 17% (22/159) · gap 1% · délai 393.5min · rebond 71% (14/22) (MFE +1.35%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.99%) → stop au-delà de −0.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.46%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.54%) → stop au-delà de −0.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=508 jambes) : jambe baissière méd −1.07% (p90 −2.52%) · ~7.6 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 58% (25/44)
      · −2.0% : fill 68% (32/45) · rebond 62% (21/32)
      · −3.0% : fill 61% (28/45) · rebond 74% (21/28)
      · −4.0% : fill 49% (23/45) · rebond 68% (16/23)
      · −5.0% : fill 33% (15/45) · rebond 69% (10/15)
   - **flat** (27 séances) :
      · −1.0% : fill 62% (18/27) · rebond 55% (12/18)
      · −2.0% : fill 30% (8/27) · rebond 35% (3/8)
      · −3.0% : fill 23% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 20% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 12% (2/27) · rebond 74% (1/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 49% (37/87) · rebond 52% (20/37)
      · −2.0% : fill 30% (23/87) · rebond 50% (12/23)
      · −3.0% : fill 22% (16/87) · rebond 68% (12/16)
      · −4.0% : fill 16% (11/87) · rebond 68% (8/11)
      · −5.0% : fill 8% (5/87) · rebond 76% (3/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 85% si les 15 1res min sont vertes (81 cas) · 19% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.27% .. +2.21%] · haut q95 +2.87% · bas q05 -2.81%
   - 60min (n=160) : retour [-2.46% .. +2.31%] · haut q95 +3.04% · bas q05 -3.38%
   - session (n=160) : retour [-5.15% .. +4.5%] · haut q95 +6.0% · bas q05 -6.18%


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.55 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.3  _(neutre)_
- **ADX** : 18.9  _(pas de tendance nette)_
- **MACD** : hist 1.396  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 19.4%
- **ATR** : 7.45 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.101  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 40.9  _(transition)_
- **MA** : MA20 158.76 · MA50 168.96 · MA200 137.13  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 -5.4% · MA200 +16.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (40658 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

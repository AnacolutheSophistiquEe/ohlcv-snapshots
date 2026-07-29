# SMR

**Generated** : 2026-07-29T00:28:49.187584+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $8.22  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot $8.22 (+3.1% vs entrée) · entrée $7.97 · stop $7.78 · T1 $8.18 · R/R 1.11  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.141 _(réel 5 s)_ (GBM 0.073) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.37% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

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

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.93–$8.01 (mid $7.97)
- Spot actuel : $8.22 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : $7.78 (stop swing_plan-based (-9.49%))
- Targets : T1 $8.18 · R/R 1.11 | T2 $8.39 · R/R 2.21 | T3 $8.59 · R/R 3.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.78


## Edge, scénarios & sizing

- EV/risk : 0.073 | EV/share : $0.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.082 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 80.2 | bear 12.8 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.074% → cible +2.622% / stop −2.368%, p_fill 48%, n_eff≈19.8) : P(cible|rempli) **30%** · **EV/risk -0.141** (×p_fill ; si rempli -0.70% du capital)
  - **swing** (entrée dip −6.756% → cible +5.863% / stop −2.932%, p_fill 29%, n_eff≈12.0) : P(cible|rempli) **13%** · **EV/risk -0.184** (×p_fill ; si rempli -1.84% du capital)
  - **deep** (entrée dip −10.447% → cible +8.292% / stop −4.146%, p_fill 39%, n_eff≈13.2) : P(cible|rempli) **5%** · **EV/risk -0.333** (×p_fill ; si rempli -3.56% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→65% · +3.0%→57% · +5.0%→40% · +8.0%→18%
- Range intraday médian 7.8% (p90 12.61%) · excursion haute méd. +3.54% / basse méd. −3.15%
- Profil de vol intra : ouverture 5.09% vs midi 1.55% vs clôture 1.791% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. -0.121% ; recovery-V 34%
- **σ réalisé intraday** 4.812% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 68% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 8.3022 (VA 8.1872–8.4603 ; dernier close 8.54)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 52% · rebond 75% · **stop −6.04%** sous le fill (sous le bruit) · cible +2.35% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. -0.52% · baisse 58% (gap-down >1% 42% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.07% (p90 −3.24%) · haut méd +1.09% · range méd 2.65%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.75%) · haut méd +1.48% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.79% (p90 −4.69%) · haut méd +2.14% · range méd 4.36%
- Excursion ouverture 60min (n=160) : bas méd −2.14% (p90 −5.93%) · haut méd +2.65% · range méd 5.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 8.54 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 81% (130/159) · gap 50% · délai 0.0min · rebond 68% (81/130) (MFE +1.76%)
   - −1.0% : fill 30min 67% · séance 77% (124/159) · gap 42% · délai 0.0min · rebond 69% (83/124) (MFE +2.08%)
   - −1.5% : fill 30min 62% · séance 75% (118/159) · gap 37% · délai 0.0min · rebond 76% (87/118) (MFE +2.23%)
   - −2.0% : fill 30min 58% · séance 68% (111/159) · gap 28% · délai 0.2min · rebond 70% (81/111) (MFE +2.4%)
   - −3.0% : fill 30min 46% · séance 60% (99/159) · gap 10% · délai 2.8min · rebond 73% (80/99) (MFE +2.58%)
   - −4.0% : fill 30min 35% · séance 52% (83/159) · gap 5% · délai 11.4min · rebond 75% (63/83) (MFE +2.35%)
   - −5.0% : fill 30min 25% · séance 40% (62/159) · gap 3% · délai 19.7min · rebond 68% (45/62) (MFE +1.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.69%) → stop au-delà de −1.84% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.7%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.02% (p90 −2.74%) → stop au-delà de −2.34% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1177 jambes) : jambe baissière méd −1.39% (p90 −3.22%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 100% (83/83) · rebond 71% (56/83)
      · −2.0% : fill 94% (79/83) · rebond 77% (61/79)
      · −3.0% : fill 84% (74/83) · rebond 75% (61/74)
      · −4.0% : fill 73% (64/83) · rebond 80% (52/64)
      · −5.0% : fill 57% (46/83) · rebond 71% (35/46)
   - **flat** (14 séances) :
      · −1.0% : fill 80% (11/14) · rebond 54% (7/11)
      · −2.0% : fill 69% (9/14) · rebond 22% (4/9)
      · −3.0% : fill 66% (7/14) · rebond 47% (4/7)
      · −4.0% : fill 66% (7/14) · rebond 55% (3/7)
      · −5.0% : fill 56% (6/14) · rebond 80% (5/6)
   - **gap-up** (62 séances) :
      · −1.0% : fill 45% (30/62) · rebond 70% (20/30)
      · −2.0% : fill 32% (23/62) · rebond 66% (16/23)
      · −3.0% : fill 25% (18/62) · rebond 80% (15/18)
      · −4.0% : fill 18% (12/62) · rebond 67% (8/12)
      · −5.0% : fill 13% (10/62) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 62% si les 15 1res min sont vertes (73 cas) · 30% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **40min** → P(séance verte=clôture>ouverture) 68% si début vert vs 16% si rouge (base 46% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **68%** · continue >prix actuel 44% ; creux résiduel méd -3.13% (q20 -5.01%) → **SL/trailing à −5.01%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.13% / q75 +3.93% → **scale +2.13% / runner +3.93%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **16%** (continue à baisser 55%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.88%** (au-delà de la MAE q10 -6.88%), cible rebond +1.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.48% .. +4.91%] · haut q95 +6.54% · bas q05 -6.02%
   - 60min (n=160) : retour [-6.45% .. +5.49%] · haut q95 +7.67% · bas q05 -7.78%
   - 2h (n=160) : retour [-7.62% .. +7.62%] · haut q95 +11.1% · bas q05 -8.57%
   - 4h (n=160) : retour [-8.23% .. +7.75%] · haut q95 +11.07% · bas q05 -10.54%
   - 6h (n=160) : retour [-8.04% .. +8.35%] · haut q95 +11.35% · bas q05 -10.64%
   - session (n=160) : retour [-7.93% .. +10.12%] · haut q95 +11.46% · bas q05 -10.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — SMR earnings (J-5 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — SMR earnings (J-5 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 44.5  _(momentum baissier)_
- **ADX** : 23.1  _(pas de tendance nette)_
- **MACD** : hist 0.068  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 32.5%
- **ATR** : 0.63 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.042  _(neutre)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 8.75 · MA50 10.11 · MA200 16.94  _(prix < MA20)_
- **Dist MA** : MA20 -6.1% · MA50 -18.7% · MA200 -51.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84905 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

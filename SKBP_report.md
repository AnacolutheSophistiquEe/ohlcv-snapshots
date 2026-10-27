# 326030

**Generated** : 2026-10-27T22:02:10.211393+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩74900.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩74900.00 (+5.5% vs entrée) · entrée ₩70995.00 · stop ₩67777.14 · T1 ₩74592.67 · R/R 1.12  
> ↳ ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈210) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 74900.0 · ATR Wilder 3014.76 (4.03 %)_
- **Swing** : plage **70855.19 → 68833.4** (-5.4 % a -8.1 % sous la cloture, 0.67 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 65818.64 (-4.38 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **68833.4 → 62998.7** (-8.1 % a -15.89 % sous la cloture, 1.94 ATR) — touchee 49 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 59983.94 (-4.79 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- ACHAT PAS CHER : inactif (1.03 ATR sous le plus haut 20 s., RSI(2) 28.5 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Resistances reelles au-dessus : 76300.0-77100.0 (B, 1.87 %) ; 78000.0-79300.0 (A, 4.14 %) ; 79700.0-81000.0 (A, 6.41 %) ; 81700.0-82800.0 (A, 9.08 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.07 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.51 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 9.51 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.578 % | p01 -3.013 % | pire -5.539 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0048** [0.0004 ; 0.0249] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.414** [0.363 ; 0.4665] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.4382** [0.3866 ; 0.4908] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 46.3 observations effectives », dont la borne haute a 95 % vaut environ 6.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (26.3 pt), swing (39.4 pt), deep (39.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.34 %** | CVaR **-6.25 %** | vol 2.97 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.67 % contre 3.06 % aujourd'hui, rapport 0.55)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.27 % vs -8.65 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5711** (β de hausse 0.4328, asymétrie 1.3193) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.209 | EV/share : ₩-671.268 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 10 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈210) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 28.5 | side 66.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 253.0 (= 5 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.37% → cible +2.2% / stop −8.0%, p_fill 40%, n_eff≈46.3) : P(cible|rempli) **32%** · **EV/risk +0.018** (×p_fill ; si rempli +0.36% du capital)
  - **swing** (entrée dip −5.214% → cible +5.068% / stop −4.533%, p_fill 19%, n_eff≈22.3) : P(cible|rempli) **52%** · **EV/risk +0.041** (×p_fill ; si rempli +1.00% du capital)
  - **deep** (entrée dip −8.056% → cible +7.388% / stop −7.009%, p_fill 16%, n_eff≈18.4) : P(cible|rempli) **71%** · **EV/risk +0.076** (×p_fill ; si rempli +3.25% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→42% · +3.0%→27% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.08% (p90 7.08%) · excursion haute méd. +1.51% / basse méd. −2.09%
- Profil de vol intra : ouverture 2.677% vs midi 0.822% vs clôture 0.886% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓0% ; spike-down 60% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.111)_ ; drift intra méd. 0.077% ; recovery-V 24%
- **σ réalisé intraday** 2.491% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 60% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 76828.75 (VA 75598.75–77341.25 ; dernier close 76500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 30% · rebond 59% · **stop −2.56%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.5 (high win-rate)
- Gaps overnight (n=152) : méd. -0.1% · baisse 50% (gap-down >1% 21% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.73% (p90 −2.18%) · haut méd +0.47% · range méd 1.52%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.59%) · haut méd +0.57% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −2.64%) · haut méd +0.78% · range méd 2.35%
- Excursion ouverture 60min (n=160) : bas méd −1.21% (p90 −2.88%) · haut méd +0.9% · range méd 2.77%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 76900.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 81% (118/152) · gap 34% · délai 0.0min · rebond 46% (50/118) (MFE +0.85%)
   - −1.0% : fill 30min 52% · séance 73% (107/152) · gap 21% · délai 0.5min · rebond 49% (49/107) (MFE +0.9%)
   - −1.5% : fill 30min 40% · séance 61% (88/152) · gap 8% · délai 5.2min · rebond 59% (50/88) (MFE +1.25%)
   - −2.0% : fill 30min 31% · séance 47% (70/152) · gap 4% · délai 5.3min · rebond 54% (39/70) (MFE +1.2%)
   - −3.0% : fill 30min 15% · séance 30% (46/152) · gap 3% · délai 24.9min · rebond 59% (25/46) (MFE +1.28%)
   - −4.0% : fill 30min 7% · séance 14% (29/152) · gap 2% · délai 49.8min · rebond 70% (19/29) (MFE +1.28%)
   - −5.0% : fill 30min 3% · séance 8% (17/152) · gap 1% · délai 74.1min · rebond 83% (11/17) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.61% (p90 −2.45%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −1.55%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.6% (p90 −1.38%) → stop au-delà de −1.24% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=593 jambes) : jambe baissière méd −1.0% (p90 −2.27%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 94% (52/55) · rebond 58% (28/52)
      · −2.0% : fill 72% (41/55) · rebond 65% (25/41)
      · −3.0% : fill 54% (30/55) · rebond 63% (18/30)
      · −4.0% : fill 25% (19/55) · rebond 64% (12/19)
      · −5.0% : fill 13% (11/55) · rebond 84% (7/11)
   - **flat** (40 séances) :
      · −1.0% : fill 75% (30/40) · rebond 38% (10/30)
      · −2.0% : fill 45% (18/40) · rebond 36% (9/18)
      · −3.0% : fill 23% (11/40) · rebond 38% (3/11)
      · −4.0% : fill 16% (9/40) · rebond 81% (6/9)
      · −5.0% : fill 9% (6/40) · rebond 80% (4/6)
   - **gap-up** (57 séances) :
      · −1.0% : fill 46% (25/57) · rebond 42% (11/25)
      · −2.0% : fill 19% (11/57) · rebond 39% (5/11)
      · −3.0% : fill 7% (5/57) · rebond 87% (4/5)
      · −4.0% : fill 1% (1/57) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/57) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 59% si les 15 1res min sont vertes (60 cas) · 24% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **33min** → P(séance verte=clôture>ouverture) 76% si début vert vs 19% si rouge (base 38% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 192min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=57) : tient le vert **76%** · continue >prix actuel 58% ; creux résiduel méd -1.06% (q20 -2.78%) → **SL/trailing à −2.78%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.93% / q75 +2.93% → **scale +1.93% / runner +2.93%**, sortie à la clôture
  - **si ROUGE au coude** (n=103) : edge inversé — récupère vert seulement **19%** (continue à baisser 54%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.66%** (au-delà de la MAE q10 -2.66%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.47% .. +2.44%] · haut q95 +3.55% · bas q05 -3.16%
   - 60min (n=160) : retour [-2.72% .. +3.69%] · haut q95 +4.38% · bas q05 -3.43%
   - 2h (n=160) : retour [-3.05% .. +3.6%] · haut q95 +4.6% · bas q05 -3.62%
   - 4h (n=160) : retour [-3.04% .. +5.01%] · haut q95 +6.24% · bas q05 -4.28%
   - 6h (n=160) : retour [-3.56% .. +4.33%] · haut q95 +6.97% · bas q05 -4.59%
   - session (n=160) : retour [-3.57% .. +4.79%] · haut q95 +6.97% · bas q05 -4.63%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **volatil sans tendance propre (choppy)** (vol intra méd 2.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.06 · part idiosyncratique 0.94
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.8  _(neutre)_
- **ADX** : 15.5  _(pas de tendance nette)_
- **MACD** : hist 665.388  _(pas de croisement recent)_
- **BB** : %B 0.56 · largeur 12.4%
- **ATR** : 3217.86 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.063  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 56.7  _(transition)_
- **MA** : MA20 74310.0 · MA50 80030.0 · MA200 94106.5  _(prix > MA20)_
- **Dist MA** : MA20 +0.8% · MA50 -6.4% · MA200 -20.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (492733 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

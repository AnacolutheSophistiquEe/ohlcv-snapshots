# 012450

**Generated** : 2026-08-21T21:55:36.118532+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1085000.00  

> 🟡 **WAIT-FOR-DIP** — spot +7.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩1085000.00 (+7.6% vs entrée) · entrée ₩1008241.12 · stop ₩935741.12 · T1 ₩1070086.28 · R/R 0.85  
> ↳ P(T1 av. stop) 55 % _(réel 5 s)_ · EV/risk 0.02 _(réel 5 s)_ (GBM 0.027) · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩995872.08–₩1020610.15 (mid ₩1008241.12)
- Spot actuel : ₩1085000.00 (+7.6% au-dessus de la zone — repli à attendre)
- Stop : ₩935741.12 (stop swing_plan-based (-13.76%))
- Targets : T1 ₩1070086.28 · R/R 0.85 | T2 ₩1131931.44 · R/R 1.71 | T3 ₩1193776.60 · R/R 2.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩935741.12


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (13.76 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.76 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.827 % | pire -13.219 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2391** [0.1802 ; 0.3066] _(largeur 12.6 pt, n_eff 173.1)_
   - swing : **0.4759** [0.4236 ; 0.5286] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5239** [0.4712 ; 0.5762] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.6 pt), swing (47.4 pt), deep (46.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-5.52 %** | CVaR **-7.52 %** | vol 3.9 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.67 % contre 4.51 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.29 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.857 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5263** (β de hausse 0.2937, asymétrie 1.7922) vs KS11 — 553 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.312× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : 0.027 | EV/share : ₩1946.660 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 21 % | T3 11 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 23.1 | bear 71.9 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.217% → cible +2.743% / stop −8.0%, p_fill 38%, n_eff≈17.6) : P(cible|rempli) **48%** · **EV/risk -0.013** (×p_fill ; si rempli -0.28% du capital)
  - **swing** (entrée dip −7.078% → cible +6.134% / stop −7.191%, p_fill 30%, n_eff≈14.4) : P(cible|rempli) **55%** · **EV/risk +0.020** (×p_fill ; si rempli +0.48% du capital)
  - **deep** (entrée dip −10.937% → cible +8.675% / stop −11.253%, p_fill 26%, n_eff≈14.7) : P(cible|rempli) **59%** · **EV/risk +0.004** (×p_fill ; si rempli +0.17% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→66% · +2.0%→46% · +3.0%→31% · +5.0%→19% · +8.0%→4%
- Range intraday médian 6.4% (p90 9.56%) · excursion haute méd. +1.92% / basse méd. −3.01%
- Profil de vol intra : ouverture 4.551% vs midi 1.261% vs clôture 1.31% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.045)_ ; drift intra méd. -0.34% ; recovery-V 34%
- **σ réalisé intraday** 4.573% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 47% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 1170250.0 (VA 1166450.0–1194950.0 ; dernier close 1170000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 32% · rebond 78% · **stop −5.03%** sous le fill (sous le bruit) · cible +2.07% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.63% · baisse 32% (gap-down >1% 19% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −1.54% (p90 −4.05%) · haut méd +1.0% · range méd 2.94%
- Excursion ouverture 15min (n=160) : bas méd −1.98% (p90 −5.04%) · haut méd +1.28% · range méd 3.67%
- Excursion ouverture 30min (n=160) : bas méd −2.13% (p90 −5.71%) · haut méd +1.29% · range méd 4.14%
- Excursion ouverture 60min (n=160) : bas méd −2.22% (p90 −5.82%) · haut méd +1.57% · range méd 4.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1170000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 70% (113/159) · gap 21% · délai 0.1min · rebond 53% (58/113) (MFE +1.12%)
   - −1.0% : fill 30min 56% · séance 66% (108/159) · gap 19% · délai 0.8min · rebond 58% (64/108) (MFE +1.09%)
   - −1.5% : fill 30min 50% · séance 59% (99/159) · gap 11% · délai 1.4min · rebond 61% (57/99) (MFE +1.39%)
   - −2.0% : fill 30min 43% · séance 52% (82/159) · gap 9% · délai 3.6min · rebond 66% (51/82) (MFE +1.61%)
   - −3.0% : fill 30min 28% · séance 43% (61/159) · gap 4% · délai 5.3min · rebond 76% (43/61) (MFE +1.93%)
   - −4.0% : fill 30min 17% · séance 32% (46/159) · gap 2% · délai 21.8min · rebond 78% (37/46) (MFE +2.07%)
   - −5.0% : fill 30min 11% · séance 22% (33/159) · gap 1% · délai 26.0min · rebond 80% (27/33) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −2.26%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.64% (p90 −2.79%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.72% (p90 −2.83%) → stop au-delà de −2.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=789 jambes) : jambe baissière méd −1.2% (p90 −3.22%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (37 séances) :
      · −1.0% : fill 88% (35/37) · rebond 50% (16/35)
      · −2.0% : fill 83% (32/37) · rebond 64% (19/32)
      · −3.0% : fill 80% (29/37) · rebond 79% (21/29)
      · −4.0% : fill 64% (25/37) · rebond 90% (21/25)
      · −5.0% : fill 37% (16/37) · rebond 88% (14/16)
   - **flat** (20 séances) :
      · −1.0% : fill 90% (19/20) · rebond 49% (10/19)
      · −2.0% : fill 69% (15/20) · rebond 48% (7/15)
      · −3.0% : fill 53% (9/20) · rebond 37% (3/9)
      · −4.0% : fill 53% (9/20) · rebond 48% (5/9)
      · −5.0% : fill 51% (8/20) · rebond 52% (4/8)
   - **gap-up** (102 séances) :
      · −1.0% : fill 51% (54/102) · rebond 68% (38/54)
      · −2.0% : fill 36% (35/102) · rebond 76% (25/35)
      · −3.0% : fill 26% (23/102) · rebond 89% (19/23)
      · −4.0% : fill 13% (12/102) · rebond 80% (11/12)
      · −5.0% : fill 10% (9/102) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 76% si les 15 1res min sont vertes (56 cas) · 19% si rouges (104 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 87% si début vert vs 9% si rouge (base 42% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=57) : tient le vert **87%** · continue >prix actuel 55% ; creux résiduel méd -1.59% (q20 -3.2%) → **SL/trailing à −3.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.72% / q75 +4.3% → **scale +2.72% / runner +4.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=103) : edge inversé — récupère vert seulement **9%** (continue à baisser 47%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.79%** (au-delà de la MAE q10 -5.79%), cible rebond +1.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.7% .. +3.86%] · haut q95 +5.45% · bas q05 -6.96%
   - 60min (n=160) : retour [-5.11% .. +4.73%] · haut q95 +6.77% · bas q05 -7.26%
   - 2h (n=160) : retour [-6.83% .. +6.1%] · haut q95 +7.17% · bas q05 -8.42%
   - 4h (n=160) : retour [-7.37% .. +5.9%] · haut q95 +7.85% · bas q05 -8.86%
   - 6h (n=160) : retour [-6.81% .. +6.31%] · haut q95 +8.47% · bas q05 -9.11%
   - session (n=160) : retour [-6.93% .. +6.32%] · haut q95 +8.47% · bas q05 -9.11%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.58%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 65.6  _(momentum haussier)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist 12952.738  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 47.0%
- **ATR** : 72500.0 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.029  _(neutre)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 40.3  _(transition)_
- **MA** : MA20 1037600.0 · MA50 1039200.0 · MA200 1147120.37  _(prix > MA20)_
- **Dist MA** : MA20 +4.6% · MA50 +4.4% · MA200 -5.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (605758 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# 012450

**Generated** : 2026-10-15T21:56:18.287988+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩824000.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (7 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩824000.00 (+1.2% vs entrée) · entrée ₩813954.46 · stop ₩793034.06 · T1 ₩855795.24 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 15.1 < 20 (tendance pas encore confirmée) alors que Choppiness 30.1 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-15 : 824000.0 · ATR Wilder 53752.05 (6.52 %)_
- **Swing** : plage **760002.6 → 723267.29** (-7.77 % a -12.22 % sous la cloture, 0.68 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 739005.77-763528.87 (A). stop INDICATIF 668483.77 (-7.57 % sous le bas ; sous le support 695359.79-714206.92 (- 0,5 ATR)).
- **Deep** : plage **723267.29 → 632449.6** (-12.22 % a -23.25 % sous la cloture, 1.69 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 695359.79-714206.92 (C) ; 630882.78-639810.36 (B). stop INDICATIF 560360.75 (-11.4 % sous le bas ; sous le support 587236.78-603108.04 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.1 ATR sous le plus haut 20 s., RSI(2) 5.2. Limite **797123.97** (seance suivante), stop catastrophe 582115.75, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 802490.8-806458.62 (A, -2.13 %) ; 774716.09-798522.98 (A, -3.09 %) ; 739005.77-763528.87 (A, -7.34 %) ; 695359.79-714206.92 (C, -13.32 %) ; 630882.78-639810.36 (B, -22.35 %) ; 587236.78-603108.04 (A, -26.81 %)
- Resistances reelles au-dessus : 862000.0-885814.95 (A, 4.61 %) ; 891766.7-918549.41 (A, 8.22 %) ; 955000.0-979058.66 (A, 15.9 %) ; 994929.92-1021000.0 (A, 20.74 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.59 %)** : le gap seul le franchit 0.246 % des séances (3 fois sur 1219).
   - exécution **4.568 pt plus bas** dans le cas TYPIQUE (médiane), 4.617 au p90, **4.629 au pire**
   - perte réelle **11.779 %** en moyenne _(tirée par la queue)_, jusqu'à **13.219 %** — au lieu des 8.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0078 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.814 % | p01 -3.826 % | pire -13.219 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5249** [0.4506 ; 0.5984] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4268** [0.3754 ; 0.4794] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.418** [0.3669 ; 0.4705] _(largeur 10.4 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-5.94 %** | CVaR **-7.72 %** | vol 3.98 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.44 % contre 3.99 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.6 % vs -12.04 % si l'on extrapolait par √5 _(rapport 0.88 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5228** (β de hausse 0.2894, asymétrie 1.8068) vs KS11 — 556 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.289× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 72.6 | bear 5.0 | side 22.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.221% → cible +5.14% / stop −2.57%, p_fill 80%, n_eff≈86.2) : P(cible|rempli) **16%** · **EV/risk -0.080** (×p_fill ; si rempli -0.26% du capital)
  - **swing** (entrée dip −2.678% → cible +6.721% / stop −6.075%, p_fill 66%, n_eff≈77.2) : P(cible|rempli) **32%** · **EV/risk -0.089** (×p_fill ; si rempli -0.82% du capital)
  - **deep** (entrée dip −4.142% → cible +9.752% / stop −9.251%, p_fill 63%, n_eff≈71.9) : P(cible|rempli) **34%** · **EV/risk -0.110** (×p_fill ; si rempli -1.63% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→65% · +2.0%→43% · +3.0%→30% · +5.0%→14% · +8.0%→3%
- Range intraday médian 5.56% (p90 8.69%) · excursion haute méd. +1.85% / basse méd. −2.64%
- Profil de vol intra : ouverture 3.964% vs midi 1.029% vs clôture 1.113% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.151 ; mean-reverting — autocorr -0.077)_ ; drift intra méd. -0.494% ; recovery-V 31%
- **σ réalisé intraday** 3.186% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 48% / whipsaw 7%
- POC intraday (dernière séance, temps-au-prix) : 1052650.0 (VA 1050050.0–1076050.0 ; dernier close 1071000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 78% · **stop −4.73%** sous le fill (sous le bruit) · cible +1.63% · R/R 0.34 (high win-rate)
- Gaps overnight (n=152) : méd. 0.51% · baisse 25% (gap-down >1% 11% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −1.23% (p90 −3.6%) · haut méd +0.83% · range méd 2.43%
- Excursion ouverture 15min (n=160) : bas méd −1.57% (p90 −4.14%) · haut méd +1.08% · range méd 3.23%
- Excursion ouverture 30min (n=160) : bas méd −1.83% (p90 −4.54%) · haut méd +1.09% · range méd 3.65%
- Excursion ouverture 60min (n=160) : bas méd −1.98% (p90 −4.99%) · haut méd +1.28% · range méd 4.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1072000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 76% (115/152) · gap 17% · délai 0.3min · rebond 59% (61/115) (MFE +1.25%)
   - −1.0% : fill 30min 53% · séance 66% (102/152) · gap 11% · délai 1.4min · rebond 54% (51/102) (MFE +1.12%)
   - −1.5% : fill 30min 40% · séance 51% (85/152) · gap 8% · délai 1.5min · rebond 47% (39/85) (MFE +0.97%)
   - −2.0% : fill 30min 33% · séance 45% (78/152) · gap 4% · délai 4.5min · rebond 59% (43/78) (MFE +1.15%)
   - −3.0% : fill 30min 24% · séance 38% (62/152) · gap 1% · délai 18.1min · rebond 63% (37/62) (MFE +1.33%)
   - −4.0% : fill 30min 14% · séance 27% (48/152) · gap 1% · délai 25.3min · rebond 74% (35/48) (MFE +1.61%)
   - −5.0% : fill 30min 10% · séance 18% (34/152) · gap 1% · délai 8.8min · rebond 78% (28/34) (MFE +1.63%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −2.18%) → stop au-delà de −1.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.62%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −2.64%) → stop au-delà de −1.96% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=765 jambes) : jambe baissière méd −1.19% (p90 −3.21%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (37 séances) :
      · −1.0% : fill 100% (37/37) · rebond 40% (13/37)
      · −2.0% : fill 87% (33/37) · rebond 57% (16/33)
      · −3.0% : fill 85% (31/37) · rebond 66% (18/31)
      · −4.0% : fill 70% (26/37) · rebond 67% (17/26)
      · −5.0% : fill 50% (21/37) · rebond 83% (18/21)
   - **flat** (29 séances) :
      · −1.0% : fill 83% (25/29) · rebond 78% (17/25)
      · −2.0% : fill 54% (19/29) · rebond 52% (10/19)
      · −3.0% : fill 42% (12/29) · rebond 48% (6/12)
      · −4.0% : fill 24% (9/29) · rebond 84% (7/9)
      · −5.0% : fill 15% (5/29) · rebond 32% (2/5)
   - **gap-up** (86 séances) :
      · −1.0% : fill 47% (40/86) · rebond 47% (21/40)
      · −2.0% : fill 27% (26/86) · rebond 67% (17/26)
      · −3.0% : fill 19% (19/86) · rebond 69% (13/19)
      · −4.0% : fill 13% (13/86) · rebond 79% (11/13)
      · −5.0% : fill 7% (8/86) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 77% si les 15 1res min sont vertes (54 cas) · 21% si rouges (106 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **45min** → P(séance verte=clôture>ouverture) 83% si début vert vs 17% si rouge (base 40% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=56) : tient le vert **83%** · continue >prix actuel 48% ; creux résiduel méd -1.39% (q20 -3.07%) → **SL/trailing à −3.07%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.2% / q75 +3.72% → **scale +2.2% / runner +3.72%**, sortie à la clôture
  - **si ROUGE au coude** (n=104) : edge inversé — récupère vert seulement **17%** (continue à baisser 58%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.65%** (au-delà de la MAE q10 -4.65%), cible rebond +1.14% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.71% .. +3.46%] · haut q95 +4.32% · bas q05 -5.91%
   - 60min (n=160) : retour [-4.92% .. +3.54%] · haut q95 +5.34% · bas q05 -6.05%
   - 2h (n=160) : retour [-5.52% .. +3.53%] · haut q95 +6.63% · bas q05 -8.05%
   - 4h (n=160) : retour [-6.56% .. +5.04%] · haut q95 +7.04% · bas q05 -8.31%
   - 6h (n=160) : retour [-6.64% .. +5.0%] · haut q95 +7.06% · bas q05 -8.39%
   - session (n=160) : retour [-6.48% .. +4.91%] · haut q95 +7.06% · bas q05 -8.39%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.48%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 20.0  _(survente)_
- **ADX** : 15.1  _(pas de tendance nette)_
- **MACD** : hist -23318.963  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 38.0%
- **ATR** : 48714.29 (17.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.32  _(distribution)_
- **Vol ratio** : 1.13  _(volume normal)_
- **Choppiness** : 30.1  _(marche directionnel)_
- **MA** : MA20 999350.0 · MA50 1049200.0 · MA200 1167818.03  _(prix < MA20)_
- **Dist MA** : MA20 -17.5% · MA50 -21.5% · MA200 -29.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (550241 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# 005930

**Generated** : 2026-10-16T21:53:44.104815+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩215500.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (8 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩215500.00 (+0.8% vs entrée) · entrée ₩213709.63 · stop ₩208740.89 · T1 ₩223647.12 · R/R 2.0  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.32% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 17.8 < 20 (tendance pas encore confirmée) alors que Choppiness 29.2 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 215500.0 · ATR Wilder 13022.24 (6.04 %)_
- **Swing** : plage **199783.2 → 190033.31** (-7.29 % a -11.82 % sous la cloture, 0.75 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 189200.0-194183.48 (A). stop INDICATIF 177011.08 (-6.85 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **190033.31 → 162582.29** (-11.82 % a -24.56 % sous la cloture, 2.11 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 189200.0-194183.48 (A) ; 166770.51-168863.88 (A). stop INDICATIF 142216.68 (-12.53 % sous le bas ; sous le support 148727.8-151120.2 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.38 ATR sous le plus haut 20 s., RSI(2) 27.8. Limite **208988.88** (seance suivante), stop catastrophe 156899.94, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 189200.0-194183.48 (A, -9.89 %) ; 166770.51-168863.88 (A, -21.64 %) ; 148727.8-151120.2 (B, -29.87 %) ; 141351.23-144042.66 (A, -33.16 %) ; 128093.31-132280.01 (B, -38.62 %) ; 109617.41-111502.24 (C, -48.26 %)
- Resistances reelles au-dessus : 222294.24-227500.0 (A, 3.15 %) ; 240000.0-246500.0 (A, 11.37 %) ; 261711.37-267000.0 (A, 21.44 %) ; 276000.0-281500.0 (A, 28.07 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.27 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.63 %)** : le gap seul le franchit 0.246 % des séances (3 fois sur 1219).
   - exécution **0.181 pt plus bas** dans le cas TYPIQUE (médiane), 2.686 au p90, **3.312 au pire**
   - perte réelle **8.848 %** en moyenne _(tirée par la queue)_, jusqu'à **10.942 %** — au lieu des 7.63 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.003 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.529 % | p01 -4.987 % | pire -10.942 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4095** [0.3382 ; 0.4838] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.3004** [0.2539 ; 0.3502] _(largeur 9.6 pt, n_eff 345.6)_
   - deep : **0.283** [0.2375 ; 0.3322] _(largeur 9.5 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.82 %** | CVaR **-9.95 %** | vol 4.83 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.87 % contre 5.66 % aujourd'hui, rapport 0.51)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.76 % vs -7.58 % si l'on extrapolait par √5 _(rapport 0.893 ; < 1 = le √5 surestime)_
- **β de baisse : 1.179** (β de hausse 1.3399, asymétrie 0.8799) vs KS11 — 556 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.007 | EV/share : ₩-33.183 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 17 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 77.7 | bear 5.0 | side 17.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.834% → cible +4.65% / stop −2.325%, p_fill 73%, n_eff≈80.6) : P(cible|rempli) **12%** · **EV/risk -0.132** (×p_fill ; si rempli -0.42% du capital)
  - **swing** (entrée dip −1.83% → cible +6.606% / stop −5.908%, p_fill 67%, n_eff≈78.3) : P(cible|rempli) **35%** · **EV/risk -0.116** (×p_fill ; si rempli -1.02% du capital)
  - **deep** (entrée dip −2.83% → cible +15.681% / stop −8.954%, p_fill 67%, n_eff≈74.0) : P(cible|rempli) **22%** · **EV/risk +0.066** (×p_fill ; si rempli +0.88% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→67% · +2.0%→43% · +3.0%→30% · +5.0%→18% · +8.0%→3%
- Range intraday médian 4.91% (p90 9.02%) · excursion haute méd. +1.77% / basse méd. −2.09%
- Profil de vol intra : ouverture 2.584% vs midi 1.124% vs clôture 1.267% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓1% ; spike-down 56% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.092)_ ; drift intra méd. -0.045% ; recovery-V 21%
- **σ réalisé intraday** 2.631% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 69% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 275968.75 (VA 275281.25–276931.25 ; dernier close 275300.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 48% · **stop −6.29%** sous le fill (sous le bruit) · cible +0.82% · R/R 0.13 (high win-rate)
- Gaps overnight (n=152) : méd. 0.32% · baisse 45% (gap-down >1% 31% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.43%) · haut méd +0.58% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.18%) · haut méd +0.73% · range méd 1.82%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.73%) · haut méd +0.92% · range méd 2.19%
- Excursion ouverture 60min (n=160) : bas méd −1.17% (p90 −3.4%) · haut méd +1.17% · range méd 2.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 276000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 65% (91/152) · gap 36% · délai 0.0min · rebond 47% (43/91) (MFE +0.92%)
   - −1.0% : fill 30min 43% · séance 56% (82/152) · gap 31% · délai 0.0min · rebond 58% (44/82) (MFE +1.3%)
   - −1.5% : fill 30min 36% · séance 46% (70/152) · gap 24% · délai 0.0min · rebond 57% (38/70) (MFE +1.5%)
   - −2.0% : fill 30min 29% · séance 40% (64/152) · gap 21% · délai 0.0min · rebond 56% (36/64) (MFE +1.24%)
   - −3.0% : fill 30min 24% · séance 34% (56/152) · gap 20% · délai 0.0min · rebond 47% (30/56) (MFE +0.92%)
   - −4.0% : fill 30min 18% · séance 28% (44/152) · gap 9% · délai 3.7min · rebond 54% (26/44) (MFE +1.19%)
   - −5.0% : fill 30min 9% · séance 18% (31/152) · gap 6% · délai 40.6min · rebond 48% (19/31) (MFE +0.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.76%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.45% (p90 −2.45%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.4%) → stop au-delà de −1.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=740 jambes) : jambe baissière méd −1.18% (p90 −2.82%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 98% (54/56) · rebond 52% (25/54)
      · −2.0% : fill 73% (45/56) · rebond 42% (21/45)
      · −3.0% : fill 70% (44/56) · rebond 44% (23/44)
      · −4.0% : fill 61% (36/56) · rebond 52% (21/36)
      · −5.0% : fill 39% (26/56) · rebond 38% (14/26)
   - **flat** (15 séances) :
      · −1.0% : fill 57% (11/15) · rebond 64% (6/11)
      · −2.0% : fill 41% (7/15) · rebond 85% (5/7)
      · −3.0% : fill 18% (4/15) · rebond 18% (1/4)
      · −4.0% : fill 12% (2/15) · rebond 0% (0/2)
      · −5.0% : fill 12% (2/15) · rebond 100% (2/2)
   - **gap-up** (81 séances) :
      · −1.0% : fill 25% (17/81) · rebond 72% (13/17)
      · −2.0% : fill 16% (12/81) · rebond 86% (10/12)
      · −3.0% : fill 10% (8/81) · rebond 78% (6/8)
      · −4.0% : fill 7% (6/81) · rebond 93% (5/6)
      · −5.0% : fill 3% (3/81) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 64% si les 15 1res min sont vertes (78 cas) · 22% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:17** → P(séance verte=clôture>ouverture) 81% si début vert vs 11% si rouge (base 43% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **81%** · continue >prix actuel 60% ; creux résiduel méd -1.13% (q20 -2.54%) → **SL/trailing à −2.54%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +3.01% → **scale +1.5% / runner +3.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **11%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.84%** (au-delà de la MAE q10 -5.84%), cible rebond +0.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +2.46%] · haut q95 +3.12% · bas q05 -3.57%
   - 60min (n=160) : retour [-2.81% .. +3.45%] · haut q95 +4.39% · bas q05 -3.67%
   - 2h (n=160) : retour [-4.15% .. +4.5%] · haut q95 +5.64% · bas q05 -5.14%
   - 4h (n=160) : retour [-5.6% .. +5.04%] · haut q95 +6.29% · bas q05 -7.01%
   - 6h (n=160) : retour [-5.93% .. +4.97%] · haut q95 +6.76% · bas q05 -7.24%
   - session (n=160) : retour [-5.53% .. +5.29%] · haut q95 +6.76% · bas q05 -7.24%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.92%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.25 · part idiosyncratique 0.75
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 22.3  _(survente)_
- **ADX** : 17.8  _(pas de tendance nette)_
- **MACD** : hist -6809.085  _(pas de croisement recent)_
- **BB** : %B -0.0 · largeur 32.7%
- **ATR** : 12500.0 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.2  _(distribution)_
- **Vol ratio** : 1.04  _(volume normal)_
- **Choppiness** : 29.2  _(marche directionnel)_
- **MA** : MA20 257850.0 · MA50 256840.0 · MA200 231815.36  _(prix < MA20)_
- **Dist MA** : MA20 -16.4% · MA50 -16.1% · MA200 -7.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (494220 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

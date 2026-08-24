# 000660

**Generated** : 2026-08-24T00:14:08.027579+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1730000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1730000.00 (+0.8% vs entrée) · entrée ₩1715569.94 · stop ₩1645854.91 · T1 ₩1855000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 2 % _(réel 5 s)_ · EV/risk -0.336 _(réel 5 s)_ (GBM -0.137) · ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.06% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.210 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1701139.88–₩1730000.00 (mid ₩1715569.94)
- Spot actuel : ₩1730000.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : ₩1645854.91 (stop swing_plan-based (-11.14%))
- Targets : T1 ₩1855000.00 · R/R 2.0 | T2 ₩1920434.17 · R/R 2.94 | T3 ₩1985868.34 · R/R 3.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1645854.91


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.08 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.14 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.14 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.338 % | p01 -7.0 % | pire -10.86 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2398** [0.1809 ; 0.3074] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.4015** [0.3508 ; 0.4538] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.433** [0.3815 ; 0.4856] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.3 pt), swing (31.1 pt), deep (29.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.71 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 3.49 % contre 7.24 % aujourd'hui, rapport 0.48)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.39 % si l'on extrapolait par √5 _(rapport 0.905 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4119** (β de hausse 1.6127, asymétrie 0.8755) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.137 | EV/share : ₩-9526.798 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 28 % | T3 28 %
- Kelly (position) : f* 0.101 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 33.7 | bear 24.8 | side 41.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.83% → cible +8.127% / stop −4.064%, p_fill 89%, n_eff≈36.6) : P(cible|rempli) **2%** · **EV/risk -0.336** (×p_fill ; si rempli -1.53% du capital)
  - **swing** (entrée dip −1.84% → cible +18.948% / stop −9.474%, p_fill 82%, n_eff≈33.8) : P(cible|rempli) **17%** · **EV/risk -0.269** (×p_fill ; si rempli -3.11% du capital)
  - **deep** (entrée dip −2.683% → cible +16.608% / stop −12.277%, p_fill 88%, n_eff≈33.1) : P(cible|rempli) **21%** · **EV/risk -0.415** (×p_fill ; si rempli -5.81% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→79% · +2.0%→55% · +3.0%→44% · +5.0%→30% · +8.0%→14%
- Range intraday médian 7.44% (p90 11.62%) · excursion haute méd. +2.24% / basse méd. −3.4%
- Profil de vol intra : ouverture 3.417% vs midi 1.481% vs clôture 1.699% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 17% · trend ↑2%/↓0% ; spike-down 73% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; neutre — autocorr -0.029)_ ; drift intra méd. -1.326% ; recovery-V 28%
- **σ réalisé intraday** 4.847% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 70% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 1757975.0 (VA 1729925.0–1757975.0 ; dernier close 1728000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 66% · **stop −8.17%** sous le fill (sous le bruit) · cible +2.43% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. 0.6% · baisse 46% (gap-down >1% 35% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.78% (p90 −2.1%) · haut méd +0.79% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.74%) · haut méd +0.99% · range méd 2.41%
- Excursion ouverture 30min (n=160) : bas méd −1.57% (p90 −3.72%) · haut méd +1.3% · range méd 2.96%
- Excursion ouverture 60min (n=160) : bas méd −1.75% (p90 −4.92%) · haut méd +1.51% · range méd 3.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1728000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 66% (100/159) · gap 40% · délai 0.0min · rebond 56% (53/100) (MFE +1.23%)
   - −1.0% : fill 30min 51% · séance 62% (92/159) · gap 35% · délai 0.0min · rebond 63% (57/92) (MFE +1.74%)
   - −1.5% : fill 30min 44% · séance 57% (83/159) · gap 32% · délai 0.0min · rebond 65% (52/83) (MFE +2.16%)
   - −2.0% : fill 30min 39% · séance 52% (75/159) · gap 27% · délai 0.0min · rebond 62% (48/75) (MFE +1.93%)
   - −3.0% : fill 30min 37% · séance 46% (65/159) · gap 23% · délai 0.1min · rebond 63% (44/65) (MFE +2.09%)
   - −4.0% : fill 30min 28% · séance 39% (51/159) · gap 15% · délai 2.3min · rebond 69% (37/51) (MFE +2.16%)
   - −5.0% : fill 30min 17% · séance 34% (43/159) · gap 10% · délai 24.4min · rebond 66% (31/43) (MFE +2.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.45%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −3.01%) → stop au-delà de −2.29% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.63%) → stop au-delà de −2.32% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=866 jambes) : jambe baissière méd −1.31% (p90 −3.53%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (67 séances) :
      · −1.0% : fill 98% (65/67) · rebond 51% (34/65)
      · −2.0% : fill 87% (56/67) · rebond 52% (31/56)
      · −3.0% : fill 83% (51/67) · rebond 62% (33/51)
      · −4.0% : fill 72% (43/67) · rebond 61% (29/43)
      · −5.0% : fill 64% (37/67) · rebond 58% (25/37)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (80 séances) :
      · −1.0% : fill 29% (18/80) · rebond 89% (16/18)
      · −2.0% : fill 19% (12/80) · rebond 90% (11/12)
      · −3.0% : fill 16% (9/80) · rebond 59% (6/9)
      · −4.0% : fill 13% (6/80) · rebond 100% (6/6)
      · −5.0% : fill 11% (5/80) · rebond 100% (5/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 52% si les 15 1res min sont vertes (83 cas) · 33% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 73% si début vert vs 21% si rouge (base 43% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **73%** · continue >prix actuel 43% ; creux résiduel méd -1.91% (q20 -6.19%) → **SL/trailing à −6.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +2.65% → **scale +1.31% / runner +2.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **21%** (continue à baisser 62%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.78%** (au-delà de la MAE q10 -6.78%), cible rebond +1.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.36% .. +2.89%] · haut q95 +3.66% · bas q05 -4.55%
   - 60min (n=160) : retour [-3.88% .. +4.83%] · haut q95 +5.85% · bas q05 -5.57%
   - 2h (n=160) : retour [-5.04% .. +4.93%] · haut q95 +7.82% · bas q05 -7.33%
   - 4h (n=160) : retour [-6.76% .. +6.06%] · haut q95 +8.19% · bas q05 -8.26%
   - 6h (n=160) : retour [-7.04% .. +6.97%] · haut q95 +8.54% · bas q05 -8.86%
   - session (n=160) : retour [-7.13% .. +7.23%] · haut q95 +8.54% · bas q05 -8.86%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 14% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 50.5  _(neutre)_
- **ADX** : 24.6  _(pas de tendance nette)_
- **MACD** : hist 45260.484  _(pas de croisement recent)_
- **BB** : %B 0.79 · largeur 34.7%
- **ATR** : 137785.71 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.207  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 57.9  _(transition)_
- **MA** : MA20 1573250.0 · MA50 2010160.0 · MA200 1251865.31  _(prix > MA20)_
- **Dist MA** : MA20 +10.0% · MA50 -13.9% · MA200 +38.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (759684 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

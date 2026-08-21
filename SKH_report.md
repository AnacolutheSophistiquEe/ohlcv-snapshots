# 000660

**Generated** : 2026-08-21T00:14:45.976333+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1691000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1691000.00 (+0.7% vs entrée) · entrée ₩1679532.51 · stop ₩1591798.76 · T1 ₩1855000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.38 _(réel 5 s)_ (GBM -0.144) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −5.22% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.200 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1668065.02–₩1691000.00 (mid ₩1679532.51)
- Spot actuel : ₩1691000.00 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : ₩1591798.76 (stop swing_plan-based (-11.72%))
- Targets : T1 ₩1855000.00 · R/R 2.0 | T2 ₩1900318.61 · R/R 2.52 | T3 ₩1945637.22 · R/R 3.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1591798.76


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.08 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.72 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.72 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.338 % | p01 -7.0 % | pire -10.86 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2426** [0.1834 ; 0.3104] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.4038** [0.353 ; 0.4562] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.4297** [0.3783 ; 0.4823] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.3 pt), swing (30.7 pt), deep (26.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.71 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 3.49 % contre 7.24 % aujourd'hui, rapport 0.48)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.39 % si l'on extrapolait par √5 _(rapport 0.905 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4119** (β de hausse 1.6004, asymétrie 0.8822) vs KS11 — 553 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.08 ATR (stop 3.583 %) — p(stop avant cible) 0.6258 [0.57 ; 0.68], R/R 2.929, perte reelle 5.679 % (gap inclus), EV 1.4048 % — **REFUSE**
      - refuse : p_stop_first 0.626, borne haute 0.676 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.03 ATR du spot, sous le seuil de 1 ATR : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545] sur 940 touches) contre ~35 % au-dela. L'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 14.072 %) — p(stop avant cible) 0.2768 [0.23 ; 0.33], R/R 1.182, perte reelle 14.072 % (gap inclus), EV 3.0958 % — **REFUSE**
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.07 % > budget 12.0 %
   - 🟢 support a 2.0 ATR (stop 21.62 %) — p(stop avant cible) 0.13 [0.10 ; 0.17], R/R 0.769, perte reelle 21.62 % (gap inclus), EV 3.1123 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.62 % > budget 12.0 %
   - 🟢 support a 2.81 ATR (stop 29.13 %) — p(stop avant cible) 0.058 [0.04 ; 0.09], R/R 0.571, perte reelle 29.13 % (gap inclus), EV 3.1069 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.13 % > budget 12.0 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.144 | EV/share : ₩-12621.676 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.119 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 44.7 | bear 25.4 | side 29.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.682% → cible +10.447% / stop −5.224%, p_fill 94%, n_eff≈37.2) : P(cible|rempli) **1%** · **EV/risk -0.380** (×p_fill ; si rempli -2.11% du capital)
  - **swing** (entrée dip −1.332% → cible +21.057% / stop −10.529%, p_fill 88%, n_eff≈36.1) : P(cible|rempli) **12%** · **EV/risk -0.314** (×p_fill ; si rempli -3.74% du capital)
  - **deep** (entrée dip −1.817% → cible +16.701% / stop −14.333%, p_fill 89%, n_eff≈33.6) : P(cible|rempli) **15%** · **EV/risk -0.568** (×p_fill ; si rempli -9.13% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→78% · +2.0%→54% · +3.0%→41% · +5.0%→28% · +8.0%→14%
- Range intraday médian 7.29% (p90 11.62%) · excursion haute méd. +2.16% / basse méd. −3.4%
- Profil de vol intra : ouverture 3.37% vs midi 1.463% vs clôture 1.671% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 18% · trend ↑2%/↓0% ; spike-down 74% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.045)_ ; drift intra méd. -1.857% ; recovery-V 24%
- **σ réalisé intraday** 4.941% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 77% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 1512737.5 (VA 1505637.5–1528712.5 ; dernier close 1497000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 66% · **stop −8.17%** sous le fill (sous le bruit) · cible +2.43% · R/R 0.3 (high win-rate)
- Gaps overnight (n=159) : méd. 0.58% · baisse 46% (gap-down >1% 35% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.13%) · haut méd +0.79% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.76%) · haut méd +0.99% · range méd 2.38%
- Excursion ouverture 30min (n=160) : bas méd −1.57% (p90 −3.74%) · haut méd +1.26% · range méd 2.93%
- Excursion ouverture 60min (n=160) : bas méd −1.75% (p90 −4.92%) · haut méd +1.47% · range méd 3.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1497000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 66% (101/159) · gap 40% · délai 0.0min · rebond 54% (53/101) (MFE +1.19%)
   - −1.0% : fill 30min 51% · séance 63% (93/159) · gap 35% · délai 0.0min · rebond 62% (57/93) (MFE +1.69%)
   - −1.5% : fill 30min 46% · séance 59% (84/159) · gap 33% · délai 0.0min · rebond 65% (53/84) (MFE +2.12%)
   - −2.0% : fill 30min 40% · séance 53% (76/159) · gap 28% · délai 0.0min · rebond 62% (49/76) (MFE +1.93%)
   - −3.0% : fill 30min 38% · séance 48% (66/159) · gap 24% · délai 0.1min · rebond 63% (45/66) (MFE +2.09%)
   - −4.0% : fill 30min 29% · séance 41% (52/159) · gap 16% · délai 2.4min · rebond 69% (38/52) (MFE +2.19%)
   - −5.0% : fill 30min 18% · séance 35% (43/159) · gap 10% · délai 24.4min · rebond 66% (31/43) (MFE +2.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.49%) → stop au-delà de −1.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −3.04%) → stop au-delà de −2.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.73%) → stop au-delà de −2.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=864 jambes) : jambe baissière méd −1.33% (p90 −3.55%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (68 séances) :
      · −1.0% : fill 98% (66/68) · rebond 48% (34/66)
      · −2.0% : fill 90% (57/68) · rebond 52% (32/57)
      · −3.0% : fill 87% (52/68) · rebond 62% (34/52)
      · −4.0% : fill 76% (44/68) · rebond 61% (30/44)
      · −5.0% : fill 66% (37/68) · rebond 58% (25/37)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (79 séances) :
      · −1.0% : fill 30% (18/79) · rebond 89% (16/18)
      · −2.0% : fill 20% (12/79) · rebond 90% (11/12)
      · −3.0% : fill 16% (9/79) · rebond 59% (6/9)
      · −4.0% : fill 14% (6/79) · rebond 100% (6/6)
      · −5.0% : fill 12% (5/79) · rebond 100% (5/5)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 48% si les 15 1res min sont vertes (82 cas) · 33% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 70% si début vert vs 21% si rouge (base 41% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **70%** · continue >prix actuel 43% ; creux résiduel méd -2.02% (q20 -6.38%) → **SL/trailing à −6.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +2.96% → **scale +1.31% / runner +2.96%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **21%** (continue à baisser 62%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.78%** (au-delà de la MAE q10 -6.78%), cible rebond +1.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.36% .. +2.89%] · haut q95 +3.67% · bas q05 -4.56%
   - 60min (n=160) : retour [-4.05% .. +4.99%] · haut q95 +5.69% · bas q05 -5.6%
   - 2h (n=160) : retour [-5.04% .. +5.09%] · haut q95 +7.86% · bas q05 -7.36%
   - 4h (n=160) : retour [-6.77% .. +6.27%] · haut q95 +8.26% · bas q05 -8.28%
   - 6h (n=160) : retour [-7.07% .. +7.08%] · haut q95 +8.56% · bas q05 -8.92%
   - session (n=160) : retour [-7.13% .. +7.44%] · haut q95 +8.56% · bas q05 -8.92%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **24%**. Lecture précoce 30 min : signature présente → 15% vs absente 1% (base 6%)
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
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 62.4  _(momentum haussier)_
- **ADX** : 26.5  _(tendance etablie)_
- **MACD** : hist 37998.29  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 38.7%
- **ATR** : 158642.86 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.198  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 63.2  _(marche en range (choppy))_
- **MA** : MA20 1582700.0 · MA50 2016520.0 · MA200 1245813.21  _(prix > MA20)_
- **Dist MA** : MA20 +6.8% · MA50 -16.1% · MA200 +35.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (594326 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

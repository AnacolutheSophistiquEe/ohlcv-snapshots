# 000660

**Generated** : 2026-08-20T19:58:53.781454+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1665000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1665000.00 (+4.6% vs entrée) · entrée ₩1592000.00 · stop ₩1544407.14 · T1 ₩1687013.42 · R/R 2.0  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk -0.014 _(réel 5 s)_ (GBM -0.189) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.99% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1575306.70–₩1608693.30 (mid ₩1592000.00)
- Spot actuel : ₩1665000.00 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : ₩1544407.14 (stop swing_plan-based (-20.17%))
- Targets : T1 ₩1687013.42 · R/R 2.0 | T2 ₩1764327.04 · R/R 3.62 | T3 ₩1841640.67 · R/R 5.25
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1544407.14


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.08 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (20.17 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 20.17 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.338 % | p01 -6.997 % | pire -10.86 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2426** [0.1834 ; 0.3104] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.4038** [0.353 ; 0.4562] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.4297** [0.3783 ; 0.4823] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.0 observations effectives », dont la borne haute a 95 % vaut environ 23.0 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.5 observations effectives », dont la borne haute a 95 % vaut environ 22.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (39.5 pt), swing (49.7 pt), deep (46.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.7 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 3.49 % contre 7.21 % aujourd'hui, rapport 0.48)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.38 % si l'on extrapolait par √5 _(rapport 0.905 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4119** (β de hausse 1.6005, asymétrie 0.8821) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.189 | EV/share : ₩-8976.331 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 24 % | T3 24 %
- Kelly (position) : f* 0.052 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 45.0 | bear 25.4 | side 29.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.381% → cible +5.968% / stop −2.99%, p_fill 50%, n_eff≈22.0) : P(cible|rempli) **11%** · **EV/risk -0.014** (×p_fill ; si rempli -0.08% du capital)
  - **swing** (entrée dip −9.641% → cible +23.305% / stop −11.652%, p_fill 33%, n_eff≈13.0) : P(cible|rempli) **0%** · **EV/risk -0.190** (×p_fill ; si rempli -6.62% du capital)
  - **deep** (entrée dip −14.902% → cible +42.563% / stop −18.0%, p_fill 38%, n_eff≈13.5) : P(cible|rempli) **0%** · **EV/risk -0.143** (×p_fill ; si rempli -6.72% du capital)
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

- **RSI** : 61.7  _(momentum haussier)_
- **ADX** : 26.5  _(tendance etablie)_
- **MACD** : hist 36339.03  _(pas de croisement recent)_
- **BB** : %B 0.64 · largeur 38.6%
- **ATR** : 158642.86 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.219  _(distribution)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 63.2  _(marche en range (choppy))_
- **MA** : MA20 1581400.0 · MA50 2016000.0 · MA200 1245683.21  _(prix > MA20)_
- **Dist MA** : MA20 +5.3% · MA50 -17.4% · MA200 +33.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (408144 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

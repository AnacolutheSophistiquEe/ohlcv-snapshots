# 000660

**Generated** : 2026-09-03T00:14:22.675245+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · ₩1613000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot ₩1613000.00 (+8.9% vs entrée) · entrée ₩1480836.32 · stop ₩1364669.13 · T1 ₩1580226.03 · R/R 0.86  
> ↳ P(T1 av. stop) 45 % _(réel 5 s)_ · EV/risk -0.031 _(réel 5 s)_ (GBM 0.264) · ¼-Kelly 0.037 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1460958.38–₩1500714.26 (mid ₩1480836.32)
- Spot actuel : ₩1613000.00 (+8.9% au-dessus de la zone — repli à attendre)
- Stop : ₩1364669.13 (stop swing_plan-based (-15.4%))
- Targets : T1 ₩1580226.03 · R/R 0.86 | T2 ₩1679615.74 · R/R 1.71 | T3 ₩1779005.45 · R/R 2.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1364669.13


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.33 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.4 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 15.4 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.367 % | p01 -7.0 % | pire -10.86 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0657** [0.0358 ; 0.1099] _(largeur 7.4 pt, n_eff 173.1)_
   - swing : **0.2935** [0.2474 ; 0.3431] _(largeur 9.6 pt, n_eff 345.6)_
   - deep : **0.2594** [0.2153 ; 0.3075] _(largeur 9.2 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (25.9 pt), swing (43.2 pt), deep (42.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.71 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.20 % contre 6.88 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.52 % si l'on extrapolait par √5 _(rapport 0.893 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4107** (β de hausse 1.6104, asymétrie 0.876) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.264 | EV/share : ₩30713.305 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 59 % | T2 34 % | T3 16 %
- Kelly (position) : f* 0.149 | ¼-Kelly 0.037 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 22.2 | bear 7.0 | side 70.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.728% → cible +8.611% / stop −8.0%, p_fill 49%, n_eff≈24.9) : P(cible|rempli) **7%** · **EV/risk -0.005** (×p_fill ; si rempli -0.08% du capital)
  - **swing** (entrée dip −8.198% → cible +6.712% / stop −7.845%, p_fill 38%, n_eff≈17.9) : P(cible|rempli) **45%** · **EV/risk -0.031** (×p_fill ; si rempli -0.65% du capital)
  - **deep** (entrée dip −12.668% → cible +9.492% / stop −12.369%, p_fill 42%, n_eff≈18.4) : P(cible|rempli) **57%** · **EV/risk -0.009** (×p_fill ; si rempli -0.27% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→78% · +2.0%→54% · +3.0%→42% · +5.0%→26% · +8.0%→11%
- Range intraday médian 7.29% (p90 11.62%) · excursion haute méd. +2.16% / basse méd. −3.64%
- Profil de vol intra : ouverture 3.459% vs midi 1.5% vs clôture 1.685% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑1%/↓0% ; spike-down 71% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.873% ; recovery-V 31%
- **σ réalisé intraday** 4.349% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 62% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 1696512.5 (VA 1684712.5–1699462.5 ; dernier close 1697000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 38% · rebond 71% · **stop −7.5%** sous le fill (sous le bruit) · cible +2.54% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. 0.57% · baisse 46% (gap-down >1% 37% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.04%) · haut méd +0.77% · range méd 1.68%
- Excursion ouverture 15min (n=160) : bas méd −1.05% (p90 −2.72%) · haut méd +0.92% · range méd 2.34%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.56%) · haut méd +1.23% · range méd 2.95%
- Excursion ouverture 60min (n=160) : bas méd −1.74% (p90 −4.82%) · haut méd +1.49% · range méd 3.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1693000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 66% (98/159) · gap 43% · délai 0.0min · rebond 61% (56/98) (MFE +1.31%)
   - −1.0% : fill 30min 54% · séance 63% (91/159) · gap 37% · délai 0.0min · rebond 66% (60/91) (MFE +1.75%)
   - −1.5% : fill 30min 43% · séance 55% (80/159) · gap 29% · délai 0.0min · rebond 70% (54/80) (MFE +2.08%)
   - −2.0% : fill 30min 38% · séance 51% (74/159) · gap 27% · délai 0.0min · rebond 67% (49/74) (MFE +2.03%)
   - −3.0% : fill 30min 33% · séance 47% (63/159) · gap 20% · délai 1.8min · rebond 69% (42/63) (MFE +2.29%)
   - −4.0% : fill 30min 28% · séance 38% (53/159) · gap 15% · délai 1.5min · rebond 71% (40/53) (MFE +2.54%)
   - −5.0% : fill 30min 17% · séance 32% (42/159) · gap 9% · délai 15.0min · rebond 70% (29/42) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −2.54%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.8% (p90 −2.78%) → stop au-delà de −2.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.99% (p90 −3.48%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=877 jambes) : jambe baissière méd −1.25% (p90 −3.42%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 96% (64/66) · rebond 60% (36/64)
      · −2.0% : fill 82% (56/66) · rebond 61% (33/56)
      · −3.0% : fill 78% (50/66) · rebond 64% (31/50)
      · −4.0% : fill 67% (44/66) · rebond 68% (32/44)
      · −5.0% : fill 57% (36/66) · rebond 63% (23/36)
   - **flat** (9 séances) :
      · −1.0% : fill 91% (8/9) · rebond 100% (8/8)
      · −2.0% : fill 37% (3/9) · rebond 100% (3/3)
      · −3.0% : fill 26% (2/9) · rebond 100% (2/2)
      · −4.0% : fill 0% (0/9) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/9) · rebond 0% (0/0)
   - **gap-up** (84 séances) :
      · −1.0% : fill 32% (19/84) · rebond 76% (16/19)
      · −2.0% : fill 24% (15/84) · rebond 82% (13/15)
      · −3.0% : fill 20% (11/84) · rebond 84% (9/11)
      · −4.0% : fill 15% (9/84) · rebond 82% (8/9)
      · −5.0% : fill 12% (6/84) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 55% si les 15 1res min sont vertes (82 cas) · 34% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 78% si début vert vs 13% si rouge (base 44% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **78%** · continue >prix actuel 55% ; creux résiduel méd -1.53% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.66% / q75 +3.7% → **scale +1.66% / runner +3.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **13%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.41%** (au-delà de la MAE q10 -6.41%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.33% .. +2.59%] · haut q95 +3.51% · bas q05 -4.51%
   - 60min (n=160) : retour [-3.62% .. +4.57%] · haut q95 +5.81% · bas q05 -5.46%
   - 2h (n=160) : retour [-4.97% .. +4.84%] · haut q95 +7.46% · bas q05 -7.23%
   - 4h (n=160) : retour [-6.7% .. +5.72%] · haut q95 +7.93% · bas q05 -8.17%
   - 6h (n=160) : retour [-6.91% .. +6.64%] · haut q95 +8.47% · bas q05 -8.67%
   - session (n=160) : retour [-7.13% .. +6.94%] · haut q95 +8.47% · bas q05 -8.67%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 12% vs absente 1% (base 6%)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.3  _(momentum haussier)_
- **ADX** : 16.2  _(pas de tendance nette)_
- **MACD** : hist 23199.921  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 26.3%
- **ATR** : 116167.19 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.224  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 63.3  _(marche en range (choppy))_
- **MA** : MA20 1607473.37 · MA50 1881580.77 · MA200 1295439.82  _(prix > MA20)_
- **Dist MA** : MA20 +0.3% · MA50 -14.3% · MA200 +24.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (219946 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

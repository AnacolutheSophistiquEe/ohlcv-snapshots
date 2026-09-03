# 298040

**Generated** : 2026-09-03T21:54:53.195852+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩2725000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot ₩2725000.00 (+4.0% vs entrée) · entrée ₩2620830.12 · stop ₩2452972.97 · T1 ₩2764108.45 · R/R 0.85  
> ↳ P(T1 av. stop) 66 % _(réel 5 s)_ · EV/risk 0.163 _(réel 5 s)_ (GBM 0.159) · ¼-Kelly 0.026 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2592174.45–₩2649485.78 (mid ₩2620830.12)
- Spot actuel : ₩2725000.00 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : ₩2452972.97 (stop swing_plan-based (-9.98%))
- Targets : T1 ₩2764108.45 · R/R 0.85 | T2 ₩2907386.78 · R/R 1.71 | T3 ₩3050665.12 · R/R 2.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2452972.97


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.20 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.98 %)** : le gap seul le franchit 0.082 % des séances (1 fois sur 1218).
   - exécution **1.706 pt plus bas** dans le cas TYPIQUE (médiane), 1.706 au p90, **1.706 au pire**
   - perte réelle **11.686 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 9.98 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0014 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.466 % | p01 -4.657 % | pire -11.686 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0759** [0.0433 ; 0.1225] _(largeur 7.9 pt, n_eff 173.1)_
   - swing : **0.3564** [0.3073 ; 0.4079] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3234** [0.2757 ; 0.374] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.2 pt), swing (32.1 pt), deep (33.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.96 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 3.65 % contre 5.92 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.9 % vs -12.6 % si l'on extrapolait par √5 _(rapport 0.944 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0784** (β de hausse 0.9884, asymétrie 1.091) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.159 | EV/share : ₩26661.574 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 36 % | T3 21 %
- Kelly (position) : f* 0.106 | ¼-Kelly 0.026 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 79.9 | bear 14.1 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.739% → cible +2.445% / stop −8.0%, p_fill 80%, n_eff≈34.6) : P(cible|rempli) **48%** · **EV/risk -0.010** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −3.82% → cible +5.467% / stop −6.405%, p_fill 75%, n_eff≈31.4) : P(cible|rempli) **66%** · **EV/risk +0.163** (×p_fill ; si rempli +1.39% du capital)
  - **deep** (entrée dip −5.91% → cible +7.731% / stop −9.82%, p_fill 66%, n_eff≈29.1) : P(cible|rempli) **62%** · **EV/risk +0.054** (×p_fill ; si rempli +0.81% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→61% · +2.0%→50% · +3.0%→36% · +5.0%→20% · +8.0%→5%
- Range intraday médian 6.89% (p90 10.6%) · excursion haute méd. +2.05% / basse méd. −3.98%
- Profil de vol intra : ouverture 4.525% vs midi 1.167% vs clôture 1.233% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓1% ; spike-down 83% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. -0.986% ; recovery-V 35%
- **σ réalisé intraday** 4.317% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 57% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 2903900.0 (VA 2882300.0–2909300.0 ; dernier close 2918000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 75% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.09% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.78% · baisse 33% (gap-down >1% 25% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.63% (p90 −3.31%) · haut méd +0.69% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −2.02% (p90 −4.21%) · haut méd +0.81% · range méd 3.32%
- Excursion ouverture 30min (n=160) : bas méd −2.39% (p90 −4.45%) · haut méd +0.85% · range méd 4.04%
- Excursion ouverture 60min (n=160) : bas méd −2.54% (p90 −5.29%) · haut méd +1.1% · range méd 4.44%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2916000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 69% (107/159) · gap 30% · délai 0.1min · rebond 54% (64/107) (MFE +1.13%)
   - −1.0% : fill 30min 56% · séance 63% (99/159) · gap 25% · délai 0.2min · rebond 54% (58/99) (MFE +1.22%)
   - −1.5% : fill 30min 50% · séance 56% (89/159) · gap 22% · délai 1.2min · rebond 55% (54/89) (MFE +1.11%)
   - −2.0% : fill 30min 46% · séance 54% (80/159) · gap 18% · délai 2.7min · rebond 50% (43/80) (MFE +1.0%)
   - −3.0% : fill 30min 32% · séance 46% (67/159) · gap 11% · délai 6.1min · rebond 64% (43/67) (MFE +1.46%)
   - −4.0% : fill 30min 24% · séance 40% (57/159) · gap 6% · délai 21.4min · rebond 70% (42/57) (MFE +2.23%)
   - −5.0% : fill 30min 18% · séance 35% (45/159) · gap 5% · délai 24.2min · rebond 75% (33/45) (MFE +2.09%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.92% (p90 −3.51%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −3.11%) → stop au-delà de −2.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.01% (p90 −2.67%) → stop au-delà de −2.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=860 jambes) : jambe baissière méd −1.38% (p90 −3.36%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 100% (52/52) · rebond 49% (30/52)
      · −2.0% : fill 91% (43/52) · rebond 40% (21/43)
      · −3.0% : fill 90% (42/52) · rebond 61% (26/42)
      · −4.0% : fill 88% (38/52) · rebond 71% (27/38)
      · −5.0% : fill 79% (32/52) · rebond 84% (25/32)
   - **flat** (18 séances) :
      · −1.0% : fill 80% (14/18) · rebond 57% (9/14)
      · −2.0% : fill 77% (13/18) · rebond 41% (6/13)
      · −3.0% : fill 43% (8/18) · rebond 59% (5/8)
      · −4.0% : fill 34% (7/18) · rebond 44% (5/7)
      · −5.0% : fill 25% (3/18) · rebond 24% (1/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 39% (33/89) · rebond 60% (19/33)
      · −2.0% : fill 28% (24/89) · rebond 76% (16/24)
      · −3.0% : fill 21% (17/89) · rebond 75% (12/17)
      · −4.0% : fill 13% (12/89) · rebond 79% (10/12)
      · −5.0% : fill 12% (10/89) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 55% si les 15 1res min sont vertes (61 cas) · 30% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 76% si début vert vs 19% si rouge (base 38% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **76%** · continue >prix actuel 46% ; creux résiduel méd -1.83% (q20 -3.8%) → **SL/trailing à −3.8%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +3.79% → **scale +1.78% / runner +3.79%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **19%** (continue à baisser 58%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.81%** (au-delà de la MAE q10 -5.81%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.19% .. +4.37%] · haut q95 +6.12% · bas q05 -5.24%
   - 60min (n=160) : retour [-5.24% .. +3.92%] · haut q95 +6.34% · bas q05 -5.99%
   - 2h (n=160) : retour [-6.17% .. +3.88%] · haut q95 +6.47% · bas q05 -7.35%
   - 4h (n=160) : retour [-7.04% .. +5.07%] · haut q95 +6.49% · bas q05 -9.14%
   - 6h (n=160) : retour [-7.58% .. +5.24%] · haut q95 +6.75% · bas q05 -9.19%
   - session (n=160) : retour [-6.99% .. +5.44%] · haut q95 +6.75% · bas q05 -9.34%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **55%**. Lecture précoce 30 min : signature présente → 19% vs absente 0% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


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
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.7  _(momentum baissier)_
- **ADX** : 9.1  _(pas de tendance nette)_
- **MACD** : hist -4266.114  _(bearish_recent)_
- **BB** : %B 0.19 · largeur 17.1%
- **ATR** : 167857.14 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.053  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 47.8  _(transition)_
- **MA** : MA20 2879150.0 · MA50 2853000.0 · MA200 2758175.48  _(prix < MA20)_
- **Dist MA** : MA20 -5.4% · MA50 -4.5% · MA200 -1.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (483671 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

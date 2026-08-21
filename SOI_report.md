# SOI

**Generated** : 2026-08-21T21:45:06.554582+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €109.80  

> 🟡 **WAIT-FOR-DIP** — spot +1.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €109.80 (+1.4% vs entrée) · entrée €108.32 · stop €98.47 · T1 €128.00 · R/R 2.0  
> ↳ P(T1 av. stop) 16 % _(réel 5 s)_ · EV/risk 0.085 _(réel 5 s)_ (GBM 0.171) · ¼-Kelly 0.005 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €106.83–€109.80 (mid €108.32)
- Spot actuel : €109.80 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : €98.47 (stop swing_plan-based (-10.31%))
- Targets : T1 €128.00 · R/R 2.0 | T2 €129.92 · R/R 2.19 | T3 €131.85 · R/R 2.39
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €98.47


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.31 %)** : le gap seul le franchit 0.234 % des séances (3 fois sur 1280).
   - exécution **8.409 pt plus bas** dans le cas TYPIQUE (médiane), 16.869 au p90, **18.984 au pire**
   - perte réelle **21.456 %** en moyenne _(tirée par la queue)_, jusqu'à **29.294 %** — au lieu des 10.31 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0261 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.584 % | p01 -4.832 % | pire -29.294 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2574** [0.1967 ; 0.3262] _(largeur 13.0 pt, n_eff 173.1)_
   - swing : **0.4492** [0.3974 ; 0.5019] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.494** [0.4415 ; 0.5466] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.5 pt), swing (32.3 pt), deep (31.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-13.66 %** | vol 6.49 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.44 % contre 7.71 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.17 % vs -11.25 % si l'on extrapolait par √5 _(rapport 1.082 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1312** (β de hausse 1.6123, asymétrie 0.7016) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.059× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 102.9245 sur support (0.57 ATR, 6.262 %) — p(stop avant cible) 0.6014 [0.55 ; 0.65], R/R 1.634, perte reelle 13.196 % (gap inclus), CVaR 6.305 %, EV -2.4925 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.1855 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.57 ATR (stop 6.262 %) — p(stop avant cible) 0.6014 [0.55 ; 0.65], R/R 1.634, perte reelle 13.196 % (gap inclus), EV -2.4925 % — **REFUSE**
      - refuse : p_stop_first 0.601, borne haute 0.652 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.33 ATR du spot — compartiment <1, mesure a 50.9 % de casse (IC clusterise [0.477 ; 0.544] sur 1060 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.49 %) : P(cible) 19.4 % x 21.56 % + P(rien) 20.5 % x 6.18 % ne couvrent pas P(stop) 60.1 % x 13.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.348 %) — p(stop avant cible) 0.4242 [0.37 ; 0.48], R/R 1.005, perte reelle 21.456 % (gap inclus), EV -3.1317 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.13 %) : P(cible) 24.1 % x 21.56 % + P(rien) 33.5 % x 2.33 % ne couvrent pas P(stop) 42.4 % x 21.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.36 ATR (stop 18.643 %) — p(stop avant cible) 0.1834 [0.15 ; 0.23], R/R 0.898, perte reelle 24.006 % (gap inclus), EV 1.3192 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.65 % > budget 12.00 %
   - 🟢 support a 3.71 ATR (stop 27.974 %) — p(stop avant cible) 0.0445 [0.03 ; 0.07], R/R 0.736, perte reelle 29.294 % (gap inclus), EV 2.5612 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.98 % > budget 12.00 %
   - 🟢 support a 5.89 ATR (stop 43.001 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.501, perte reelle 43.001 % (gap inclus), EV 2.6148 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.00 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.171 | EV/share : €1.683 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 20 % | T3 16 %
- Kelly (position) : f* 0.019 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 49.9 | bear 32.8 | side 17.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 110.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.614% → cible +7.9% / stop −3.95%, p_fill 88%, n_eff≈36.2) : P(cible|rempli) **6%** · **EV/risk -0.154** (×p_fill ; si rempli -0.69% du capital)
  - **swing** (entrée dip −1.346% → cible +18.172% / stop −9.086%, p_fill 81%, n_eff≈34.1) : P(cible|rempli) **16%** · **EV/risk +0.085** (×p_fill ; si rempli +0.96% du capital)
  - **deep** (entrée dip −1.99% → cible +26.14% / stop −13.07%, p_fill 81%, n_eff≈35.8) : P(cible|rempli) **23%** · **EV/risk -0.114** (×p_fill ; si rempli -1.84% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→66% · +3.0%→52% · +5.0%→35% · +8.0%→12%
- Range intraday médian 8.43% (p90 14.6%) · excursion haute méd. +3.45% / basse méd. −3.46%
- Profil de vol intra : ouverture 5.303% vs midi 1.467% vs clôture 2.317% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 13% · trend ↑0%/↓3% ; spike-down 77% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.136 ; mean-reverting — autocorr -0.073)_ ; drift intra méd. -0.683% ; recovery-V 32%
- **σ réalisé intraday** 4.88% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 56% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 109.62 (VA 108.42–110.46 ; dernier close 109.56)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 37% · rebond 75% · **stop −7.88%** sous le fill (sous le bruit) · cible +2.79% · R/R 0.35 (high win-rate)
- Gaps overnight (n=158) : méd. 0.29% · baisse 46% (gap-down >1% 30% · >2% 20%)
- Excursion ouverture 5min (n=159) : bas méd −1.14% (p90 −3.77%) · haut méd +0.91% · range méd 2.77%
- Excursion ouverture 15min (n=159) : bas méd −1.42% (p90 −5.06%) · haut méd +1.25% · range méd 3.47%
- Excursion ouverture 30min (n=159) : bas méd −1.52% (p90 −5.41%) · haut méd +1.58% · range méd 3.98%
- Excursion ouverture 60min (n=159) : bas méd −1.71% (p90 −5.87%) · haut méd +1.76% · range méd 4.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 109.56 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 79% (125/158) · gap 39% · délai 0.0min · rebond 64% (81/125) (MFE +1.83%)
   - −1.0% : fill 30min 58% · séance 74% (118/158) · gap 30% · délai 0.2min · rebond 71% (85/118) (MFE +1.82%)
   - −1.5% : fill 30min 52% · séance 68% (107/158) · gap 25% · délai 0.2min · rebond 72% (78/107) (MFE +2.16%)
   - −2.0% : fill 30min 47% · séance 62% (98/158) · gap 20% · délai 0.4min · rebond 75% (77/98) (MFE +2.65%)
   - −3.0% : fill 30min 34% · séance 48% (78/158) · gap 13% · délai 0.5min · rebond 73% (61/78) (MFE +2.64%)
   - −4.0% : fill 30min 28% · séance 40% (63/158) · gap 6% · délai 1.1min · rebond 72% (49/63) (MFE +2.44%)
   - −5.0% : fill 30min 22% · séance 37% (55/158) · gap 1% · délai 14.4min · rebond 75% (45/55) (MFE +2.79%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −3.71%) → stop au-delà de −1.9% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −2.9%) → stop au-delà de −2.14% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.37%) → stop au-delà de −1.98% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1354 jambes) : jambe baissière méd −1.3% (p90 −3.14%) · ~17.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 94% (60/62) · rebond 58% (37/60)
      · −2.0% : fill 91% (58/62) · rebond 68% (44/58)
      · −3.0% : fill 77% (48/62) · rebond 71% (38/48)
      · −4.0% : fill 67% (42/62) · rebond 77% (34/42)
      · −5.0% : fill 62% (37/62) · rebond 82% (31/37)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (79 séances) :
      · −1.0% : fill 53% (41/79) · rebond 86% (34/41)
      · −2.0% : fill 31% (25/79) · rebond 90% (21/25)
      · −3.0% : fill 19% (19/79) · rebond 83% (15/19)
      · −4.0% : fill 14% (13/79) · rebond 55% (9/13)
      · −5.0% : fill 13% (10/79) · rebond 47% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 49% en base · 69% si les 15 1res min sont vertes (74 cas) · 30% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=159) : COUDE à **38min** → P(séance verte=clôture>ouverture) 79% si début vert vs 25% si rouge (base 49% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 272min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **79%** · continue >prix actuel 62% ; creux résiduel méd -2.32% (q20 -5.45%) → **SL/trailing à −5.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.12% / q75 +4.83% → **scale +3.12% / runner +4.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **25%** (continue à baisser 64%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.69%** (au-delà de la MAE q10 -8.69%), cible rebond +2.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-5.1% .. +6.53%] · haut q95 +7.84% · bas q05 -6.24%
   - 60min (n=159) : retour [-5.69% .. +6.78%] · haut q95 +8.19% · bas q05 -6.72%
   - 2h (n=159) : retour [-6.85% .. +6.61%] · haut q95 +11.85% · bas q05 -7.77%
   - 4h (n=159) : retour [-7.22% .. +9.39%] · haut q95 +12.4% · bas q05 -8.54%
   - 6h (n=159) : retour [-8.7% .. +10.18%] · haut q95 +13.23% · bas q05 -9.46%
   - session (n=159) : retour [-12.13% .. +12.57%] · haut q95 +14.58% · bas q05 -12.93%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.3% des séances sont trend-up (mild 0% / strong 6.3%) · base = 10 séances trend-up (n_eff 5.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **23%**. Lecture précoce 30 min : signature présente → 10% vs absente 4% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.06% (p75 1.5% / p90 2.89%) · ~5.05 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **89%** (reprise méd 20.0 min, n=60)
   - −1.0% → **82%** (reprise méd 34.22 min, n=34)
   - −1.5% → **69%** (reprise méd 46.1 min, n=18)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.89%** (p90, défaut prudent ; serré/agressif −1.5%) ; extension open→close méd +7.26% (q75 +13.51% / q95 +17.04%), MFE méd +8.03% / q90 +18.1%
   - Échelle scale-out : +8.03% (33%) / +14.35% (33%) / +18.1% (34%)
- **DÉSARMER** : repli > **−2.89%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.1% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 96% du temps (retour médian dernière heure +1.92%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 50.4  _(neutre)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -1.282  _(bearish_recent)_
- **BB** : %B 0.37 · largeur 38.6%
- **ATR** : 7.57 (64.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.194  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 51.1  _(transition)_
- **MA** : MA20 115.77 · MA50 112.13 · MA200 76.97  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -2.1% · MA200 +42.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (675585 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# IONQ

**Generated** : 2026-08-21T22:04:39.621874+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $44.86  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $44.86 (+1.4% vs entrée) · entrée $44.25 · stop $43.39 · T1 $45.65 · R/R 1.63  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.035 _(réel 5 s)_ (GBM 0.085) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.95% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $43.97–$44.53 (mid $44.25)
- Spot actuel : $44.86 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : $43.39 (stop swing_plan-based (-9.4%))
- Targets : T1 $45.65 · R/R 1.63 | T2 $47.04 · R/R 3.24 | T3 $48.44 · R/R 4.87
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $43.39


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.69 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.4 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1254).
   - exécution **2.293 pt plus bas** dans le cas TYPIQUE (médiane), 9.485 au p90, **12.459 au pire**
   - perte réelle **13.966 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 9.4 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0146 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.033 % | p01 -6.63 % | pire -21.859 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2897** [0.226 ; 0.3603] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.5485** [0.4958 ; 0.6004] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.571** [0.5184 ; 0.6224] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.6 pt), swing (34.5 pt), deep (32.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.5 %** | CVaR **-10.11 %** | vol 6.18 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 9.84 % contre 5.89 % aujourd'hui, rapport 1.67)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.22 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.2336** (β de hausse 1.9862, asymétrie 1.1246) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 40.6236 sur sr_based (0.95 ATR, 9.444 %) — p(stop avant cible) 0.5925 [0.54 ; 0.64], R/R 2.222, perte reelle 13.966 % (gap inclus), CVaR 9.458 %, EV -1.5996 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.5335 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.593, borne haute 0.643 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 9.46 % > budget 4.09 %
- Budget de queue : **4.09 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.9 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.95 ATR (stop 9.444 %) — p(stop avant cible) 0.5925 [0.54 ; 0.64], R/R 2.222, perte reelle 13.966 % (gap inclus), EV -1.5996 % — **REFUSE**
      - refuse : cible atteinte seulement 14.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.593, borne haute 0.643 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 9.46 % > budget 4.09 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 14.2 % x 31.04 % + P(rien) 26.5 % x 8.52 % ne couvrent pas P(stop) 59.2 % x 13.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 2.39 ATR (stop 18.655 %) — p(stop avant cible) 0.2563 [0.21 ; 0.30], R/R 1.42, perte reelle 21.859 % (gap inclus), EV 0.3686 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.66 % > budget 4.09 %
      - ⚠ support DETECTE a 0.85 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - 🟢 support a 3.72 ATR (stop 27.171 %) — p(stop avant cible) 0.0814 [0.06 ; 0.11], R/R 1.142, perte reelle 27.171 % (gap inclus), EV 1.4015 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.17 % > budget 4.09 %
   - ⚪ swing_based a 4.74 ATR (stop 33.735 %) — p(stop avant cible) 0.0284 [0.01 ; 0.05], R/R 0.92, perte reelle 33.735 % (gap inclus), EV 1.348 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.74 % > budget 4.09 %
   - 🟢 support a 5.17 ATR (stop 36.511 %) — p(stop avant cible) 0.0156 [0.01 ; 0.03], R/R 0.85, perte reelle 36.511 % (gap inclus), EV 1.3996 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.51 % > budget 4.09 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.085 | EV/share : $0.074 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 27 % | T3 27 %
- Kelly (position) : f* 0.097 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 60.5 | bear 32.3 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 269.0 (= 6 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.358% → cible +3.157% / stop −1.948%, p_fill 71%, n_eff≈29.5) : P(cible|rempli) **25%** · **EV/risk -0.035** (×p_fill ; si rempli -0.09% du capital)
  - **swing** (entrée dip −2.994% → cible +7.059% / stop −6.604%, p_fill 55%, n_eff≈28.4) : P(cible|rempli) **60%** · **EV/risk +0.112** (×p_fill ; si rempli +1.34% du capital)
  - **deep** (entrée dip −4.62% → cible +9.984% / stop −10.076%, p_fill 63%, n_eff≈33.2) : P(cible|rempli) **51%** · **EV/risk -0.063** (×p_fill ; si rempli -1.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→68% · +3.0%→59% · +5.0%→31% · +8.0%→15%
- Range intraday médian 7.63% (p90 12.17%) · excursion haute méd. +3.64% / basse méd. −2.75%
- Profil de vol intra : ouverture 5.286% vs midi 1.482% vs clôture 1.69% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr 0.007)_ ; drift intra méd. 0.036% ; recovery-V 29%
- **σ réalisé intraday** 4.528% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 53% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 41.4134 (VA 40.8516–42.0554 ; dernier close 41.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 86% · **stop −5.07%** sous le fill (sous le bruit) · cible +2.81% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.41% · baisse 55% (gap-down >1% 37% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.21% (p90 −2.83%) · haut méd +1.3% · range méd 2.79%
- Excursion ouverture 15min (n=160) : bas méd −1.67% (p90 −4.02%) · haut méd +1.49% · range méd 3.71%
- Excursion ouverture 30min (n=160) : bas méd −1.93% (p90 −5.16%) · haut méd +1.94% · range méd 4.54%
- Excursion ouverture 60min (n=160) : bas méd −2.35% (p90 −5.64%) · haut méd +2.25% · range méd 5.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 41.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 83% (134/159) · gap 48% · délai 0.0min · rebond 63% (89/134) (MFE +1.89%)
   - −1.0% : fill 30min 70% · séance 77% (126/159) · gap 37% · délai 0.0min · rebond 72% (92/126) (MFE +2.35%)
   - −1.5% : fill 30min 63% · séance 70% (119/159) · gap 33% · délai 0.0min · rebond 64% (80/119) (MFE +2.1%)
   - −2.0% : fill 30min 56% · séance 64% (109/159) · gap 18% · délai 0.1min · rebond 72% (76/109) (MFE +2.32%)
   - −3.0% : fill 30min 47% · séance 56% (95/159) · gap 9% · délai 6.6min · rebond 74% (70/95) (MFE +2.49%)
   - −4.0% : fill 30min 30% · séance 44% (76/159) · gap 6% · délai 15.5min · rebond 74% (58/76) (MFE +2.72%)
   - −5.0% : fill 30min 18% · séance 36% (64/159) · gap 3% · délai 24.8min · rebond 86% (56/64) (MFE +2.81%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −2.94%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.91% (p90 −3.47%) → stop au-delà de −2.37% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.88% (p90 −2.76%) → stop au-delà de −1.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1124 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (79 séances) :
      · −1.0% : fill 100% (79/79) · rebond 73% (59/79)
      · −2.0% : fill 90% (73/79) · rebond 77% (56/73)
      · −3.0% : fill 78% (64/79) · rebond 76% (49/64)
      · −4.0% : fill 60% (48/79) · rebond 76% (38/48)
      · −5.0% : fill 48% (40/79) · rebond 80% (33/40)
   - **flat** (15 séances) :
      · −1.0% : fill 77% (12/15) · rebond 62% (7/12)
      · −2.0% : fill 66% (11/15) · rebond 74% (5/11)
      · −3.0% : fill 60% (9/15) · rebond 43% (4/9)
      · −4.0% : fill 60% (9/15) · rebond 51% (4/9)
      · −5.0% : fill 44% (8/15) · rebond 95% (7/8)
   - **gap-up** (65 séances) :
      · −1.0% : fill 45% (35/65) · rebond 74% (26/35)
      · −2.0% : fill 29% (25/65) · rebond 52% (15/25)
      · −3.0% : fill 25% (22/65) · rebond 79% (17/22)
      · −4.0% : fill 20% (19/65) · rebond 79% (16/19)
      · −5.0% : fill 18% (16/65) · rebond 100% (16/16)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 56% si les 15 1res min sont vertes (79 cas) · 32% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 69% si début vert vs 22% si rouge (base 45% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 234min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **69%** · continue >prix actuel 41% ; creux résiduel méd -2.95% (q20 -4.64%) → **SL/trailing à −4.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.01% / q75 +4.76% → **scale +2.01% / runner +4.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **22%** (continue à baisser 54%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +2.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.11% .. +6.89%] · haut q95 +7.87% · bas q05 -5.66%
   - 60min (n=160) : retour [-4.99% .. +6.13%] · haut q95 +8.43% · bas q05 -6.2%
   - 2h (n=160) : retour [-6.38% .. +7.98%] · haut q95 +9.11% · bas q05 -7.05%
   - 4h (n=160) : retour [-7.07% .. +7.32%] · haut q95 +10.19% · bas q05 -8.09%
   - 6h (n=160) : retour [-7.21% .. +8.53%] · haut q95 +11.03% · bas q05 -8.32%
   - session (n=160) : retour [-6.62% .. +9.03%] · haut q95 +11.15% · bas q05 -8.35%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 62.1  _(momentum haussier)_
- **ADX** : 21.4  _(pas de tendance nette)_
- **MACD** : hist 0.607  _(pas de croisement recent)_
- **BB** : %B 0.72 · largeur 42.3%
- **ATR** : 2.87 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.072  _(accumulation)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 59.5  _(transition)_
- **MA** : MA20 41.09 · MA50 44.54 · MA200 44.86  _(prix > MA20)_
- **Dist MA** : MA20 +9.2% · MA50 +0.7% · MA200 -0.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (649351 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

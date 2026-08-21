# SMCI

**Generated** : 2026-08-21T22:01:36.093280+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $37.24  

> 🟡 **WAIT-FOR-DIP** — spot +9.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $37.24 (+9.0% vs entrée) · entrée $34.16 · stop $30.79 · T1 $40.89 · R/R 2.0  
> ↳ P(T1 av. stop) 15 % · EV/risk 0.153 · ¼-Kelly 0.005 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 71.6 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $33.65–$34.66 (mid $34.16)
- Spot actuel : $37.24 (+9.0% au-dessus de la zone — repli à attendre)
- Stop : $30.79 (stop swing_plan-based (-17.32%))
- Targets : T1 $40.89 · R/R 2.0 | T2 $41.30 · R/R 2.12 | T3 $41.71 · R/R 2.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $30.79


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.32 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1254).
   - exécution **7.337 pt plus bas** dans le cas TYPIQUE (médiane), 10.855 au p90, **11.731 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 17.32 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0243 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.763 % | p01 -10.29 % | pire -29.051 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1851** [0.1327 ; 0.2479] _(largeur 11.5 pt, n_eff 173.1)_
   - swing : **0.5092** [0.4566 ; 0.5616] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5479** [0.4952 ; 0.5998] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.9 pt), swing (55.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.73 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.19 % contre 7.15 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.68 % vs -16.02 % si l'on extrapolait par √5 _(rapport 1.042 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5462** (β de hausse 1.2484, asymétrie 1.2386) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.944× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 33.4171 sur atr_based (1.5 ATR, 10.266 %) — p(stop avant cible) 0.4107 [0.36 ; 0.46], R/R 0.712, perte reelle 16.875 % (gap inclus), CVaR 10.335 %, EV -2.2268 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 2.9998 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.71 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 10.33 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.9 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.48 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.266 %) — p(stop avant cible) 0.4107 [0.36 ; 0.46], R/R 0.712, perte reelle 16.875 % (gap inclus), EV -2.2268 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.33 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.23 %) : P(cible) 38.7 % x 12.01 % + P(rien) 20.2 % x 0.25 % ne couvrent pas P(stop) 41.1 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.3 ATR (stop 18.036 %) — p(stop avant cible) 0.1625 [0.13 ; 0.20], R/R 0.482, perte reelle 24.92 % (gap inclus), EV 0.2312 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.06 % > budget 3.00 %
   - 🟢 support a 3.74 ATR (stop 27.897 %) — p(stop avant cible) 0.0848 [0.06 ; 0.12], R/R 0.414, perte reelle 29.051 % (gap inclus), EV 0.7434 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.90 % > budget 3.00 %
   - 🟢 support a 4.64 ATR (stop 34.073 %) — p(stop avant cible) 0.0651 [0.04 ; 0.09], R/R 0.353, perte reelle 34.073 % (gap inclus), EV 0.4816 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.07 % > budget 3.00 %
   - 🟢 support a 5.44 ATR (stop 39.524 %) — p(stop avant cible) 0.0174 [0.01 ; 0.04], R/R 0.304, perte reelle 39.524 % (gap inclus), EV 0.6205 % — **REFUSE**
      - refuse : R/R 0.30 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.52 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.161 | EV/share : $0.543 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 18 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.018 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.3 | bear 5.0 | side 80.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 633.0 (= 17 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.757% → cible +3.297% / stop −2.133%, p_fill 36%, n_eff≈16.2) : P(cible|rempli) **43%** · **EV/risk +0.134** (×p_fill ; si rempli +0.80% du capital)
  - **swing** (entrée dip −8.279% → cible +19.714% / stop −9.857%, p_fill 15%, n_eff≈9.7) : P(cible|rempli) **16%** · **EV/risk +0.005** (×p_fill ; si rempli +0.35% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→62% · +3.0%→50% · +5.0%→29% · +8.0%→14%
- Range intraday médian 6.69% (p90 11.21%) · excursion haute méd. +3.0% / basse méd. −2.68%
- Profil de vol intra : ouverture 4.167% vs midi 1.281% vs clôture 1.676% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.053)_ ; drift intra méd. 0.038% ; recovery-V 28%
- **σ réalisé intraday** 4.162% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 65% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 36.6956 (VA 35.9331–37.0769 ; dernier close 36.49)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 81% · **stop −4.21%** sous le fill (sous le bruit) · cible +2.62% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.3% · baisse 45% (gap-down >1% 32% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.83% (p90 −2.85%) · haut méd +1.02% · range méd 2.23%
- Excursion ouverture 15min (n=160) : bas méd −1.24% (p90 −3.26%) · haut méd +1.46% · range méd 2.89%
- Excursion ouverture 30min (n=160) : bas méd −1.57% (p90 −3.79%) · haut méd +1.56% · range méd 3.74%
- Excursion ouverture 60min (n=160) : bas méd −1.86% (p90 −4.4%) · haut méd +1.83% · range méd 4.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 36.49 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 74% (121/159) · gap 40% · délai 0.0min · rebond 58% (73/121) (MFE +1.31%)
   - −1.0% : fill 30min 53% · séance 70% (112/159) · gap 32% · délai 0.0min · rebond 62% (67/112) (MFE +1.48%)
   - −1.5% : fill 30min 45% · séance 62% (99/159) · gap 22% · délai 0.1min · rebond 65% (60/99) (MFE +1.55%)
   - −2.0% : fill 30min 42% · séance 53% (87/159) · gap 17% · délai 0.8min · rebond 70% (56/87) (MFE +1.75%)
   - −3.0% : fill 30min 32% · séance 48% (76/159) · gap 12% · délai 8.2min · rebond 63% (47/76) (MFE +1.96%)
   - −4.0% : fill 30min 20% · séance 38% (57/159) · gap 7% · délai 26.3min · rebond 74% (37/57) (MFE +1.97%)
   - −5.0% : fill 30min 15% · séance 31% (46/159) · gap 4% · délai 39.5min · rebond 81% (33/46) (MFE +2.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.9%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.59% (p90 −3.0%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.87%) → stop au-delà de −1.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=898 jambes) : jambe baissière méd −1.21% (p90 −2.88%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 96% (70/72) · rebond 50% (38/70)
      · −2.0% : fill 89% (63/72) · rebond 65% (37/63)
      · −3.0% : fill 85% (58/72) · rebond 59% (34/58)
      · −4.0% : fill 69% (45/72) · rebond 73% (29/45)
      · −5.0% : fill 56% (37/72) · rebond 80% (26/37)
   - **flat** (11 séances) :
      · −1.0% : fill 97% (10/11) · rebond 96% (9/10)
      · −2.0% : fill 44% (6/11) · rebond 89% (4/6)
      · −3.0% : fill 28% (3/11) · rebond 100% (3/3)
      · −4.0% : fill 24% (2/11) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/11) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 44% (32/76) · rebond 74% (20/32)
      · −2.0% : fill 25% (18/76) · rebond 81% (15/18)
      · −3.0% : fill 20% (15/76) · rebond 70% (10/15)
      · −4.0% : fill 14% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 13% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 68% si les 15 1res min sont vertes (78 cas) · 22% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:18** → P(séance verte=clôture>ouverture) 78% si début vert vs 12% si rouge (base 45% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **78%** · continue >prix actuel 47% ; creux résiduel méd -1.61% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.0% / q75 +3.08% → **scale +2.0% / runner +3.08%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **12%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.66%** (au-delà de la MAE q10 -4.66%), cible rebond +2.18% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.07% .. +4.47%] · haut q95 +6.21% · bas q05 -4.33%
   - 60min (n=160) : retour [-4.25% .. +5.68%] · haut q95 +6.89% · bas q05 -5.29%
   - 2h (n=160) : retour [-4.78% .. +6.97%] · haut q95 +8.58% · bas q05 -5.82%
   - 4h (n=160) : retour [-5.26% .. +7.39%] · haut q95 +9.07% · bas q05 -6.9%
   - 6h (n=160) : retour [-5.78% .. +6.99%] · haut q95 +10.36% · bas q05 -6.93%
   - session (n=160) : retour [-7.16% .. +7.84%] · haut q95 +10.36% · bas q05 -7.87%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.5)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **13%**. Lecture précoce 30 min : signature présente → 7% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.96% (p75 1.84% / p90 2.17%) · ~4.0 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **80%** (reprise méd 14.9 min, n=37)
   - −1.0% → **72%** (reprise méd 30.0 min, n=17)
   - −1.5% → **57%** (reprise méd 48.62 min, n=13)
   - −2.0% → **85%** (reprise méd 120.86 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.17%** (p90, défaut prudent ; serré/agressif −1.84%) ; extension open→close méd +7.84% (q75 +8.68% / q95 +9.89%), MFE méd +8.72% / q90 +10.39%
   - Échelle scale-out : +8.72% (33%) / +9.19% (33%) / +10.39% (34%)
- **DÉSARMER** : repli > **−2.17%** depuis le plus-haut = décay → P(retournement) **18%** (préavis méd 100.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.39% : P(retournement après) 0% (mèche méd 1.08%)
- **CONTEXTE** : la dernière heure tient les gains 92% du temps (retour médian dernière heure +1.13%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 71.6  _(surachat)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist 0.495  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 54.3%
- **ATR** : 2.55 (72.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.018  _(neutre)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 37.6  _(marche directionnel)_
- **MA** : MA20 32.85 · MA50 30.48 · MA200 31.45  _(prix > MA20)_
- **Dist MA** : MA20 +13.4% · MA50 +22.2% · MA200 +18.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (643475 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

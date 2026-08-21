# SMCI

**Generated** : 2026-08-21T00:25:47.981296+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $36.50  

> 🟡 **WAIT-FOR-DIP** — spot +7.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $36.50 (+7.9% vs entrée) · entrée $33.83 · stop $30.29 · T1 $40.89 · R/R 1.99  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk 0.087 _(réel 5 s)_ (GBM 0.168) · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 70.9 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $33.32–$34.33 (mid $33.83)
- Spot actuel : $36.50 (+7.9% au-dessus de la zone — repli à attendre)
- Stop : $30.29 (stop swing_plan-based (-17.01%))
- Targets : T1 $40.89 · R/R 1.99 | T2 $41.15 · R/R 2.07 | T3 $41.41 · R/R 2.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $30.29


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.01 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **7.647 pt plus bas** dans le cas TYPIQUE (médiane), 11.165 au p90, **12.041 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 17.01 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0255 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.765 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1873** [0.1346 ; 0.2503] _(largeur 11.6 pt, n_eff 173.1)_
   - swing : **0.5064** [0.4538 ; 0.5589] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5511** [0.4984 ; 0.6029] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.8 pt), swing (50.2 pt), deep (53.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.73 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.19 % contre 7.15 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.05 % si l'on extrapolait par √5 _(rapport 1.04 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5462** (β de hausse 1.2487, asymétrie 1.2382) vs IWM — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.944× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.544 %) — p(stop avant cible) 0.4013 [0.35 ; 0.45], R/R 0.713, perte reelle 16.875 % (gap inclus), EV -1.9959 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.00 %) : P(cible) 39.2 % x 12.03 % + P(rien) 20.7 % x 0.31 % ne couvrent pas P(stop) 40.1 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.0 ATR (stop 16.135 %) — p(stop avant cible) 0.209 [0.17 ; 0.25], R/R 0.514, perte reelle 23.404 % (gap inclus), EV -0.5665 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.16 % > budget 12.0 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 42.2 % x 12.03 % + P(rien) 36.9 % x -2.05 % ne couvrent pas P(stop) 20.9 % x 23.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.43 ATR (stop 26.191 %) — p(stop avant cible) 0.0891 [0.06 ; 0.12], R/R 0.43, perte reelle 27.955 % (gap inclus), EV 0.7443 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.19 % > budget 12.0 %
   - 🟢 support a 4.32 ATR (stop 32.492 %) — p(stop avant cible) 0.072 [0.05 ; 0.10], R/R 0.37, perte reelle 32.492 % (gap inclus), EV 0.4664 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.49 % > budget 12.0 %
   - 🟢 support a 5.11 ATR (stop 38.054 %) — p(stop avant cible) 0.044 [0.03 ; 0.07], R/R 0.316, perte reelle 38.054 % (gap inclus), EV 0.39 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.05 % > budget 12.0 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.168 | EV/share : $0.592 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 16 % | T3 16 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.6 | bear 5.0 | side 80.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 620.0 (= 17 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.331% → cible +3.343% / stop −2.181%, p_fill 41%, n_eff≈17.1) : P(cible|rempli) **28%** · **EV/risk +0.124** (×p_fill ; si rempli +0.66% du capital)
  - **swing** (entrée dip −7.329% → cible +20.893% / stop −10.447%, p_fill 24%, n_eff≈12.0) : P(cible|rempli) **22%** · **EV/risk +0.087** (×p_fill ; si rempli +3.82% du capital)
  - **deep** (entrée dip −11.33% → cible +30.721% / stop −15.361%, p_fill 22%, n_eff≈11.1) : P(cible|rempli) **35%** · **EV/risk +0.114** (×p_fill ; si rempli +8.05% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→62% · +3.0%→49% · +5.0%→28% · +8.0%→14%
- Range intraday médian 6.47% (p90 11.21%) · excursion haute méd. +2.72% / basse méd. −2.66%
- Profil de vol intra : ouverture 4.126% vs midi 1.279% vs clôture 1.668% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 70% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. 0.095% ; recovery-V 30%
- **σ réalisé intraday** 4.099% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 36.8312 (VA 36.4433–37.3162 ; dernier close 36.57)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 81% · **stop −4.21%** sous le fill (sous le bruit) · cible +2.62% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.28% · baisse 46% (gap-down >1% 32% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −0.88% (p90 −2.86%) · haut méd +0.97% · range méd 2.21%
- Excursion ouverture 15min (n=160) : bas méd −1.28% (p90 −3.28%) · haut méd +1.41% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.62% (p90 −3.81%) · haut méd +1.49% · range méd 3.73%
- Excursion ouverture 60min (n=160) : bas méd −1.9% (p90 −4.4%) · haut méd +1.77% · range méd 4.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 36.57 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 74% (121/159) · gap 41% · délai 0.0min · rebond 57% (73/121) (MFE +1.26%)
   - −1.0% : fill 30min 54% · séance 70% (112/159) · gap 32% · délai 0.0min · rebond 61% (67/112) (MFE +1.39%)
   - −1.5% : fill 30min 45% · séance 62% (98/159) · gap 22% · délai 0.1min · rebond 64% (59/98) (MFE +1.53%)
   - −2.0% : fill 30min 43% · séance 52% (86/159) · gap 17% · délai 0.5min · rebond 69% (55/86) (MFE +1.73%)
   - −3.0% : fill 30min 33% · séance 49% (76/159) · gap 13% · délai 8.2min · rebond 63% (47/76) (MFE +1.96%)
   - −4.0% : fill 30min 20% · séance 39% (57/159) · gap 7% · délai 26.3min · rebond 74% (37/57) (MFE +1.97%)
   - −5.0% : fill 30min 15% · séance 31% (46/159) · gap 4% · délai 39.5min · rebond 81% (33/46) (MFE +2.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.54% (p90 −2.93%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.65% (p90 −3.02%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.73% (p90 −2.91%) → stop au-delà de −1.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=895 jambes) : jambe baissière méd −1.2% (p90 −2.87%) · ~12.0 jambes/séance
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
      · −1.0% : fill 42% (32/76) · rebond 72% (20/32)
      · −2.0% : fill 22% (17/76) · rebond 78% (14/17)
      · −3.0% : fill 20% (15/76) · rebond 70% (10/15)
      · −4.0% : fill 15% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 14% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 70% si les 15 1res min sont vertes (77 cas) · 22% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **58min** → P(séance verte=clôture>ouverture) 80% si début vert vs 14% si rouge (base 46% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **80%** · continue >prix actuel 50% ; creux résiduel méd -2.11% (q20 -3.76%) → **SL/trailing à −3.76%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.37% → **scale +2.05% / runner +3.37%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **14%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.42%** (au-delà de la MAE q10 -5.42%), cible rebond +1.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.09% .. +4.52%] · haut q95 +6.22% · bas q05 -4.34%
   - 60min (n=160) : retour [-4.27% .. +5.69%] · haut q95 +7.24% · bas q05 -5.3%
   - 2h (n=160) : retour [-4.78% .. +7.17%] · haut q95 +8.6% · bas q05 -5.82%
   - 4h (n=160) : retour [-5.26% .. +7.42%] · haut q95 +9.14% · bas q05 -6.91%
   - 6h (n=160) : retour [-5.79% .. +6.99%] · haut q95 +10.41% · bas q05 -6.94%
   - session (n=160) : retour [-7.2% .. +7.84%] · haut q95 +10.41% · bas q05 -7.92%


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

- **RSI** : 70.9  _(surachat)_
- **ADX** : 25.1  _(tendance etablie)_
- **MACD** : hist 0.627  _(pas de croisement recent)_
- **BB** : %B 0.73 · largeur 53.9%
- **ATR** : 2.57 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.001  _(neutre)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 33.4  _(marche directionnel)_
- **MA** : MA20 32.49 · MA50 30.32 · MA200 31.52  _(prix > MA20)_
- **Dist MA** : MA20 +12.3% · MA50 +20.4% · MA200 +15.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (600819 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

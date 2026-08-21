# PLTR

**Generated** : 2026-08-21T00:27:14.521636+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · $173.96  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $173.96 (+9.2% vs entrée) · entrée $159.30 · stop $142.44 · T1 $193.00 · R/R 2.0  
> ↳ P(T1 av. stop) 6 % · EV/risk -0.052 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 9/10 élevée alors que : RSI 78.2 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $156.68–$161.91 (mid $159.30)
- Spot actuel : $173.96 (+9.2% au-dessus de la zone — repli à attendre)
- Stop : $142.44 (stop swing_plan-based (-18.12%))
- Targets : T1 $193.00 · R/R 2.0 | T2 $195.71 · R/R 2.16 | T3 $198.43 · R/R 2.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $142.44


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.79 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (18.12 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1253).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 18.12 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.882 % | p01 -6.139 % | pire -17.932 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0908** [0.0547 ; 0.1404] _(largeur 8.6 pt, n_eff 173.1)_
   - swing : **0.4203** [0.3691 ; 0.4728] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5055** [0.4529 ; 0.558] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.2 %** | CVaR **-8.48 %** | vol 4.27 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -13.44 % vs -13.82 % si l'on extrapolait par √5 _(rapport 0.972 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7055** (β de hausse 1.418, asymétrie 1.2028) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 7.92 %) — p(stop avant cible) 0.3866 [0.34 ; 0.44], R/R 0.781, perte reelle 11.982 % (gap inclus), EV -0.8551 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 39.1 % x 9.36 % + P(rien) 22.3 % x 0.54 % ne couvrent pas P(stop) 38.7 % x 11.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.0 ATR (stop 17.437 %) — p(stop avant cible) 0.1051 [0.08 ; 0.14], R/R 0.522, perte reelle 17.932 % (gap inclus), EV 0.5121 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.44 % > budget 12.0 %
   - 🟢 support a 6.1 ATR (stop 33.816 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.277, perte reelle 33.816 % (gap inclus), EV 1.0254 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.82 % > budget 12.0 %
   - 🟢 support a 7.36 ATR (stop 40.438 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.232, perte reelle 40.438 % (gap inclus), EV 1.03 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.44 % > budget 12.0 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : $0.630 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 5 % | T2 5 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 14.1 | side 80.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 522.0 (= 3 part(s) × prix) · cible 640.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→79% · +2.0%→50% · +3.0%→28% · +5.0%→10% · +8.0%→4%
- Range intraday médian 3.89% (p90 7.17%) · excursion haute méd. +2.0% / basse méd. −1.67%
- Profil de vol intra : ouverture 3.053% vs midi 0.755% vs clôture 0.847% _(ouverture ~4.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 22% · trend ↑2%/↓0% ; spike-down 53% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.632% ; recovery-V 34%
- **σ réalisé intraday** 2.703% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 46% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 175.0889 (VA 173.7069–176.1254 ; dernier close 175.19)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 15% · rebond 51% · **stop −3.08%** sous le fill (sous le bruit) · cible +1.02% · R/R 0.33 (high win-rate)
- Gaps overnight (n=159) : méd. -0.11% · baisse 56% (gap-down >1% 26% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.08%) · haut méd +0.97% · range méd 1.99%
- Excursion ouverture 15min (n=160) : bas méd −0.86% (p90 −2.82%) · haut méd +1.18% · range méd 2.4%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −3.48%) · haut méd +1.31% · range méd 2.8%
- Excursion ouverture 60min (n=160) : bas méd −1.33% (p90 −3.78%) · haut méd +1.5% · range méd 3.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 175.19 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 75% (119/159) · gap 37% · délai 0.0min · rebond 57% (66/119) (MFE +1.21%)
   - −1.0% : fill 30min 54% · séance 65% (108/159) · gap 26% · délai 0.0min · rebond 63% (65/108) (MFE +1.34%)
   - −1.5% : fill 30min 42% · séance 54% (92/159) · gap 21% · délai 0.6min · rebond 67% (61/92) (MFE +1.25%)
   - −2.0% : fill 30min 37% · séance 49% (79/159) · gap 13% · délai 1.8min · rebond 65% (50/79) (MFE +1.43%)
   - −3.0% : fill 30min 22% · séance 31% (55/159) · gap 7% · délai 5.0min · rebond 56% (27/55) (MFE +1.44%)
   - −4.0% : fill 30min 14% · séance 20% (38/159) · gap 4% · délai 11.2min · rebond 55% (19/38) (MFE +1.02%)
   - −5.0% : fill 30min 9% · séance 15% (27/159) · gap 1% · délai 25.2min · rebond 51% (13/27) (MFE +1.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.38% (p90 −2.01%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −1.89%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.48% (p90 −1.37%) → stop au-delà de −1.06% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=558 jambes) : jambe baissière méd −1.05% (p90 −2.5%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 91% (70/74) · rebond 65% (43/70)
      · −2.0% : fill 73% (58/74) · rebond 67% (38/58)
      · −3.0% : fill 52% (41/74) · rebond 54% (20/41)
      · −4.0% : fill 35% (30/74) · rebond 51% (14/30)
      · −5.0% : fill 29% (23/74) · rebond 58% (12/23)
   - **flat** (28 séances) :
      · −1.0% : fill 74% (22/28) · rebond 36% (10/22)
      · −2.0% : fill 60% (14/28) · rebond 53% (8/14)
      · −3.0% : fill 32% (10/28) · rebond 57% (5/10)
      · −4.0% : fill 20% (7/28) · rebond 84% (5/7)
      · −5.0% : fill 10% (3/28) · rebond 9% (1/3)
   - **gap-up** (57 séances) :
      · −1.0% : fill 30% (16/57) · rebond 79% (12/16)
      · −2.0% : fill 13% (7/57) · rebond 72% (4/7)
      · −3.0% : fill 5% (4/57) · rebond 73% (2/4)
      · −4.0% : fill 1% (1/57) · rebond 0% (0/1)
      · −5.0% : fill 1% (1/57) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 70% si les 15 1res min sont vertes (81 cas) · 32% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 80% si début vert vs 24% si rouge (base 53% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **80%** · continue >prix actuel 55% ; creux résiduel méd -1.17% (q20 -1.75%) → **SL/trailing à −1.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.46% → **scale +1.46% / runner +2.46%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **24%** (continue à baisser 46%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.24%** (au-delà de la MAE q10 -3.24%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.73% .. +3.83%] · haut q95 +4.36% · bas q05 -4.07%
   - 60min (n=160) : retour [-3.64% .. +4.18%] · haut q95 +5.08% · bas q05 -4.41%
   - 2h (n=160) : retour [-3.92% .. +5.69%] · haut q95 +6.64% · bas q05 -4.57%
   - 4h (n=160) : retour [-4.3% .. +5.7%] · haut q95 +6.68% · bas q05 -5.58%
   - 6h (n=160) : retour [-4.66% .. +6.3%] · haut q95 +7.32% · bas q05 -5.75%
   - session (n=160) : retour [-4.31% .. +6.3%] · haut q95 +7.34% · bas q05 -5.76%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 2.5% / strong 3.7%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **36%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.81% (p75 1.11% / p90 1.47%) · ~3.0 replis/séance, durée méd 75.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 30.0 min, n=33)
   - −1.0% → **51%** (reprise méd 64.44 min, n=9)
   - −1.5% → **36%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−1.47%** (p90, défaut prudent ; serré/agressif −1.11%) ; extension open→close méd +6.19% (q75 +7.89% / q95 +12.13%), MFE méd +7.32% / q90 +13.49%
   - Échelle scale-out : +7.32% (33%) / +9.14% (33%) / +13.49% (34%)
- **DÉSARMER** : repli > **−1.47%** depuis le plus-haut = décay → P(retournement) **64%** (préavis méd 92.5 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.49% : P(retournement après) 0% (mèche méd 1.36%)
- **CONTEXTE** : la dernière heure tient les gains 62% du temps (retour médian dernière heure +0.21%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 78.2  _(surachat)_
- **ADX** : 31.5  _(tendance etablie)_
- **MACD** : hist 1.242  _(pas de croisement recent)_
- **BB** : %B 0.71 · largeur 60.2%
- **ATR** : 9.19 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.2  _(accumulation)_
- **Vol ratio** : 0.58  _(volume atone)_
- **Choppiness** : 31.1  _(marche directionnel)_
- **MA** : MA20 154.42 · MA50 137.94 · MA200 151.64  _(prix > MA20)_
- **Dist MA** : MA20 +12.7% · MA50 +26.1% · MA200 +14.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (592935 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

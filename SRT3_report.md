# SRT3

**Generated** : 2026-08-21T21:37:36.767388+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €246.80  

> 🟡 **WAIT-FOR-DIP** — spot +2.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €246.80 (+2.3% vs entrée) · entrée €241.17 · stop €233.93 · T1 €247.53 · R/R 0.88  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk 0.086 _(réel 5 s)_ (GBM 0.062) · ¼-Kelly 0.036 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 71.6 > 70 (surachat) ; extension étirée (≥2×ATR au-dessus de la MA20) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €240.57–€241.77 (mid €241.17)
- Spot actuel : €246.80 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : €233.93 (stop swing_plan-based (-8.09%))
- Targets : T1 €247.53 · R/R 0.88 | T2 €248.82 · R/R 1.06 | T3 €250.11 · R/R 1.23
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €233.93


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.09 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **1.567 pt plus bas** dans le cas TYPIQUE (médiane), 4.422 au p90, **6.115 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 8.09 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0079 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0372** [0.0162 ; 0.0734] _(largeur 5.7 pt, n_eff 173.1)_
   - swing : **0.3514** [0.3025 ; 0.4028] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.4844** [0.432 ; 0.537] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.18 %** | CVaR **-6.61 %** | vol 2.86 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0659** (β de hausse 1.1726, asymétrie 0.9091) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.352× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 235.4321 sur atr_based (1.5 ATR, 4.606 %) — p(stop avant cible) 0.3987 [0.35 ; 0.45], R/R 0.359, perte reelle 7.948 % (gap inclus), CVaR 4.635 %, EV -1.4887 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.3203 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 0.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 4.63 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.9 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 1.53 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.606 %) — p(stop avant cible) 0.3987 [0.35 ; 0.45], R/R 0.359, perte reelle 7.948 % (gap inclus), EV -1.4887 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 4.63 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.49 %) : P(cible) 59.1 % x 2.86 % + P(rien) 1.1 % x -0.70 % ne couvrent pas P(stop) 39.9 % x 7.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 3.07 ATR (stop 11.609 %) — p(stop avant cible) 0.1195 [0.09 ; 0.16], R/R 0.201, perte reelle 14.205 % (gap inclus), EV -0.3284 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.61 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 72.0 % x 2.86 % + P(rien) 16.0 % x -4.29 % ne couvrent pas P(stop) 11.9 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 7.94 ATR (stop 26.543 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.108, perte reelle 26.543 % (gap inclus), EV 0.2139 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.54 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.062 | EV/share : €0.448 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 25 % | T3 18 %
- Kelly (position) : f* 0.144 | ¼-Kelly 0.036 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.8 | bear 6.6 | side 82.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 494.0 (= 2 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.278% → cible +2.639% / stop −3.0%, p_fill 27%, n_eff≈14.0) : P(cible|rempli) **28%** · **EV/risk +0.086** (×p_fill ; si rempli +0.95% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→49% · +3.0%→26% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.37% (p90 6.59%) · excursion haute méd. +1.94% / basse méd. −1.45%
- Profil de vol intra : ouverture 2.048% vs midi 0.852% vs clôture 0.985% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.103 ; neutre — autocorr -0.015)_ ; drift intra méd. 0.176% ; recovery-V 28%
- **σ réalisé intraday** 2.555% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 68% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 245.9162 (VA 244.7038–248.0987 ; dernier close 249.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 57% · rebond 74% · **stop −2.26%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.73 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 48% (gap-down >1% 14% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −1.83%) · haut méd +0.5% · range méd 1.23%
- Excursion ouverture 15min (n=160) : bas méd −0.58% (p90 −1.94%) · haut méd +0.63% · range méd 1.51%
- Excursion ouverture 30min (n=160) : bas méd −0.61% (p90 −2.09%) · haut méd +0.79% · range méd 1.72%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −2.51%) · haut méd +0.79% · range méd 1.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 249.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 76% (125/159) · gap 24% · délai 0.3min · rebond 54% (65/125) (MFE +1.18%)
   - −1.0% : fill 30min 43% · séance 64% (105/159) · gap 14% · délai 2.8min · rebond 57% (58/105) (MFE +1.31%)
   - −1.5% : fill 30min 35% · séance 57% (96/159) · gap 6% · délai 4.7min · rebond 74% (62/96) (MFE +1.66%)
   - −2.0% : fill 30min 18% · séance 38% (74/159) · gap 3% · délai 60.5min · rebond 63% (45/74) (MFE +1.67%)
   - −3.0% : fill 30min 6% · séance 16% (39/159) · gap 1% · délai 134.1min · rebond 57% (23/39) (MFE +1.68%)
   - −4.0% : fill 30min 3% · séance 9% (21/159) · gap 0% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 6% (12/159) · gap 0% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.99%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −2.24%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.59%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=446 jambes) : jambe baissière méd −1.04% (p90 −2.35%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 80% (57/69) · rebond 66% (35/57)
      · −2.0% : fill 50% (42/69) · rebond 58% (26/42)
      · −3.0% : fill 27% (27/69) · rebond 49% (15/27)
      · −4.0% : fill 13% (15/69) · rebond 71% (11/15)
      · −5.0% : fill 7% (7/69) · rebond 92% (6/7)
   - **flat** (33 séances) :
      · −1.0% : fill 68% (21/33) · rebond 54% (10/21)
      · −2.0% : fill 47% (16/33) · rebond 62% (8/16)
      · −3.0% : fill 16% (6/33) · rebond 66% (4/6)
      · −4.0% : fill 12% (4/33) · rebond 70% (3/4)
      · −5.0% : fill 12% (4/33) · rebond 24% (2/4)
   - **gap-up** (57 séances) :
      · −1.0% : fill 47% (27/57) · rebond 45% (13/27)
      · −2.0% : fill 22% (16/57) · rebond 77% (11/16)
      · −3.0% : fill 6% (6/57) · rebond 78% (4/6)
      · −4.0% : fill 4% (2/57) · rebond 100% (2/2)
      · −5.0% : fill 3% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 57% si les 15 1res min sont vertes (87 cas) · 38% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 59% si début vert vs 38% si rouge (base 49% · écart 21 pts) ; prédictivité sature ensuite (plafond brut 268min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **59%** · continue >prix actuel 48% ; creux résiduel méd -1.42% (q20 -2.36%) → **SL/trailing à −2.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.37% / q75 +2.36% → **scale +1.37% / runner +2.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **38%** (continue à baisser 53%) → **RÉDUIRE ~62%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.46%** (au-delà de la MAE q10 -4.46%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.89% .. +2.12%] · haut q95 +2.63% · bas q05 -3.29%
   - 60min (n=160) : retour [-2.79% .. +2.34%] · haut q95 +2.84% · bas q05 -3.68%
   - 2h (n=160) : retour [-2.18% .. +2.5%] · haut q95 +2.94% · bas q05 -3.83%
   - 4h (n=160) : retour [-2.54% .. +2.28%] · haut q95 +3.26% · bas q05 -3.83%
   - 6h (n=160) : retour [-2.59% .. +2.94%] · haut q95 +3.63% · bas q05 -3.98%
   - session (n=160) : retour [-3.61% .. +4.14%] · haut q95 +5.6% · bas q05 -4.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 71.6  _(surachat)_
- **ADX** : 13.0  _(pas de tendance nette)_
- **MACD** : hist 1.663  _(pas de croisement recent)_
- **BB** : %B 0.94 · largeur 15.2%
- **ATR** : 7.58 (28.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.091  _(distribution)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 48.0  _(transition)_
- **MA** : MA20 231.23 · MA50 229.93 · MA200 231.94  _(prix > MA20)_
- **Dist MA** : MA20 +6.7% · MA50 +7.3% · MA200 +6.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (660663 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

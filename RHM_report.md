# RHM

**Generated** : 2026-08-21T21:36:09.871382+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1155.40  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1155.40 (+0.5% vs entrée) · entrée €1149.50 · stop €1126.51 · T1 €1163.87 · R/R 0.63  
> ↳ P(T1 av. stop) 58 % _(réel 5 s)_ · EV/risk 0.0 _(réel 5 s)_ (GBM 0.106) · ¼-Kelly 0.038 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1146.63–€1152.37 (mid €1149.50)
- Spot actuel : €1155.40 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €1126.51 (stop swing_plan-based (-5.32%))
- Targets : T1 €1163.87 · R/R 0.63 | T2 €1178.24 · R/R 1.25 | T3 €1192.61 · R/R 1.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1126.51


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.32 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **2.532 pt plus bas** dans le cas TYPIQUE (médiane), 14.194 au p90, **17.109 au pire**
   - perte réelle **12.114 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 5.32 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.016 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0864** [0.0513 ; 0.1351] _(largeur 8.4 pt, n_eff 173.1)_
   - swing : **0.4018** [0.3511 ; 0.4541] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.5136** [0.461 ; 0.566] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.7 pt), swing (27.3 pt), deep (32.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.86 %** | CVaR **-6.73 %** | vol 2.97 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.99 % contre 3.38 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.6 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.846 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5007** (β de hausse 0.587, asymétrie 0.853) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.227× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 1074.0622 sur support (1.16 ATR, 7.04 %) — p(stop avant cible) 0.4442 [0.39 ; 0.50], R/R 3.427, perte reelle 15.141 % (gap inclus), CVaR 7.053 %, EV -3.5354 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9993 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.59 ATR (stop 4.638 %) — p(stop avant cible) 0.6103 [0.56 ; 0.66], R/R 5.017, perte reelle 10.343 % (gap inclus), EV -3.2599 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.610, borne haute 0.661 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.26 %) : P(cible) 0.0 % x 51.90 % + P(rien) 39.0 % x 7.83 % ne couvrent pas P(stop) 61.0 % x 10.34 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.16 ATR (stop 7.04 %) — p(stop avant cible) 0.4442 [0.39 ; 0.50], R/R 3.427, perte reelle 15.141 % (gap inclus), EV -3.5354 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - ⚠ support DETECTE a 0.49 ATR du spot — compartiment <1, mesure a 50.9 % de casse (IC clusterise [0.477 ; 0.544] sur 1060 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.54 %) : P(cible) 0.0 % x 51.90 % + P(rien) 55.6 % x 5.73 % ne couvrent pas P(stop) 44.4 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.67 ATR (stop 21.788 %) — p(stop avant cible) 0.0382 [0.02 ; 0.06], R/R 2.314, perte reelle 22.429 % (gap inclus), EV -0.3236 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 21.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 51.90 % + P(rien) 96.2 % x 0.55 % ne couvrent pas P(stop) 3.8 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.106 | EV/share : €2.428 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 62 % | T2 38 % | T3 22 %
- Kelly (position) : f* 0.153 | ¼-Kelly 0.038 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 40.9 | bear 52.0 | side 7.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.51% → cible +1.25% / stop −2.0%, p_fill 83%, n_eff≈34.7) : P(cible|rempli) **58%** · **EV/risk +0.000** (×p_fill ; si rempli +0.00% du capital)
  - **swing** (entrée dip −1.12% → cible +2.795% / stop −4.248%, p_fill 66%, n_eff≈29.2) : P(cible|rempli) **82%** · **EV/risk +0.245** (×p_fill ; si rempli +1.57% du capital)
  - **deep** (entrée dip −1.74% → cible +3.953% / stop −6.412%, p_fill 67%, n_eff≈26.7) : P(cible|rempli) **74%** · **EV/risk +0.174** (×p_fill ; si rempli +1.65% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→71% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.05% / basse méd. −1.62%
- Profil de vol intra : ouverture 2.671% vs midi 0.942% vs clôture 1.125% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.09 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.164% ; recovery-V 25%
- **σ réalisé intraday** 2.771% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 63% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 1168.83 (VA 1165.71–1174.29 ; dernier close 1160.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 17% · rebond 64% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.29% · baisse 31% (gap-down >1% 10% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.69% (p90 −1.73%) · haut méd +0.57% · range méd 1.37%
- Excursion ouverture 15min (n=160) : bas méd −0.89% (p90 −1.95%) · haut méd +0.68% · range méd 1.75%
- Excursion ouverture 30min (n=160) : bas méd −0.92% (p90 −2.22%) · haut méd +0.88% · range méd 2.03%
- Excursion ouverture 60min (n=160) : bas méd −0.94% (p90 −2.63%) · haut méd +1.0% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1160.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 70% (117/159) · gap 21% · délai 0.5min · rebond 54% (61/117) (MFE +1.11%)
   - −1.0% : fill 30min 38% · séance 64% (108/159) · gap 10% · délai 7.3min · rebond 61% (62/108) (MFE +1.27%)
   - −1.5% : fill 30min 27% · séance 53% (87/159) · gap 6% · délai 28.3min · rebond 61% (49/87) (MFE +1.37%)
   - −2.0% : fill 30min 18% · séance 41% (74/159) · gap 5% · délai 33.7min · rebond 66% (46/74) (MFE +1.58%)
   - −3.0% : fill 30min 8% · séance 25% (46/159) · gap 3% · délai 120.4min · rebond 58% (27/46) (MFE +1.31%)
   - −4.0% : fill 30min 3% · séance 17% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 9% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.61%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.75%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.77%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=530 jambes) : jambe baissière méd −1.07% (p90 −2.48%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 94% (46/48) · rebond 65% (27/46)
      · −2.0% : fill 80% (38/48) · rebond 66% (25/38)
      · −3.0% : fill 53% (26/48) · rebond 63% (16/26)
      · −4.0% : fill 41% (16/48) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/48) · rebond 83% (7/9)
   - **flat** (46 séances) :
      · −1.0% : fill 65% (33/46) · rebond 72% (21/33)
      · −2.0% : fill 25% (17/46) · rebond 72% (10/17)
      · −3.0% : fill 17% (10/46) · rebond 55% (5/10)
      · −4.0% : fill 15% (8/46) · rebond 36% (2/8)
      · −5.0% : fill 10% (6/46) · rebond 22% (1/6)
   - **gap-up** (65 séances) :
      · −1.0% : fill 48% (29/65) · rebond 48% (14/29)
      · −2.0% : fill 30% (19/65) · rebond 63% (11/19)
      · −3.0% : fill 14% (10/65) · rebond 49% (6/10)
      · −4.0% : fill 6% (4/65) · rebond 61% (3/4)
      · −5.0% : fill 2% (1/65) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (78 cas) · 34% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:37** → P(séance verte=clôture>ouverture) 73% si début vert vs 20% si rouge (base 48% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **73%** · continue >prix actuel 44% ; creux résiduel méd -1.19% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.78% / q75 +1.81% → **scale +0.78% / runner +1.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.75%** (au-delà de la MAE q10 -3.75%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.28%] · haut q95 +3.77% · bas q05 -3.13%
   - 60min (n=160) : retour [-2.79% .. +3.22%] · haut q95 +4.42% · bas q05 -3.9%
   - 2h (n=160) : retour [-3.21% .. +3.06%] · haut q95 +4.42% · bas q05 -4.5%
   - 4h (n=160) : retour [-3.44% .. +3.33%] · haut q95 +4.87% · bas q05 -4.64%
   - 6h (n=160) : retour [-4.17% .. +3.32%] · haut q95 +4.96% · bas q05 -5.05%
   - session (n=160) : retour [-5.42% .. +3.98%] · haut q95 +5.07% · bas q05 -5.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 45.6  _(neutre)_
- **ADX** : 21.5  _(pas de tendance nette)_
- **MACD** : hist -1.413  _(bearish_recent)_
- **BB** : %B 0.47 · largeur 13.8%
- **ATR** : 48.53 (15.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.141  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 66.5  _(marche en range (choppy))_
- **MA** : MA20 1159.78 · MA50 1094.02 · MA200 1417.7  _(prix < MA20)_
- **Dist MA** : MA20 -0.4% · MA50 +5.6% · MA200 -18.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (668860 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

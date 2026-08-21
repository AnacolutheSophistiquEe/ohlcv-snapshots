# ENR

**Generated** : 2026-08-21T21:40:32.508314+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €153.36  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €153.36 (+0.7% vs entrée) · entrée €152.35 · stop €144.09 · T1 €168.86 · R/R 2.0  
> ↳ P(T1 av. stop) 9 % _(réel 5 s)_ · EV/risk -0.176 _(réel 5 s)_ (GBM 0.039) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.270 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €151.33–€153.36 (mid €152.35)
- Spot actuel : €153.36 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €144.09 (stop swing_plan-based (-6.05%))
- Targets : T1 €168.86 · R/R 2.0 | T2 €169.10 · R/R 2.03 | T3 €169.34 · R/R 2.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €144.09


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.05 %)** : le gap seul le franchit 0.628 % des séances (8 fois sur 1274).
   - exécution **1.857 pt plus bas** dans le cas TYPIQUE (médiane), 15.996 au p90, **29.707 au pire**
   - perte réelle **12.609 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 6.05 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0412 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0987** [0.0609 ; 0.1498] _(largeur 8.9 pt, n_eff 173.1)_
   - swing : **0.4171** [0.366 ; 0.4696] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4839** [0.4315 ; 0.5365] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 36.0 observations effectives », dont la borne haute a 95 % vaut environ 8.3 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 36.2 observations effectives », dont la borne haute a 95 % vaut environ 8.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.1 pt), swing (33.4 pt), deep (31.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.6 %** | vol 3.22 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 6.22 % contre 3.39 % aujourd'hui, rapport 1.83)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.74 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.37** (β de hausse 1.0854, asymétrie 1.2623) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.441× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 147.3676 sur support (0.26 ATR, 3.907 %) — p(stop avant cible) 0.6413 [0.59 ; 0.69], R/R 2.999, perte reelle 7.407 % (gap inclus), CVaR 3.973 %, EV -1.8482 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.4111 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.641, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 3.97 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.171 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.9 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.29 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.26 ATR (stop 3.907 %) — p(stop avant cible) 0.6413 [0.59 ; 0.69], R/R 2.999, perte reelle 7.407 % (gap inclus), EV -1.8482 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.641, borne haute 0.691 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 3.97 % > budget 3.00 %
      - ⚠ support DETECTE a 0.26 ATR du spot — compartiment <1, mesure a 50.9 % de casse (IC clusterise [0.477 ; 0.544] sur 1060 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.85 %) : P(cible) 2.5 % x 22.21 % + P(rien) 33.3 % x 7.02 % ne couvrent pas P(stop) 64.1 % x 7.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 6.04 %) — p(stop avant cible) 0.4867 [0.43 ; 0.54], R/R 1.762, perte reelle 12.609 % (gap inclus), EV -2.8154 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.08 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.82 %) : P(cible) 2.8 % x 22.21 % + P(rien) 48.6 % x 5.57 % ne couvrent pas P(stop) 48.7 % x 12.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.45 ATR (stop 16.737 %) — p(stop avant cible) 0.0382 [0.02 ; 0.06], R/R 0.621, perte reelle 35.757 % (gap inclus), EV 1.0861 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.75 % > budget 3.00 %
   - 🟢 support a 7.01 ATR (stop 31.072 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.621, perte reelle 35.757 % (gap inclus), EV 2.0161 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.08 % > budget 3.00 %
   - 🟢 support a 11.4 ATR (stop 48.752 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.456, perte reelle 48.752 % (gap inclus), EV 2.0305 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.46 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.75 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.039 | EV/share : €0.319 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 8.6 | bear 5.7 | side 85.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 307.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.315% → cible +1.663% / stop −8.0%, p_fill 87%, n_eff≈36.0) : P(cible|rempli) **41%** · **EV/risk -0.076** (×p_fill ; si rempli -0.70% du capital)
  - **swing** (entrée dip −0.665% → cible +10.842% / stop −5.421%, p_fill 76%, n_eff≈32.1) : P(cible|rempli) **9%** · **EV/risk -0.176** (×p_fill ; si rempli -1.25% du capital)
  - **deep** (entrée dip −0.969% → cible +5.259% / stop −6.1%, p_fill 91%, n_eff≈36.2) : P(cible|rempli) **43%** · **EV/risk -0.207** (×p_fill ; si rempli -1.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→60% · +2.0%→41% · +3.0%→22% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.95% (p90 6.15%) · excursion haute méd. +1.47% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.126% vs midi 0.909% vs clôture 1.119% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 58% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.522% ; recovery-V 12%
- **σ réalisé intraday** 2.593% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 68% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 153.5763 (VA 152.4468–154.3293 ; dernier close 152.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 63% · **stop −3.81%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.28 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 34% (gap-down >1% 20% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.57% (p90 −1.67%) · haut méd +0.47% · range méd 1.25%
- Excursion ouverture 15min (n=160) : bas méd −0.75% (p90 −2.21%) · haut méd +0.64% · range méd 1.59%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.28%) · haut méd +0.67% · range méd 1.98%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.62%) · haut méd +0.77% · range méd 2.16%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 152.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 71% (115/159) · gap 26% · délai 0.5min · rebond 55% (65/115) (MFE +1.17%)
   - −1.0% : fill 30min 42% · séance 66% (106/159) · gap 20% · délai 5.3min · rebond 64% (64/106) (MFE +1.45%)
   - −1.5% : fill 30min 34% · séance 61% (96/159) · gap 15% · délai 17.2min · rebond 64% (62/96) (MFE +1.58%)
   - −2.0% : fill 30min 21% · séance 45% (73/159) · gap 10% · délai 50.0min · rebond 63% (46/73) (MFE +1.47%)
   - −3.0% : fill 30min 13% · séance 29% (51/159) · gap 3% · délai 120.2min · rebond 58% (35/51) (MFE +1.41%)
   - −4.0% : fill 30min 5% · séance 19% (38/159) · gap 2% · délai 221.1min · rebond 63% (27/38) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 14% (24/159) · gap 0% · délai 350.7min · rebond 55% (15/24) (MFE +1.13%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.78%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.95%) → stop au-delà de −0.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=535 jambes) : jambe baissière méd −1.07% (p90 −2.64%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 97% (49/50) · rebond 58% (27/49)
      · −2.0% : fill 76% (39/50) · rebond 53% (24/39)
      · −3.0% : fill 61% (32/50) · rebond 45% (20/32)
      · −4.0% : fill 47% (26/50) · rebond 59% (18/26)
      · −5.0% : fill 38% (18/50) · rebond 50% (11/18)
   - **flat** (23 séances) :
      · −1.0% : fill 66% (17/23) · rebond 81% (12/17)
      · −2.0% : fill 29% (9/23) · rebond 71% (5/9)
      · −3.0% : fill 10% (4/23) · rebond 85% (3/4)
      · −4.0% : fill 8% (3/23) · rebond 83% (2/3)
      · −5.0% : fill 6% (2/23) · rebond 74% (1/2)
   - **gap-up** (86 séances) :
      · −1.0% : fill 49% (40/86) · rebond 65% (25/40)
      · −2.0% : fill 33% (25/86) · rebond 74% (17/25)
      · −3.0% : fill 16% (15/86) · rebond 81% (12/15)
      · −4.0% : fill 7% (9/86) · rebond 69% (7/9)
      · −5.0% : fill 4% (4/86) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 76% si les 15 1res min sont vertes (77 cas) · 22% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 24% si rouge (base 47% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 282min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **83%** · continue >prix actuel 55% ; creux résiduel méd -1.27% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +2.55% → **scale +1.78% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **24%** (continue à baisser 55%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.19%** (au-delà de la MAE q10 -4.19%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.13% .. +2.23%] · haut q95 +2.68% · bas q05 -2.61%
   - 60min (n=160) : retour [-2.5% .. +2.34%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.66%] · haut q95 +3.05% · bas q05 -3.77%
   - 4h (n=160) : retour [-3.39% .. +2.67%] · haut q95 +3.75% · bas q05 -4.29%
   - 6h (n=160) : retour [-3.82% .. +3.52%] · haut q95 +4.4% · bas q05 -4.81%
   - session (n=160) : retour [-5.07% .. +4.34%] · haut q95 +5.43% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **45 min** → P(reste trend-up à la clôture) **15%**. Lecture précoce 30 min : signature présente → 14% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


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

- **RSI** : 60.2  _(momentum haussier)_
- **ADX** : 12.7  _(pas de tendance nette)_
- **MACD** : hist 0.142  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 19.1%
- **ATR** : 6.18 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.271  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 59.1  _(transition)_
- **MA** : MA20 152.26 · MA50 155.82 · MA200 148.41  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 -1.6% · MA200 +3.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (680954 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

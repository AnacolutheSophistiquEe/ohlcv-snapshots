# PRY

**Generated** : 2026-08-21T21:48:04.809105+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €124.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €124.00 (+0.3% vs entrée) · entrée €123.63 · stop €113.74 · T1 €125.36 · R/R 0.17  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.083 _(réel 5 s)_ (GBM -0.055) · ¼-Kelly 0.097 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €123.28–€123.97 (mid €123.63)
- Spot actuel : €124.00 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €113.74 (stop swing_plan-based (-4.51%))
- Targets : T1 €125.36 · R/R 0.17 | T2 €127.10 · R/R 0.35 | T3 €128.83 · R/R 0.53
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €113.74


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.50 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.51 %)** : le gap seul le franchit 0.63 % des séances (8 fois sur 1270).
   - exécution **0.759 pt plus bas** dans le cas TYPIQUE (médiane), 3.512 au p90, **5.488 au pire**
   - perte réelle **6.062 %** en moyenne _(tirée par la queue)_, jusqu'à **9.998 %** — au lieu des 4.51 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0098 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.846 % | p01 -3.346 % | pire -9.998 % _(sur 1270 séances)_
- **P(stop avant cible)** _(source : daily, 1271 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0628** [0.0337 ; 0.1063] _(largeur 7.3 pt, n_eff 173.1)_
   - swing : **0.3374** [0.2891 ; 0.3884] _(largeur 9.9 pt, n_eff 345.8)_
   - deep : **0.4324** [0.3809 ; 0.485] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 35.4 observations effectives », dont la borne haute a 95 % vaut environ 8.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.8 pt), swing (31.7 pt), deep (30.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-4.24 %** | CVaR **-5.72 %** | vol 2.62 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 1.79 % contre 2.94 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.46 % vs -7.47 % si l'on extrapolait par √5 _(rapport 0.865 ; < 1 = le √5 surestime)_
- **β de baisse : 1.038** (β de hausse 1.2267, asymétrie 0.8461) vs FTSEMIB — 562 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.42× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 116.5161 sur atr_based (1.5 ATR, 6.035 %) — p(stop avant cible) 0.3871 [0.34 ; 0.44], R/R 3.117, perte reelle 7.909 % (gap inclus), CVaR 6.039 %, EV 0.2303 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.8813 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.16 ATR (stop 3.265 %) — p(stop avant cible) 0.6106 [0.56 ; 0.66], R/R 4.654, perte reelle 5.296 % (gap inclus), EV -0.5598 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.611, borne haute 0.661 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.16 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 1.4 % x 24.65 % + P(rien) 37.5 % x 6.20 % ne couvrent pas P(stop) 61.1 % x 5.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 6.035 %) — p(stop avant cible) 0.3871 [0.34 ; 0.44], R/R 3.117, perte reelle 7.909 % (gap inclus), EV 0.2303 % — **REFUSE**
      - refuse : cible atteinte seulement 1.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - ⚪ swing_based a 2.95 ATR (stop 14.472 %) — p(stop avant cible) 0.0404 [0.02 ; 0.07], R/R 1.703, perte reelle 14.472 % (gap inclus), EV 1.9031 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.47 % > budget 12.00 %
   - 🟢 support a 4.01 ATR (stop 18.769 %) — p(stop avant cible) 0.0126 [0.00 ; 0.03], R/R 1.313, perte reelle 18.769 % (gap inclus), EV 1.9333 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.77 % > budget 12.00 %
   - 🟢 support a 10.31 ATR (stop 44.088 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.559, perte reelle 44.088 % (gap inclus), EV 1.9315 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.09 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.055 | EV/share : €-0.546 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 31 % | T3 14 %
- Kelly (position) : f* 0.388 | ¼-Kelly 0.097 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 40.4 | bear 24.1 | side 35.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 124.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +1.403% / stop −8.0%, p_fill 86%, n_eff≈35.4) : P(cible|rempli) **48%** · **EV/risk -0.083** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −0.486% → cible +3.137% / stop −4.043%, p_fill 86%, n_eff≈34.4) : P(cible|rempli) **38%** · **EV/risk -0.291** (×p_fill ; si rempli -1.36% du capital)
  - **deep** (entrée dip −0.714% → cible +4.436% / stop −6.079%, p_fill 98%, n_eff≈38.5) : P(cible|rempli) **41%** · **EV/risk -0.302** (×p_fill ; si rempli -1.88% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→68% · +2.0%→41% · +3.0%→29% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.35% (p90 6.42%) · excursion haute méd. +1.5% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.463% vs midi 0.821% vs clôture 1.193% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; neutre — autocorr -0.009)_ ; drift intra méd. -0.753% ; recovery-V 23%
- **σ réalisé intraday** 2.67% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 122.1885 (VA 121.1985–122.6835 ; dernier close 122.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 74% · **stop −2.38%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.61 (high win-rate)
- Gaps overnight (n=158) : méd. 0.28% · baisse 41% (gap-down >1% 16% · >2% 9%)
- Excursion ouverture 5min (n=159) : bas méd −0.84% (p90 −2.07%) · haut méd +0.29% · range méd 1.4%
- Excursion ouverture 15min (n=159) : bas méd −1.04% (p90 −2.53%) · haut méd +0.55% · range méd 1.75%
- Excursion ouverture 30min (n=159) : bas méd −1.08% (p90 −2.94%) · haut méd +0.64% · range méd 2.03%
- Excursion ouverture 60min (n=159) : bas méd −1.23% (p90 −3.16%) · haut méd +0.86% · range méd 2.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 122.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 70% (114/158) · gap 24% · délai 0.3min · rebond 60% (71/114) (MFE +1.25%)
   - −1.0% : fill 30min 50% · séance 62% (97/158) · gap 16% · délai 0.6min · rebond 58% (58/97) (MFE +1.5%)
   - −1.5% : fill 30min 35% · séance 54% (84/158) · gap 13% · délai 4.5min · rebond 52% (46/84) (MFE +1.09%)
   - −2.0% : fill 30min 23% · séance 44% (68/158) · gap 9% · délai 13.1min · rebond 62% (43/68) (MFE +1.23%)
   - −3.0% : fill 30min 11% · séance 33% (49/158) · gap 3% · délai 77.1min · rebond 64% (33/49) (MFE +1.64%)
   - −4.0% : fill 30min 3% · séance 19% (26/158) · gap 1% · délai 185.0min · rebond 74% (19/26) (MFE +1.45%)
   - −5.0% : fill 30min 1% · séance 13% (18/158) · gap 1% · délai 394.2min · rebond 65% (13/18) (MFE +1.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −1.78%) → stop au-delà de −1.53% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.41% (p90 −2.02%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.85%) → stop au-delà de −1.09% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=495 jambes) : jambe baissière méd −1.07% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 91% (49/54) · rebond 47% (27/49)
      · −2.0% : fill 71% (39/54) · rebond 59% (26/39)
      · −3.0% : fill 59% (30/54) · rebond 64% (22/30)
      · −4.0% : fill 40% (17/54) · rebond 70% (12/17)
      · −5.0% : fill 31% (13/54) · rebond 60% (9/13)
   - **flat** (31 séances) :
      · −1.0% : fill 71% (18/31) · rebond 58% (11/18)
      · −2.0% : fill 46% (10/31) · rebond 91% (8/10)
      · −3.0% : fill 24% (6/31) · rebond 63% (3/6)
      · −4.0% : fill 7% (3/31) · rebond 59% (2/3)
      · −5.0% : fill 4% (2/31) · rebond 25% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 40% (30/73) · rebond 74% (20/30)
      · −2.0% : fill 26% (19/73) · rebond 43% (9/19)
      · −3.0% : fill 21% (13/73) · rebond 63% (8/13)
      · −4.0% : fill 11% (6/73) · rebond 86% (5/6)
      · −5.0% : fill 5% (3/73) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 46% en base · 67% si les 15 1res min sont vertes (73 cas) · 30% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=159) : COUDE à **1:09** → P(séance verte=clôture>ouverture) 80% si début vert vs 22% si rouge (base 46% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **80%** · continue >prix actuel 60% ; creux résiduel méd -1.19% (q20 -1.97%) → **SL/trailing à −1.97%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.5% / q75 +2.65% → **scale +1.5% / runner +2.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **22%** (continue à baisser 63%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.1%** (au-delà de la MAE q10 -4.1%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-2.84% .. +2.94%] · haut q95 +3.44% · bas q05 -3.39%
   - 60min (n=159) : retour [-3.34% .. +2.49%] · haut q95 +3.9% · bas q05 -3.55%
   - 2h (n=159) : retour [-3.58% .. +2.64%] · haut q95 +3.99% · bas q05 -4.45%
   - 4h (n=159) : retour [-3.52% .. +3.29%] · haut q95 +4.11% · bas q05 -4.6%
   - 6h (n=159) : retour [-3.71% .. +3.77%] · haut q95 +4.56% · bas q05 -4.88%
   - session (n=159) : retour [-4.33% .. +4.03%] · haut q95 +5.38% · bas q05 -6.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 57.2  _(momentum haussier)_
- **ADX** : 26.0  _(tendance etablie)_
- **MACD** : hist 0.392  _(pas de croisement recent)_
- **BB** : %B 0.5 · largeur 14.5%
- **ATR** : 4.99 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.188  _(distribution)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 55.5  _(transition)_
- **MA** : MA20 123.93 · MA50 133.25 · MA200 113.21  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -6.9% · MA200 +9.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (649061 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

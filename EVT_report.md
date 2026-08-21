# EVT

**Generated** : 2026-08-21T21:39:04.612236+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.36  

> 🟡 **WAIT-FOR-DIP** — spot +1.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.36 (+1.5% vs entrée) · entrée €3.31 · stop €3.26 · T1 €3.38 · R/R 1.4  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk 0.035 _(réel 5 s)_ (GBM -0.029) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.30–€3.32 (mid €3.31)
- Spot actuel : €3.36 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : €3.26 (stop swing_plan-based (-7.67%))
- Targets : T1 €3.38 · R/R 1.4 | T2 €3.42 · R/R 2.2 | T3 €3.47 · R/R 3.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.26


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.35 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.67 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **6.154 pt plus bas** dans le cas TYPIQUE (médiane), 20.422 au p90, **24.743 au pire**
   - perte réelle **18.001 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 7.67 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0405 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.984 % | pire -32.413 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0657** [0.0358 ; 0.1099] _(largeur 7.4 pt, n_eff 173.1)_
   - swing : **0.4215** [0.3703 ; 0.474] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4868** [0.4344 ; 0.5394] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.4 pt), swing (46.4 pt), deep (44.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-5.11 %** | CVaR **-9.26 %** | vol 3.81 %/j
   - _fenêtre arrêtée : rupture de regime a 1260 seances en arriere (volatilite 2.12 % contre 3.96 % aujourd'hui, rapport 0.53)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.164 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1125** (β de hausse 0.9496, asymétrie 1.1715) vs GDAXI — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 3.0939 sur support (1.14 ATR, 7.81 %) — p(stop avant cible) 0.3974 [0.35 ; 0.45], R/R 1.772, perte reelle 18.001 % (gap inclus), CVaR 7.85 %, EV -4.2097 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9033 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.05 ATR (stop 2.676 %) — p(stop avant cible) 0.7626 [0.72 ; 0.81], R/R 5.459, perte reelle 5.843 % (gap inclus), EV -2.2864 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.763, borne haute 0.805 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.29 %) : P(cible) 0.9 % x 31.90 % + P(rien) 22.8 % x 8.20 % ne couvrent pas P(stop) 76.3 % x 5.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.14 ATR (stop 7.81 %) — p(stop avant cible) 0.3974 [0.35 ; 0.45], R/R 1.772, perte reelle 18.001 % (gap inclus), EV -4.2097 % — **REFUSE**
      - refuse : cible atteinte seulement 1.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.21 %) : P(cible) 1.5 % x 31.90 % + P(rien) 58.8 % x 4.22 % ne couvrent pas P(stop) 39.7 % x 18.00 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.029 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 16 % | T3 6 %
- Kelly (position) : f* 0.018 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.0 | bear 7.4 | side 14.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.339% → cible +2.084% / stop −1.501%, p_fill 67%, n_eff≈24.9) : P(cible|rempli) **29%** · **EV/risk +0.035** (×p_fill ; si rempli +0.08% du capital)
  - **swing** (entrée dip −2.95% → cible +3.516% / stop −4.863%, p_fill 40%, n_eff≈15.3) : P(cible|rempli) **40%** · **EV/risk -0.101** (×p_fill ; si rempli -1.23% du capital)
  - **deep** (entrée dip −4.56% → cible +4.973% / stop −7.418%, p_fill 26%, n_eff≈17.0) : P(cible|rempli) **21%** · **EV/risk -0.121** (×p_fill ; si rempli -3.46% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→70% · +2.0%→45% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.9% (p90 6.57%) · excursion haute méd. +1.77% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.716% vs midi 1.23% vs clôture 1.198% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.094 ; mean-reverting — autocorr -0.12)_ ; drift intra méd. -0.801% ; recovery-V 29%
- **σ réalisé intraday** 3.173% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 71% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 3.3734 (VA 3.3554–3.3914 ; dernier close 3.338)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−0.5%** sous le close veille · fill 83% · rebond 73% · **stop −3.48%** sous le fill (sous le bruit) · cible +1.61% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.18% · baisse 38% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.41%) · haut méd +0.52% · range méd 1.48%
- Excursion ouverture 15min (n=160) : bas méd −0.86% (p90 −2.83%) · haut méd +0.78% · range méd 1.82%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −2.84%) · haut méd +0.91% · range méd 2.23%
- Excursion ouverture 60min (n=160) : bas méd −1.21% (p90 −3.28%) · haut méd +0.96% · range méd 2.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.338 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 83% (133/159) · gap 23% · délai 0.4min · rebond 73% (89/133) (MFE +1.61%)
   - −1.0% : fill 30min 48% · séance 70% (116/159) · gap 16% · délai 2.1min · rebond 70% (74/116) (MFE +1.6%)
   - −1.5% : fill 30min 36% · séance 55% (95/159) · gap 11% · délai 7.8min · rebond 66% (60/95) (MFE +1.79%)
   - −2.0% : fill 30min 23% · séance 44% (80/159) · gap 7% · délai 23.5min · rebond 58% (50/80) (MFE +1.32%)
   - −3.0% : fill 30min 11% · séance 27% (55/159) · gap 4% · délai 51.4min · rebond 66% (40/55) (MFE +1.36%)
   - −4.0% : fill 30min 6% · séance 16% (32/159) · gap 2% · délai 53.0min · rebond 60% (20/32) (MFE +1.67%)
   - −5.0% : fill 30min 4% · séance 8% (18/159) · gap 1% · délai 56.0min · rebond 60% (12/18) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.49%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.36% (p90 −1.71%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.89%) → stop au-delà de −1.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=815 jambes) : jambe baissière méd −1.06% (p90 −2.31%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (57 séances) :
      · −1.0% : fill 95% (54/57) · rebond 70% (31/54)
      · −2.0% : fill 65% (41/57) · rebond 60% (25/41)
      · −3.0% : fill 38% (29/57) · rebond 68% (21/29)
      · −4.0% : fill 27% (20/57) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/57) · rebond 57% (9/13)
   - **flat** (43 séances) :
      · −1.0% : fill 65% (30/43) · rebond 73% (23/30)
      · −2.0% : fill 48% (20/43) · rebond 64% (13/20)
      · −3.0% : fill 34% (13/43) · rebond 77% (10/13)
      · −4.0% : fill 17% (6/43) · rebond 46% (2/6)
      · −5.0% : fill 6% (3/43) · rebond 27% (1/3)
   - **gap-up** (59 séances) :
      · −1.0% : fill 56% (32/59) · rebond 66% (20/32)
      · −2.0% : fill 25% (19/59) · rebond 46% (12/19)
      · −3.0% : fill 14% (13/59) · rebond 40% (9/13)
      · −4.0% : fill 8% (6/59) · rebond 90% (4/6)
      · −5.0% : fill 5% (2/59) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 64% si les 15 1res min sont vertes (72 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 36% si rouge (base 49% · écart 30 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.75% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.43% → **scale +1.55% / runner +2.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **36%** (continue à baisser 52%) → **RÉDUIRE ~64%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.68%** (au-delà de la MAE q10 -4.68%), cible rebond +1.7% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +2.3%] · haut q95 +3.38% · bas q05 -3.94%
   - 60min (n=160) : retour [-3.65% .. +2.7%] · haut q95 +3.47% · bas q05 -4.67%
   - 2h (n=160) : retour [-4.02% .. +2.67%] · haut q95 +3.92% · bas q05 -5.05%
   - 4h (n=160) : retour [-3.49% .. +3.11%] · haut q95 +3.94% · bas q05 -6.57%
   - 6h (n=160) : retour [-3.74% .. +3.41%] · haut q95 +4.92% · bas q05 -6.57%
   - session (n=160) : retour [-4.6% .. +4.26%] · haut q95 +6.53% · bas q05 -7.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 44.2  _(momentum baissier)_
- **ADX** : 32.2  _(tendance etablie)_
- **MACD** : hist 0.024  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 14.6%
- **ATR** : 0.16 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.353  _(distribution)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 48.2  _(transition)_
- **MA** : MA20 3.48 · MA50 4.08 · MA200 5.03  _(prix < MA20)_
- **Dist MA** : MA20 -3.6% · MA50 -17.7% · MA200 -33.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (659583 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

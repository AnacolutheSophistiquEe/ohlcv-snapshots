# SMR

**Generated** : 2026-08-21T00:32:57.718705+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $9.07  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot $9.07 (+0.4% vs entrée) · entrée $9.03 · stop $8.71 · T1 $9.66 · R/R 1.97  
> ↳ P(T1 av. stop) 22 % _(réel 5 s)_ · EV/risk 0.132 _(réel 5 s)_ (GBM 0.066) · ¼-Kelly 0.043 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.53% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 169 % hors [0,100] (R² max 0.71). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $8.98–$9.07 (mid $9.03)
- Spot actuel : $9.07 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $8.71 (stop swing_plan-based (-8.32%))
- Targets : T1 $9.66 · R/R 1.97 | T2 $9.79 · R/R 2.38 | T3 $9.91 · R/R 2.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.71


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.33 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (8.32 %)** : le gap seul le franchit 0.891 % des séances (10 fois sur 1122).
   - exécution **3.11 pt plus bas** dans le cas TYPIQUE (médiane), 10.222 au p90, **22.003 au pire**
   - perte réelle **13.499 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 8.32 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0462 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.434 % | p01 -6.963 % | pire -30.323 % _(sur 1122 séances)_
- **P(stop avant cible)** _(source : daily, 1123 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3098** [0.2445 ; 0.3814] _(largeur 13.7 pt, n_eff 173.1)_
   - swing : **0.6014** [0.5491 ; 0.652] _(largeur 10.3 pt, n_eff 345.2)_
   - deep : **0.6166** [0.5645 ; 0.6668] _(largeur 10.2 pt, n_eff 345.1)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.8 pt), swing (31.1 pt), deep (32.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.4 %** | CVaR **-11.92 %** | vol 6.95 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 11.03 % contre 5.84 % aujourd'hui, rapport 1.89)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.01 % vs -18.72 % si l'on extrapolait par √5 _(rapport 1.016 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6149** (β de hausse 1.3786, asymétrie 1.1713) vs IWM — 532 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.031× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.33 ATR (stop 4.616 %) — p(stop avant cible) 0.7544 [0.71 ; 0.80], R/R 1.328, perte reelle 8.845 % (gap inclus), EV -3.9188 % — **REFUSE**
      - refuse : p_stop_first 0.754, borne haute 0.798 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.33 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.15 ATR du spot, sous le seuil de 1 ATR : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545] sur 940 touches) contre ~35 % au-dela. L'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.92 %) : P(cible) 23.4 % x 11.74 % + P(rien) 1.1 % x 0.34 % ne couvrent pas P(stop) 75.4 % x 8.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 10.957 %) — p(stop avant cible) 0.5006 [0.45 ; 0.55], R/R 0.665, perte reelle 17.667 % (gap inclus), EV -4.0378 % — **REFUSE**
      - refuse : p_stop_first 0.501, borne haute 0.553 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 0.66 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.04 %) : P(cible) 42.5 % x 11.74 % + P(rien) 7.4 % x -2.47 % ne couvrent pas P(stop) 50.1 % x 17.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.51 ATR (stop 20.52 %) — p(stop avant cible) 0.2128 [0.17 ; 0.26], R/R 0.387, perte reelle 30.323 % (gap inclus), EV -2.5238 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.53 % > budget 12.0 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.52 %) : P(cible) 49.8 % x 11.74 % + P(rien) 28.9 % x -6.62 % ne couvrent pas P(stop) 21.3 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.81 ATR (stop 22.698 %) — p(stop avant cible) 0.163 [0.13 ; 0.20], R/R 0.387, perte reelle 30.323 % (gap inclus), EV -1.5857 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.70 % > budget 12.0 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.59 %) : P(cible) 49.9 % x 11.74 % + P(rien) 33.8 % x -7.42 % ne couvrent pas P(stop) 16.3 % x 30.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.066 | EV/share : $0.021 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.17 | ¼-Kelly 0.043 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 82.3 | bear 6.3 | side 11.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 154.0 (= 17 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.472% → cible +7.069% / stop −3.535%, p_fill 92%, n_eff≈36.7) : P(cible|rempli) **22%** · **EV/risk +0.132** (×p_fill ; si rempli +0.51% du capital)
  - **swing** (entrée dip −1.015% → cible +12.892% / stop −7.379%, p_fill 93%, n_eff≈36.7) : P(cible|rempli) **23%** · **EV/risk -0.015** (×p_fill ; si rempli -0.12% du capital)
  - **deep** (entrée dip −1.48% → cible +22.797% / stop −11.399%, p_fill 83%, n_eff≈34.0) : P(cible|rempli) **10%** · **EV/risk -0.113** (×p_fill ; si rempli -1.54% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→82% · +2.0%→66% · +3.0%→61% · +5.0%→40% · +8.0%→12%
- Range intraday médian 7.55% (p90 12.48%) · excursion haute méd. +3.55% / basse méd. −3.15%
- Profil de vol intra : ouverture 4.787% vs midi 1.504% vs clôture 1.839% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.055)_ ; drift intra méd. 0.264% ; recovery-V 40%
- **σ réalisé intraday** 4.661% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 68% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 9.1524 (VA 8.9154–9.3301 ; dernier close 9.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 50% · rebond 78% · **stop −5.18%** sous le fill (sous le bruit) · cible +2.67% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.47% · baisse 57% (gap-down >1% 35% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −3.02%) · haut méd +1.19% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.82%) · haut méd +1.86% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.74% (p90 −4.63%) · haut méd +2.25% · range méd 4.42%
- Excursion ouverture 60min (n=160) : bas méd −2.1% (p90 −5.6%) · haut méd +2.62% · range méd 5.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 82% (131/159) · gap 50% · délai 0.0min · rebond 67% (81/131) (MFE +2.03%)
   - −1.0% : fill 30min 67% · séance 79% (126/159) · gap 35% · délai 0.0min · rebond 70% (84/126) (MFE +2.23%)
   - −1.5% : fill 30min 62% · séance 74% (119/159) · gap 32% · délai 0.1min · rebond 73% (87/119) (MFE +2.05%)
   - −2.0% : fill 30min 55% · séance 66% (110/159) · gap 26% · délai 0.9min · rebond 67% (78/110) (MFE +2.2%)
   - −3.0% : fill 30min 43% · séance 55% (97/159) · gap 10% · délai 4.4min · rebond 75% (78/97) (MFE +2.36%)
   - −4.0% : fill 30min 34% · séance 50% (87/159) · gap 5% · délai 8.7min · rebond 78% (68/87) (MFE +2.67%)
   - −5.0% : fill 30min 23% · séance 40% (65/159) · gap 2% · délai 19.9min · rebond 71% (47/65) (MFE +2.06%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −2.67%) → stop au-delà de −1.82% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.69%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.18% (p90 −3.26%) → stop au-delà de −2.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1172 jambes) : jambe baissière méd −1.36% (p90 −3.15%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 100% (86/86) · rebond 67% (57/86)
      · −2.0% : fill 92% (81/86) · rebond 74% (61/81)
      · −3.0% : fill 82% (75/86) · rebond 78% (62/75)
      · −4.0% : fill 75% (69/86) · rebond 81% (57/69)
      · −5.0% : fill 60% (50/86) · rebond 74% (38/50)
   - **flat** (11 séances) :
      · −1.0% : fill 79% (8/11) · rebond 54% (5/8)
      · −2.0% : fill 68% (6/11) · rebond 18% (2/6)
      · −3.0% : fill 68% (6/11) · rebond 46% (3/6)
      · −4.0% : fill 68% (6/11) · rebond 56% (3/6)
      · −5.0% : fill 57% (5/11) · rebond 79% (4/5)
   - **gap-up** (62 séances) :
      · −1.0% : fill 51% (32/62) · rebond 81% (22/32)
      · −2.0% : fill 30% (23/62) · rebond 60% (15/23)
      · −3.0% : fill 17% (16/62) · rebond 80% (13/16)
      · −4.0% : fill 13% (12/62) · rebond 67% (8/12)
      · −5.0% : fill 9% (10/62) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 65% si les 15 1res min sont vertes (71 cas) · 31% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:01** → P(séance verte=clôture>ouverture) 88% si début vert vs 10% si rouge (base 47% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **88%** · continue >prix actuel 53% ; creux résiduel méd -1.77% (q20 -3.46%) → **SL/trailing à −3.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.63% → **scale +2.05% / runner +3.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **10%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.35% .. +4.91%] · haut q95 +6.22% · bas q05 -5.85%
   - 60min (n=160) : retour [-5.39% .. +5.56%] · haut q95 +6.78% · bas q05 -6.41%
   - 2h (n=160) : retour [-6.39% .. +5.57%] · haut q95 +9.0% · bas q05 -8.0%
   - 4h (n=160) : retour [-7.13% .. +7.33%] · haut q95 +9.71% · bas q05 -9.04%
   - 6h (n=160) : retour [-7.31% .. +8.39%] · haut q95 +10.95% · bas q05 -9.32%
   - session (n=160) : retour [-7.21% .. +9.17%] · haut q95 +11.02% · bas q05 -9.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 55.8  _(momentum haussier)_
- **ADX** : 13.7  _(pas de tendance nette)_
- **MACD** : hist 0.016  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 28.2%
- **ATR** : 0.66 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.01  _(neutre)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 61.2  _(transition)_
- **MA** : MA20 9.04 · MA50 9.3 · MA200 14.12  _(prix > MA20)_
- **Dist MA** : MA20 +0.4% · MA50 -2.5% · MA200 -35.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (594898 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

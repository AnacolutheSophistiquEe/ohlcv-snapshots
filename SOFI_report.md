# SOFI

**Generated** : 2026-09-29T00:47:59.831488+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.93  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $15.93 (+1.3% vs entrée) · entrée $15.73 · stop $15.10 · T1 $15.95 · R/R 0.35  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk -0.03 _(réel 5 s)_ (GBM 0.033) · ¼-Kelly 0.073 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +2.5 % ≠ (strike 17.0 − spot 15.93)/spot = +6.7 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -65 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.230 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.68–$15.77 (mid $15.73)
- Spot actuel : $15.93 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $15.10 (plancher anti-bruit 5 s — stop EV-optimal −4% (first-passage 5 s réel) ; -4.01 % depuis l'entree)
- Targets : T1 $15.95 · R/R 0.35 | T2 $16.17 · R/R 0.7 | T3 $16.39 · R/R 1.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.10


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.83 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (6.71 %)** : le gap seul le franchit 0.958 % des séances (12 fois sur 1253).
   - exécution **1.461 pt plus bas** dans le cas TYPIQUE (médiane), 3.14 au p90, **4.395 au pire**
   - perte réelle **8.457 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 6.71 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0167 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 12 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1185** [0.0767 ; 0.1729] _(largeur 9.6 pt, n_eff 173.1)_
   - swing : **0.4249** [0.3736 ; 0.4775] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4375** [0.3859 ; 0.4901] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.9 observations effectives », dont la borne haute a 95 % vaut environ 15.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.5 pt), swing (38.9 pt), deep (36.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-6.29 %** | CVaR **-8.7 %** | vol 4.14 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8327** (β de hausse 1.713, asymétrie 1.0699) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.36× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 14.0529 sur atr_grid (3.0 ATR, 11.784 %) — p(stop avant cible) 0.2484 [0.21 ; 0.30], R/R 1.688, perte reelle 11.784 % (gap inclus), CVaR 11.784 %, EV -0.3491 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 5.892 %) — p(stop avant cible) 0.5742 [0.52 ; 0.63], R/R 2.574, perte reelle 7.728 % (gap inclus), EV -1.2818 % — **REFUSE**
      - refuse : cible atteinte seulement 8.7 % du temps (< 15 %) meme a 10 seances : le R/R de 2.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.574, borne haute 0.625 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.28 %) : P(cible) 8.7 % x 19.89 % + P(rien) 33.8 % x 4.19 % ne couvrent pas P(stop) 57.4 % x 7.73 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 1.39 ATR (stop 8.036 %) — p(stop avant cible) 0.4247 [0.37 ; 0.48], R/R 2.049, perte reelle 9.707 % (gap inclus), EV -0.9989 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.00 %) : P(cible) 9.0 % x 19.89 % + P(rien) 48.5 % x 2.75 % ne couvrent pas P(stop) 42.5 % x 9.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 1.68 ATR (stop 9.172 %) — p(stop avant cible) 0.3778 [0.33 ; 0.43], R/R 2.007, perte reelle 9.913 % (gap inclus), EV -0.7463 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 9.0 % x 19.89 % + P(rien) 53.2 % x 2.26 % ne couvrent pas P(stop) 37.8 % x 9.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 0.982 %) — p(stop avant cible) 0.9373 [0.91 ; 0.96], R/R 8.067, perte reelle 2.466 % (gap inclus), EV -1.4467 % — **REFUSE**
      - refuse : cible atteinte seulement 2.7 % du temps (< 15 %) meme a 10 seances : le R/R de 8.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.937, borne haute 0.959 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 2.7 % x 19.89 % + P(rien) 3.5 % x 9.12 % ne couvrent pas P(stop) 93.7 % x 2.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.964 %) — p(stop avant cible) 0.8948 [0.86 ; 0.92], R/R 5.574, perte reelle 3.569 % (gap inclus), EV -1.8221 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.895, borne haute 0.924 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.82 %) : P(cible) 4.5 % x 19.89 % + P(rien) 6.0 % x 7.87 % ne couvrent pas P(stop) 89.5 % x 3.57 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 2.946 %) — p(stop avant cible) 0.8216 [0.78 ; 0.86], R/R 4.219, perte reelle 4.715 % (gap inclus), EV -1.9704 % — **REFUSE**
      - refuse : cible atteinte seulement 6.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.822, borne haute 0.859 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.97 %) : P(cible) 6.1 % x 19.89 % + P(rien) 11.8 % x 5.93 % ne couvrent pas P(stop) 82.2 % x 4.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 3.928 %) — p(stop avant cible) 0.7231 [0.67 ; 0.77], R/R 3.271, perte reelle 6.082 % (gap inclus), EV -1.9067 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.723, borne haute 0.768 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 7.0 % x 19.89 % + P(rien) 20.7 % x 5.29 % ne couvrent pas P(stop) 72.3 % x 6.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 1.39 ATR (stop 6.634 %) — p(stop avant cible) 0.5091 [0.46 ; 0.56], R/R 2.39, perte reelle 8.322 % (gap inclus), EV -1.0367 % — **REFUSE**
      - refuse : cible atteinte seulement 8.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.509, borne haute 0.561 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 8.9 % x 19.89 % + P(rien) 40.2 % x 3.55 % ne couvrent pas P(stop) 50.9 % x 8.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 9.82 %) — p(stop avant cible) 0.3496 [0.30 ; 0.40], R/R 1.898, perte reelle 10.482 % (gap inclus), EV -0.7534 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.75 %) : P(cible) 9.0 % x 19.89 % + P(rien) 56.0 % x 1.99 % ne couvrent pas P(stop) 35.0 % x 10.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 10.802 %) — p(stop avant cible) 0.2993 [0.25 ; 0.35], R/R 1.791, perte reelle 11.105 % (gap inclus), EV -0.5302 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 9.0 % x 19.89 % + P(rien) 61.0 % x 1.63 % ne couvrent pas P(stop) 29.9 % x 11.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 11.784 %) — p(stop avant cible) 0.2484 [0.21 ; 0.30], R/R 1.688, perte reelle 11.784 % (gap inclus), EV -0.3491 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 9.0 % x 19.89 % + P(rien) 66.1 % x 1.18 % ne couvrent pas P(stop) 24.8 % x 11.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 13.748 %) — p(stop avant cible) 0.1672 [0.13 ; 0.21], R/R 1.447, perte reelle 13.748 % (gap inclus), EV 0.0305 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.75 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 15.712 %) — p(stop avant cible) 0.107 [0.08 ; 0.14], R/R 1.266, perte reelle 15.712 % (gap inclus), EV 0.2286 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.71 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 17.676 %) — p(stop avant cible) 0.06 [0.04 ; 0.09], R/R 1.125, perte reelle 17.676 % (gap inclus), EV 0.268 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.68 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 19.639 %) — p(stop avant cible) 0.05 [0.03 ; 0.08], R/R 1.013, perte reelle 19.639 % (gap inclus), EV 0.222 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.64 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 21.603 %) — p(stop avant cible) 0.0331 [0.02 ; 0.06], R/R 0.921, perte reelle 21.603 % (gap inclus), EV 0.194 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.60 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 23.567 %) — p(stop avant cible) 0.0239 [0.01 ; 0.04], R/R 0.844, perte reelle 23.567 % (gap inclus), EV 0.1998 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.57 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 25.531 %) — p(stop avant cible) 0.0156 [0.01 ; 0.03], R/R 0.779, perte reelle 25.531 % (gap inclus), EV 0.2274 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 27.495 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.724, perte reelle 27.495 % (gap inclus), EV 0.3175 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.49 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 29.459 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.675, perte reelle 29.459 % (gap inclus), EV 0.3234 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.46 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 31.423 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.633, perte reelle 31.423 % (gap inclus), EV 0.3194 % — **REFUSE**
      - refuse : cible atteinte seulement 9.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.42 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.93, ATR14 0.6257 (3.928 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.376 ATR = 1.477 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.196 % | 15.8987 | 92.85 % | 95.77 % | 97.07 % | 97.47 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.393 % | 15.8674 | 85.2 % | 89.42 % | 92.03 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.589 % | 15.8361 | 78.95 % | 84.68 % | 87.99 % | 90.39 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.786 % | 15.8049 | 71.6 % | 79.44 % | 83.35 % | 86.86 % | 90.55 % | 93.33 % |
| 0.25 ATR | 0.982 % | 15.7736 | 66.26 % | 74.9 % | 79.92 % | 84.13 % | 88.92 % | 91.89 % |
| 0.35 ATR | 1.375 % | 15.711 | 52.57 % | 65.12 % | 71.85 % | 78.26 % | 85.37 % | 88.6 % |
| 0.5 ATR | 1.964 % | 15.6171 | 37.66 % | 53.02 % | 61.45 % | 69.06 % | 79.37 % | 84.5 % |
| 0.75 ATR | 2.946 % | 15.4607 | 20.64 % | 36.9 % | 46.72 % | 56.83 % | 69.61 % | 77.72 % |
| 1.0 ATR | 3.928 % | 15.3043 | 8.86 % | 24.5 % | 33.8 % | 44.79 % | 59.35 % | 69.1 % |
| 1.25 ATR | 4.91 % | 15.1479 | 4.23 % | 15.02 % | 23.92 % | 35.19 % | 50.1 % | 62.42 % |
| 1.5 ATR | 5.892 % | 14.9914 | 2.01 % | 9.38 % | 16.55 % | 27.1 % | 42.28 % | 56.06 % |
| 2.0 ATR | 7.856 % | 14.6786 | 0.7 % | 4.44 % | 8.38 % | 15.07 % | 28.96 % | 45.28 % |
| 2.5 ATR | 9.82 % | 14.3657 | 0.3 % | 1.92 % | 3.94 % | 9.4 % | 19.51 % | 35.63 % |
| 3.0 ATR | 11.784 % | 14.0529 | 0.1 % | 0.91 % | 2.83 % | 6.07 % | 13.62 % | 28.23 % |
| 4.0 ATR | 15.712 % | 13.4271 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.42 % | 14.68 % |
| 6.0 ATR | 23.567 % | 12.1757 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.69 ATR | 0.76 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.47 ATR | 1.94 ATR |
| **3 s.** | 0.31 ATR | 0.69 ATR | 0.78 ATR | 1.02 ATR | 1.22 ATR | 1.38 ATR | 1.90 ATR | 2.38 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 1.00 ATR | 1.32 ATR | 1.59 ATR | 1.79 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.41 ATR | 1.85 ATR | 2.21 ATR | 2.47 ATR | 3.58 ATR | 4.74 ATR |
| **20 s.** | 0.83 ATR | 1.78 ATR | 2.02 ATR | 2.68 ATR | 3.24 ATR | 3.61 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.964 %, prix 15.6171), p(touche) 37.66 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.624–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.946 %, prix 15.4607), p(touche) 36.9 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.783–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.928 %, prix 15.3043), p(touche) 33.8 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.996–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.928 %, prix 15.3043), p(touche) 44.79 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.413–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.892 %, prix 14.9914), p(touche) 42.28 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.015–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (9.82 %, prix 14.3657), p(touche) 35.63 % (en stress 98.98 %)  ✅ optimum identifie (75.0 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.033 | EV/share : $0.021 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 41 % | T3 20 %
- Kelly (position) : f* 0.29 | ¼-Kelly 0.073 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.2 | bear 8.1 | side 77.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.27% → cible +1.392% / stop −4.0%, p_fill 60%, n_eff≈28.0) : P(cible|rempli) **51%** · **EV/risk -0.030** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −2.782% → cible +3.114% / stop −4.04%, p_fill 55%, n_eff≈21.7) : P(cible|rempli) **61%** · **EV/risk +0.042** (×p_fill ; si rempli +0.31% du capital)
  - **deep** (entrée dip −4.308% → cible +4.404% / stop −6.157%, p_fill 41%, n_eff≈18.9) : P(cible|rempli) **77%** · **EV/risk +0.129** (×p_fill ; si rempli +1.93% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→71% · +2.0%→50% · +3.0%→38% · +5.0%→14% · +8.0%→1%
- Range intraday médian 4.39% (p90 7.54%) · excursion haute méd. +2.04% / basse méd. −2.17%
- Profil de vol intra : ouverture 3.063% vs midi 0.835% vs clôture 0.985% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑2%/↓0% ; spike-down 59% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.15 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.123% ; recovery-V 26%
- **σ réalisé intraday** 2.603% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 52% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 18.1833 (VA 18.1547–18.2972 ; dernier close 18.21)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 47% · rebond 67% · **stop −3.09%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. 0.19% · baisse 43% (gap-down >1% 24% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.69%) · haut méd +0.72% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −0.92% (p90 −2.67%) · haut méd +1.07% · range méd 2.26%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −3.18%) · haut méd +1.23% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.28% (p90 −3.59%) · haut méd +1.33% · range méd 3.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.22 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (121/159) · gap 31% · délai 0.0min · rebond 51% (64/121) (MFE +1.13%)
   - −1.0% : fill 30min 52% · séance 64% (109/159) · gap 24% · délai 1.2min · rebond 53% (62/109) (MFE +1.01%)
   - −1.5% : fill 30min 41% · séance 60% (100/159) · gap 21% · délai 7.1min · rebond 62% (66/100) (MFE +1.35%)
   - −2.0% : fill 30min 35% · séance 47% (80/159) · gap 11% · délai 3.8min · rebond 67% (55/80) (MFE +1.72%)
   - −3.0% : fill 30min 11% · séance 32% (57/159) · gap 2% · délai 50.3min · rebond 54% (37/57) (MFE +1.08%)
   - −4.0% : fill 30min 8% · séance 17% (36/159) · gap 2% · délai 48.8min · rebond 52% (23/36) (MFE +1.2%)
   - −5.0% : fill 30min 3% · séance 10% (20/159) · gap 2% · délai 192.2min · rebond 44% (10/20) (MFE +0.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.43% (p90 −1.73%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −1.81%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.44%) → stop au-delà de −1.18% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=664 jambes) : jambe baissière méd −1.08% (p90 −2.75%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 98% (65/66) · rebond 51% (38/65)
      · −2.0% : fill 86% (56/66) · rebond 72% (40/56)
      · −3.0% : fill 63% (42/66) · rebond 57% (28/42)
      · −4.0% : fill 36% (28/66) · rebond 60% (20/28)
      · −5.0% : fill 21% (16/66) · rebond 54% (9/16)
   - **flat** (21 séances) :
      · −1.0% : fill 59% (12/21) · rebond 42% (5/12)
      · −2.0% : fill 40% (7/21) · rebond 55% (4/7)
      · −3.0% : fill 31% (6/21) · rebond 38% (3/6)
      · −4.0% : fill 19% (3/21) · rebond 30% (1/3)
      · −5.0% : fill 11% (1/21) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 41% (32/72) · rebond 62% (19/32)
      · −2.0% : fill 20% (17/72) · rebond 58% (11/17)
      · −3.0% : fill 10% (9/72) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/72) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/72) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 64% si les 15 1res min sont vertes (75 cas) · 27% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **52min** → P(séance verte=clôture>ouverture) 82% si début vert vs 12% si rouge (base 44% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **82%** · continue >prix actuel 61% ; creux résiduel méd -0.98% (q20 -2.13%) → **SL/trailing à −2.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.83% → **scale +1.34% / runner +2.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **12%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.24%** (au-delà de la MAE q10 -3.24%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.86% .. +3.66%] · haut q95 +4.01% · bas q05 -3.38%
   - 60min (n=160) : retour [-3.12% .. +4.25%] · haut q95 +4.63% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +4.46%] · haut q95 +5.16% · bas q05 -4.56%
   - 4h (n=160) : retour [-4.23% .. +4.54%] · haut q95 +5.67% · bas q05 -5.12%
   - 6h (n=160) : retour [-4.69% .. +4.63%] · haut q95 +5.7% · bas q05 -5.61%
   - session (n=160) : retour [-4.65% .. +4.94%] · haut q95 +5.7% · bas q05 -5.84%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.9  _(survente)_
- **ADX** : 10.2  _(pas de tendance nette)_
- **MACD** : hist -0.117  _(pas de croisement recent)_
- **BB** : %B -0.01 · largeur 14.7%
- **ATR** : 0.63 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.228  _(distribution)_
- **Vol ratio** : 1.24  _(volume normal)_
- **Choppiness** : 53.4  _(transition)_
- **MA** : MA20 17.23 · MA50 17.56 · MA200 19.16  _(prix < MA20)_
- **Dist MA** : MA20 -7.5% · MA50 -9.3% · MA200 -16.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (858504 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

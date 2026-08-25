# MSTR

**Generated** : 2026-08-25T17:48:25.217276+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $122.63  

> 🟡 **WAIT-FOR-DIP** — spot +1.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $122.63 (+1.1% vs entrée) · entrée $121.32 · stop $116.47 · T1 $123.51 · R/R 0.45  
> ↳ P(T1 av. stop) 56 % _(réel 5 s)_ · EV/risk 0.051 _(réel 5 s)_ (GBM -0.054) · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -13.8 % ≠ (strike 110.0 − spot 122.63)/spot = -10.3 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -5905 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 18.2 < 20 (tendance pas encore confirmée) alors que Choppiness 34.3 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $120.89–$121.76 (mid $121.32)
- Spot actuel : $122.63 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : $116.47 (stop swing_plan-based (-9.07%))
- Targets : T1 $123.51 · R/R 0.45 | T2 $126.93 · R/R 1.16 | T3 $130.35 · R/R 1.86
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $116.47


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.21 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.07 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **4.243 pt plus bas** dans le cas TYPIQUE (médiane), 17.905 au p90, **18.302 au pire**
   - perte réelle **17.215 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 9.07 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.039 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.43 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1545** [0.1066 ; 0.2139] _(largeur 10.7 pt, n_eff 173.1)_
   - swing : **0.5453** [0.4926 ; 0.5972] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.5761** [0.5236 ; 0.6274] _(largeur 10.4 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (32.9 pt), swing (35.0 pt), deep (34.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.92 %** | CVaR **-10.5 %** | vol 5.46 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.39 % contre 4.78 % aujourd'hui, rapport 1.75)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.77 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3349** (β de hausse 1.8636, asymétrie 1.2529) vs IWM — 602 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 108.238 sur atr_grid (2.25 ATR, 11.736 %) — p(stop avant cible) 0.4073 [0.36 ; 0.46], R/R 1.18, perte reelle 20.144 % (gap inclus), CVaR 11.763 %, EV -4.7605 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 25 des 25 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 50.7 % de la queue et il ne reste que -199.12 EUR a partager. Prix du risque -0.086 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.97 ATR (stop 7.422 %) — p(stop avant cible) 0.6046 [0.55 ; 0.66], R/R 2.054, perte reelle 11.572 % (gap inclus), EV -3.6467 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.605, borne haute 0.655 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.82 ATR du spot — compartiment <1, mesure a 47.2 % de casse (IC clusterise [0.438 ; 0.506] sur 1074 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.65 %) : P(cible) 7.9 % x 23.77 % + P(rien) 31.7 % x 4.68 % ne couvrent pas P(stop) 60.5 % x 11.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.89 ATR (stop 17.395 %) — p(stop avant cible) 0.2206 [0.18 ; 0.27], R/R 0.881, perte reelle 26.975 % (gap inclus), EV -4.0858 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.41 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.09 %) : P(cible) 8.6 % x 23.77 % + P(rien) 69.3 % x -0.26 % ne couvrent pas P(stop) 22.1 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.22 ATR (stop 29.595 %) — p(stop avant cible) 0.0566 [0.04 ; 0.08], R/R 0.803, perte reelle 29.595 % (gap inclus), EV -2.3363 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.34 %) : P(cible) 8.6 % x 23.77 % + P(rien) 85.7 % x -3.16 % ne couvrent pas P(stop) 5.7 % x 29.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.304 %) — p(stop avant cible) 0.9502 [0.92 ; 0.97], R/R 7.33, perte reelle 3.243 % (gap inclus), EV -2.4727 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 7.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.950, borne haute 0.970 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.47 %) : P(cible) 1.4 % x 23.77 % + P(rien) 3.6 % x 7.93 % ne couvrent pas P(stop) 95.0 % x 3.24 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 9.128 %) — p(stop avant cible) 0.5218 [0.47 ; 0.57], R/R 1.381, perte reelle 17.215 % (gap inclus), EV -5.419 % — **REFUSE**
      - refuse : cible atteinte seulement 8.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.522, borne haute 0.574 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.38 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.42 %) : P(cible) 8.1 % x 23.77 % + P(rien) 39.8 % x 4.15 % ne couvrent pas P(stop) 52.2 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 11.736 %) — p(stop avant cible) 0.4073 [0.36 ; 0.46], R/R 1.18, perte reelle 20.144 % (gap inclus), EV -4.7605 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.76 %) : P(cible) 8.3 % x 23.77 % + P(rien) 50.9 % x 2.88 % ne couvrent pas P(stop) 40.7 % x 20.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 20.864 %) — p(stop avant cible) 0.1597 [0.12 ; 0.20], R/R 0.881, perte reelle 26.975 % (gap inclus), EV -3.1293 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.87 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.13 %) : P(cible) 8.6 % x 23.77 % + P(rien) 75.4 % x -1.15 % ne couvrent pas P(stop) 16.0 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 23.472 %) — p(stop avant cible) 0.1245 [0.09 ; 0.16], R/R 0.881, perte reelle 26.975 % (gap inclus), EV -2.7042 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.88 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.70 %) : P(cible) 8.6 % x 23.77 % + P(rien) 78.9 % x -1.77 % ne couvrent pas P(stop) 12.4 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 31.296 %) — p(stop avant cible) 0.0377 [0.02 ; 0.06], R/R 0.76, perte reelle 31.296 % (gap inclus), EV -2.2118 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.76 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.30 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.21 %) : P(cible) 8.6 % x 23.77 % + P(rien) 87.6 % x -3.52 % ne couvrent pas P(stop) 3.8 % x 31.30 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 33.904 %) — p(stop avant cible) 0.0233 [0.01 ; 0.04], R/R 0.701, perte reelle 33.904 % (gap inclus), EV -2.2038 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.90 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.20 %) : P(cible) 8.6 % x 23.77 % + P(rien) 89.0 % x -3.89 % ne couvrent pas P(stop) 2.3 % x 33.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 36.512 %) — p(stop avant cible) 0.0153 [0.01 ; 0.03], R/R 0.651, perte reelle 36.512 % (gap inclus), EV -2.1385 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.65 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.65 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 8.6 % x 23.77 % + P(rien) 89.8 % x -4.04 % ne couvrent pas P(stop) 1.5 % x 36.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 39.12 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.608, perte reelle 39.12 % (gap inclus), EV -2.0312 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.03 %) : P(cible) 8.6 % x 23.77 % + P(rien) 91.2 % x -4.40 % ne couvrent pas P(stop) 0.2 % x 39.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 41.728 %) — p(stop avant cible) 0.0008 [0.00 ; 0.01], R/R 0.57, perte reelle 41.728 % (gap inclus), EV -2.0173 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.57 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 8.6 % x 23.77 % + P(rien) 91.3 % x -4.42 % ne couvrent pas P(stop) 0.1 % x 41.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 122.63, ATR14 6.3964 (5.216 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 5s | p(touche) 20s |
|---|---|---|---|---|---|
| 0.25 ATR | 1.304 % | 121.0309 | 67.88 % | 86.15 % | 92.3 % |
| 0.5 ATR | 2.608 % | 119.4318 | 38.27 % | 71.28 % | 84.91 % |
| 0.75 ATR | 3.912 % | 117.8327 | 19.23 % | 58.34 % | 77.62 % |
| 1.0 ATR | 5.216 % | 116.2336 | 9.37 % | 46.81 % | 70.53 % |
| 1.25 ATR | 6.52 % | 114.6345 | 4.13 % | 36.5 % | 63.45 % |
| 1.5 ATR | 7.824 % | 113.0354 | 2.11 % | 29.32 % | 57.6 % |
| 2.0 ATR | 10.432 % | 109.8371 | 0.2 % | 16.38 % | 47.64 % |
| 2.5 ATR | 13.04 % | 106.6389 | 0.1 % | 8.8 % | 37.89 % |
| 3.0 ATR | 15.648 % | 103.4407 | 0.1 % | 4.65 % | 28.23 % |
| 4.0 ATR | 20.864 % | 97.0443 | 0.0 % | 0.81 % | 18.17 % |
| 6.0 ATR | 31.296 % | 84.2514 | 0.0 % | 0.0 % | 4.41 % |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.25–0.5 ATR — optimum 0.25 ATR (1.304 %, prix 121.0309), p(touche) 67.88 % (en stress 94.0 %)
- **5 seance(s)** : plage utile 0.25–1.5 ATR — optimum 0.25 ATR (1.304 %, prix 121.0309), p(touche) 86.15 % (en stress 100.0 %)
- **20 seance(s)** : plage utile 0.25–3.0 ATR — optimum 1.5 ATR (7.824 %, prix 113.0354), p(touche) 57.6 % (en stress 100.0 %)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.


## Edge, scénarios & sizing

- EV/risk : -0.054 | EV/share : $-0.264 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 60 % | T2 17 % | T3 15 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.5 | bear 10.4 | side 11.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 368.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.062% → cible +1.802% / stop −4.0%, p_fill 74%, n_eff≈32.4) : P(cible|rempli) **56%** · **EV/risk +0.051** (×p_fill ; si rempli +0.28% du capital)
  - **swing** (entrée dip −2.344% → cible +13.775% / stop −6.888%, p_fill 69%, n_eff≈28.2) : P(cible|rempli) **17%** · **EV/risk +0.052** (×p_fill ; si rempli +0.52% du capital)
  - **deep** (entrée dip −3.626% → cible +7.847% / stop −8.118%, p_fill 65%, n_eff≈27.9) : P(cible|rempli) **65%** · **EV/risk +0.208** (×p_fill ; si rempli +2.59% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→72% · +2.0%→56% · +3.0%→40% · +5.0%→15% · +8.0%→8%
- Range intraday médian 5.44% (p90 9.85%) · excursion haute méd. +2.41% / basse méd. −2.6%
- Profil de vol intra : ouverture 3.394% vs midi 1.211% vs clôture 1.366% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr -0.003)_ ; drift intra méd. 0.265% ; recovery-V 22%
- **σ réalisé intraday** 3.736% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 79% / bas 60% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 120.1996 (VA 118.8924–120.4901 ; dernier close 119.24)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 27% · rebond 77% · **stop −4.68%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. -0.03% · baisse 50% (gap-down >1% 38% · >2% 24%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.12%) · haut méd +0.71% · range méd 1.77%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.9%) · haut méd +1.18% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.44%) · haut méd +1.37% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.58% (p90 −3.66%) · haut méd +1.72% · range méd 3.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 119.24 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 75% (124/159) · gap 44% · délai 0.0min · rebond 50% (61/124) (MFE +1.01%)
   - −1.0% : fill 30min 58% · séance 69% (118/159) · gap 38% · délai 0.0min · rebond 57% (68/118) (MFE +1.08%)
   - −1.5% : fill 30min 50% · séance 64% (109/159) · gap 31% · délai 0.0min · rebond 59% (64/109) (MFE +1.51%)
   - −2.0% : fill 30min 46% · séance 57% (99/159) · gap 24% · délai 0.0min · rebond 62% (63/99) (MFE +1.4%)
   - −3.0% : fill 30min 31% · séance 46% (77/159) · gap 13% · délai 2.0min · rebond 60% (47/77) (MFE +1.66%)
   - −4.0% : fill 30min 21% · séance 38% (64/159) · gap 5% · délai 18.1min · rebond 63% (40/64) (MFE +1.65%)
   - −5.0% : fill 30min 14% · séance 27% (47/159) · gap 3% · délai 31.7min · rebond 77% (34/47) (MFE +1.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −2.46%) → stop au-delà de −1.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.68%) → stop au-delà de −1.84% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.95% (p90 −2.54%) → stop au-delà de −1.83% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=972 jambes) : jambe baissière méd −1.13% (p90 −2.69%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 100% (76/77) · rebond 52% (38/76)
      · −2.0% : fill 91% (70/77) · rebond 60% (41/70)
      · −3.0% : fill 80% (62/77) · rebond 60% (37/62)
      · −4.0% : fill 66% (52/77) · rebond 65% (34/52)
      · −5.0% : fill 50% (40/77) · rebond 80% (30/40)
   - **flat** (18 séances) :
      · −1.0% : fill 69% (15/18) · rebond 74% (11/15)
      · −2.0% : fill 52% (11/18) · rebond 61% (8/11)
      · −3.0% : fill 22% (5/18) · rebond 55% (3/5)
      · −4.0% : fill 14% (4/18) · rebond 7% (1/4)
      · −5.0% : fill 11% (3/18) · rebond 9% (1/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 34% (27/64) · rebond 63% (19/27)
      · −2.0% : fill 18% (18/64) · rebond 71% (14/18)
      · −3.0% : fill 12% (10/64) · rebond 57% (7/10)
      · −4.0% : fill 11% (8/64) · rebond 68% (5/8)
      · −5.0% : fill 5% (4/64) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 53% si les 15 1res min sont vertes (82 cas) · 36% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 71% si début vert vs 21% si rouge (base 45% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **71%** · continue >prix actuel 47% ; creux résiduel méd -1.78% (q20 -3.88%) → **SL/trailing à −3.88%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.69% / q75 +3.57% → **scale +1.69% / runner +3.57%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **21%** (continue à baisser 53%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.71%** (au-delà de la MAE q10 -4.71%), cible rebond +2.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.36% .. +3.61%] · haut q95 +3.97% · bas q05 -3.82%
   - 60min (n=160) : retour [-4.73% .. +3.98%] · haut q95 +5.43% · bas q05 -5.04%
   - 2h (n=160) : retour [-4.37% .. +5.62%] · haut q95 +6.54% · bas q05 -5.18%
   - 4h (n=160) : retour [-5.7% .. +7.99%] · haut q95 +9.02% · bas q05 -6.89%
   - 6h (n=160) : retour [-5.9% .. +6.91%] · haut q95 +9.84% · bas q05 -7.3%
   - session (n=160) : retour [-5.09% .. +6.26%] · haut q95 +9.84% · bas q05 -7.78%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0.6% / strong 5.0%) · base = 9 séances trend-up (n_eff 4.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 12% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.22% (p75 2.61% / p90 4.03%) · ~3.12 replis/séance, durée méd 49.07 min. P(nouveau plus-haut après repli) :
   - −0.5% → **75%** (reprise méd 15.0 min, n=30)
   - −1.0% → **57%** (reprise méd 38.91 min, n=17)
   - −1.5% → **43%** (reprise méd 74.97 min, n=13)
   - −2.0% → **28%** (reprise méd 89.44 min, n=8)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−4.03%** (p90, défaut prudent ; serré/agressif −2.61%) ; extension open→close méd +8.28% (q75 +9.94% / q95 +16.06%), MFE méd +11.04% / q90 +15.91%
   - Échelle scale-out : +11.04% (33%) / +12.88% (33%) / +15.91% (34%)
- **DÉSARMER** : repli > **−4.03%** depuis le plus-haut = décay → P(retournement) **29%** (préavis méd 300.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +15.91% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 98% du temps (retour médian dernière heure +0.79%)


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : extreme
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

- **RSI** : 72.0  _(surachat)_
- **ADX** : 18.2  _(pas de tendance nette)_
- **MACD** : hist 3.361  _(pas de croisement recent)_
- **BB** : %B 1.17 · largeur 34.1%
- **ATR** : 6.4 (10.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.106  _(accumulation)_
- **Vol ratio** : 1.86  _(volume au-dessus de la moyenne)_
- **Choppiness** : 34.3  _(marche directionnel)_
- **MA** : MA20 99.77 · MA50 99.83 · MA200 143.33  _(prix > MA20)_
- **Dist MA** : MA20 +22.9% · MA50 +22.8% · MA200 -14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (882255 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

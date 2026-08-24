# ENR

**Generated** : 2026-08-24T21:40:16.583737+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €148.74  

> 🟡 **WAIT-FOR-DIP** — spot +8.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €148.74 (+8.5% vs entrée) · entrée €137.09 · stop €130.91 · T1 €142.27 · R/R 0.84  
> ↳ P(T1 av. stop) 77 % · EV/risk 0.47 · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €136.06–€138.13 (mid €137.09)
- Spot actuel : €148.74 (+8.5% au-dessus de la zone — repli à attendre)
- Stop : €130.91 (stop swing_plan-based (-11.99%))
- Targets : T1 €142.27 · R/R 0.84 | T2 €147.45 · R/R 1.68 | T3 €152.63 · R/R 2.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €130.91


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (11.99 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **4.18 pt plus bas** dans le cas TYPIQUE (médiane), 19.85 au p90, **23.767 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 11.99 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0232 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.307 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0976** [0.06 ; 0.1485] _(largeur 8.8 pt, n_eff 173.1)_
   - swing : **0.4204** [0.3692 ; 0.4729] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4812** [0.4289 ; 0.5338] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 11.6 observations effectives », dont la borne haute a 95 % vaut environ 25.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (51.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.6 %** | vol 3.22 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 6.23 % contre 3.38 % aujourd'hui, rapport 1.84)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.74 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3648** (β de hausse 1.0874, asymétrie 1.2552) vs GDAXI — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.425× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 142.5586 sur atr_grid (1.0 ATR, 4.156 %) — p(stop avant cible) 0.6062 [0.55 ; 0.66], R/R 3.297, perte reelle 7.889 % (gap inclus), CVaR 4.218 %, EV -1.758 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5996 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.606, borne haute 0.657 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.22 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.84 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.234 %) — p(stop avant cible) 0.4815 [0.43 ; 0.53], R/R 1.921, perte reelle 13.536 % (gap inclus), EV -3.2362 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.27 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.24 %) : P(cible) 1.1 % x 26.01 % + P(rien) 50.8 % x 5.92 % ne couvrent pas P(stop) 48.1 % x 13.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.7 ATR (stop 13.215 %) — p(stop avant cible) 0.1082 [0.08 ; 0.14], R/R 1.19, perte reelle 21.854 % (gap inclus), EV 0.5283 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.24 % > budget 3.00 %
   - ⚪ sr_based a 3.53 ATR (stop 16.655 %) — p(stop avant cible) 0.0379 [0.02 ; 0.06], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.0579 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.67 % > budget 3.00 %
   - 🟢 support a 6.25 ATR (stop 27.994 %) — p(stop avant cible) 0.0038 [0.00 ; 0.02], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.9371 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.00 % > budget 3.00 %
   - 🟢 support a 10.64 ATR (stop 46.224 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.563, perte reelle 46.224 % (gap inclus), EV 1.9969 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.22 % > budget 3.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 4.156 %) — p(stop avant cible) 0.6062 [0.55 ; 0.66], R/R 3.297, perte reelle 7.889 % (gap inclus), EV -1.758 % — **REFUSE**
      - refuse : cible atteinte seulement 1.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.30 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.606, borne haute 0.657 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.22 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.76 %) : P(cible) 1.0 % x 26.01 % + P(rien) 38.4 % x 7.22 % ne couvrent pas P(stop) 60.6 % x 7.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 7.273 %) — p(stop avant cible) 0.408 [0.36 ; 0.46], R/R 1.4, perte reelle 18.578 % (gap inclus), EV -4.1787 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 7.31 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.18 %) : P(cible) 1.1 % x 26.01 % + P(rien) 58.1 % x 5.36 % ne couvrent pas P(stop) 40.8 % x 18.58 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 9.351 %) — p(stop avant cible) 0.2901 [0.24 ; 0.34], R/R 1.19, perte reelle 21.854 % (gap inclus), EV -2.9333 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.19 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.38 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.93 %) : P(cible) 1.1 % x 26.01 % + P(rien) 69.9 % x 4.46 % ne couvrent pas P(stop) 29.0 % x 21.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 18.701 %) — p(stop avant cible) 0.0302 [0.02 ; 0.05], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.2719 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.71 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 20.779 %) — p(stop avant cible) 0.0093 [0.00 ; 0.02], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.7596 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.79 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.857 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.8502 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.87 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 24.935 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.9139 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.94 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 29.091 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.9553 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.10 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 31.169 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.9823 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.17 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 33.247 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 0.727, perte reelle 35.757 % (gap inclus), EV 1.9823 % — **REFUSE**
      - refuse : cible atteinte seulement 1.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.25 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.07 | EV/share : €0.433 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 30 % | T3 9 %
- Kelly (position) : f* 0.034 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 8.6 | bear 5.7 | side 85.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.554% → cible +1.689% / stop −8.0%, p_fill 25%, n_eff≈11.6) : P(cible|rempli) **59%** · **EV/risk +0.019** (×p_fill ; si rempli +0.62% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→60% · +2.0%→40% · +3.0%→21% · +5.0%→8% · +8.0%→1%
- Range intraday médian 3.89% (p90 6.15%) · excursion haute méd. +1.33% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.118% vs midi 0.904% vs clôture 1.113% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 57% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr -0.013)_ ; drift intra méd. -0.513% ; recovery-V 12%
- **σ réalisé intraday** 2.549% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 70% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 154.3315 (VA 153.7155–154.7165 ; dernier close 153.12)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 63% · **stop −3.81%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.28 (high win-rate)
- Gaps overnight (n=159) : méd. 0.45% · baisse 34% (gap-down >1% 19% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.56% (p90 −1.67%) · haut méd +0.45% · range méd 1.23%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.61% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.28%) · haut méd +0.67% · range méd 1.98%
- Excursion ouverture 60min (n=160) : bas méd −0.95% (p90 −2.6%) · haut méd +0.78% · range méd 2.15%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 153.12 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 71% (115/159) · gap 26% · délai 0.5min · rebond 54% (64/115) (MFE +1.12%)
   - −1.0% : fill 30min 42% · séance 65% (106/159) · gap 19% · délai 5.3min · rebond 64% (64/106) (MFE +1.45%)
   - −1.5% : fill 30min 33% · séance 60% (96/159) · gap 14% · délai 17.2min · rebond 64% (62/96) (MFE +1.58%)
   - −2.0% : fill 30min 20% · séance 44% (73/159) · gap 10% · délai 50.0min · rebond 63% (46/73) (MFE +1.47%)
   - −3.0% : fill 30min 13% · séance 28% (51/159) · gap 3% · délai 120.2min · rebond 58% (35/51) (MFE +1.41%)
   - −4.0% : fill 30min 5% · séance 19% (38/159) · gap 2% · délai 221.1min · rebond 63% (27/38) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 14% (24/159) · gap 0% · délai 350.7min · rebond 55% (15/24) (MFE +1.13%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.54% (p90 −1.72%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.95%) → stop au-delà de −0.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=534 jambes) : jambe baissière méd −1.07% (p90 −2.63%) · ~7.0 jambes/séance
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
      · −1.0% : fill 48% (40/86) · rebond 65% (25/40)
      · −2.0% : fill 32% (25/86) · rebond 74% (17/25)
      · −3.0% : fill 16% (15/86) · rebond 81% (12/15)
      · −4.0% : fill 7% (9/86) · rebond 69% (7/9)
      · −5.0% : fill 4% (4/86) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 76% si les 15 1res min sont vertes (76 cas) · 21% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 79% si début vert vs 24% si rouge (base 46% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 282min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **79%** · continue >prix actuel 52% ; creux résiduel méd -1.18% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.47% → **scale +1.55% / runner +2.47%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **24%** (continue à baisser 55%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.19%** (au-delà de la MAE q10 -4.19%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.12% .. +2.22%] · haut q95 +2.68% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.5% .. +2.34%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.65%] · haut q95 +3.03% · bas q05 -3.76%
   - 4h (n=160) : retour [-3.36% .. +2.67%] · haut q95 +3.74% · bas q05 -4.27%
   - 6h (n=160) : retour [-3.79% .. +3.51%] · haut q95 +4.35% · bas q05 -4.77%
   - session (n=160) : retour [-5.04% .. +4.33%] · haut q95 +5.4% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 1.3% / strong 4.4%) · base = 9 séances trend-up (n_eff 6.6)
- **ARMER** : fenêtre la + prédictive = **20 min** → P(reste trend-up à la clôture) **15%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.19% / p90 1.45%) · ~3.0 replis/séance, durée méd 78.78 min. P(nouveau plus-haut après repli) :
   - −0.5% → **99%** (reprise méd 55.57 min, n=25)
   - −1.0% → **100%** (reprise méd 80.0 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.19%) ; extension open→close méd +4.46% (q75 +6.49% / q95 +8.61%), MFE méd +5.07% / q90 +9.14%
   - Échelle scale-out : +5.07% (33%) / +6.83% (33%) / +9.14% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.14% : P(retournement après) 0% (mèche méd 0.54%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.37%)


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

- **RSI** : 46.5  _(neutre)_
- **ADX** : 12.8  _(pas de tendance nette)_
- **MACD** : hist -0.328  _(bearish_recent)_
- **BB** : %B 0.38 · largeur 19.0%
- **ATR** : 6.18 (40.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.259  _(distribution)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 55.9  _(transition)_
- **MA** : MA20 152.28 · MA50 155.67 · MA200 148.62  _(prix < MA20)_
- **Dist MA** : MA20 -2.3% · MA50 -4.5% · MA200 +0.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (847841 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# CEG

**Generated** : 2026-08-21T00:31:32.113244+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $272.92  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $272.92 (+0.8% vs entrée) · entrée $270.63 · stop $266.57 · T1 $275.90 · R/R 1.3  
> ↳ P(T1 av. stop) 25 % _(réel 5 s)_ · EV/risk -0.161 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 192 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.350 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $269.97–$271.30 (mid $270.63)
- Spot actuel : $272.92 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $266.57 (stop swing_plan-based (-5.71%))
- Targets : T1 $275.90 · R/R 1.3 | T2 $278.25 · R/R 1.88 | T3 $280.61 · R/R 2.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $266.57


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.00 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.71 %)** : le gap seul le franchit 0.435 % des séances (5 fois sur 1150).
   - exécution **2.18 pt plus bas** dans le cas TYPIQUE (médiane), 7.752 au p90, **10.114 au pire**
   - perte réelle **9.329 %** en moyenne _(tirée par la queue)_, jusqu'à **15.824 %** — au lieu des 5.71 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0157 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.823 % | p01 -4.438 % | pire -15.824 % _(sur 1150 séances)_
- **P(stop avant cible)** _(source : daily, 1151 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0579** [0.0302 ; 0.1002] _(largeur 7.0 pt, n_eff 173.1)_
   - swing : **0.4199** [0.3687 ; 0.4724] _(largeur 10.4 pt, n_eff 345.3)_
   - deep : **0.5074** [0.4548 ; 0.5599] _(largeur 10.5 pt, n_eff 345.3)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 19.9 observations effectives », dont la borne haute a 95 % vaut environ 15.0 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 21.0 observations effectives », dont la borne haute a 95 % vaut environ 14.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.8 pt), swing (41.4 pt), deep (35.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-4.5 %** | CVaR **-6.9 %** | vol 3.12 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 5.65 % contre 2.88 % aujourd'hui, rapport 1.96)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.64 % vs -9.6 % si l'on extrapolait par √5 _(rapport 1.004 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1867** (β de hausse 1.1932, asymétrie 0.9945) vs SPY — 528 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : cela veut dire que la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier n'est alors PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable.**
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.97 ATR (stop 4.898 %) — p(stop avant cible) 0.1709 [0.13 ; 0.21], R/R 0.113, perte reelle 7.568 % (gap inclus), EV -0.5868 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 82.9 % x 0.85 % + P(rien) 0.1 % x -2.94 % ne couvrent pas P(stop) 17.1 % x 7.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.4 ATR (stop 6.566 %) — p(stop avant cible) 0.1232 [0.09 ; 0.16], R/R 0.076, perte reelle 11.211 % (gap inclus), EV -0.6391 % — **REFUSE**
      - refuse : R/R 0.08 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 87.5 % x 0.85 % + P(rien) 0.1 % x -3.86 % ne couvrent pas P(stop) 12.3 % x 11.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 4.23 ATR (stop 17.516 %) — p(stop avant cible) 0.018 [0.01 ; 0.04], R/R 0.049, perte reelle 17.516 % (gap inclus), EV 0.1837 % — **REFUSE**
      - refuse : R/R 0.05 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.52 % > budget 12.0 %
      - ⚠ support DETECTE a 0.87 ATR du spot, sous le seuil de 1 ATR : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545] sur 940 touches) contre ~35 % au-dela. L'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : $0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 19 % | T3 7 %
- Kelly (position) : f* 0.023 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.3 | bear 7.1 | side 8.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 273.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.843% → cible +1.945% / stop −1.5%, p_fill 65%, n_eff≈27.5) : P(cible|rempli) **25%** · **EV/risk -0.161** (×p_fill ; si rempli -0.37% du capital)
  - **swing** (entrée dip −1.844% → cible +2.748% / stop −3.938%, p_fill 46%, n_eff≈19.9) : P(cible|rempli) **51%** · **EV/risk -0.076** (×p_fill ; si rempli -0.65% du capital)
  - **deep** (entrée dip −2.852% → cible +3.887% / stop −5.968%, p_fill 54%, n_eff≈21.0) : P(cible|rempli) **75%** · **EV/risk +0.112** (×p_fill ; si rempli +1.24% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→69% · +2.0%→39% · +3.0%→18% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.38% (p90 5.5%) · excursion haute méd. +1.48% / basse méd. −1.41%
- Profil de vol intra : ouverture 2.493% vs midi 0.671% vs clôture 0.79% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 48% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. -0.415% ; recovery-V 7%
- **σ réalisé intraday** 2.351% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 58% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 271.3474 (VA 270.6464–272.0484 ; dernier close 274.19)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 44% · **stop −2.3%** sous le fill (sous le bruit) · cible +0.96% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.45% · baisse 35% (gap-down >1% 15% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −1.87%) · haut méd +0.86% · range méd 1.71%
- Excursion ouverture 15min (n=160) : bas méd −0.66% (p90 −2.28%) · haut méd +1.02% · range méd 2.04%
- Excursion ouverture 30min (n=160) : bas méd −0.8% (p90 −3.03%) · haut méd +1.1% · range méd 2.27%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −3.19%) · haut méd +1.3% · range méd 2.65%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 274.19 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 50% · séance 66% (114/159) · gap 22% · délai 1.3min · rebond 46% (57/114) (MFE +0.94%)
   - −1.0% : fill 30min 42% · séance 56% (99/159) · gap 15% · délai 2.1min · rebond 49% (54/99) (MFE +0.97%)
   - −1.5% : fill 30min 32% · séance 42% (83/159) · gap 9% · délai 4.2min · rebond 45% (44/83) (MFE +0.79%)
   - −2.0% : fill 30min 24% · séance 37% (67/159) · gap 6% · délai 10.3min · rebond 54% (41/67) (MFE +1.07%)
   - −3.0% : fill 30min 9% · séance 24% (41/159) · gap 2% · délai 46.1min · rebond 44% (16/41) (MFE +0.96%)
   - −4.0% : fill 30min 5% · séance 13% (25/159) · gap 1% · délai 50.1min · rebond 53% (12/25) (MFE +0.97%)
   - −5.0% : fill 30min 2% · séance 6% (15/159) · gap 0% · délai 44.6min · rebond 75% (10/15) (MFE +1.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.32% (p90 −1.24%) → stop au-delà de −0.81% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.02%) → stop au-delà de −0.88% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.38%) → stop au-delà de −1.07% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=471 jambes) : jambe baissière méd −1.07% (p90 −2.64%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 96% (53/54) · rebond 52% (30/53)
      · −2.0% : fill 77% (41/54) · rebond 53% (26/41)
      · −3.0% : fill 55% (28/54) · rebond 38% (12/28)
      · −4.0% : fill 37% (19/54) · rebond 53% (9/19)
      · −5.0% : fill 18% (13/54) · rebond 76% (9/13)
   - **flat** (28 séances) :
      · −1.0% : fill 57% (16/28) · rebond 34% (5/16)
      · −2.0% : fill 29% (9/28) · rebond 48% (3/9)
      · −3.0% : fill 19% (7/28) · rebond 21% (1/7)
      · −4.0% : fill 9% (4/28) · rebond 20% (1/4)
      · −5.0% : fill 3% (2/28) · rebond 61% (1/2)
   - **gap-up** (77 séances) :
      · −1.0% : fill 35% (30/77) · rebond 51% (19/30)
      · −2.0% : fill 19% (17/77) · rebond 58% (12/17)
      · −3.0% : fill 9% (6/77) · rebond 76% (3/6)
      · −4.0% : fill 1% (2/77) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/77) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 65% si les 15 1res min sont vertes (92 cas) · 25% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:23** → P(séance verte=clôture>ouverture) 85% si début vert vs 8% si rouge (base 48% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 194min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **85%** · continue >prix actuel 46% ; creux résiduel méd -1.01% (q20 -1.86%) → **SL/trailing à −1.86%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.83% / q75 +1.44% → **scale +0.83% / runner +1.44%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **8%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.64%** (au-delà de la MAE q10 -2.64%), cible rebond +0.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.11% .. +2.3%] · haut q95 +2.64% · bas q05 -3.48%
   - 60min (n=160) : retour [-3.71% .. +2.58%] · haut q95 +3.3% · bas q05 -4.7%
   - 2h (n=160) : retour [-3.72% .. +2.91%] · haut q95 +4.06% · bas q05 -4.81%
   - 4h (n=160) : retour [-3.75% .. +3.35%] · haut q95 +4.16% · bas q05 -4.87%
   - 6h (n=160) : retour [-4.28% .. +3.2%] · haut q95 +4.48% · bas q05 -4.91%
   - session (n=160) : retour [-4.18% .. +3.3%] · haut q95 +4.55% · bas q05 -4.91%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 4.4% / strong 1.9%) · base = 10 séances trend-up (n_eff 6.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 13% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.05% (p75 1.33% / p90 1.45%) · ~1.45 replis/séance, durée méd 90.1 min. P(nouveau plus-haut après repli) :
   - −0.5% → **65%** (reprise méd 23.89 min, n=22)
   - −1.0% → **74%** (reprise méd 54.64 min, n=10)
- **RIDER — climb (trail + cibles)** : trail **−1.45%** (p90, défaut prudent ; serré/agressif −1.33%) ; extension open→close méd +3.33% (q75 +4.19% / q95 +6.07%), MFE méd +3.68% / q90 +5.35%
   - Échelle scale-out : +3.68% (33%) / +4.76% (33%) / +5.35% (34%)
- **DÉSARMER** : repli > **−1.45%** depuis le plus-haut = décay → P(retournement) **70%** (préavis méd 295.0 min, n=0) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +5.35% : P(retournement après) 0% (mèche méd 0.23%)
- **CONTEXTE** : la dernière heure tient les gains 93% du temps (retour médian dernière heure +0.39%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict buy_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 57.7  _(momentum haussier)_
- **ADX** : 18.2  _(pas de tendance nette)_
- **MACD** : hist 0.041  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 10.6%
- **ATR** : 10.55 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.346  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 65.4  _(marche en range (choppy))_
- **MA** : MA20 269.96 · MA50 262.13 · MA200 299.37  _(prix > MA20)_
- **Dist MA** : MA20 +1.1% · MA50 +4.1% · MA200 -8.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (598490 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

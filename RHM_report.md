# RHM

**Generated** : 2026-08-21T00:02:08.076295+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1160.40  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1160.40 (+1.2% vs entrée) · entrée €1146.21 · stop €1095.75 · T1 €1178.42 · R/R 0.64  
> ↳ P(T1 av. stop) 80 % _(réel 5 s)_ · EV/risk 0.214 _(réel 5 s)_ (GBM -0.016) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.150 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €1139.77–€1152.65 (mid €1146.21)
- Spot actuel : €1160.40 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €1095.75 (stop swing_plan-based (-5.57%))
- Targets : T1 €1178.42 · R/R 0.64 | T2 €1210.62 · R/R 1.28 | T3 €1242.83 · R/R 1.91
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1095.75


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.57 %)** : le gap seul le franchit 0.236 % des séances (3 fois sur 1273).
   - exécution **2.282 pt plus bas** dans le cas TYPIQUE (médiane), 13.944 au p90, **16.859 au pire**
   - perte réelle **12.114 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 5.57 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0154 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.747 % | pire -22.429 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0884** [0.0529 ; 0.1375] _(largeur 8.5 pt, n_eff 173.1)_
   - swing : **0.4064** [0.3556 ; 0.4588] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.5196** [0.467 ; 0.5719] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.3 pt), swing (29.0 pt), deep (31.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.86 %** | CVaR **-6.73 %** | vol 2.98 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 2.07 % contre 3.39 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.6 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.846 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5019** (β de hausse 0.5854, asymétrie 0.8573) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.23× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.016 | EV/share : €-0.808 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 34 % | T3 19 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 39.8 | bear 24.0 | side 36.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.551% → cible +1.257% / stop −2.0%, p_fill 82%, n_eff≈34.8) : P(cible|rempli) **61%** · **EV/risk +0.058** (×p_fill ; si rempli +0.14% du capital)
  - **swing** (entrée dip −1.222% → cible +2.81% / stop −4.402%, p_fill 64%, n_eff≈27.2) : P(cible|rempli) **80%** · **EV/risk +0.214** (×p_fill ; si rempli +1.46% du capital)
  - **deep** (entrée dip −1.887% → cible +3.974% / stop −6.648%, p_fill 63%, n_eff≈25.0) : P(cible|rempli) **78%** · **EV/risk +0.142** (×p_fill ; si rempli +1.49% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→72% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.17% (p90 6.98%) · excursion haute méd. +2.05% / basse méd. −1.58%
- Profil de vol intra : ouverture 2.661% vs midi 0.939% vs clôture 1.11% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.088 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.066% ; recovery-V 26%
- **σ réalisé intraday** 2.775% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 61% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 1181.57 (VA 1177.91–1204.75 ; dernier close 1180.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 17% · rebond 64% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.54 (high win-rate)
- Gaps overnight (n=159) : méd. 0.25% · baisse 32% (gap-down >1% 10% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −1.5%) · haut méd +0.57% · range méd 1.35%
- Excursion ouverture 15min (n=160) : bas méd −0.87% (p90 −1.95%) · haut méd +0.72% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −0.92% (p90 −2.22%) · haut méd +0.88% · range méd 2.01%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.45%) · haut méd +1.01% · range méd 2.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1180.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 70% (117/159) · gap 22% · délai 0.4min · rebond 56% (62/117) (MFE +1.19%)
   - −1.0% : fill 30min 37% · séance 63% (107/159) · gap 10% · délai 8.7min · rebond 62% (62/107) (MFE +1.3%)
   - −1.5% : fill 30min 25% · séance 52% (86/159) · gap 6% · délai 41.2min · rebond 60% (48/86) (MFE +1.36%)
   - −2.0% : fill 30min 18% · séance 40% (73/159) · gap 5% · délai 34.7min · rebond 64% (45/73) (MFE +1.45%)
   - −3.0% : fill 30min 9% · séance 25% (46/159) · gap 4% · délai 120.4min · rebond 58% (27/46) (MFE +1.31%)
   - −4.0% : fill 30min 4% · séance 17% (28/159) · gap 1% · délai 245.4min · rebond 64% (16/28) (MFE +1.5%)
   - −5.0% : fill 30min 1% · séance 9% (16/159) · gap 1% · délai 293.4min · rebond 56% (8/16) (MFE +1.7%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.56% (p90 −1.61%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.44% (p90 −1.75%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.28% (p90 −1.77%) → stop au-delà de −1.25% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=530 jambes) : jambe baissière méd −1.07% (p90 −2.5%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 94% (46/48) · rebond 65% (27/46)
      · −2.0% : fill 80% (38/48) · rebond 66% (25/38)
      · −3.0% : fill 53% (26/48) · rebond 63% (16/26)
      · −4.0% : fill 41% (16/48) · rebond 75% (11/16)
      · −5.0% : fill 22% (9/48) · rebond 83% (7/9)
   - **flat** (47 séances) :
      · −1.0% : fill 64% (33/47) · rebond 72% (21/33)
      · −2.0% : fill 25% (17/47) · rebond 72% (10/17)
      · −3.0% : fill 17% (10/47) · rebond 55% (5/10)
      · −4.0% : fill 15% (8/47) · rebond 36% (2/8)
      · −5.0% : fill 10% (6/47) · rebond 22% (1/6)
   - **gap-up** (64 séances) :
      · −1.0% : fill 46% (28/64) · rebond 52% (14/28)
      · −2.0% : fill 27% (18/64) · rebond 58% (10/18)
      · −3.0% : fill 15% (10/64) · rebond 49% (6/10)
      · −4.0% : fill 6% (4/64) · rebond 61% (3/4)
      · −5.0% : fill 2% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 62% si les 15 1res min sont vertes (79 cas) · 36% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:37** → P(séance verte=clôture>ouverture) 73% si début vert vs 21% si rouge (base 48% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **73%** · continue >prix actuel 44% ; creux résiduel méd -1.19% (q20 -2.72%) → **SL/trailing à −2.72%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.78% / q75 +1.81% → **scale +0.78% / runner +1.81%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **21%** (continue à baisser 56%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.79%** (au-delà de la MAE q10 -3.79%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.62% .. +3.28%] · haut q95 +3.78% · bas q05 -3.15%
   - 60min (n=160) : retour [-2.79% .. +3.22%] · haut q95 +4.45% · bas q05 -3.95%
   - 2h (n=160) : retour [-3.23% .. +3.08%] · haut q95 +4.45% · bas q05 -4.52%
   - 4h (n=160) : retour [-3.48% .. +3.35%] · haut q95 +4.87% · bas q05 -4.64%
   - 6h (n=160) : retour [-4.2% .. +3.34%] · haut q95 +4.97% · bas q05 -5.07%
   - session (n=160) : retour [-5.54% .. +4.13%] · haut q95 +5.08% · bas q05 -6.03%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 54.1  _(neutre)_
- **ADX** : 23.0  _(pas de tendance nette)_
- **MACD** : hist 2.256  _(pas de croisement recent)_
- **BB** : %B 0.56 · largeur 20.0%
- **ATR** : 50.46 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.148  _(distribution)_
- **Vol ratio** : 0.27  _(volume atone)_
- **Choppiness** : 68.0  _(marche en range (choppy))_
- **MA** : MA20 1147.65 · MA50 1096.58 · MA200 1423.56  _(prix > MA20)_
- **Dist MA** : MA20 +1.1% · MA50 +5.8% · MA200 -18.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (577863 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# ENR

**Generated** : 2026-08-20T19:49:26.554403+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €152.58  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €152.58 (+0.5% vs entrée) · entrée €151.78 · stop €143.34 · T1 €168.66 · R/R 2.0  
> ↳ P(T1 av. stop) 9 % _(réel 5 s)_ · EV/risk -0.147 _(réel 5 s)_ (GBM 0.032) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.240 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €150.98–€152.58 (mid €151.78)
- Spot actuel : €152.58 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €143.34 (stop swing_plan-based (-6.06%))
- Targets : T1 €168.66 · R/R 2.0 | T2 €168.73 · R/R 2.01 | T3 €168.80 · R/R 2.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €143.34


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.51 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.06 %)** : le gap seul le franchit 0.628 % des séances ; quand il le franchit, l'exécution est **6.549 points plus bas** → perte réelle **12.609 %** _(et non 6.06 %)_
- Chocs d'ouverture : p05 -2.307 % | p01 -5.092 % | pire -35.757 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1009** [0.0626 ; 0.1524] _(largeur 9.0 pt, n_eff 173.1)_
   - swing : **0.4105** [0.3596 ; 0.4629] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.4839** [0.4315 ; 0.5365] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.6 pt), swing (32.0 pt), deep (30.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-4.63 %** | CVaR **-6.6 %** | vol 3.22 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 6.20 % contre 3.42 % aujourd'hui, rapport 1.81)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.74 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.37** (β de hausse 1.0874, asymétrie 1.2599) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.441× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : €0.271 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 8.4 | bear 5.9 | side 85.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 305.0 (= 2 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.315% → cible +1.672% / stop −1.5%, p_fill 86%, n_eff≈35.9) : P(cible|rempli) **39%** · **EV/risk -0.113** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −0.528% → cible +11.122% / stop −5.561%, p_fill 80%, n_eff≈35.1) : P(cible|rempli) **9%** · **EV/risk -0.147** (×p_fill ; si rempli -1.03% du capital)
  - **deep** (entrée dip −0.758% → cible +5.286% / stop −6.411%, p_fill 95%, n_eff≈37.4) : P(cible|rempli) **43%** · **EV/risk -0.236** (×p_fill ; si rempli -1.59% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→61% · +2.0%→42% · +3.0%→24% · +5.0%→8% · +8.0%→1%
- Range intraday médian 4.01% (p90 6.15%) · excursion haute méd. +1.54% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.125% vs midi 0.908% vs clôture 1.121% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓0% ; spike-down 57% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr -0.02)_ ; drift intra méd. -0.426% ; recovery-V 12%
- **σ réalisé intraday** 2.618% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 67% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 154.2903 (VA 153.5577–155.1693 ; dernier close 154.74)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 63% · **stop −3.81%** sous le fill (sous le bruit) · cible +1.06% · R/R 0.28 (high win-rate)
- Gaps overnight (n=159) : méd. 0.4% · baisse 35% (gap-down >1% 20% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.55% (p90 −1.67%) · haut méd +0.48% · range méd 1.3%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.67% · range méd 1.62%
- Excursion ouverture 30min (n=160) : bas méd −0.85% (p90 −2.28%) · haut méd +0.67% · range méd 1.99%
- Excursion ouverture 60min (n=160) : bas méd −0.95% (p90 −2.65%) · haut méd +0.78% · range méd 2.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 154.74 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 70% (114/159) · gap 27% · délai 0.4min · rebond 56% (65/114) (MFE +1.22%)
   - −1.0% : fill 30min 43% · séance 65% (105/159) · gap 20% · délai 3.8min · rebond 66% (64/105) (MFE +1.57%)
   - −1.5% : fill 30min 34% · séance 60% (95/159) · gap 15% · délai 15.8min · rebond 66% (62/95) (MFE +1.76%)
   - −2.0% : fill 30min 21% · séance 44% (72/159) · gap 10% · délai 41.2min · rebond 62% (45/72) (MFE +1.49%)
   - −3.0% : fill 30min 13% · séance 29% (51/159) · gap 3% · délai 120.2min · rebond 58% (35/51) (MFE +1.41%)
   - −4.0% : fill 30min 6% · séance 19% (38/159) · gap 2% · délai 221.1min · rebond 63% (27/38) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 15% (24/159) · gap 0% · délai 350.7min · rebond 55% (15/24) (MFE +1.13%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −1.78%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.95%) → stop au-delà de −0.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.42% (p90 −0.97%) → stop au-delà de −0.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=536 jambes) : jambe baissière méd −1.07% (p90 −2.64%) · ~7.0 jambes/séance
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
      · −1.0% : fill 47% (39/86) · rebond 70% (25/39)
      · −2.0% : fill 30% (24/86) · rebond 71% (16/24)
      · −3.0% : fill 17% (15/86) · rebond 81% (12/15)
      · −4.0% : fill 7% (9/86) · rebond 69% (7/9)
      · −5.0% : fill 4% (4/86) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 76% si les 15 1res min sont vertes (77 cas) · 22% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:24** → P(séance verte=clôture>ouverture) 83% si début vert vs 24% si rouge (base 48% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 282min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=73) : tient le vert **83%** · continue >prix actuel 55% ; creux résiduel méd -1.27% (q20 -2.02%) → **SL/trailing à −2.02%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +2.55% → **scale +1.78% / runner +2.55%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **24%** (continue à baisser 54%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.22%** (au-delà de la MAE q10 -4.22%), cible rebond +1.45% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.14% .. +2.24%] · haut q95 +2.68% · bas q05 -2.63%
   - 60min (n=160) : retour [-2.51% .. +2.34%] · haut q95 +2.72% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.85% .. +2.66%] · haut q95 +3.06% · bas q05 -3.81%
   - 4h (n=160) : retour [-3.42% .. +2.68%] · haut q95 +3.76% · bas q05 -4.32%
   - 6h (n=160) : retour [-3.84% .. +3.54%] · haut q95 +4.44% · bas q05 -4.85%
   - session (n=160) : retour [-5.1% .. +4.34%] · haut q95 +5.43% · bas q05 -6.21%


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
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 61.0  _(momentum haussier)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist 0.428  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 18.9%
- **ATR** : 6.47 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.237  _(distribution)_
- **Vol ratio** : 0.48  _(volume atone)_
- **Choppiness** : 53.5  _(transition)_
- **MA** : MA20 152.31 · MA50 155.81 · MA200 148.0  _(prix > MA20)_
- **Dist MA** : MA20 +0.2% · MA50 -2.1% · MA200 +3.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (416989 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

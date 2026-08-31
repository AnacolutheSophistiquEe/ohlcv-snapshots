# 000660

**Generated** : 2026-08-31T21:49:53.133475+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1645000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1645000.00 (+10.0% vs entrée) · entrée ₩1495236.32 · stop ₩1339781.04 · T1 ₩1806146.88 · R/R 2.0  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.142 _(réel 5 s)_ (GBM 0.343) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

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
- Entry (zone de repli) : ₩1474098.35–₩1516374.29 (mid ₩1495236.32)
- Spot actuel : ₩1645000.00 (+10.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1339781.04 (stop swing_plan-based (-18.55%))
- Targets : T1 ₩1806146.88 · R/R 2.0 | T2 ₩1808745.97 · R/R 2.02 | T3 ₩1811345.06 · R/R 2.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1339781.04


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.24 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (18.55 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 18.55 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.356 % | p01 -6.997 % | pire -10.86 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0673** [0.037 ; 0.1119] _(largeur 7.5 pt, n_eff 173.1)_
   - swing : **0.2327** [0.1905 ; 0.2794] _(largeur 8.9 pt, n_eff 345.6)_
   - deep : **0.2674** [0.2228 ; 0.3159] _(largeur 9.3 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.4 observations effectives », dont la borne haute a 95 % vaut environ 20.8 %.
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.1 observations effectives », dont la borne haute a 95 % vaut environ 21.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.3 pt), swing (47.4 pt), deep (46.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.71 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.38 % contre 7.01 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.38 % si l'on extrapolait par √5 _(rapport 0.905 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4107** (β de hausse 1.6107, asymétrie 0.8758) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.343 | EV/share : ₩53387.567 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 16 % | T3 15 %
- Kelly (position) : f* 0.016 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.6 | bear 8.5 | side 71.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.141% → cible +6.958% / stop −8.0%, p_fill 42%, n_eff≈23.3) : P(cible|rempli) **9%** · **EV/risk -0.012** (×p_fill ; si rempli -0.23% du capital)
  - **swing** (entrée dip −9.099% → cible +20.793% / stop −10.397%, p_fill 35%, n_eff≈14.4) : P(cible|rempli) **0%** · **EV/risk -0.142** (×p_fill ; si rempli -4.27% du capital)
  - **deep** (entrée dip −14.069% → cible +9.966% / stop −12.744%, p_fill 31%, n_eff≈14.1) : P(cible|rempli) **61%** · **EV/risk +0.030** (×p_fill ; si rempli +1.20% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→78% · +2.0%→54% · +3.0%→44% · +5.0%→29% · +8.0%→11%
- Range intraday médian 7.29% (p90 11.62%) · excursion haute méd. +2.16% / basse méd. −3.64%
- Profil de vol intra : ouverture 3.445% vs midi 1.492% vs clôture 1.701% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑2%/↓0% ; spike-down 73% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr -0.024)_ ; drift intra méd. -1.239% ; recovery-V 27%
- **σ réalisé intraday** 4.485% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 68% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 1709512.5 (VA 1682062.5–1714087.5 ; dernier close 1663000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 70% · **stop −7.66%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.29 (high win-rate)
- Gaps overnight (n=159) : méd. 0.65% · baisse 44% (gap-down >1% 37% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.04%) · haut méd +0.79% · range méd 1.74%
- Excursion ouverture 15min (n=160) : bas méd −1.05% (p90 −2.72%) · haut méd +0.96% · range méd 2.39%
- Excursion ouverture 30min (n=160) : bas méd −1.51% (p90 −3.61%) · haut méd +1.23% · range méd 2.98%
- Excursion ouverture 60min (n=160) : bas méd −1.79% (p90 −4.86%) · haut méd +1.4% · range méd 3.75%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1653000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 65% (98/159) · gap 43% · délai 0.0min · rebond 59% (55/98) (MFE +1.31%)
   - −1.0% : fill 30min 52% · séance 61% (90/159) · gap 37% · délai 0.0min · rebond 63% (58/90) (MFE +1.62%)
   - −1.5% : fill 30min 43% · séance 56% (80/159) · gap 29% · délai 0.0min · rebond 69% (53/80) (MFE +1.78%)
   - −2.0% : fill 30min 38% · séance 51% (74/159) · gap 26% · délai 0.0min · rebond 66% (49/74) (MFE +1.78%)
   - −3.0% : fill 30min 33% · séance 46% (63/159) · gap 19% · délai 1.9min · rebond 68% (42/63) (MFE +2.14%)
   - −4.0% : fill 30min 27% · séance 38% (52/159) · gap 15% · délai 2.4min · rebond 69% (39/52) (MFE +2.36%)
   - −5.0% : fill 30min 18% · séance 33% (42/159) · gap 9% · délai 15.0min · rebond 70% (29/42) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.55%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.69% (p90 −2.95%) → stop au-delà de −2.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.53%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=877 jambes) : jambe baissière méd −1.26% (p90 −3.43%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 96% (62/64) · rebond 56% (34/62)
      · −2.0% : fill 85% (55/64) · rebond 59% (32/55)
      · −3.0% : fill 81% (49/64) · rebond 62% (30/49)
      · −4.0% : fill 68% (43/64) · rebond 66% (31/43)
      · −5.0% : fill 62% (36/64) · rebond 63% (23/36)
   - **flat** (11 séances) :
      · −1.0% : fill 89% (9/11) · rebond 96% (8/9)
      · −2.0% : fill 38% (4/11) · rebond 100% (4/4)
      · −3.0% : fill 28% (3/11) · rebond 100% (3/3)
      · −4.0% : fill 0% (0/11) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/11) · rebond 0% (0/0)
   - **gap-up** (84 séances) :
      · −1.0% : fill 32% (19/84) · rebond 76% (16/19)
      · −2.0% : fill 24% (15/84) · rebond 82% (13/15)
      · −3.0% : fill 20% (11/84) · rebond 84% (9/11)
      · −4.0% : fill 15% (9/84) · rebond 82% (8/9)
      · −5.0% : fill 12% (6/84) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 53% si les 15 1res min sont vertes (82 cas) · 32% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 76% si début vert vs 13% si rouge (base 42% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **76%** · continue >prix actuel 51% ; creux résiduel méd -1.57% (q20 -4.3%) → **SL/trailing à −4.3%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.66% / q75 +3.73% → **scale +1.66% / runner +3.73%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **13%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.41%** (au-delà de la MAE q10 -6.41%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.34% .. +2.69%] · haut q95 +3.57% · bas q05 -4.52%
   - 60min (n=160) : retour [-3.63% .. +4.64%] · haut q95 +5.83% · bas q05 -5.49%
   - 2h (n=160) : retour [-4.99% .. +4.85%] · haut q95 +7.58% · bas q05 -7.26%
   - 4h (n=160) : retour [-6.72% .. +5.74%] · haut q95 +7.98% · bas q05 -8.2%
   - 6h (n=160) : retour [-6.95% .. +6.74%] · haut q95 +8.48% · bas q05 -8.72%
   - session (n=160) : retour [-7.13% .. +7.01%] · haut q95 +8.48% · bas q05 -8.72%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 14% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 63.5  _(momentum haussier)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist 31161.584  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 25.9%
- **ATR** : 120092.57 (69.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.271  _(distribution)_
- **Vol ratio** : 0.42  _(volume atone)_
- **Choppiness** : 52.7  _(transition)_
- **MA** : MA20 1597889.29 · MA50 1928516.13 · MA200 1284612.58  _(prix > MA20)_
- **Dist MA** : MA20 +2.9% · MA50 -14.7% · MA200 +28.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (512036 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

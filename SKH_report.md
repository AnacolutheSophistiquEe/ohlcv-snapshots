# 000660

**Generated** : 2026-09-21T21:56:43.522551+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1868000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1868000.00 (+0.4% vs entrée) · entrée ₩1861207.31 · stop ₩1712310.72 · T1 ₩1897271.95 · R/R 0.24  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.117 _(réel 5 s)_ (GBM -0.081) · ¼-Kelly 0.062 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1854414.61–₩1868000.00 (mid ₩1861207.31)
- Spot actuel : ₩1868000.00 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : ₩1712310.72 (stop swing_plan-based (-5.48%))
- Targets : T1 ₩1897271.95 · R/R 0.24 | T2 ₩1933336.59 · R/R 0.48 | T3 ₩1969401.23 · R/R 0.73
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1712310.72


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.48 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.48 %)** : le gap seul le franchit 1.559 % des séances (19 fois sur 1219).
   - exécution **2.314 pt plus bas** dans le cas TYPIQUE (médiane), 4.544 au p90, **5.38 au pire**
   - perte réelle **7.903 %** en moyenne _(tirée par la queue)_, jusqu'à **10.86 %** — au lieu des 5.48 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0378 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.444 % | p01 -6.994 % | pire -10.86 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0441** [0.0207 ; 0.0826] _(largeur 6.2 pt, n_eff 173.1)_
   - swing : **0.3955** [0.345 ; 0.4477] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.347** [0.2983 ; 0.3983] _(largeur 10.0 pt, n_eff 345.6)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 36.3 observations effectives », dont la borne haute a 95 % vaut environ 8.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.5 pt), swing (31.0 pt), deep (31.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-8.77 %** | CVaR **-11.36 %** | vol 5.75 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.19 % contre 6.82 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.4 % vs -10.58 % si l'on extrapolait par √5 _(rapport 0.888 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4126** (β de hausse 1.6188, asymétrie 0.8726) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.081 | EV/share : ₩-12084.337 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 33 % | T3 25 %
- Kelly (position) : f* 0.248 | ¼-Kelly 0.062 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.5 | bear 6.8 | side 7.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.359% → cible +1.938% / stop −8.0%, p_fill 91%, n_eff≈38.7) : P(cible|rempli) **48%** · **EV/risk -0.117** (×p_fill ; si rempli -1.03% du capital)
  - **swing** (entrée dip −0.807% → cible +4.333% / stop −4.711%, p_fill 89%, n_eff≈36.9) : P(cible|rempli) **43%** · **EV/risk -0.202** (×p_fill ; si rempli -1.07% du capital)
  - **deep** (entrée dip −1.181% → cible +6.128% / stop −7.093%, p_fill 92%, n_eff≈36.3) : P(cible|rempli) **41%** · **EV/risk -0.274** (×p_fill ; si rempli -2.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→54% · +3.0%→42% · +5.0%→25% · +8.0%→10%
- Range intraday médian 7.08% (p90 11.5%) · excursion haute méd. +2.16% / basse méd. −3.64%
- Profil de vol intra : ouverture 3.423% vs midi 1.481% vs clôture 1.675% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑1%/↓0% ; spike-down 69% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.838% ; recovery-V 28%
- **σ réalisé intraday** 4.074% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 62% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1643750.0 (VA 1628750.0–1654250.0 ; dernier close 1649000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 70% · **stop −7.66%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.29 (high win-rate)
- Gaps overnight (n=159) : méd. 0.61% · baisse 46% (gap-down >1% 37% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −0.74% (p90 −1.99%) · haut méd +0.75% · range méd 1.6%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.67%) · haut méd +0.95% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.34% (p90 −3.52%) · haut méd +1.26% · range méd 2.93%
- Excursion ouverture 60min (n=160) : bas méd −1.68% (p90 −4.69%) · haut méd +1.51% · range méd 3.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1647000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 66% (98/159) · gap 43% · délai 0.0min · rebond 58% (54/98) (MFE +1.23%)
   - −1.0% : fill 30min 52% · séance 63% (91/159) · gap 37% · délai 0.0min · rebond 62% (58/91) (MFE +1.62%)
   - −1.5% : fill 30min 42% · séance 56% (81/159) · gap 30% · délai 0.0min · rebond 69% (54/81) (MFE +1.67%)
   - −2.0% : fill 30min 38% · séance 52% (76/159) · gap 27% · délai 0.0min · rebond 66% (50/76) (MFE +1.82%)
   - −3.0% : fill 30min 34% · séance 48% (65/159) · gap 21% · délai 1.8min · rebond 71% (44/65) (MFE +2.29%)
   - −4.0% : fill 30min 26% · séance 38% (54/159) · gap 14% · délai 2.4min · rebond 67% (40/54) (MFE +2.35%)
   - −5.0% : fill 30min 16% · séance 30% (42/159) · gap 8% · délai 15.0min · rebond 70% (29/42) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.52% (p90 −2.51%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.73%) → stop au-delà de −2.29% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.29%) → stop au-delà de −2.34% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=866 jambes) : jambe baissière méd −1.25% (p90 −3.4%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 96% (64/66) · rebond 57% (35/64)
      · −2.0% : fill 83% (57/66) · rebond 58% (33/57)
      · −3.0% : fill 80% (51/66) · rebond 66% (32/51)
      · −4.0% : fill 68% (45/66) · rebond 64% (32/45)
      · −5.0% : fill 55% (36/66) · rebond 63% (23/36)
   - **flat** (8 séances) :
      · −1.0% : fill 91% (7/8) · rebond 100% (7/7)
      · −2.0% : fill 38% (3/8) · rebond 100% (3/3)
      · −3.0% : fill 27% (2/8) · rebond 100% (2/2)
      · −4.0% : fill 0% (0/8) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/8) · rebond 0% (0/0)
   - **gap-up** (85 séances) :
      · −1.0% : fill 33% (20/85) · rebond 68% (16/20)
      · −2.0% : fill 26% (16/85) · rebond 85% (14/16)
      · −3.0% : fill 22% (12/85) · rebond 86% (10/12)
      · −4.0% : fill 14% (9/85) · rebond 82% (8/9)
      · −5.0% : fill 11% (6/85) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 54% si les 15 1res min sont vertes (83 cas) · 33% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 78% si début vert vs 12% si rouge (base 44% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **78%** · continue >prix actuel 56% ; creux résiduel méd -1.45% (q20 -3.68%) → **SL/trailing à −3.68%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.69% → **scale +1.72% / runner +3.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **12%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.28%** (au-delà de la MAE q10 -6.28%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.27% .. +2.58%] · haut q95 +3.42% · bas q05 -4.49%
   - 60min (n=160) : retour [-3.6% .. +4.48%] · haut q95 +5.79% · bas q05 -5.42%
   - 2h (n=160) : retour [-4.9% .. +4.73%] · haut q95 +7.27% · bas q05 -7.18%
   - 4h (n=160) : retour [-6.67% .. +5.68%] · haut q95 +7.88% · bas q05 -8.12%
   - 6h (n=160) : retour [-6.85% .. +6.46%] · haut q95 +8.45% · bas q05 -8.59%
   - session (n=160) : retour [-7.12% .. +6.75%] · haut q95 +8.45% · bas q05 -8.59%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **22%**. Lecture précoce 30 min : signature présente → 11% vs absente 1% (base 6%)
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

- **RSI** : 62.0  _(momentum haussier)_
- **ADX** : 10.6  _(pas de tendance nette)_
- **MACD** : hist 16852.32  _(pas de croisement recent)_
- **BB** : %B 0.89 · largeur 19.6%
- **ATR** : 87285.71 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.08  _(accumulation)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 49.4  _(transition)_
- **MA** : MA20 1734194.77 · MA50 1700399.62 · MA200 1373293.67  _(prix > MA20)_
- **Dist MA** : MA20 +7.7% · MA50 +9.9% · MA200 +36.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (542480 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

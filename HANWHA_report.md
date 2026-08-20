# 012450

**Generated** : 2026-08-20T21:55:27.559302+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1167000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1167000.00 (+5.0% vs entrée) · entrée ₩1111609.60 · stop ₩1022680.83 · T1 ₩1191116.67 · R/R 0.89  
> ↳ P(T1 av. stop) 0 % _(réel 5 s)_ · EV/risk -0.043 _(réel 5 s)_ (GBM -0.115) · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 18.1 < 20 (tendance pas encore confirmée) alors que Choppiness 35.9 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._
- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 79.7 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1105682.96–₩1117536.24 (mid ₩1111609.60)
- Spot actuel : ₩1167000.00 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1022680.83 (stop swing_plan-based (-16.58%))
- Targets : T1 ₩1191116.67 · R/R 0.89 | T2 ₩1195678.25 · R/R 0.95 | T3 ₩1200239.83 · R/R 1.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1022680.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (16.58 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 16.58 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.758 % | p01 -3.827 % | pire -13.219 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2419** [0.1827 ; 0.3096] _(largeur 12.7 pt, n_eff 173.1)_
   - swing : **0.4787** [0.4264 ; 0.5314] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.527** [0.4743 ; 0.5792] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_target_first, p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 13.8 observations effectives », dont la borne haute a 95 % vaut environ 21.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (16.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-5.51 %** | CVaR **-7.48 %** | vol 3.89 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.67 % contre 4.47 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.29 % vs -11.94 % si l'on extrapolait par √5 _(rapport 0.862 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5263** (β de hausse 0.306, asymétrie 1.7202) vs KS11 — 553 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.312× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.115 | EV/share : ₩-10193.460 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 19 % | T3 19 %
- Kelly (position) : f* 0.093 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 38.3 | bear 56.2 | side 5.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.75% → cible +7.152% / stop −8.0%, p_fill 29%, n_eff≈13.8) : P(cible|rempli) **0%** · **EV/risk -0.043** (×p_fill ; si rempli -1.16% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=6))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→66% · +2.0%→48% · +3.0%→31% · +5.0%→19% · +8.0%→4%
- Range intraday médian 6.39% (p90 9.56%) · excursion haute méd. +1.92% / basse méd. −2.94%
- Profil de vol intra : ouverture 4.532% vs midi 1.255% vs clôture 1.303% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -0.274% ; recovery-V 36%
- **σ réalisé intraday** 4.561% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 45% / whipsaw 10%
- POC intraday (dernière séance, temps-au-prix) : 1168187.5 (VA 1160912.5–1190012.5 ; dernier close 1179000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 32% · rebond 78% · **stop −5.03%** sous le fill (sous le bruit) · cible +2.07% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.61% · baisse 33% (gap-down >1% 19% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −1.53% (p90 −4.05%) · haut méd +0.98% · range méd 2.92%
- Excursion ouverture 15min (n=160) : bas méd −1.97% (p90 −5.04%) · haut méd +1.28% · range méd 3.66%
- Excursion ouverture 30min (n=160) : bas méd −2.1% (p90 −5.73%) · haut méd +1.29% · range méd 4.1%
- Excursion ouverture 60min (n=160) : bas méd −2.17% (p90 −5.86%) · haut méd +1.59% · range méd 4.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1179000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 69% (112/159) · gap 21% · délai 0.1min · rebond 52% (57/112) (MFE +1.09%)
   - −1.0% : fill 30min 55% · séance 65% (107/159) · gap 19% · délai 0.8min · rebond 57% (63/107) (MFE +1.01%)
   - −1.5% : fill 30min 49% · séance 58% (98/159) · gap 12% · délai 1.3min · rebond 59% (56/98) (MFE +1.26%)
   - −2.0% : fill 30min 42% · séance 52% (81/159) · gap 10% · délai 3.5min · rebond 65% (50/81) (MFE +1.58%)
   - −3.0% : fill 30min 29% · séance 42% (60/159) · gap 4% · délai 4.3min · rebond 75% (42/60) (MFE +1.83%)
   - −4.0% : fill 30min 18% · séance 32% (46/159) · gap 2% · délai 21.8min · rebond 78% (37/46) (MFE +2.07%)
   - −5.0% : fill 30min 11% · séance 22% (33/159) · gap 1% · délai 26.0min · rebond 80% (27/33) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.54% (p90 −2.4%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.64% (p90 −2.79%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.72% (p90 −2.83%) → stop au-delà de −2.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=785 jambes) : jambe baissière méd −1.21% (p90 −3.23%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (37 séances) :
      · −1.0% : fill 88% (35/37) · rebond 50% (16/35)
      · −2.0% : fill 83% (32/37) · rebond 64% (19/32)
      · −3.0% : fill 80% (29/37) · rebond 79% (21/29)
      · −4.0% : fill 64% (25/37) · rebond 90% (21/25)
      · −5.0% : fill 37% (16/37) · rebond 88% (14/16)
   - **flat** (20 séances) :
      · −1.0% : fill 90% (19/20) · rebond 49% (10/19)
      · −2.0% : fill 69% (15/20) · rebond 48% (7/15)
      · −3.0% : fill 53% (9/20) · rebond 37% (3/9)
      · −4.0% : fill 53% (9/20) · rebond 48% (5/9)
      · −5.0% : fill 51% (8/20) · rebond 52% (4/8)
   - **gap-up** (102 séances) :
      · −1.0% : fill 50% (53/102) · rebond 66% (37/53)
      · −2.0% : fill 34% (34/102) · rebond 74% (24/34)
      · −3.0% : fill 23% (22/102) · rebond 87% (18/22)
      · −4.0% : fill 14% (12/102) · rebond 80% (11/12)
      · −5.0% : fill 10% (9/102) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 76% si les 15 1res min sont vertes (57 cas) · 20% si rouges (103 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 87% si début vert vs 9% si rouge (base 43% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=57) : tient le vert **87%** · continue >prix actuel 55% ; creux résiduel méd -1.59% (q20 -3.2%) → **SL/trailing à −3.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.72% / q75 +4.3% → **scale +2.72% / runner +4.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=103) : edge inversé — récupère vert seulement **9%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.83%** (au-delà de la MAE q10 -5.83%), cible rebond +1.88% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.7% .. +3.88%] · haut q95 +5.48% · bas q05 -7.08%
   - 60min (n=160) : retour [-5.14% .. +4.75%] · haut q95 +6.81% · bas q05 -7.32%
   - 2h (n=160) : retour [-6.87% .. +6.13%] · haut q95 +7.2% · bas q05 -8.42%
   - 4h (n=160) : retour [-7.38% .. +5.91%] · haut q95 +7.85% · bas q05 -8.87%
   - 6h (n=160) : retour [-6.81% .. +6.44%] · haut q95 +8.48% · bas q05 -9.13%
   - session (n=160) : retour [-6.94% .. +6.38%] · haut q95 +8.48% · bas q05 -9.13%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.56%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 79.7  _(surachat)_
- **ADX** : 18.1  _(pas de tendance nette)_
- **MACD** : hist 21874.274  _(pas de croisement recent)_
- **BB** : %B 0.78 · largeur 47.6%
- **ATR** : 71642.86 (54.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.045  _(neutre)_
- **Vol ratio** : 1.09  _(volume normal)_
- **Choppiness** : 35.9  _(marche directionnel)_
- **MA** : MA20 1031250.0 · MA50 1038120.0 · MA200 1146635.31  _(prix > MA20)_
- **Dist MA** : MA20 +13.2% · MA50 +12.4% · MA200 +1.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (570954 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

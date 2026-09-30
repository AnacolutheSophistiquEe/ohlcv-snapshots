# 326030

**Generated** : 2026-09-30T00:24:10.078549+00:00  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩74900.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩74900.00 (+3.2% vs entrée) · entrée ₩72542.86 · stop ₩71817.43 · T1 ₩73165.83 · R/R 0.86  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -28 % hors [0,100] (R² max 0.16). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 17.8 < 20 (tendance pas encore confirmée) alors que Choppiness 37.1 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩72418.26–₩72667.45 (mid ₩72542.86)
- Spot actuel : ₩74900.00 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : ₩71817.43 (plancher anti-bruit (R/R<2) ; -1.00 % depuis l'entree)
- Targets : T1 ₩73165.83 · R/R 0.86 | T2 ₩73788.80 · R/R 1.72 | T3 ₩74411.77 · R/R 2.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩71817.43


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.07 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.44 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 9.44 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.578 % | p01 -3.015 % | pire -5.539 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5393** [0.4649 ; 0.6124] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4092** [0.3583 ; 0.4616] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.3813** [0.3313 ; 0.4333] _(largeur 10.2 pt, n_eff 345.6)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.5 observations effectives », dont la borne haute a 95 % vaut environ 20.7 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.2 pt), swing (41.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.18 %** | CVaR **-6.25 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.79 % contre 3.01 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.18 % vs -8.8 % si l'on extrapolait par √5 _(rapport 0.93 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6039** (β de hausse 0.4331, asymétrie 1.3944) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 78.2 | side 16.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.152% → cible +0.859% / stop −1.0%, p_fill 27%, n_eff≈29.8) : P(cible|rempli) **57%** · **EV/risk +0.020** (×p_fill ; si rempli +0.07% du capital)
  - **swing** (entrée dip −6.293% → cible +1.92% / stop −3.358%, p_fill 12%, n_eff≈14.5) : P(cible|rempli) **75%** · **EV/risk +0.018** (×p_fill ; si rempli +0.47% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→40% · +3.0%→24% · +5.0%→8% · +8.0%→4%
- Range intraday médian 4.08% (p90 7.06%) · excursion haute méd. +1.43% / basse méd. −2.11%
- Profil de vol intra : ouverture 2.635% vs midi 0.814% vs clôture 0.828% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 9% · trend ↑1%/↓1% ; spike-down 62% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.108)_ ; drift intra méd. 0.09% ; recovery-V 24%
- **σ réalisé intraday** 3.109% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 53% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 86400.0 (VA 86320.0–86800.0 ; dernier close 86500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 75% · **stop −2.84%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.45 (high win-rate)
- Gaps overnight (n=153) : méd. 0.0% · baisse 47% (gap-down >1% 18% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.79% (p90 −2.31%) · haut méd +0.64% · range méd 1.88%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −2.94%) · haut méd +0.71% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −2.98%) · haut méd +0.91% · range méd 2.67%
- Excursion ouverture 60min (n=160) : bas méd −1.23% (p90 −3.17%) · haut méd +1.15% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 86600.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 77% (114/153) · gap 31% · délai 0.0min · rebond 47% (46/114) (MFE +0.97%)
   - −1.0% : fill 30min 52% · séance 68% (104/153) · gap 18% · délai 1.1min · rebond 53% (48/104) (MFE +1.13%)
   - −1.5% : fill 30min 42% · séance 58% (81/153) · gap 11% · délai 2.3min · rebond 68% (46/81) (MFE +1.41%)
   - −2.0% : fill 30min 32% · séance 44% (63/153) · gap 4% · délai 3.1min · rebond 64% (34/63) (MFE +1.56%)
   - −3.0% : fill 30min 18% · séance 35% (45/153) · gap 3% · délai 24.9min · rebond 53% (22/45) (MFE +1.26%)
   - −4.0% : fill 30min 10% · séance 23% (32/153) · gap 2% · délai 69.3min · rebond 75% (20/32) (MFE +1.28%)
   - −5.0% : fill 30min 3% · séance 11% (18/153) · gap 1% · délai 123.5min · rebond 79% (11/18) (MFE +1.61%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −2.01%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.59%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.46%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=573 jambes) : jambe baissière méd −1.1% (p90 −2.39%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 89% (51/54) · rebond 57% (25/51)
      · −2.0% : fill 69% (39/54) · rebond 70% (21/39)
      · −3.0% : fill 60% (29/54) · rebond 60% (16/29)
      · −4.0% : fill 39% (22/54) · rebond 71% (13/22)
      · −5.0% : fill 18% (12/54) · rebond 78% (7/12)
   - **flat** (36 séances) :
      · −1.0% : fill 73% (26/36) · rebond 34% (9/26)
      · −2.0% : fill 47% (15/36) · rebond 48% (8/15)
      · −3.0% : fill 36% (11/36) · rebond 18% (2/11)
      · −4.0% : fill 33% (9/36) · rebond 81% (6/9)
      · −5.0% : fill 18% (6/36) · rebond 80% (4/6)
   - **gap-up** (63 séances) :
      · −1.0% : fill 46% (27/63) · rebond 64% (14/27)
      · −2.0% : fill 17% (9/63) · rebond 64% (5/9)
      · −3.0% : fill 10% (5/63) · rebond 87% (4/5)
      · −4.0% : fill 1% (1/63) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/63) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 72% si les 15 1res min sont vertes (59 cas) · 22% si rouges (101 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **55min** → P(séance verte=clôture>ouverture) 75% si début vert vs 15% si rouge (base 42% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **75%** · continue >prix actuel 52% ; creux résiduel méd -1.73% (q20 -3.27%) → **SL/trailing à −3.27%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +2.46% → **scale +1.32% / runner +2.46%**, sortie à la clôture
  - **si ROUGE au coude** (n=97) : edge inversé — récupère vert seulement **15%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.32%** (au-delà de la MAE q10 -3.32%), cible rebond +1.23% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.65% .. +2.48%] · haut q95 +3.57% · bas q05 -3.82%
   - 60min (n=160) : retour [-2.98% .. +3.85%] · haut q95 +4.54% · bas q05 -4.08%
   - 2h (n=160) : retour [-3.36% .. +4.01%] · haut q95 +4.98% · bas q05 -4.19%
   - 4h (n=160) : retour [-3.54% .. +6.04%] · haut q95 +6.81% · bas q05 -5.03%
   - 6h (n=160) : retour [-4.45% .. +4.86%] · haut q95 +7.67% · bas q05 -5.48%
   - session (n=160) : retour [-4.5% .. +5.12%] · haut q95 +7.67% · bas q05 -5.48%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **volatil sans tendance propre (choppy)** (vol intra méd 2.62%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.1 · part idiosyncratique 0.9
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 14.2  _(survente)_
- **ADX** : 17.8  _(pas de tendance nette)_
- **MACD** : hist -666.002  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 21.9%
- **ATR** : 2357.14 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.091  _(distribution)_
- **Vol ratio** : 0.86  _(volume normal)_
- **Choppiness** : 37.1  _(marche directionnel)_
- **MA** : MA20 81210.0 · MA50 82384.0 · MA200 99281.5  _(prix < MA20)_
- **Dist MA** : MA20 -7.8% · MA50 -9.1% · MA200 -24.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (552292 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

# 012450

**Generated** : 2026-09-30T00:22:02.229681+00:00  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩1012000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩1012000.00 (+1.9% vs entrée) · entrée ₩993375.55 · stop ₩913905.51 · T1 ₩1009621.14 · R/R 0.2  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩990126.43–₩996624.67 (mid ₩993375.55)
- Spot actuel : ₩1012000.00 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : ₩913905.51 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩1009621.14 · R/R 0.2 | T2 ₩1025866.72 · R/R 0.41 | T3 ₩1042112.31 · R/R 0.61
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩913905.51


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.02 %)** : le gap seul le franchit 0.164 % des séances (2 fois sur 1218).
   - exécution **4.168 pt plus bas** dans le cas TYPIQUE (médiane), 4.193 au p90, **4.199 au pire**
   - perte réelle **13.188 %** en moyenne _(tirée par la queue)_, jusqu'à **13.219 %** — au lieu des 9.02 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0068 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.827 % | pire -13.219 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0497** [0.0245 ; 0.0898] _(largeur 6.5 pt, n_eff 173.1)_
   - swing : **0.3814** [0.3314 ; 0.4334] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.4057** [0.3549 ; 0.4581] _(largeur 10.3 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-5.93 %** | CVaR **-7.65 %** | vol 3.96 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.37 % contre 3.92 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.29 % vs -12.04 % si l'on extrapolait par √5 _(rapport 0.855 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5108** (β de hausse 0.2908, asymétrie 1.7563) vs KS11 — 553 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.259× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.097 | EV/share : ₩-7692.898 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 28 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.1 | bear 5.0 | side 84.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.837% → cible +1.635% / stop −8.0%, p_fill 72%, n_eff≈78.3) : P(cible|rempli) **59%** · **EV/risk -0.014** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −4.051% → cible +3.657% / stop −5.179%, p_fill 55%, n_eff≈62.7) : P(cible|rempli) **53%** · **EV/risk -0.066** (×p_fill ; si rempli -0.63% du capital)
  - **deep** (entrée dip −6.257% → cible +5.172% / stop −7.951%, p_fill 52%, n_eff≈58.2) : P(cible|rempli) **62%** · **EV/risk -0.002** (×p_fill ; si rempli -0.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→64% · +2.0%→46% · +3.0%→30% · +5.0%→14% · +8.0%→5%
- Range intraday médian 5.67% (p90 9.2%) · excursion haute méd. +1.86% / basse méd. −2.96%
- Profil de vol intra : ouverture 4.102% vs midi 1.08% vs clôture 1.147% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -0.688% ; recovery-V 31%
- **σ réalisé intraday** 3.894% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 55% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 1044912.5 (VA 1043362.5–1050337.5 ; dernier close 1056000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 35% · rebond 78% · **stop −4.43%** sous le fill (sous le bruit) · cible +1.62% · R/R 0.37 (high win-rate)
- Gaps overnight (n=153) : méd. 0.76% · baisse 30% (gap-down >1% 13% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −1.45% (p90 −3.95%) · haut méd +0.95% · range méd 2.82%
- Excursion ouverture 15min (n=160) : bas méd −1.89% (p90 −4.87%) · haut méd +1.08% · range méd 3.63%
- Excursion ouverture 30min (n=160) : bas méd −2.08% (p90 −5.16%) · haut méd +1.08% · range méd 3.96%
- Excursion ouverture 60min (n=160) : bas méd −2.19% (p90 −5.4%) · haut méd +1.28% · range méd 4.27%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1055000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 74% (114/153) · gap 21% · délai 0.1min · rebond 56% (58/114) (MFE +1.24%)
   - −1.0% : fill 30min 58% · séance 68% (103/153) · gap 13% · délai 0.7min · rebond 58% (53/103) (MFE +1.38%)
   - −1.5% : fill 30min 46% · séance 55% (88/153) · gap 10% · délai 1.1min · rebond 54% (44/88) (MFE +1.06%)
   - −2.0% : fill 30min 41% · séance 51% (82/153) · gap 4% · délai 2.7min · rebond 60% (47/82) (MFE +1.21%)
   - −3.0% : fill 30min 31% · séance 44% (63/153) · gap 2% · délai 14.7min · rebond 62% (38/63) (MFE +1.36%)
   - −4.0% : fill 30min 17% · séance 35% (50/153) · gap 1% · délai 35.1min · rebond 78% (37/50) (MFE +1.62%)
   - −5.0% : fill 30min 11% · séance 22% (35/153) · gap 1% · délai 12.4min · rebond 76% (29/35) (MFE +1.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.71% (p90 −2.28%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.68%) → stop au-delà de −2.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −2.72%) → stop au-delà de −2.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=788 jambes) : jambe baissière méd −1.19% (p90 −3.22%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (39 séances) :
      · −1.0% : fill 100% (39/39) · rebond 43% (14/39)
      · −2.0% : fill 86% (35/39) · rebond 53% (17/35)
      · −3.0% : fill 84% (33/39) · rebond 63% (20/33)
      · −4.0% : fill 68% (27/39) · rebond 75% (18/27)
      · −5.0% : fill 46% (21/39) · rebond 81% (18/21)
   - **flat** (26 séances) :
      · −1.0% : fill 72% (22/26) · rebond 78% (14/22)
      · −2.0% : fill 61% (19/26) · rebond 75% (12/19)
      · −3.0% : fill 41% (10/26) · rebond 47% (5/10)
      · −4.0% : fill 39% (9/26) · rebond 84% (7/9)
      · −5.0% : fill 24% (5/26) · rebond 32% (2/5)
   - **gap-up** (88 séances) :
      · −1.0% : fill 52% (42/88) · rebond 62% (25/42)
      · −2.0% : fill 32% (28/88) · rebond 59% (18/28)
      · −3.0% : fill 27% (20/88) · rebond 68% (13/20)
      · −4.0% : fill 19% (14/88) · rebond 79% (12/14)
      · −5.0% : fill 11% (9/88) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 68% si les 15 1res min sont vertes (52 cas) · 23% si rouges (108 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 81% si début vert vs 16% si rouge (base 39% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=53) : tient le vert **81%** · continue >prix actuel 48% ; creux résiduel méd -1.73% (q20 -2.96%) → **SL/trailing à −2.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.25% / q75 +3.72% → **scale +2.25% / runner +3.72%**, sortie à la clôture
  - **si ROUGE au coude** (n=107) : edge inversé — récupère vert seulement **16%** (continue à baisser 49%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.6%** (au-delà de la MAE q10 -5.6%), cible rebond +1.47% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.29% .. +3.7%] · haut q95 +5.12% · bas q05 -6.3%
   - 60min (n=160) : retour [-5.16% .. +4.3%] · haut q95 +6.17% · bas q05 -6.75%
   - 2h (n=160) : retour [-6.68% .. +4.76%] · haut q95 +7.03% · bas q05 -8.38%
   - 4h (n=160) : retour [-7.34% .. +5.73%] · haut q95 +7.64% · bas q05 -8.73%
   - 6h (n=160) : retour [-6.79% .. +5.44%] · haut q95 +7.99% · bas q05 -8.93%
   - session (n=160) : retour [-6.81% .. +5.6%] · haut q95 +7.99% · bas q05 -8.93%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.52%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.15 · part idiosyncratique 0.85
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.2  _(neutre)_
- **ADX** : 10.1  _(pas de tendance nette)_
- **MACD** : hist -7500.204  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 11.5%
- **ATR** : 50285.71 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.244  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 58.1  _(transition)_
- **MA** : MA20 1058450.0 · MA50 1041760.0 · MA200 1166042.58  _(prix < MA20)_
- **Dist MA** : MA20 -4.4% · MA50 -2.9% · MA200 -13.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (552696 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

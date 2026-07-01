# ENR

**Generated** : 2026-07-01T00:05:54.805003+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €165.98  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot €165.98 (+9.2% vs entrée) · entrée €151.94 · stop €139.78 · T1 €155.06 · R/R 0.26  
> ↳ P(T1 av. stop) 47 % · EV/risk -0.021 · ¼-Kelly 0.076 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : RSI 70.7 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €151.31–€152.56 (mid €151.94)
- Spot actuel : €165.98 (+9.2% au-dessus de la zone — repli à attendre)
- Stop : €139.78 (stop swing_plan-based (-20.48%))
- Targets : T1 €155.06 · R/R 0.26 | T2 €158.19 · R/R 0.51 | T3 €161.32 · R/R 0.77
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €139.78


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : €-0.258 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 16 % | T3 9 %
- Kelly (position) : f* 0.304 | ¼-Kelly 0.076 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 43.1 | bear 26.2 | side 30.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 498.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→65% · +2.0%→49% · +3.0%→26% · +5.0%→9% · +8.0%→1%
- Range intraday médian 4.38% (p90 6.09%) · excursion haute méd. +1.69% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.154% vs midi 1.008% vs clôture 1.222% _(ouverture ~2.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 59% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.019)_ ; drift intra méd. -0.412% ; recovery-V 16%
- **σ réalisé intraday** 2.626% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 66% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 154.0913 (VA 153.0938–154.8038 ; dernier close 157.38)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 75% · **stop −1.46%** sous le fill (sous le bruit) · cible +1.5% · R/R 1.03 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 40% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.82%) · haut méd +0.45% · range méd 1.23%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −2.21%) · haut méd +0.6% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.41%) · haut méd +0.6% · range méd 1.85%
- Excursion ouverture 60min (n=160) : bas méd −1.01% (p90 −2.57%) · haut méd +0.77% · range méd 2.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 157.38 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 73% (112/159) · gap 28% · délai 0.4min · rebond 49% (55/112) (MFE +0.97%)
   - −1.0% : fill 30min 48% · séance 67% (100/159) · gap 21% · délai 1.4min · rebond 54% (57/100) (MFE +1.09%)
   - −1.5% : fill 30min 38% · séance 61% (87/159) · gap 18% · délai 12.9min · rebond 61% (54/87) (MFE +1.47%)
   - −2.0% : fill 30min 24% · séance 43% (63/159) · gap 11% · délai 16.5min · rebond 58% (37/63) (MFE +1.18%)
   - −3.0% : fill 30min 17% · séance 36% (49/159) · gap 4% · délai 126.0min · rebond 70% (36/49) (MFE +1.61%)
   - −4.0% : fill 30min 8% · séance 27% (37/159) · gap 2% · délai 302.8min · rebond 64% (25/37) (MFE +1.67%)
   - −5.0% : fill 30min 2% · séance 17% (21/159) · gap 1% · délai 378.8min · rebond 75% (14/21) (MFE +1.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.01%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −2.38%) → stop au-delà de −1.58% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.54%) → stop au-delà de −0.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=504 jambes) : jambe baissière méd −1.07% (p90 −2.53%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 55% (24/44)
      · −2.0% : fill 70% (32/45) · rebond 65% (21/32)
      · −3.0% : fill 63% (28/45) · rebond 67% (20/28)
      · −4.0% : fill 52% (23/45) · rebond 61% (16/23)
      · −5.0% : fill 37% (15/45) · rebond 74% (10/15)
   - **flat** (28 séances) :
      · −1.0% : fill 67% (19/28) · rebond 63% (13/19)
      · −2.0% : fill 27% (8/28) · rebond 35% (3/8)
      · −3.0% : fill 20% (5/28) · rebond 80% (3/5)
      · −4.0% : fill 17% (4/28) · rebond 76% (2/4)
      · −5.0% : fill 10% (2/28) · rebond 74% (1/2)
   - **gap-up** (86 séances) :
      · −1.0% : fill 49% (37/86) · rebond 48% (20/37)
      · −2.0% : fill 32% (23/86) · rebond 56% (13/23)
      · −3.0% : fill 24% (16/86) · rebond 74% (13/16)
      · −4.0% : fill 14% (10/86) · rebond 67% (7/10)
      · −5.0% : fill 7% (4/86) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 85% si les 15 1res min sont vertes (78 cas) · 20% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **17min** → P(séance verte=clôture>ouverture) 84% si début vert vs 24% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 244min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **84%** · continue >prix actuel 67% ; creux résiduel méd -1.19% (q20 -2.47%) → **SL/trailing à −2.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.08% → **scale +2.05% / runner +3.08%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **24%** (continue à baisser 62%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.02%** (au-delà de la MAE q10 -5.02%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.1%] · haut q95 +2.76% · bas q05 -2.74%
   - 60min (n=160) : retour [-2.43% .. +2.16%] · haut q95 +2.92% · bas q05 -3.27%
   - 2h (n=160) : retour [-3.1% .. +2.61%] · haut q95 +3.52% · bas q05 -3.75%
   - 4h (n=160) : retour [-3.04% .. +2.74%] · haut q95 +4.26% · bas q05 -3.89%
   - 6h (n=160) : retour [-3.22% .. +4.09%] · haut q95 +4.88% · bas q05 -4.48%
   - session (n=160) : retour [-4.99% .. +4.45%] · haut q95 +5.84% · bas q05 -6.08%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.64 · part idiosyncratique 0.36
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 70.7  _(surachat)_
- **ADX** : 17.0  _(pas de tendance nette)_
- **MACD** : hist 0.748  _(pas de croisement recent)_
- **BB** : %B 0.75 · largeur 19.6%
- **ATR** : 7.49 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.065  _(distribution)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 42.8  _(transition)_
- **MA** : MA20 158.35 · MA50 168.23 · MA200 138.49  _(prix > MA20)_
- **Dist MA** : MA20 +4.8% · MA50 -1.3% · MA200 +19.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92962 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._

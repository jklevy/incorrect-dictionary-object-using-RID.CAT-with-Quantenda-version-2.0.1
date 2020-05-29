# incorrect-dictionary-object-using-RID.CAT-with-Quantenda-version-2.0.1

There is a savvy tutorial available on the Quantendra blog discussing how to use Quantendra's dictionary functionality with application to the 10th US Republican Presidential Candidate Debate:  https://blog.quanteda.org/2019/02/12/text-analysis-of-the-10th-republican-presidential-candidate-debate/ 

I tried to copy the code word for word from the above tutorial:
https://blog.quanteda.org/2019/02/12/text-analysis-of-the-10th-republican-presidential-candidate-debate/ 

The magnanimous Dr. Ken Benoit immediately sent me the RID.CAT file from the Provalis webiste that he downloaded yesterday (May 27, 2020):
 http://provalisresearch.com/Download/RID.ZIP

We both ran the code from the above tutorial with the same RID.CAT file. However, I ALWAYS obtain the incorrect answer: a dictionary object with only ONE primary key entry and 3 nested levels.
ictionary object with 1 primary key entry and 3 nested levels.
- [PRIMARY]:
  - [NEED]:
    - [ORALITY]:
      - absinth*, ale, ales, alimentary, ambrosia*, ambrosial*, appetit*, apple*, artichok*, asparagu*, bacon*, banana*, bean*, beef*, beer*, belch*, bellies, belly, berri*, berry* [ ... and 225 more ]
    - [ANALITY]:
      - anal, anus, anuses, arse, arsehol*, asses, ass-hol*, asshol*, beshat*, beshit*, besmear*, bile*, bowel*, buttock*, cack*, cesspool*, cloaca*, clot, clots*, constipat* [ ... and 39 more ]
      - [BE]:
      
***************
**************
*************
This compares with what Ken obtained for the same tutorial and the same RID.CAT file


Using Quantenda version 2.0.9 Ken obtains the correct results: a dictionary object with THREE primary keys entry and 3 nested levels.

dict_rid <- dictionary(file = "~/Downloads/RID/RID.CAT")
dict_rid
## Dictionary object with 3 primary key entries and 3 nested levels.
## - [PRIMARY]:
##   - [NEED]:
##     - [ORALITY]:
##       - absinth*, ale, ales, alimentary, ambrosia*, ambrosial*, appetit*, apple*, artichok*, asparagu*, bacon*, banana*, bean*, beef*, beer*, belch*, bellies, belly, berri*, berry* [ ... and 225 more ]
##     - [ANALITY]:
##       - anal, anus, anuses, arse, arsehol*, asses, ass-hol*, asshol*, beshat*, beshit*, besmear*, bile*, bowel*, buttock*, cack*, cesspool*, cloaca*, clot, clots*, constipat* [ ... and 73 more ]
##     - [SEX]:
##       - venereal*, adulterer*, adultery*, allur*, bawd*, bawdy*, bitch*, brothel*, caress*, carnal*, circumcis*, clitori*, cohabit*, coitu*, concubin*, copulat*, coquett*, coquettish*, courtesan*, cuckold* [ ... and 96 more ]
##   - [SENSATION]:
##     - [TOUCH]:
##       - brush*, coars*, contact*, cudd*, cuddl*, handl*, itch*, itchy*, massag*, prickl*, rough*, rub, rubb*, rubs, scaly, scratch*, sharp*, slick*, slippery*, smooth* [ ... and 10 more ]
##     - [TASTE]:
##       - aftertast*, bitter*, delectabl*, deliciou*, flavor*, gall, honi*, lusciou*, piquant*, savor*, savory*, savour*, savoury*, sour*, spic*, spicy*, sugary*, sweet*, sweetnes*, tang* [ ... and 9 more ]
##     - [ODOR]:
##       - aroma*, aromatic*, breath*, cologn*, fragranc*, fragrant*, fume*, fuming*, incens*, inhal*, musk*, musky*, musty*, nose*, nostril*, odor*, odour*, perfum*, pungenc*, pungent* [ ... and 5 more ]
##     - [GEN_SENSATION]:
##       - apperceive, apperceptive, attent*, awar*, awarenes*, balmy*, bask*, beautiful*, beauty*, charm*, comfort*, comfortabl*, creamy*, fair*, impress*, lovelines*, lush*, luxuriou*, luxury*, milky* [ ... and 14 more ]
##     - [SOUND]:
##       - auditorilly, aloud*, audibl*, audition, auditory*, aural, bang*, bell*, binaural, blar*, boom*, buzz*, chord*, choru*, clack*, clamor*, clamour*, clang*, crackl*, croak* [ ... and 65 more ]
##     - [VISION]:
##       - blink*, illuminant, invisibility, monocular, amber*, appear*, appearanc*, aurora*, azur*, beam*, behold*, binocular, blue*, bluish*, bright*, brown*, brunett*, chromatic*, color*, colour* [ ... and 105 more ]
##     [ reached max_nkey ... 3 more keys ]
##   - [DEFENSIVE_SYMBOL]:
##     - [PASSIVITY]:
##       - stagnant, apathetic*, apathy*, bed, bedd*, beds, boredom*, calm*, contented*, contentment*, couch*, cozy*, dead*, death*, decay*, die, died*, dies, dormant*, drift* [ ... and 84 more ]
##     - [VOYAGE]:
##       - caravan*, chas*, cruis*, desert*, driv*, embark*, emigrat*, explor*, immigrat*, immigrant*, journey*, migrat*, navigat*, nomad*, nomadic*, oscillat*, pilgrim*, pilgrimag*, ride, rides [ ... and 22 more ]
##     - [RANDOM MOVEMENT]:
##       - activiti*, activity*, agitat*, churn*, commot*, convuls*, expand*, expans*, fidget*, flounder*, flurri*, flurry*, jerk*, lurch*, orbit*, pitch*, pivot*, puls*, pulsat*, quak* [ ... and 32 more ]
##     - [DIFFUSION]:
##       - blur*, cloud*, cloudy*, curtain*, darken*, diffus*, dim, dimm*, dims, equivocal*, fade, faded, fades*, fading*, fog, fogg*, fogs, haze*, hazing*, hazy* [ ... and 23 more ]
##     - [CHAOS]:
##       - aimles*, ambiguit*, ambiguou*, anarchy*, chanc*, chao*, char, chars, catastrophe, confus*, crowd*, discord*, discordant*, dishevel*, disorder*, entangl*, gordian*, haphazard*, irregular*, jumbl* [ ... and 14 more ]
##   - [REGR_KNOL]:
##     - [UNKNOW]:
##       - bizzar*, bodiles*, boundles*, cryptic*, enigma*, esoteric*, exotic*, fantastic*, formles*, immeasurabl*, inconceivabl*, incredibl*, indescribabl*, ineffabl*, infinity*, inscrutabl*, limitles*, magi*, magic*, magu* [ ... and 22 more ]
##     - [TIMELESSNES]:
##       - aeon*, ceaseles*, centuri*, century*, continual*, continuou*, endles*, endur*, eon*, eternal*, eternity*, everlast*, forever*, immortal*, incessant*, lifetim*, outliv*, permanenc*, permanent*, perpetual* [ ... and 4 more ]
##       - [TEST5]:
##     - [COUNSCIOUS]:
##       - amuck*, asleep*, awak*, awaken*, bedlam*, coma*, craz*, crazy*, deliriou*, delirium*, delphic*, dement*, doze, dozed, dozes, dozing, dream*, dreamy*, drowsy*, ecstacy* [ ... and 73 more ]
##     - [BRINK-PASSAGE]:
##       - acces*, aisl*, aqueduct*, arteri*, artery*, avenu*, barrier*, border*, boundari*, boundary*, bridg*, brim*, brink*, canal*, channel*, coast*, conduit*, corridor*, curb*, door* [ ... and 53 more ]
##     - [NARCISSISM]:
##       - arm, arms, beard*, blood*, bodi*, body*, bone, bones, brain*, brow, brows, cheek*, chest*, chin*, corps*, eye*, face, faces, facies, feet* [ ... and 32 more ]
##     - [CONCRETENESS]:
##       - acros*, afar*, afield*, ahead*, along*, among*, apart*, asid*, at, away*, back*, behind*, besid*, between*, center*, centr*, circl*, clos*, closer*, corner* [ ... and 72 more ]
##   - [ICARIAN_IM]:
##     - [ASCEND]:
##       - aloft*, aris*, arisen*, aros*, ascend*, ascens*, bounc*, climb*, dangl*, dawn*, flap*, fled, flew*, flier*, flight*, fling*, float*, flown*, flung*, flutter* [ ... and 29 more ]
##     - [HEIGHT]:
##       - abov*, aerial*, airplan*, arch, atmospher*, balcony*, battlement*, bird*, branch*, ceil*, cliff*, crag*, craggy*, dome, domes, doming, elevat*, erect*, grew*, grow* [ ... and 45 more ]
##     - [DESCENT]:
##       - base, bases, buri*, burrow*, bury*, descend*, descent*, dig, digg*, digs, dip, dipp*, dips, dive*, downhill*, downstream*, droop*, drop, drops, dug [ ... and 20 more ]
##     - [DEPTH]:
##       - below*, beneath*, bottom*, canyon*, cave*, caving*, cellar*, chasm*, crevas*, deep*, deeper*, depth*, ditch*, downward*, gutter*, hole, holes, low*, pit, pits [ ... and 12 more ]
##     - [FIRE]:
##       - solar, ablaz*, afir*, ash, ashes, blast*, blaz*, boil*, broil*, burn*, burnt*, candl*, charcoal*, coal*, combust*, ember*, fiery*, fire*, flam*, hearth* [ ... and 24 more ]
##     - [WATER]:
##       - bath*, beach*, brook*, bubbl*, bucket*, creek*, dam, damm*, damp*, dams, dew, dews, dewy, dike*, downpour*, drench*, shoring, surf, surfing, drip* [ ... and 52 more ]
## - [SECONDARY]:
##   - [ABSTRACT_TOUGHT]:
##     - diverse, diversification, diversified, diversity, evident, evidential, guess*, logistic, abstract*, almost*, alternativ*, analy*, attribut*, axiom*, basic*, belief*, believ*, calculat*, caus*, certain* [ ... and 125 more ]
##   - [SOCIAL_BEHAVIOR]:
##     - guest*, quota, quota-*, quotas, acquiescence, approbation, consensus*, consult, prosocial, sociable, able*, accept*, acceptanc*, addres*, admit*, advic*, advis*, agre*, aid*, allow* [ ... and 132 more ]
##   - [INSTRU_BEHAVIOR]:
##     - avail, caveat*, divestment*, dividend*, foundr*, laborator*, spin-off*, availability, component*, ingredient, logistics, merchandise, provision*, achiev*, achievement*, acquir*, acquisit*, afford*, aim*, applic* [ ... and 139 more ]
##   - [RESTRAINT]:
##     - comptroller*, discipline, magist*, penaliz*, peniten*(ciary, arrest*, assign*, authoriz*, bar, barred, barring, bars, bind*, block*, blockad*, bound*, cag*, captiv*, captivity*, captur* [ ... and 80 more ]
##   - [ORDER]:
##     - ordinal, accurat*, arrang*, array*, balanc*, catalog*, class*, consistenc*, consistent*, constanc*, constant*, divid*, form*, formula*, grad*, index*, list*, measur*, method*, moderat* [ ... and 21 more ]
##   - [TEMPORAL_REPERE]:
##     - full-time, long-term, longevit*, part-time, short-term, abrupt*, again, ago, already*, ancient, brevity*, brief*, clock*, daily*, date, dated, dates, dating, decad*, dur* [ ... and 52 more ]
##   [ reached max_nkey ... 1 more key ]
## - [EMOTIONS]:
##   - [POSITIVE_AFFECT]:
##     - amus*, amusement*, blith*, carefre*, celebrat*, cheer*, cheerful*, cheery*, chuckl*, delight*, delightful*, elat*, enjoy*, enjoyabl*, enjoyment*, entertain*, entertainment*, enthusiasm*, enthusiastic*, excit* [ ... and 50 more ]
##   - [ANXIETY]:
##     - tremor, afraid*, aghast*, alarm*, anguish*, anxi*, avoid*, blush*, cares, coward*, cower*, crisi*, dangerou*, desperat*, distres*, dread*, dreadful*, fear*, fearful*, frantic* [ ... and 29 more ]
##   - [SADNESS]:
##     - aggrieved, alas, deject*, depres*, depress*, despair*, despondant*, despondent*, dirg*, disappoint*, disappointment*, disconsolat*, discourag*, dishearten*, dismal*, dissatisfi*, dissatisfy*, distraught*, doldrum*, downcast* [ ... and 55 more ]
##   - [AFFECTION]:
##     - affect*, affectionat*, amorou*, amourou*, appreciat*, attractiv*, befriend*, belov*, bosom*, bridal*, bride*, cherish*, congenial*, cordial*, courtship*, darl*, dear*, devot*, embrac*, enamor* [ ... and 45 more ]
##   - [AGGRESSION]:
##     - abhor*, abus*, abusiv*, accus*, afflict*, aggress*, aggressiv*, ambush*, anger*, angri*, angrier*, angry*, annihilat*, annoy*, annoyanc*, antagoniz*, argu*, argument*, army*, arrow* [ ... and 202 more ]
##   - [EXPRESSIVE_BEH]:
##     - art, arts*, bard*, bark*, bawl*, bellow*, bleat*, carol*, chant*, clown*, crie*, criing, cry, danc*, exclaim*, expressiv*, frisk*, frolic*, game*, guitar* [ ... and 32 more ]
##   [ reached max_nkey ... 1 more key ]
```

D
 

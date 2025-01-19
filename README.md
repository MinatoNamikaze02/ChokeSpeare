# ChokeSpeare - following [makemore](https://github.com/karpathy/makemore)
Makemore is this interesting video [series](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ) by Andrej Karpathy which is imo one of the best practical learning materials out there for NN/DL.

I have attempted to replicate the approach in the context of **poem** generation, exploring similar techniques to create poetic structures and verses.

## Background
1. Used a haiku dataset. Haikus follow a certain rule (5-7-5 syllable pattern). I did not choose to build this constraint into my model. I just let the model learn word coherence (on a character level of ourse) and let it "freestyle".
2. Have followed a semi-bare bones structure.

## Approaches
1. [x] Bigrams
2. [x] Simple NN with optimizations
3. [ ] Not sure yet...

## Loss
1. Bigrams saturates negative log likelihood at around 2.5, which is not so great.
<br/>

![bigramloss.png](./assets/bigramloss.png)

Results:
```
'mof tieru arber itost thinot bontikin .
t t s by  bf  is lltudske sine e  s lountss me .
.
ceve,usetllitplor n it pesoubug t ts bung  pln tinge y blsthere  y iticogimati jzcere den le  y desyoncthom .
vesusie tep.
.
merrnond o or slichee  pzzwanojutikdd ng hitg t .
in .
.
peasievethinoma trofon nomof pl unxxrkeh fqoupe ts tumy sugile hay  ve acachee conthe nd avidorthi's   desithay .
tarus furured hismps fu tr itetsheveryhithe n t tt f ithi'ving  t   wing he s diqnere cl .
cak ybarer hetand che  y tibo mymere an she n .
 fe  jnordsh w'qqlis chajs awashenorea gen mbneg'so atjs b,qjud s t  .
 bl gher mzve an powi l a  d .
d sticrd bitora matold ancamean to cir aricanspp se nenge ad  s mowveng ndowily ocashxwenioutous  inanete'f cher  icat  s s d  pas huttee ie kes pere is xormbesiorofrghesloxun ksctam'soy te t g tof mest atpe miore owhe,p,sath wqike m d m anteaith .
  .
be ctheaconos cedadalicts t ing tispepe shthe  wsword tereee c t kdesckis tamago twindefish  mu'd pin d itay d  pronculilaju ant fereworineriy  p g ce .
ifi  gse  mo gs .
 inca wa ises bold .
inon powhas gethe  bmyacr hid inveete bouin sow.

```

2. Simple NN with a single hidden layer after optimizations through weight initialisation and HPT hits 1.5. You could argue that this is not a great improvement, but compare the generated results to better understand the 0.1 loss improvement!
<br/>

![mlploss.png](./assets/mlploss.png)

Results:
```
my like afting on all that it sun i go hill toshine wide i smell slicking the but and brang 

love 

ear word is sun sins colds of on in cold 

the eder samer firer's yeged to blanchone poean 

my hair and it of godtinn sumwelling always 

must hundertain therent be vame  drest i smill now a chold breame clashbove griend tone 

sione watch all good grinco nights all chank tiges a move  

a swife the were from the me and exhelpemeding agains  

mome no not ander light bus you was sight leave tring natain  

to blast i cry reflecty blue's no mes hode tosess perfling in hear am heir  was  here 

i ted to your patting rains the mile celiness 

stone nowhy or fricall seekze to word they 

i leave cool a ver the have sucked to bothe red and nevellinessed in home 

easks solflyain a forghour shy fend to your splayresh at up 

the the for again theys of my he won't ther the like morn 

wine woulderf cretempere day in my carreft the soft and close actans has down a p all cly 

prengone forning grave is ands alched and but in unds it bongivence my and manight anxed time 

my stake morever soges spe but string cared be ampile reaf the day you 

```
PS: Ignore the extra spaces in the generated results. It was a preprocessing issue :p

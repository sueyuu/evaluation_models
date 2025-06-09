you may run your code local. colab's python Version is 3.11 and i cannot downgrade it to 3.9. python 3.11 cannot load pickle in correct form.

requirement:
first create and env with python 3.9.21 and use conda to install the following
pandas 2.2.3
numpy 1.26.3
scipy 1.13.1
tslearn 0.6.3
sktime 0.36.0
seaborn 0.13.2
matplotlib 3.9.4

and use pip to install
torch 2.6.0 (you need to install with command in official website)
torchdrift 0.1.0

if you want to run in colab. you need to find a way to downgrade python version to 3.9

for task 1 and tast 2: suggest compare for tir groups and age groups in single source dataset

for task 5: 
some suggestion:

wadwa closed loop compare with brown closed loop(to see even under modern closed loop system, is there any difference between pediatric and adult patterns?)

wadwa tir group 0 or 1 compare to lynch and brown 0 or 1(to see even if under similar, well controled tir, will there be any difference between patterns?)

brown sap compare to brown clc

aleppo basic pump compare to tamborlane basic pump

lynch, wadwa, brown, aleppo's tir 0 compare to shah

note: because there are lots of clusters. tSNE and histogram may be hard to interpret.

especially histogram, don't too rely on kde line because the clusters are not really ordinal.

if you find kde line disturbing. you can turn off it in draw_histogram function.

tips: you can first see MMD and TS test's result and p value and then turn back to explain plot.
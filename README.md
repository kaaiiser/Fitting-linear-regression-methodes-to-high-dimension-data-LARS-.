# Fitting linear regression methodes to high dimension data LARS 

## Opis projekta
U statistici , regresija najmanjeg ugla (LARS) algoritam je za prilagođavanje modela linearne regresije visokodimenzionalnim podacima, koji je razvio Bradley Efron , Trevor Hastie , Iain Johnstone i Robert Tibshirani .

Pretpostavimo da očekujemo da će varijabla odgovora biti određena linearnom kombinacijom podskupine potencijalnih kovarijacija. Tada algoritam LARS pruža način za izradu procjene koje varijable treba uključiti, kao i njihove koeficijente.

Umjesto da daje vektorski rezultat, rješenje LARS sastoji se od krivulje koja označava rješenje za svaku vrijednost L1 norme vektora parametra. Algoritam je sličan prosljeđivanju postupne regresije , ali umjesto uključivanja varijabli u svakom koraku, procijenjeni parametri povećavaju se u smjeru jednakomjernom korelacijama svakog s ostatkom.

### Osnovni koraci Algoritam regresije najmanjeg ugla su:

Počnite sa svim koeficijentima β jednakim nuli.

Pronađite prediktor <img src="https://latex.codecogs.com/svg.image?x_{j}" title="x_{j}" /> najviše korelira s y

Povećava koeficijent <img src="https://latex.codecogs.com/svg.image?\beta_{j}&space;" title="\beta_{j} " /> u smjeru znaka njegove korelacije s y . Uzmite ostatke <img src="https://latex.codecogs.com/svg.image?r=y-{\hat{y}}" title="r=y-{\hat{y}}" /> usput. Zaustavite se kada neki drugi prediktor <img src="https://latex.codecogs.com/svg.image?x_{k}" title="x_{k}" /> ima jednaku korelaciju s r  kao <img src="https://latex.codecogs.com/svg.image?x_{j}" title="x_{j}" />.

Povećati <img src="https://latex.codecogs.com/svg.image?\beta_{j}&space;" title="\beta_{j} " />  ,  <img src="https://latex.codecogs.com/svg.image?\beta&space;_{k}" title="\beta _{k}" />  u njihovom smjeru najmanjih kvadrata, sve dok neki drugi prediktor <img src="https://latex.codecogs.com/svg.image?x_{m}" title="x_{m}" /> ne bude imao toliko korelacije s rezidualnim r  .

Povećaj <img src="https://latex.codecogs.com/svg.image?\beta&space;_{j}" title="\beta _{j}" /> , <img src="https://latex.codecogs.com/svg.image?\beta&space;_{k}" title="\beta _{k}" /> , <img src="https://latex.codecogs.com/svg.image?\beta&space;_{m}" title="\beta _{m}" /> u njihovom zajedničkom smjeru najmanjih kvadrata, sve dok neki drugi prediktor <img src="https://latex.codecogs.com/svg.image?x&space;_{n}" title="x _{n}" /> ne bude imao toliko korelacije s rezidualnim r.


#### Skup podataka

Skup podataka korišćen za treniranje modela je "Residential Building Data Set".


#### Literatura 

https://venali.medium.com/conventional-guide-to-supervised-learning-with-scikit-learn-least-angle-regression-generalized-11b4ce2dec89

https://hr.wikiarabi.org/wiki/Least-angle_regression

https://www.datatechnotes.com/2019/11/least-angle-regression-example-in-python.html

https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Lars.html

https://scikit-learn.org/stable/auto_examples/linear_model/plot_lasso_lars.html

https://github.com/hughperkins/selfstudy-LARS/blob/master/test_lars.ipynb

https://machinelearningmastery.com/lars-regression-with-python/

https://archive.ics.uci.edu/ml/datasets/Residential+Building+Data+Set

##### Izradio: Adil Kolaković

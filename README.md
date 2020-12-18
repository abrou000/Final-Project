# Final-Project
Project on the determinants Heath coverage in New York 

 knitr::opts_chunk$set(echo = TRUE)
> NY2019drop_var_respondent<-read.csv("NY2019drop_var_respondent.csv",header = TRUE)
> NY2019_lr<- NY2019drop_var_respondent%>%select(X_STATE,WEIGHT2,HEIGHT3,X_SEX, X_AGE80,MARITAL,X_HISPANC,X_PRACE1,EDUCA,INCOME2,MEDCOST,HLTHPLN1,EMPLOY1,PERSDOC2)
> attach(NY2019_lr)
The following objects are masked from NY2019 (pos = 5):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 7):

    X_AGE80

The following objects are masked from NY2019 (pos = 8):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following objects are masked from NY2019 (pos = 9):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 10):

    X_AGE80

The following objects are masked from NY2019 (pos = 11):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following objects are masked from NY2019 (pos = 12):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 13):

    X_AGE80

The following objects are masked from NY2019 (pos = 14):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following objects are masked from NY2019 (pos = 16):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 17):

    X_AGE80

The following object is masked from dataforanalysis (pos = 19):

    X_AGE80

The following object is masked from dataforanalysis (pos = 20):

    X_AGE80

The following object is masked from dataforanalysis (pos = 21):

    X_AGE80

The following object is masked from dataforanalysis (pos = 22):

    X_AGE80

The following object is masked from dataforanalysis (pos = 23):

    X_AGE80

The following objects are masked from NY2019 (pos = 24):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following objects are masked from NY2019 (pos = 25):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 27):

    X_AGE80

> usevar<- (X_AGE80>=18) & (X_AGE80<=55)
> NY2019<-subset(NY2019_lr,usevar)
> detach()
> attach(NY2019)
The following objects are masked from NY2019 (pos = 5):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 7):

    X_AGE80

The following objects are masked from NY2019 (pos = 8):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following objects are masked from NY2019 (pos = 9):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 10):

    X_AGE80

The following objects are masked from NY2019 (pos = 11):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following objects are masked from NY2019 (pos = 12):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 13):

    X_AGE80

The following objects are masked from NY2019 (pos = 14):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following objects are masked from NY2019 (pos = 16):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 17):

    X_AGE80

The following object is masked from dataforanalysis (pos = 19):

    X_AGE80

The following object is masked from dataforanalysis (pos = 20):

    X_AGE80

The following object is masked from dataforanalysis (pos = 21):

    X_AGE80

The following object is masked from dataforanalysis (pos = 22):

    X_AGE80

The following object is masked from dataforanalysis (pos = 23):

    X_AGE80

The following objects are masked from NY2019 (pos = 24):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following objects are masked from NY2019 (pos = 25):

    EDUCA, EMPLOY1, HEIGHT3, HLTHPLN1, INCOME2, MARITAL, MEDCOST, PERSDOC2, WEIGHT2, X_AGE80,
    X_HISPANC, X_PRACE1, X_SEX, X_STATE

The following object is masked from dataforanalysis (pos = 27):

    X_AGE80

> summary(NY2019)
    X_STATE      WEIGHT2          HEIGHT3         X_SEX          X_AGE80         MARITAL     
 Min.   :36   Min.   :  50.0   Min.   : 300   Min.   :1.000   Min.   :18.00   Min.   :1.000  
 1st Qu.:36   1st Qu.: 150.0   1st Qu.: 504   1st Qu.:1.000   1st Qu.:30.00   1st Qu.:1.000  
 Median :36   Median : 180.0   Median : 507   Median :2.000   Median :40.00   Median :2.000  
 Mean   :36   Mean   : 920.1   Mean   :1005   Mean   :1.518   Mean   :38.98   Mean   :3.039  
 3rd Qu.:36   3rd Qu.: 215.0   3rd Qu.: 511   3rd Qu.:2.000   3rd Qu.:49.00   3rd Qu.:5.000  
 Max.   :36   Max.   :9999.0   Max.   :9999   Max.   :2.000   Max.   :55.00   Max.   :9.000  
              NA's   :233      NA's   :262                                                   
   X_HISPANC        X_PRACE1          EDUCA          INCOME2         MEDCOST         HLTHPLN1    
 Min.   :1.000   Min.   : 1.000   Min.   :1.000   Min.   : 1.00   Min.   :1.000   Min.   :1.000  
 1st Qu.:2.000   1st Qu.: 1.000   1st Qu.:4.000   1st Qu.: 5.00   1st Qu.:2.000   1st Qu.:1.000  
 Median :2.000   Median : 1.000   Median :5.000   Median : 8.00   Median :2.000   Median :1.000  
 Mean   :1.942   Mean   : 6.338   Mean   :5.024   Mean   :20.76   Mean   :1.889   Mean   :1.143  
 3rd Qu.:2.000   3rd Qu.: 2.000   3rd Qu.:6.000   3rd Qu.: 8.00   3rd Qu.:2.000   3rd Qu.:1.000  
 Max.   :9.000   Max.   :99.000   Max.   :9.000   Max.   :99.00   Max.   :9.000   Max.   :9.000  
                                                  NA's   :171                                    
    EMPLOY1         PERSDOC2    
 Min.   :1.000   Min.   :1.000  
 1st Qu.:1.000   1st Qu.:1.000  
 Median :1.000   Median :1.000  
 Mean   :2.526   Mean   :1.599  
 3rd Qu.:4.000   3rd Qu.:2.000  
 Max.   :9.000   Max.   :9.000  
 NA's   :63                     
> model1<-lm(HLTHPLN1~X_AGE80+ I(X_AGE80^2) + I(INCOME2^2)+X_SEX+MARITAL+X_PRACE1+X_HISPANC , data = NY2019)
> summary(model1)

Call:
lm(formula = HLTHPLN1 ~ X_AGE80 + I(X_AGE80^2) + I(INCOME2^2) + 
    X_SEX + MARITAL + X_PRACE1 + X_HISPANC, data = NY2019)

Residuals:
    Min      1Q  Median      3Q     Max 
-0.6171 -0.1723 -0.1120 -0.0576  7.9033 

Coefficients:
               Estimate Std. Error t value Pr(>|t|)    
(Intercept)   9.131e-01  9.537e-02   9.575  < 2e-16 ***
X_AGE80       1.255e-02  4.942e-03   2.539 0.011126 *  
I(X_AGE80^2) -1.775e-04  6.421e-05  -2.764 0.005734 ** 
I(INCOME2^2)  8.556e-06  2.168e-06   3.946 8.05e-05 ***
X_SEX        -4.614e-02  1.330e-02  -3.470 0.000525 ***
MARITAL       2.374e-02  3.498e-03   6.787 1.25e-11 ***
X_PRACE1      2.608e-03  3.611e-04   7.223 5.67e-13 ***
X_HISPANC    -8.140e-04  6.933e-03  -0.117 0.906539    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.5239 on 6251 degrees of freedom
  (171 observations deleted due to missingness)
Multiple R-squared:  0.0272,	Adjusted R-squared:  0.02611 
F-statistic: 24.97 on 7 and 6251 DF,  p-value: < 2.2e-16

> 
> NY2019$HCOV<- if_else(NY2019$HLTHPLN1==1,1,0)
> NY2019$female<-if_else(NY2019$X_SEX==2,1,0)
> NY2019$Black<-if_else(NY2019$X_PRACE1==2,1,0)
> NY2019$White<-if_else(NY2019$X_PRACE1==1,1,0)
> NY2019$Asian<-if_else(NY2019$X_PRACE1==4,1,0)
> NY2019$HISPANIC<-if_else(NY2019$X_HISPANC==1,1,0)
> NY2019$NOHS<-if_else(NY2019$EDUCA<4,1,0)
> NY2019$HS<-if_else(NY2019$EDUCA==4,1,0)
> NY2019$Somecol<-if_else(NY2019$EDUCA==5,1,0)
> NY2019$BMdegr<-if_else(NY2019$EDUCA==6,1,0)
> NY2019$Student<-if_else(NY2019$EMPLOY1==6,1,0,missing = 0)
> NY2019$Sefemploy<-if_else(NY2019$EMPLOY1==2,1,0,missing = 0)
> NY2019$Hired<-if_else(NY2019$EMPLOY1==1,1,0,missing = 0)
> NY2019$Married<-if_else(NY2019$MARITAL==1,1,0)
> NY2019$Divorced<-if_else(NY2019$MARITAL==2,1,0)
> NY2019$Single<-if_else(NY2019$MARITAL==5,1,0)
> NY2019$Lessthan10000<-if_else(NY2019$INCOME2==1,1,0,missing = 0)
> NY2019$Lessthan25000<-if_else(NY2019$INCOME2==4,1,0,missing = 0)
> NY2019$Lessthan35000<-if_else(NY2019$INCOME2==5,1,0,missing = 0)
> NY2019$Lessthan50000<-if_else(NY2019$INCOME2==6,1,0,missing = 0)
> NY2019$Morethan75000<-if_else(NY2019$INCOME2==8,1,0, missing = 0)
> 
> dataforanalysis<-data.frame(NY2019$HCOV,
+                             NY2019$X_AGE80,
+                             NY2019$female,
+                             NY2019$Black,
+                             NY2019$White,
+                             NY2019$Asian,
+                             NY2019$HISPANIC,
+                             NY2019$Married,
+                             NY2019$Divorced,
+                             NY2019$Single,
+                             NY2019$NOHS,
+                             NY2019$HS,
+                             NY2019$Somecol,
+                             NY2019$BMdegr,
+                             NY2019$Student,
+                             NY2019$Sefemploy,
+                             NY2019$Hired,
+                             NY2019$Lessthan10000,
+                             NY2019$Lessthan25000,
+                             NY2019$Lessthan35000,
+                             NY2019$Lessthan50000,
+                             NY2019$Morethan75000
+ 
+                             
+                             )
> 
> names(dataforanalysis)<- c("HCOV",
+                            "X_AGE80",
+                            "female",
+                            "Black",
+                            "White",
+                            "Asian",
+                            "HISPANIC",
+                            "Married",
+                            "Divorced",
+                            "Single",
+                            "NOHS",
+                            "HS",
+                            "Somecol",
+                            "BMdegr",
+                            "Student",
+                            "Sefemploy",
+                            "Hired",
+                            "Lessthan10000",
+                            "Lessthan25000",
+                            "Lessthan35000",
+                            "Lessthan50000",
+                            "Morethan75000"
+ 
+                            )
> detach()
> attach(dataforanalysis)
The following object is masked from NY2019 (pos = 5):

    X_AGE80

The following objects are masked from dataforanalysis (pos = 7):

    Asian, Black, BMdegr, Divorced, female, HCOV, HISPANIC, HS, Married, NOHS, Single,
    Somecol, White, X_AGE80

The following object is masked from NY2019 (pos = 8):

    X_AGE80

The following object is masked from NY2019 (pos = 9):

    X_AGE80

The following objects are masked from dataforanalysis (pos = 10):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following object is masked from NY2019 (pos = 11):

    X_AGE80

The following object is masked from NY2019 (pos = 12):

    X_AGE80

The following objects are masked from dataforanalysis (pos = 13):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following object is masked from NY2019 (pos = 14):

    X_AGE80

The following objects are masked from data_now:

    Asian, female

The following object is masked from NY2019 (pos = 16):

    X_AGE80

The following objects are masked from dataforanalysis (pos = 17):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following objects are masked from dataforanalysis (pos = 19):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following objects are masked from dataforanalysis (pos = 20):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy, Single, Somecol,
    Student, White, X_AGE80

The following objects are masked from dataforanalysis (pos = 21):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following objects are masked from dataforanalysis (pos = 22):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following objects are masked from dataforanalysis (pos = 23):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following objects are masked from NY2019 (pos = 24):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following objects are masked from NY2019 (pos = 25):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

The following objects are masked from dataforanalysis (pos = 27):

    Asian, Black, BMdegr, Divorced, female, HCOV, Hired, HISPANIC, HS, Lessthan10000,
    Lessthan25000, Lessthan35000, Lessthan50000, Married, Morethan75000, NOHS, Sefemploy,
    Single, Somecol, Student, White, X_AGE80

> require("standardize")
> set.seed(654321)
> NN<-length(dataforanalysis$HCOV)
> restrict_1<-(runif(NN)<0.7)
> summary(restrict_1)
   Mode   FALSE    TRUE 
logical    1945    4485 
> dat_train<-subset(dataforanalysis,restrict_1)
> dat_test<-subset(dataforanalysis,!restrict_1)
> sobj<-standardize(HCOV~X_AGE80+I(X_AGE80^2)+female+Black+White+Asian+HISPANIC+ (Black + White +Asian +HISPANIC)*female+  +Married+Divorced+Single+NOHS+HS + Somecol+ BMdegr +(female+Black+White+Asian+HISPANIC)*Lessthan25000 +  Student+Sefemploy+Hired + Lessthan25000+Lessthan50000+Morethan75000, dat_train, family = binomial)
> s_data_test<- predict(sobj,dat_test)
> summary(s_data_test)
      X_AGE80.V1       I_X_AGE80.pow.2.V1  female   Black    White    Asian    HISPANIC Married  Divorced
 Min.   :-1.9280323   Min.   :-1.5868772   1:1031   1: 242   1:1267   1: 115   1: 340   1: 845   1: 170  
 1st Qu.:-0.8326149   1st Qu.:-0.8977823   0: 914   0:1703   0: 678   0:1830   0:1605   0:1100   0:1775  
 Median : 0.0802329   Median :-0.0603406                                                                 
 Mean   :-0.0415584   Mean   :-0.0431914                                                                 
 3rd Qu.: 0.9017959   3rd Qu.: 0.8979319                                                                 
 Max.   : 1.4495046   Max.   : 1.6444514                                                                 
 Single   NOHS     HS       Somecol  BMdegr   Lessthan25000 Student  Sefemploy Hired    Lessthan50000
 1: 656   1: 159   1: 482   1: 458   1: 826   1: 146        1: 141   1: 224    1:1147   1: 161       
 0:1289   0:1786   0:1463   0:1487   0:1119   0:1799        0:1804   0:1721    0: 798   0:1784       
                                                                                                     
                                                                                                     
                                                                                                     
                                                                                                     
 Morethan75000
 1: 635       
 0:1310       
              
              
              
              
> 
> #LPM
> model_lpm1<-lm(sobj$formula,  data = sobj$data)
> summary(model_lpm1)

Call:
lm(formula = sobj$formula, data = sobj$data)

Residuals:
     Min       1Q   Median       3Q      Max 
-1.04653  0.01587  0.07006  0.12947  0.61264 

Coefficients:
                           Estimate Std. Error t value Pr(>|t|)    
(Intercept)               0.8381162  0.0610193  13.735  < 2e-16 ***
X_AGE80                  -0.0633673  0.0409861  -1.546 0.122159    
I_X_AGE80.pow.2           0.0847852  0.0398001   2.130 0.033203 *  
female1                   0.0111377  0.0175150   0.636 0.524878    
Black1                    0.0392870  0.0160401   2.449 0.014352 *  
White1                    0.0374437  0.0135655   2.760 0.005800 ** 
Asian1                   -0.0124863  0.0217185  -0.575 0.565378    
HISPANIC1                -0.0516758  0.0120839  -4.276 1.94e-05 ***
Married1                  0.0248251  0.0071092   3.492 0.000484 ***
Divorced1                 0.0259671  0.0097037   2.676 0.007478 ** 
Single1                   0.0274699  0.0075241   3.651 0.000264 ***
NOHS1                    -0.0803764  0.0270644  -2.970 0.002996 ** 
HS1                       0.0099261  0.0262449   0.378 0.705291    
Somecol1                  0.0263258  0.0262451   1.003 0.315879    
BMdegr1                   0.0325463  0.0261993   1.242 0.214207    
Lessthan250001           -0.0084319  0.0285507  -0.295 0.767754    
Student1                  0.0303473  0.0117222   2.589 0.009661 ** 
Sefemploy1               -0.0225435  0.0085629  -2.633 0.008500 ** 
Hired1                    0.0167477  0.0059820   2.800 0.005137 ** 
Lessthan500001           -0.0137909  0.0086866  -1.588 0.112447    
Morethan750001            0.0142790  0.0057136   2.499 0.012486 *  
female1:Black1           -0.0013863  0.0090772  -0.153 0.878621    
female1:White1           -0.0066750  0.0073841  -0.904 0.366062    
female1:Asian1           -0.0196057  0.0115892  -1.692 0.090769 .  
female1:HISPANIC1         0.0122996  0.0068814   1.787 0.073945 .  
female1:Lessthan250001   -0.0005769  0.0091261  -0.063 0.949602    
Black1:Lessthan250001     0.0189148  0.0159763   1.184 0.236504    
White1:Lessthan250001     0.0019210  0.0135643   0.142 0.887387    
Asian1:Lessthan250001    -0.0128632  0.0216321  -0.595 0.552117    
HISPANIC1:Lessthan250001 -0.0075768  0.0119335  -0.635 0.525514    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.3031 on 4455 degrees of freedom
Multiple R-squared:  0.1255,	Adjusted R-squared:  0.1198 
F-statistic: 22.05 on 29 and 4455 DF,  p-value: < 2.2e-16

> predi_val_lpm<-predict(model_lpm1, s_data_test)
contrasts dropped from factor femalecontrasts dropped from factor Blackcontrasts dropped from factor Whitecontrasts dropped from factor Asiancontrasts dropped from factor HISPANICcontrasts dropped from factor Marriedcontrasts dropped from factor Divorcedcontrasts dropped from factor Singlecontrasts dropped from factor NOHScontrasts dropped from factor HScontrasts dropped from factor Somecolcontrasts dropped from factor BMdegrcontrasts dropped from factor Lessthan25000contrasts dropped from factor Studentcontrasts dropped from factor Sefemploycontrasts dropped from factor Hiredcontrasts dropped from factor Lessthan50000contrasts dropped from factor Morethan75000
> predi_model_lpm1<-(predi_val_lpm>0.6)
> table(pred = predi_model_lpm1, true = dat_test$HCOV)
       true
pred       0    1
  FALSE   39   32
  TRUE   217 1657
> #GPM
> model_logit1<-glm(sobj$formula,family= binomial,data = sobj$data)
> summary(model_logit1)

Call:
glm(formula = sobj$formula, family = binomial, data = sobj$data)

Deviance Residuals: 
    Min       1Q   Median       3Q      Max  
-2.9337   0.2576   0.3584   0.4893   1.6314  

Coefficients:
                          Estimate Std. Error z value Pr(>|z|)    
(Intercept)               2.230947   0.529482   4.213 2.51e-05 ***
X_AGE80                  -0.835849   0.439941  -1.900 0.057444 .  
I_X_AGE80.pow.2           1.085693   0.436404   2.488 0.012853 *  
female1                   0.081530   0.163863   0.498 0.618799    
Black1                    0.249202   0.150525   1.656 0.097813 .  
White1                    0.260634   0.113111   2.304 0.021210 *  
Asian1                   -0.192035   0.179775  -1.068 0.285432    
HISPANIC1                -0.363016   0.104522  -3.473 0.000514 ***
Married1                  0.224456   0.069464   3.231 0.001232 ** 
Divorced1                 0.225548   0.104204   2.164 0.030428 *  
Single1                   0.230002   0.072816   3.159 0.001585 ** 
NOHS1                    -0.396022   0.229354  -1.727 0.084224 .  
HS1                       0.065928   0.226209   0.291 0.770709    
Somecol1                  0.231031   0.228064   1.013 0.311057    
BMdegr1                   0.332131   0.228281   1.455 0.145691    
Lessthan250001           -0.023437   0.240679  -0.097 0.922427    
Student1                  0.319434   0.129484   2.467 0.013626 *  
Sefemploy1               -0.167721   0.080801  -2.076 0.037919 *  
Hired1                    0.199133   0.061842   3.220 0.001282 ** 
Lessthan500001           -0.150568   0.086445  -1.742 0.081547 .  
Morethan750001            0.240339   0.074290   3.235 0.001216 ** 
female1:Black1            0.018714   0.087893   0.213 0.831394    
female1:White1           -0.006371   0.068816  -0.093 0.926236    
female1:Asian1           -0.184267   0.110499  -1.668 0.095396 .  
female1:HISPANIC1         0.008827   0.063550   0.139 0.889524    
female1:Lessthan250001   -0.013157   0.084692  -0.155 0.876547    
Black1:Lessthan250001     0.157573   0.149491   1.054 0.291854    
White1:Lessthan250001    -0.029872   0.113087  -0.264 0.791666    
Asian1:Lessthan250001    -0.079420   0.177927  -0.446 0.655335    
HISPANIC1:Lessthan250001 -0.031168   0.103091  -0.302 0.762392    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

(Dispersion parameter for binomial family taken to be 1)

    Null deviance: 3262.5  on 4484  degrees of freedom
Residual deviance: 2782.9  on 4455  degrees of freedom
AIC: 2842.9

Number of Fisher Scoring iterations: 5

> predi_val_glm<-predict(model_logit1, s_data_test, type = "response")
contrasts dropped from factor femalecontrasts dropped from factor Blackcontrasts dropped from factor Whitecontrasts dropped from factor Asiancontrasts dropped from factor HISPANICcontrasts dropped from factor Marriedcontrasts dropped from factor Divorcedcontrasts dropped from factor Singlecontrasts dropped from factor NOHScontrasts dropped from factor HScontrasts dropped from factor Somecolcontrasts dropped from factor BMdegrcontrasts dropped from factor Lessthan25000contrasts dropped from factor Studentcontrasts dropped from factor Sefemploycontrasts dropped from factor Hiredcontrasts dropped from factor Lessthan50000contrasts dropped from factor Morethan75000
> predi_model_logit1<-(predi_val_glm>0.6)
> table(pred = predi_model_logit1, true = dat_test$HCOV)
       true
pred       0    1
  FALSE   40   42
  TRUE   216 1647
> require(e1071)
> # figure best parameters and input into next
> svm.model <- svm(as.factor(HCOV) ~ ., data = sobj$data, cost = 10, gamma = 0.1)
> svm.pred <- predict(svm.model, s_data_test)
> table(pred = svm.pred, true = dat_test$HCOV)
    true
pred    0    1
   0   33   58
   1  223 1631
> vif(model_logit1)
               X_AGE80        I_X_AGE80.pow.2                 female                  Black 
             72.646154              69.270247              10.745341               4.604763 
                 White                  Asian               HISPANIC                Married 
              5.175616               3.864493               3.940130               1.820657 
              Divorced                 Single                   NOHS                     HS 
              1.318966               1.904457              13.171142              17.071616 
               Somecol                 BMdegr          Lessthan25000                Student 
             14.668499              17.010074               8.256103               1.465518 
             Sefemploy                  Hired          Lessthan50000          Morethan75000 
              1.379729               1.546046               1.089133               1.292756 
          female:Black           female:White           female:Asian        female:HISPANIC 
              3.108625               1.909729               4.884218               1.620913 
  female:Lessthan25000    Black:Lessthan25000    White:Lessthan25000    Asian:Lessthan25000 
              2.869376               6.223336               5.172290               6.876912 
HISPANIC:Lessthan25000 
              3.879473 
> round(cor(dataforanalysis),
+   digits = 2
+ )
               HCOV X_AGE80 female Black White Asian HISPANIC Married Divorced Single  NOHS    HS Somecol
HCOV           1.00    0.08   0.06 -0.02  0.16 -0.02    -0.22    0.08     0.01  -0.01 -0.23 -0.05    0.04
X_AGE80        0.08    1.00   0.06  0.00  0.08 -0.10    -0.11    0.30     0.20  -0.43  0.00 -0.05   -0.06
female         0.06    0.06   1.00  0.05 -0.02 -0.02     0.03    0.03     0.03  -0.08 -0.01 -0.05    0.01
Black         -0.02    0.00   0.05  1.00 -0.53 -0.10    -0.03   -0.10     0.01   0.11 -0.01  0.02    0.05
White          0.16    0.08  -0.02 -0.53  1.00 -0.35    -0.29    0.12     0.01  -0.10 -0.13 -0.01    0.01
Asian         -0.02   -0.10  -0.02 -0.10 -0.35  1.00    -0.12    0.00    -0.05   0.05 -0.04 -0.02   -0.06
HISPANIC      -0.22   -0.11   0.03 -0.03 -0.29 -0.12     1.00   -0.08    -0.01   0.01  0.31  0.02   -0.05
Married        0.08    0.30   0.03 -0.10  0.12  0.00    -0.08    1.00    -0.28  -0.61 -0.04 -0.04   -0.09
Divorced       0.01    0.20   0.03  0.01  0.01 -0.05    -0.01   -0.28     1.00  -0.22  0.01  0.00    0.03
Single        -0.01   -0.43  -0.08  0.11 -0.10  0.05     0.01   -0.61    -0.22   1.00 -0.03  0.04    0.08
NOHS          -0.23    0.00  -0.01 -0.01 -0.13 -0.04     0.31   -0.04     0.01  -0.03  1.00 -0.17   -0.17
HS            -0.05   -0.05  -0.05  0.02 -0.01 -0.02     0.02   -0.04     0.00   0.04 -0.17  1.00   -0.32
Somecol        0.04   -0.06   0.01  0.05  0.01 -0.06    -0.05   -0.09     0.03   0.08 -0.17 -0.32    1.00
BMdegr         0.15    0.09   0.04 -0.06  0.09  0.09    -0.14    0.13    -0.03  -0.08 -0.26 -0.48   -0.49
Student        0.03   -0.38  -0.03  0.00 -0.04  0.12    -0.01   -0.19    -0.07   0.28 -0.05  0.01    0.12
Sefemploy     -0.09    0.09  -0.08 -0.04 -0.01  0.00     0.04    0.04     0.00  -0.06  0.03  0.01   -0.04
Hired          0.11    0.02  -0.04  0.00  0.07 -0.03    -0.05    0.09    -0.01  -0.08 -0.12 -0.10   -0.05
Lessthan10000 -0.06    0.00   0.01  0.03 -0.04 -0.01     0.07   -0.12     0.02   0.07  0.13  0.07    0.00
Lessthan25000 -0.06   -0.02   0.03  0.04 -0.06 -0.01     0.08   -0.07     0.03   0.02  0.07  0.08    0.01
Lessthan35000 -0.04   -0.05   0.01  0.01 -0.04  0.03     0.03   -0.06     0.01   0.02  0.03  0.08    0.01
Lessthan50000 -0.03   -0.02   0.00  0.00  0.00  0.00     0.01   -0.04     0.04   0.02 -0.04  0.06    0.04
Morethan75000  0.15    0.11  -0.05 -0.08  0.18 -0.01    -0.16    0.25    -0.08  -0.14 -0.18 -0.22   -0.07
              BMdegr Student Sefemploy Hired Lessthan10000 Lessthan25000 Lessthan35000 Lessthan50000
HCOV            0.15    0.03     -0.09  0.11         -0.06         -0.06         -0.04         -0.03
X_AGE80         0.09   -0.38      0.09  0.02          0.00         -0.02         -0.05         -0.02
female          0.04   -0.03     -0.08 -0.04          0.01          0.03          0.01          0.00
Black          -0.06    0.00     -0.04  0.00          0.03          0.04          0.01          0.00
White           0.09   -0.04     -0.01  0.07         -0.04         -0.06         -0.04          0.00
Asian           0.09    0.12      0.00 -0.03         -0.01         -0.01          0.03          0.00
HISPANIC       -0.14   -0.01      0.04 -0.05          0.07          0.08          0.03          0.01
Married         0.13   -0.19      0.04  0.09         -0.12         -0.07         -0.06         -0.04
Divorced       -0.03   -0.07      0.00 -0.01          0.02          0.03          0.01          0.04
Single         -0.08    0.28     -0.06 -0.08          0.07          0.02          0.02          0.02
NOHS           -0.26   -0.05      0.03 -0.12          0.13          0.07          0.03         -0.04
HS             -0.48    0.01      0.01 -0.10          0.07          0.08          0.08          0.06
Somecol        -0.49    0.12     -0.04 -0.05          0.00          0.01          0.01          0.04
BMdegr          1.00   -0.08      0.01  0.20         -0.12         -0.12         -0.09         -0.06
Student        -0.08    1.00     -0.09 -0.32          0.03         -0.01          0.02          0.01
Sefemploy       0.01   -0.09      1.00 -0.43         -0.01          0.02          0.02          0.01
Hired           0.20   -0.32     -0.43  1.00         -0.18         -0.04         -0.01          0.04
Lessthan10000  -0.12    0.03     -0.01 -0.18          1.00         -0.06         -0.06         -0.06
Lessthan25000  -0.12   -0.01      0.02 -0.04         -0.06          1.00         -0.08         -0.08
Lessthan35000  -0.09    0.02      0.02 -0.01         -0.06         -0.08          1.00         -0.09
Lessthan50000  -0.06    0.01      0.01  0.04         -0.06         -0.08         -0.09          1.00
Morethan75000   0.36   -0.06      0.00  0.23         -0.14         -0.19         -0.20         -0.21
              Morethan75000
HCOV                   0.15
X_AGE80                0.11
female                -0.05
Black                 -0.08
White                  0.18
Asian                 -0.01
HISPANIC              -0.16
Married                0.25
Divorced              -0.08
Single                -0.14
NOHS                  -0.18
HS                    -0.22
Somecol               -0.07
BMdegr                 0.36
Student               -0.06
Sefemploy              0.00
Hired                  0.23
Lessthan10000         -0.14
Lessthan25000         -0.19
Lessthan35000         -0.20
Lessthan50000         -0.21
Morethan75000          1.00

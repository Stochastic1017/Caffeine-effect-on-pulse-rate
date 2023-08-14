Studying the effect of caffeine on pulse rate
================
S. Sudhir
2023-05-11

# Introduction

I am interested in conducting a rigorous statistical analysis to study
how caffeine affects pulse rate. In order to conduct this experiment, I
chose three of my friends as participants and had them consume 50 mg,
100 mg, and 200 mg caffeine pills on separate days and then recorded the
change in average pulse rate before and after the consumption of each
caffeine pill. It is well-studied in papers like [Gonzaga LA et
al.](https://www.nature.com/articles/s41598-017-14540-4) and [Karapetian
GK et al.](https://pubmed.ncbi.nlm.nih.gov/22499570/) that caffeine is
attributed to a subsequent decrease in pulse rate. This research however
studies the effect of caffeine on decrease in pulse rate specifically
based on quantity of caffeine consumed (50 mg, 100 mg, and 200 mg).

# Experimental Design

I chose a 3-by-3 Latin Square Design for this experiment with the
following parameters:

- **`Day` \[blocking\]:**
  - 1: 04/24/2023
  - 2: 04/25/2023
  - 3: 04/26/2023

- **`Participant` \[blocking\]:**
  - 1: age - 21, sex - female
  - 2: age - 20, sex - male
  - 3: age - 21, sex - male

- **`Caffeine` \[treatment\]:**
  - A: $50$ mg
  - B: $100$ mg
  - C: $200$ mg.

- **`Decrease` $y_{ijk}$ \[response\]:**
  - $i:$ `Day`, i.e., $i = 1,2,3$
  - $j:$ `Participant`, i.e., $j = 1,2,3$
  - $k:$ `Caffeine`, i.e., $k = A, B, C$

## Advantages of Design

1.  Allows us to block two nuisance variables we wish to keep separate
    (`Day` and `Participant`).

2.  Permits us to study $3$ treatments simultaneously, with $2$ blocking
    variables, each at $3$ levels, i.e., test each caffeine pill $(k)$,
    once on each participant $(j)$, and on each day $(i)$.

3.  Only 9 number of runs required, making our experiment both time and
    cost effective.

## Shortcomings of Design

1.  The number of levels of each blocking variable must be the same as
    the levels of treatment factor. As two of my participants are male,
    and one is female, the design does not allow us to block the
    confounding effect of gender.

2.  The experiment was not conducted in a controlled setting, any
    underlying confounding effects could not be controlled (such as the
    time of day at which a caffeine pill was consumed).

3.  Due to the non-replication nature of the design, no interaction
    effect between treatment and blocking variable can be studied.

# Setting Up Design

After randomizing experimental participants, along with the day, and
capsule consumption, the design used for this experiment is given below:

         Participant 1 Participant 2 Participant 3
    [1,] "A (y_11A)"   "C (y_12C)"   "B (y_13B)"  
    [2,] "B (y_21B)"   "A (y_22A)"   "C (y_23C)"  
    [3,] "C (y_31C)"   "B (y_32B)"   "A (y_33A)"  

The interpretation of the matrix is as follows:

- **Day 1 \[04/24/2023\]:**

  - Participant 1 takes 50 mg caffeine pill, i.e., $\mathbf{y_{11A}}$.
  - Participant 2 takes 200 mg caffeine pill, i.e., $\mathbf{y_{12C}}$.
  - Participant 3 takes 100 mg caffeine pill, i.e., $\mathbf{y_{13B}}$.

- **Day 2 \[04/25/2023\]:**

  - Participant 1 takes 100 mg caffeine pill, i.e., $\mathbf{y_{21B}}$.
  - Participant 2 takes 50 mg caffeine pill, i.e., $\mathbf{y_{22A}}$.
  - Participant 3 takes 200 mg caffeine pill, i.e., $\mathbf{y_{23C}}$.

- **Day 3 \[04/26/2023\]:**

  - Participant 1 takes 200 mg caffeine pill, i.e., $\mathbf{y_{31C}}$.
  - Participant 2 takes 100 mg caffeine pill, i.e., $\mathbf{y_{32B}}$.
  - Participant 3 takes 50 mg caffeine pill, i.e., $\mathbf{y_{33A}}$.

# Apparatus Used

To administer caffeine pills, I bought the [Nutricost Caffeine
Pills](https://www.amazon.com/dp/B01MY5CW7S?ref=ppx_yo2ov_dt_b_product_details&th=1)
100 mg per serving, 250 capsules bottle.

- For 50 mg (A) caffeine, I administered half a capsule.

- For 100 mg (B) caffeine, I administered one entire capsule.

- For 200 mg (C), I administered two capsules.

To measure pulse rate, I used the [EMAY Bluetooth Pulse Oximeter
Fingertip](https://www.amazon.com/dp/B08FFHG69C?psc=1&ref=ppx_yo2ov_dt_b_product_details).

- For initial measurements, I used the Oximeter for five minutes and
  recorded the data.

- I then administered the designated dosage of caffeine pill, waited for
  approximately 45 minutes, then re-took measurements for 5 minutes and
  recorded the data.

# Data Collected

## Day 1

### Participant 1 \[50 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consuming 50 mg pill for Participant 1 is 8.997 (y_11A)"

### Participant 2 \[200 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consuming 200 mg pill for Participant 2 is 12.323 (y_12C)"

### Participant 3 \[100 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consuming 100 mg caffeine pill for Participant 3 is 8.193 (y_13B)"

**Visualizing Data for Day 1**

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

## Day 2

### Participant 1 \[100 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consumption of 100 mg pill in the afternoon for Participant 1 is 10.043 (y_21B)"

### Participant 2 \[50 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-16-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consuming 50 mg pill for Participant 2 is 9.667 (y_22A)"

### Participant 3 \[200 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-19-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consuming 200 mg pill for Participant 3 is 8.547 (y_23C)"

**Visualizing Data for Day 2**

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-21-1.png)<!-- -->

## Day 3

### Participant 1 \[200 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-23-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consuming 200 mg pill for Participant 1 is 14.547 (y_31C)"

### Participant 2 \[100 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-26-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consuming 100 mg pill for Participant 2 is 15.6 (y_32B)"

### Participant 3 \[50 mg\]

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-29-1.png)<!-- -->

    [1] "The difference in average pulse rate before and after consuming 50 mg pill for Participant 3 is 9.997 (y_33A)"

**Visualizing Data for Day 3**

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-31-1.png)<!-- -->

# Data Table

          Participant 1 Participant 2 Participant 3
    Day 1 "A (8.997)"   "C (12.323)"  "B (8.193)"  
    Day 2 "B (10.043)"  "A (9.667)"   "C (8.547)"  
    Day 3 "C (14.547)"  "B (15.6)"    "A (9.997)"  

      Participant Day Caffeine Decrease
    1           1   1        A    8.997
    2           2   1        C   12.323
    3           3   1        B    8.193
    4           1   2        B   10.043
    5           2   2        A    9.667
    6           3   2        C    8.547
    7           1   3        C   14.547
    8           2   3        B   15.600
    9           3   3        A    9.997

# Analysis of Variance \[ANOVA\]

## Linear Model for Latin Square Design

The linear model for our Latin Square Design is as follows:

$$
y_{ijk} = \eta + \alpha_i + \beta_j + \tau_k + \epsilon_{ijk}
$$

where:

- $\eta$ is the grand mean.

- $\alpha_i$ is the i-th row effect \[`Day`\]

- $\beta_j$ is the j-th column effect \[`Participant`\]

- $\tau_k$ is the k-th treatment effect of the letters ($A,B,C$)
  \[`Caffeine`\]

- $\epsilon_{ijk}$ are independent $N(0,\sigma^2)$.

There are no interaction terms as they cannot be estimated in an
un-replicated experiment.

Using the zero-sum constraints, we have that:

$$
y_{ijk} = \hat{\eta} + \hat{\alpha}_i + \hat{\beta}_j + \hat{\tau}_k + r_{ijk}
$$

where:

- $\hat\eta = \bar{y}_{....}$

- $\hat{\alpha}_i = (\bar{y}_{i..} - \bar{y}_{...})$

- $\hat{\beta}_j = (\bar{y}_{.j.} - \bar{y}_{...})$

- $\hat{\tau}_k = (\bar{y}_{..k} - \bar{y}_{...})$

- $\hat{r}_{ijk} = (y_{ijk} - \bar{y}_{i..} - \bar{y}_{.j.} - \bar{y}_{..k} + 2 \bar{y}_{...})$

Then, subtracting $\bar{y}_{...}$, squaring both sides, and summing over
all observations, we have that:

$$
\underbrace{\displaystyle\sum_{(i,j,k) \in S} (y_{ijk} - \bar{y}_{...})^2}_{SSE_{total}}
 =\underbrace{\displaystyle\sum_{i \in \{1,2,3\}} 3(\bar{y}_{i..} - \bar{y}_{...})^2}_{SSE_{row}} + \underbrace{\displaystyle\sum_{j \in \{1,2,3\}} 3(\bar{y}_{.j.} - \bar{y}_{...})^2}_{SSE_{column}} + \underbrace{\displaystyle\sum_{k \in \{A,B,C\}} 3(\bar{y}_{..k} - \bar{y}_{...})^2}_{SSE_{treatment}} + \underbrace{\displaystyle\sum_{(i,j,k) \in S} (y_{ijk} - \bar{y}_{i..} - \bar{y}_{.j.} - \bar{y}_{..k} + 2 \bar{y}_{...})^2}_{SSE_{residual}}
$$

where the set of $3^2$ values dictated by the particular Latin square
triplets $(i,j,k)$ is denoted by $S$.

The above derivation tells us that the corrected total sum of squares on
the left equals the sum of the row sum of squares, column sum of
squares, treatment sum of squares, and residual sum of squares.

## Code for ANOVA Table Latin Square Design

``` r
## Degrees of Freedom
n = 3
df_row = n-1
df_col = n-1
df_treat = n-1
df_resid = (n-1)*(n-2)

## Grand mean
y_... = mean(data$Decrease)  

## Row Effects [Day]
y_i.. = c(mean(data[which(data$Participant == '1'), ]$Decrease), 
          mean(data[which(data$Participant == '2'), ]$Decrease), 
          mean(data[which(data$Participant == '3'), ]$Decrease))
SSE_row = n*sum((y_i.. - y_...)^2)
MSE_row = SSE_row/df_row

## Column Effects [Participant]
y_.j. = c(mean(data[which(data$Day == '1'), ]$Decrease), 
          mean(data[which(data$Day == '2'), ]$Decrease), 
          mean(data[which(data$Day == '3'), ]$Decrease))
SSE_col = n*sum((y_.j. - y_...)^2)
MSE_col = SSE_col/df_col

## Treatment Effects [Caffeine]
y_..k = c(mean(data[which(data$Caffeine == 'A'), ]$Decrease),
          mean(data[which(data$Caffeine == 'B'), ]$Decrease),
          mean(data[which(data$Caffeine == 'C'), ]$Decrease))
SSE_treat = n*sum((y_..k - y_...)^2)
MSE_treat = SSE_treat/df_treat

## Residuals
SSE_resid = sum((data$Decrease - y_...)^2) - SSE_row - SSE_col - SSE_treat
MSE_resid = SSE_resid/df_resid

## F-values
F_row = MSE_row/MSE_resid
F_col = MSE_col/MSE_resid
F_treat = MSE_treat/MSE_resid

## P-value
Pval_row = 1 - pf(F_row, 2, 2)
Pval_col = 1 - pf(F_col, 2, 2)
Pval_treat = 1 - pf(F_treat, 2, 2)
```

**ANOVA Table:**

    ##        Source Df    SSE    MSE       F  pval
    ## 1         Day  2 20.082 10.041 156.471 0.006
    ## 2 Participant  2 28.433 14.216 221.543 0.004
    ## 3    Caffeine  2  8.325  4.162  64.865 0.015
    ## 4   Residuals  2  0.128  0.064              
    ## 5      Totals  8 65.293 28.484

## Analysis of Latin Square Design ANOVA Table

The null hypothesis of our model is that there are no treatment effect
differences, i.e.,

$$
H_0: \tau_i = \tau_j\;\;for\;all\;i,j \in \{A,B,C\}
$$

The alternative hypothesis of our model is that there is at least one
treatment effect difference, i.e.,

$$
H_1: \tau_i \neq \tau_j\;\;for\;some\;i,j \in \{A,B.C\}
$$

Given the degrees of freedom $n - 1 = 3-1 = 2$ and
$(n-1)(n-2) = (2)(1) = 2$, along with following F-values:

1.  F-statistic = 19 (coral)
2.  F-value \[`Day`\] = 156.471 (navyblue)
3.  F-value \[`Participant`\] = 221.453 (limegreen)
4.  F-value \[`Caffeine`\] = 64.865 (purple)

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-35-1.png)<!-- -->

We can see that both our blocking factors \[`Day` and `Participants`\]
are statistically significant, i.e., null hypothesis rejected as p-value
\< 0.05. This implies that even upon taking into account the effects of
Day and Participant on decrease in pulse rate after consuming caffeine
pill, those variables seem to have a significant effect on our analysis.

More importantly, we can see that the p-value of treatment factor
`Caffeine` is also lesser than 0.05, but greater than 0.01. This could
imply that among the three levels of the treatment factor, at least one
pair of group means is not significant. In order to study this, we
conduct a Tukey Multiple-Comparisons 95% family-wise confidence level
test.

## Tukey Multiple-Comparisons for ANOVA

``` r
require(multcomp)
Tukey_posthoc = confint(glht(lm(Decrease ~ Day + Participant + Caffeine, data), linfct = mcp(Caffeine = 'Tukey')))
Tukey_posthoc
```

    ## 
    ##   Simultaneous Confidence Intervals
    ## 
    ## Multiple Comparisons of Means: Tukey Contrasts
    ## 
    ## 
    ## Fit: lm(formula = Decrease ~ Day + Participant + Caffeine, data = data)
    ## 
    ## Quantile = 5.8939
    ## 95% family-wise confidence level
    ##  
    ## 
    ## Linear Hypotheses:
    ##            Estimate lwr     upr    
    ## B - A == 0  1.7250   0.5059  2.9441
    ## C - A == 0  2.2520   1.0329  3.4711
    ## C - B == 0  0.5270  -0.6921  1.7461

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-37-1.png)<!-- -->

We can see that the paired-groups B-A \[100 mg caffeine vs 50 mg
caffeine\] and groups C-A \[200 mg caffeine vs 50 mg caffeine\] are
statistically significant. However, the paired-group C-B \[200 mg vs 100
caffeine\] is not statistically significant. This could imply that the
effects of caffeine on pulse rate is most significant when taking over
50 mg, not when taking over 100 mg or 200 mg.

## Visual Interpretation of Inference

Given below is a summary table of our treatment factor group `Caffeine`
and its corresponding means and sd in relation to `Decrease`.

    ## # A tibble: 3 × 4
    ##   group count  mean    sd
    ##   <chr> <int> <dbl> <dbl>
    ## 1 A         3  9.55 0.510
    ## 2 B         3 11.3  3.85 
    ## 3 C         3 11.8  3.03

Given below is a 2d line plot where the x-axis is our treatment factor
`Caffeine` and y-axis is our response `Decrease`. This plot allows us to
see how the three levels of caffeine quantity affects response.

![](STATME_424_Project_S._Sudhir_files/figure-gfm/unnamed-chunk-39-1.png)<!-- -->

Given below is a 3d interactive scatter plot where the x-axis is our row
blocking factor `Day`, y-axis is our column blocking factor
`Participant`, and z-axis is our response `Decrease`. This plot allows
us to see how the two blocking factors affect our response.

<div class="plotly html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-32297346f20d4af5a147" style="width:576px;height:384px;"></div>
<script type="application/json" data-for="htmlwidget-32297346f20d4af5a147">{"x":{"visdat":{"11835192d95d":["function () ","plotlyVisDat"]},"cur_data":"11835192d95d","attrs":{"11835192d95d":{"x":{},"y":{},"z":{},"color":{},"colors":["#A020F0","#E7B800","#FC4E07"],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"scatter3d","mode":"markers","inherit":true}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"scene":{"xaxis":{"title":"Participant"},"yaxis":{"title":"Day"},"zaxis":{"title":"Decrease"}},"hovermode":"closest","showlegend":true},"source":"A","config":{"modeBarButtonsToAdd":["hoverclosest","hovercompare"],"showSendToCloud":false},"data":[{"x":[1,2,3],"y":[1,2,3],"z":[8.997,9.667,9.997],"type":"scatter3d","mode":"markers","name":"A","marker":{"color":"rgba(160,32,240,1)","line":{"color":"rgba(160,32,240,1)"}},"textfont":{"color":"rgba(160,32,240,1)"},"error_y":{"color":"rgba(160,32,240,1)"},"error_x":{"color":"rgba(160,32,240,1)"},"line":{"color":"rgba(160,32,240,1)"},"frame":null},{"x":[3,1,2],"y":[1,2,3],"z":[8.193,10.043,15.6],"type":"scatter3d","mode":"markers","name":"B","marker":{"color":"rgba(231,184,0,1)","line":{"color":"rgba(231,184,0,1)"}},"textfont":{"color":"rgba(231,184,0,1)"},"error_y":{"color":"rgba(231,184,0,1)"},"error_x":{"color":"rgba(231,184,0,1)"},"line":{"color":"rgba(231,184,0,1)"},"frame":null},{"x":[2,3,1],"y":[1,2,3],"z":[12.323,8.547,14.547],"type":"scatter3d","mode":"markers","name":"C","marker":{"color":"rgba(252,78,7,1)","line":{"color":"rgba(252,78,7,1)"}},"textfont":{"color":"rgba(252,78,7,1)"},"error_y":{"color":"rgba(252,78,7,1)"},"error_x":{"color":"rgba(252,78,7,1)"},"line":{"color":"rgba(252,78,7,1)"},"frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

# Conclusion

A 3-by-3 Latin Square Design was chosen to conduct this experiment with
factors: `Day`, `Participants`, `Caffeine`, and `Decrease`. The blockedc
nuisance factors were `Day` and `Participants`, the treatment factor to
be studied was `Caffeine` and the response variable was `Decrease`.
After randomizing the factors and setting up the design, pulse rate
measurements were taken before and after consumption of assigned
caffeine pill, and the difference in average pulse rates were recorded.
After $9$ trials, wherein each of the three participant consumed each of
the three pills on each separate day, an ANOVA was conducted for Latin
Square Design using the Sum Squared and Mean Squared errors for each
factor group.

The ANOVA found that there is a statistical significance between the
quantity of caffeine consumed and the subsequent decrease in heart rate.
In particular, there seems to be a statistical significance between 50
mg - 100 mg caffeine group and 50 mg - 200 mg caffeine group. This can
also be confirmed visually as we can see that the mean of 50 mg caffeine
group is significantly lower than the mean of 100 mg and 200 mg caffeine
group. Additionally, the mean of 100 mg and 200 mg caffeine groups were
relatively the same, and no statistical significance was found between
them. It was also found that even after blocking, the variables `Day`
and `Participants` were both statistically significant. This would imply
that there are significant effects between the blocking variable and
response, however due to non-replication of the experiment, the
interaction effects could not be studied. Furthermore, The variance of
treatment group A is much lesser than the variance of treatment group B
and C, which suggests that variance between groups is constant. Both
these issues could be fixed with replication, unfortunately due to time
and cost constraints, no replication was conducted for this experiment.

Due to the nature of the design, only two nuisance factors could be
blocked: the day in which caffeine was consumed and the participant who
consumed the caffeine. My intuition for blocking these two variables
were that, tolerance would increase each day of caffeine consumption,
and the prior tolerances of each candidate could significantly affect
readings of pulse rate. That said, there were some very important
confounding variables that could not be blocked. For one, the time of
day at which the caffeine pill was consumed was a primary factor I
wished to block using a 3-by-3 Graeco-Squared design for the experiment,
but unfortunately no degrees of freedom were left after estimating
factorial effects. Additionally, the sex of the candidates could also
not be blocked as a Latin-Square design requires that the blocking
factors have the same levels as treatment factors, which is not the case
here. Lastly, the experiment could not be conducted in a controlled
setting. Although I had asked the participants to refrain from consuming
any caffeine for the three days the experiment had to be done, there was
no way of knowing if they truly adhered to the instructions.
Furthermore, I had to record their readings in stressful environments
like the library or a cafe, which could have further impeded the reading
as a result.

Although the results of the experiment were interesting (it might be
jarring to know that effect of caffeine pills on pulse rate is
significant for only 50+ mg pills, but not so much for 100+ and 200+
caffeine pills), it must be noted that there are significant effects
from other extraneous factors that randomization and blocking could not
negate. A good followup to this experiment would be to conduct one where
multiple factors could be blocked by the use of a 4-by-4 or 5-by-5
Hyper-Graeco Latin Square Design or a 3^k factorial design (or
fractional factorial depending on the resources available). Placebos can
also be incorporated in the study to take into account the effect of
caffeine perception on pulse-rate. Furthermore, many replicates of the
experiment could be conducted under these design, which could help
further negate the effects of blocking variables. The setting for the
experiments should also be more controlled, and incentives should be
provided to candidates so as to make sure they stick to the instructions
to allow for better quality of readings. Lastly, the health and
well-being of participants should be of utmost importance. Studies like
[Meredith SE et
al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3777290/), [Sweeney et
al.](https://www.liebertpub.com/doi/10.1089/caff.2019.0020), and [Ali
Samaha](https://www.sciencedirect.com/science/article/pii/S2352340919312004)
have studied the effect of caffeine on physical and mental health in
great depth and have found that caffeine is not just an addictive
substance, but also has considerable negative impacts on stress and
heart-rate. An experiment involving caffeine must be conducted
carefully, with necessary precautions taken to ensure that the
participants physical and mental health are kept in check and unaffected
by caffeine pills.

# References

Ali Samaha and Ahmad (Al Tassi) and Najwa Yahfoufi and Maya Gebbawi and
Mohammad Rached and Mirna A. Fawaz. Data on the relationship between
caffeine addiction and stress among Lebanese medical students in
Lebanon. Data in Brief. Vol: 28. pp: 104845. doi:
<https://doi.org/10.1016/j.dib.2019.104845>.

Farag, Noha H. and Whitsett, Thomas L. and McKey, Barbara S. and Wilson,
Michael F. and Vincent, Andrea S. and Everson-Rose, Susan A. and
Lovallo, William R. Caffeine and Blood Pressure Response: Sex, Age, and
Hormonal Status. Journal of Women’s Health. Vol 19:6. pp: 1171-1176.
doi: 10.1089/jwh.2009.1664.

Gonzaga LA, Vanderlei LCM, Gomes RL, Valenti VE. Caffeine affects
autonomic control of heart rate and blood pressure recovery after
aerobic exercise in young adults: a crossover study. Sci Rep. 2017 Oct
26;7(1):14091. doi: 10.1038/s41598-017-14540-4. PMID: 29075019; PMCID:
PMC5658389.

Karapetian GK, Engels HJ, Gretebeck KA, Gretebeck RJ. Effect of caffeine
on LT, VT and HRVT. Int J Sports Med. 2012 Jul;33(7):507-13. doi:
10.1055/s-0032-1301904. Epub 2012 Apr 12. PMID: 22499570.

Meredith SE, Juliano LM, Hughes JR, Griffiths RR. Caffeine Use Disorder:
A Comprehensive Review and Research Agenda. J Caffeine Res. 2013
Sep;3(3):114-130. doi: 10.1089/jcr.2013.0016. PMID: 24761279; PMCID:
PMC3777290.

Sweeney, Mary M. and Weaver, Darian C. and Vincent, Kathryn B. and
Arria, Amelia M. and Griffiths, Roland R. Prevalence and Correlates of
Caffeine Use Disorder Symptoms Among a United States Sample. Journal of
Caffeine and Adenosine Research. Vol 10:1. pp: 4-11. doi:
10.1089/caff.2019.0020.

Valentina Rakic and Valerie Burke and Lawrence J. Beilin. Effects of
Coffee on Ambulatory Blood Pressure in Older Men and Women.
Hypertension. Vol 33:3. pp: 869-873. doi: 10.1161/01.HYP.33.3.869.

# Appendix

**Data for [Participant 1 \[50 mg\]](#participant-1-50-mg)**

<div id="htmlwidget-8f24a97a21fc20aff57e" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-8f24a97a21fc20aff57e">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

**Data for [Participant 2 \[200 mg\]](#participant-2-200-mg)**

<div id="htmlwidget-c7edf407d92d6fb53b4b" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-c7edf407d92d6fb53b4b">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

**Data for [Participant 3 \[100 mg\]](#participant-3-100-mg)**

<div id="htmlwidget-4d9e3a6221c6f7e08283" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-4d9e3a6221c6f7e08283">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

**Data for [Participant 1 \[100 mg\]](#participant-1-100-mg)**

<div id="htmlwidget-6834018017322d0cf728" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-6834018017322d0cf728">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

**Data for [Participant 2 \[50 mg\]](#participant-2-50-mg)**

<div id="htmlwidget-d48e6d332498fae90e6b" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-d48e6d332498fae90e6b">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

**Data for [Participant 3 \[200 mg\]](#participant-3-200-mg)**

<div id="htmlwidget-797e85b9f12b9ebc0c95" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-797e85b9f12b9ebc0c95">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

**Data for [Participant 1 \[200 mg\]](#participant-1-200-mg)**

<div id="htmlwidget-f6cc2202a0722c5d189b" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-f6cc2202a0722c5d189b">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

**Data for [Participant 2 \[100 mg\]](#participant-2-100-mg)**

<div id="htmlwidget-da62fd13006787f2b652" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-da62fd13006787f2b652">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

**Data for [Participant 3 \[50 mg\]](#participant-3-50-mg)**

<div id="htmlwidget-dde53785af0008fae6f5" class="reactable html-widget " style="width:auto;height:250px;"></div>
<script type="application/json" data-for="htmlwidget-dde53785af0008fae6f5">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"Time (in seconds)":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100,101,102,103,104,105,106,107,108,109,110,111,112,113,114,115,116,117,118,119,120,121,122,123,124,125,126,127,128,129,130,131,132,133,134,135,136,137,138,139,140,141,142,143,144,145,146,147,148,149,150,151,152,153,154,155,156,157,158,159,160,161,162,163,164,165,166,167,168,169,170,171,172,173,174,175,176,177,178,179,180,181,182,183,184,185,186,187,188,189,190,191,192,193,194,195,196,197,198,199,200,201,202,203,204,205,206,207,208,209,210,211,212,213,214,215,216,217,218,219,220,221,222,223,224,225,226,227,228,229,230,231,232,233,234,235,236,237,238,239,240,241,242,243,244,245,246,247,248,249,250,251,252,253,254,255,256,257,258,259,260,261,262,263,264,265,266,267,268,269,270,271,272,273,274,275,276,277,278,279,280,281,282,283,284,285,286,287,288,289,290,291,292,293,294,295,296,297,298,299,300],"Initial BPM":[75,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,74,61,61,61,62,62,62,63,63,64,64,65,65,64,64,64,64,64,64,64,64,66,67,67,67,67,68,68,68,68,67,67,68,69,70,71,71,72,72,73,73,73,73,73,72,71,70,69,69,69,69,69,69,70,71,71,71,71,71,71,72,72,72,73,73,74,74,75,77,78,79,78,77,76,74,74,74,74,74,74,74,73,73,72,71,70,70,70,70,70,71,71,71,72,72,72,74,76,78,78,79,81,82,83,83,84,84,84,82,80,77,75,74,74,74,74,74,74,71,69,67,65,66,66,68,70,71,73,71,70,70,70,70,70,70,69,69,68,68,67,67,68,68,69,69,70,70,70,70,69,69,69,68,68,68,69,69,69,75,78,82,82,82,80,79,77,77,76,76,76,76,76,77,77,78,78,78,81,83,85,85,85,85,85,81,78,72,72,73,73,74,74,74,74,74,72,70,69,67,68,68,69,69,69,69,68,68,68,67,67,67,67,67,67,65,64,63,62,62,62,62,62,62,62,62,62,62,62,61,61,61,61,61,62,63,63,63,62,62,62,62,63,63,63,63,64,64,64,64,65,66,67,67,68,68,68,68,68,68,66,65,63,61,61,60,61,61,61,61,61,61,61,61,61,61,61,61,61],"Final BPM":[70,70,70,70,70,70,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,62,52,52,52,52,52,52,52,56,56,56,56,56,56,56,56,56,58,61,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,66,63,61,59,57,57,57,57,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,58,57,57,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,56,59,62,65,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,69,65,61,61,54,54,54,54]},"columns":[{"id":"Time (in seconds)","name":"Time (in seconds)","type":"numeric"},{"id":"Initial BPM","name":"Initial BPM","type":"numeric"},{"id":"Final BPM","name":"Final BPM","type":"numeric"}],"defaultPageSize":25,"highlight":true,"bordered":true,"nowrap":true,"showSortable":true,"height":"250px","dataKey":"5dcc26e62a94dfdaf0d46a0506852363"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>
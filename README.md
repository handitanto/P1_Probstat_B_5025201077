# P1_Probstat_B_5025201077
Praktikum Probabilitas dan Statistik

Handitanto Herprasetyo
5025201077

 ## 1. Disribusi Geometrik
  #### a. Berapa peluang penyurvei bertemu x = 3 orang yang tidak menghadiri acara vaksinasi sebelum keberhasilan pertama ketika p = 0,20 dari populasi menghadiri acara vaksinasi ?
  ```
  x<-3
  prob<-0.2
  dgeom(x,prob)
  ```
  #### b. Mean Distribusi Geometrik dengan 10000 data random , prob = 0,20 dimana distribusi geometrik acak tersebut X = 3
  ```
  set.seed(2)
  N<-10000
  prob<-0.2
  ```

  #### karena distribusi geometrik acak x=3 maka
  ```
  random<-rgeom(9998,prob)
  random
  distribusi<-dgeom(random,prob)
  distribusi
  rata<-mean(distribusi)
  rata
  ```
  #### d. Histogram Distribusi Geometrik , Peluang X = 3 gagal Sebelum Sukses Pertama
  ```
  hist(distribusi)
  ```
  
  #### e.  Nilai Rataan (μ) dan Varian (σ²) dari Distribusi Geometrik
  
  #### rataan
  ```
  rataan<-1/prob
  rataan
  ```

  #### varian
  ```
  varian<-(1-prob)/prob^2
  varian
  ```
  
  

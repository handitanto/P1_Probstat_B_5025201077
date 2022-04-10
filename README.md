# P1_Probstat_B_5025201077
Praktikum Probabilitas dan Statistik

### Handitanto Herprasetyo
### 5025201077

 ## 1. Disribusi Geometrik
 ```
   x<-3
  prob<-0.2
  ```
 #### a. Berapa peluang penyurvei bertemu x = 3 orang yang tidak menghadiri acara vaksinasi sebelum keberhasilan pertama ketika p = 0,20 dari populasi menghadiri acara vaksinasi ?
  ```
  dgeom(x,prob)
  ```
  #### b. Mean Distribusi Geometrik dengan 10000 data random , prob = 0,20 dimana distribusi geometrik acak tersebut X = 3
 
  set.seed(2)
  N<-10000
  prob<-0.2
  

  #### karena distribusi geometrik acak x=3 maka
  ```
  random<-rgeom(9998,prob)
  random
  distribusi<-dgeom(random,prob)
  distribusi
  rata<-mean(distribusi)
  rata
  ```
  #### c. Bandingkan Hasil poin a dan b , apa kesimpulan yang bisa didapatkan?

  #### d. Histogram Distribusi Geometrik , Peluang X = 3 gagal Sebelum Sukses Pertama
  ```
  hist(distribusi)
  ```
  
  #### e. Nilai Rataan (μ) dan Varian (σ²) dari Distribusi Geometrik
  
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
  
  ## 2. Distribusi Binomial
  ```
  prob<-0.2
  size<-20
  ```
  #### a. Peluang terdapat 4 pasien yang sembuh
  ```
  sembuh<-pbinom(4,20,0.2)
  sembuh
  ```
  #### b. Gambarkan grafik histogram berdasarkan kasus tersebut
  ```
  hist(sembuh)
  ```
  #### c. Nilai Rataan (μ) dan Varian (σ²) dari Distribusi Binomial
  #### rataan
  ```
  rataan = size*prob
  rataan
  ```
  #### varian
  ```
  varian = rataan*(1-prob)
  varian
  ``` 
  
  ## 3. Distribusi Poisson
  ```
  lambda = 4.5
  ```
  #### a. Berapa peluang bahwa 6 bayi akan lahir di rumah sakit ini besok?
  ```
  lahir<-ppois(6, lambda = 4.5, lower.tail = TRUE)
  lahir
  ```
  #### b. Simulasikan dan buatlah histogram kelahiran 6 bayi akan lahir di rumah sakit ini selama setahun (n = 365)
  
  #### c. Bandingkan hasil poin a dan b , Apa kesimpulan yang bisa didapatkan
  
  #### d. 
  #### rataan
  ```
  rataan = r
  rataan
  ```
  #### varian
  ```
  varian = r
  rataan
  ```
  
  ## 4. Distribusi Chi-Square
  ```
  x<-2
  v<-10
  ```
  #### a. Fungsi Probabilitas dari Distribusi Chi-Square
  ```
  probabilitas<-pchisq(x,v)
  probabilitas
  ```
  #### b. Histogram dari Distribusi Chi-Square dengan 100 data random
  ```
  histogram <- rchisq(100, v)
  histogram
  hist(histogram)
  ```
  #### c. Nilai Rataan (μ) dan Varian (σ²) dari DistribusiChi-Square
  #### rataan
  ```
  rataan=v
  rataan
  ```
  #### varian
  ```
  varian = v*2
  varian
  ```


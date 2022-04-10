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
 
  Menggunakan `dgeom` untuk menghitung peluang bertemu dengan syntax
  ```
  dgeom(x,prob)
  ```
  sehingga didapatkan hasil
  # ![image](https://user-images.githubusercontent.com/94664744/162615954-3d7c8e56-5162-48ae-b82b-61f9c3abc211.png)

  #### b. Mean Distribusi Geometrik dengan 10000 data random , prob = 0,20 dimana distribusi geometrik acak tersebut X = 3
  ```
  set.seed(2)
  N<-10000
  prob<-0.2
  ```
  karena distribusi geometrik acak x=3 maka
  ```
  random<-rgeom(9998,prob)
  random
  distribusi<-dgeom(random,prob)
  distribusi
  rata<-mean(distribusi)
  rata
  ```
  sehingga didapatkan hasil
  # ![image](https://user-images.githubusercontent.com/94664744/162616150-78dbe9cd-8e22-45fe-a8ce-eec5c9a117bd.png)

  
  #### c. Bandingkan Hasil poin a dan b , apa kesimpulan yang bisa didapatkan?
  ```
  Jika dibandingkan hasil poin a = 0.1024 dan poin b =  0.1114001, maka bisa disimpulkan bahwa terdapat perbedaan hasil. Hal tersebut terjadi karena pada poin b dilakukan percobaan 10000 data random yang berpengaruh pada hasil akhir dari percobaan.
  ```

  #### d. Histogram Distribusi Geometrik , Peluang X = 3 gagal Sebelum Sukses Pertama
  Menampilkan grafik `distribusi`
  ```
  hist(distribusi)
  ```
  didapatkan grafik
  # ![image](https://user-images.githubusercontent.com/94664744/162616225-242b365c-da09-4266-8326-aae979a272cd.png)

  #### e. Nilai Rataan (μ) dan Varian (σ²) dari Distribusi Geometrik
  
  #### rataan
  Menggunakan 1/prob untuk mencari rataan
  ```
  rataan<-1/prob
  rataan
  ```
  #### varian
  dan menggunakan (1-prob)/prob^2 untuk mencari varian
  ```
  varian<-(1-prob)/prob^2
  varian
  ```
  sehingga didapatkan hasil rataan dan
  # ![image](https://user-images.githubusercontent.com/94664744/162616350-a3877459-4e1c-46b0-9e19-0e580020d033.png)
  
  dan hasil varian
  # ![image](https://user-images.githubusercontent.com/94664744/162616373-858132d1-9d1e-44fa-904b-3405df064fbf.png)
  
  
  ## 2. Distribusi Binomial
  ```
  prob<-0.2
  size<-20
  ```
  #### a. Peluang terdapat 4 pasien yang sembuh
  Menggunakan `pbinom` untuk mencari peluang 4 pasien sembuh
  ```
  sembuh<-pbinom(4,20,0.2)
  sembuh
  ```
  sehingga didapatkan hasil
  # ![image](https://user-images.githubusercontent.com/94664744/162616633-8f8f0f55-08cc-4b0d-b7a8-64a058b61353.png)

  #### b. Gambarkan grafik histogram berdasarkan kasus tersebut
  Menampilkan grafik `sembuh`
  ```
  hist(sembuh)
  ```
  didapatkan grafik
  # ![image](https://user-images.githubusercontent.com/94664744/162616687-ba2797f2-3e60-418d-bfac-1cadf45c521a.png)

  #### c. Nilai Rataan (μ) dan Varian (σ²) dari Distribusi Binomial
  #### rataan
  Menggunakan size*prob untuk mencari rataan
  ```
  rataan = size*prob
  rataan
  ```
  #### varian
  dan menggunakan rataan*(1-prob) untuk mencari varian
  ```
  varian = rataan*(1-prob)
  varian
  ``` 
  sehingga didapatkan hasil rataan
  # ![image](https://user-images.githubusercontent.com/94664744/162616762-8d34efb0-a9f2-4019-8675-c00cc40ac983.png)

  dan hasil varian
  # ![image](https://user-images.githubusercontent.com/94664744/162616789-dd96307d-0a73-4b0b-a732-52ee16994f38.png)
  
  ## 3. Distribusi Poisson
  ```
  lambda = 4.5
  ```
  #### a. Berapa peluang bahwa 6 bayi akan lahir di rumah sakit ini besok?
  Menggunakan `ppois` untuk mencari peluang 6 bayi lahir
  ```
  lahir<-ppois(6, lambda = 4.5, lower.tail = TRUE)
  lahir
  ```
  sehingga didapatkan hasil
  # ![image](https://user-images.githubusercontent.com/94664744/162616846-92f1d66b-c10f-4755-aca5-9e2b9cc1b725.png)

  #### b. Simulasikan dan buatlah histogram kelahiran 6 bayi akan lahir di rumah sakit ini selama setahun (n = 365)
  Menggunakan `rpois` untuk mencari simulasi kelahiran 6 bayi selama 1 tahun dengan `N=365`
  ```
  N <- 365
  hisLahir <- rpois(N,lambda)
  hist(hisLahir,main = "Grafik histogram distribusi poisson kelahiran 6 bayi selama 1 tahun")
  ```
  sehingga didapatkan grafik
  ![image](https://user-images.githubusercontent.com/94664744/162617553-8d71f290-8f6c-43dc-8d91-a89b0c9a83ca.png)
  
  #### c. Bandingkan hasil poin a dan b , Apa kesimpulan yang bisa didapatkan
  ```
  Jika dibandingkan hasil poin a dan poin b terdapat perbedaan hasil. Hal tersebut dikarenakan simulasi yang dilakukan sebanyak 365 kali sehingga menghasilkan output   yang berbeda.
  ```
  
  #### d. Nilai Rataan (μ) dan Varian (σ²) dari Distribusi Poisson
  #### rataan
  Pada Chi-Square besar rataan = varian = lambda
  ```
  rataan = lambda
  rataan
  ```
  #### varian
  ```
  varian = rataan
  varian
  ```
  sehingga didapatkan hasil
  # ![image](https://user-images.githubusercontent.com/94664744/162618344-fad296a6-d51a-4a8d-b5e2-f943f754d3c9.png)
  # ![image](https://user-images.githubusercontent.com/94664744/162618377-b78b3567-7e10-4e83-9faa-0b87bd37de6a.png)
  
  ## 4. Distribusi Chi-Square
  ```
  x<-2
  v<-10
  ```
  #### a. Fungsi Probabilitas dari Distribusi Chi-Square
  Menggunakan `pchisq` untuk mencari fungsi probabilitas Chi-Square
  ```
  probabilitas<-pchisq(x,v)
  probabilitas
  ```
  sehingga didapatkan hasil
  # ![image](https://user-images.githubusercontent.com/94664744/162618446-9d20d7d5-33be-4c72-b1a9-45e16a37b273.png)

  #### b. Histogram dari Distribusi Chi-Square dengan 100 data random
  Menggunakan `rchisq` untuk mencari distribusi Chi-Square dengan 100 data random
  ```
  disChiSquare <- rchisq(100, v)
  disChiSquare
  hist(disChiSquare)
  ```
  sehingga didapatkan grafik
  ![image](https://user-images.githubusercontent.com/94664744/162618647-eb0aaea2-0127-4446-8e3f-b5fbcc29fa48.png)

  #### c. Nilai Rataan (μ) dan Varian (σ²) dari Distribusi Chi-Square
  #### rataan
  Pada distribusi Chi-Square besar rataan = v
  ```
  rataan=v
  rataan
  ```
  #### varian
  dan besar varian = v*2
  ```
  varian = v*2
  varian
  ```
  sehingga didapatkan hasil rataan
  # ![image](https://user-images.githubusercontent.com/94664744/162618862-7efc57dd-503e-4435-ad43-e4bdac3d9c8e.png)
  
  dan hasil varian
  # ![image](https://user-images.githubusercontent.com/94664744/162618907-324248a3-ed68-4eb9-aba2-5e5529a468d6.png)


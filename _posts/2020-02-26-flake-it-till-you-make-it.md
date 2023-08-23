---
layout: post
title: Git / Github
cover-img: /assets/img/git.png
subtitle: Git Kurulumu ve Git komutları
---

Git, projenin geçmişindeki değişiklikleri izlemek   
ve birden fazla geliştiricinin aynı proje içerisinde çalışmasını sağlamak   
için kullanılan versiyon kontrol sistemidir.  

### Git Terminal ile Yapılandırılması  

Sırada ise Git'i yapılandırcağız. Github hesabımızla eşlenecek.  
Eğer Github hesabınız yok ise hesap açmak için [buradan](https://github.com/) ulaşabilirsiniz.  
Aşağıda görmüş olduğunuz adınızı ve e-posta adresinizi kendi Github bilgilerinize göre değiştirin.  
`git config --global color.ui true `  
`git config --global user.name "YOUR NAME" `  
`git config --global user.email "YOUR@EMAİL.com" `  
`ssh-keygen -t ed25519 -C "YOUR@EMAİL.com" `  

Bir sonraki adım olarak aşağıdaki komutun çıktısını kopyalayın ve buradaki <https://github.com/settings/ssh> linke giderek new SHH key yerine yapıştırın.    
`cat ~/.ssh/id_ed25519.pub`             
Herşeyi yaptıktan sonra işe yaradığını anlamanız için aşağıdaki komutu yazın.    
`ssh -T git@github.com`    
Bunu yazdıktan sonra böyle bir mesaj alıyorsan herşeyi doğru yapmışsındır.  
 **Hi excid3!** You've successfully authenticated, but GitHub does not provide shell access.

### Git Komutları  

Bir klasör oluşturup içerisinde  
`git init`  
fonksiyonu çalıştırdığımızda .git altında dosya yönetim sistemi oluşturur.   
Bu komutu yazmadan git komutlarını dosyanızda kullanamazsınız.  

a.txt ve b.txt dosyaları üstünde çalıştınız ve bu dosyaların durumunu görmek için  
kullanacağınız komut ise  
`git status`  
komutudur.  

a.txt, b.txt dosyalarını staging alana göndermek için ise  
`git add`  
komutunu kullanabiliriz.  

Staging alanında olan dosyanızı çıkarmak için  
`git reset HEAD "filename"`  
komutunu kullanabilirsiniz.  

Aşağıdaki komutu kullanarak dosyalarınızı Local Reponuza kaydedebilirsiniz   
`git commit -m "msg"`   

Tarayıcıdaki deponuza göndermek için ise  
`git push origin master`  
komutunu kullanabilirsiniz.  

Önceki yaptığımız commit mesajlarının içeriğini ve tarihçesini görmek için ise  
`git log `  
komutunu kullanabilirsiniz.  

Hangi branchde çalıştığınızı görmek için  
`git branch`  
komutunu kullanabilirsiniz.  

`git stash`  
değişiklikleri commit'lemeden yerel depoya kaydetmeyi sağlayan bir araçtır.   

`git diff`  
komutu dosyada hangi alanların değiştiğini görmek için kullanılır.   

`git checkout -dosyaadi`  
komutu ile değişikliği geriye alabilirsiniz.  

`git  shows`  
komutu ile commit içersinde yapılan değişiklikleri görebilirsiniz.  

`git merge`  
komutu ile başka bir branch'deki değişiklikleri kendi çalıştığınız branch'inize entegre etmenize yarar.  

`git pull`  
komutu ile ana proje dosyasındaki yaptığınız değişiklikleri bilgisayarınızdaki versiyona çekmeye yarar.  

`git config`  
komutu ile bilgisayarınızdaki git terminalini kendi github hesabınıza bağlamaya yarar.  make it.
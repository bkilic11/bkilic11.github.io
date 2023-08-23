---
layout: post
title: Ruby On Rails
cover-img: /assets/img/images.jpeg
subtitle: Ruby On Rails Kurulumu
--- 
Genellikle Rails olarak anılan Ruby on Rails (RoR), Ruby programlama dilinde yazılmış açık kaynaklı bir web uygulama çerçevesidir. Ortak görevleri basitleştiren bir dizi kural, en iyi uygulama ve önceden oluşturulmuş araçlar sağlayarak web geliştirmeyi daha hızlı ve daha kolay hale getirmek için tasarlanmıştır.
## Ruby On Rails Kurulum
Ruby On Rails kurmaya Homebrew kurarak başlıyalım.  
**Homebrew**, yazılım paketlerini kaynaktan kolayca kurmamızı ve derlememizi sağlar.  
Terminal'i açın ve aşağıdaki komutu yazın
       
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`  

Sonra Ruby'yi **ASDF** adlı bir sürüm yöneticisi kullanarak kuracağız.  
**ASDF** kullanmamızın nedeni ise rbenv, rvm, **ASDF** Node.js gibi diğer dilleride yönetebiliyor.         
**ASDF** kurmak basittir. Şimdi ise **ASDF** kuralım. Aşşağıdaki kodları sırasıyla yazın.                  
          
`cd`                            
`git clone https://github.com/excid3/asdf.git ~/.asdf`           
`echo '. "$HOME/.asdf/asdf.sh"' >> ~/.zshrc`  
`echo '. "$HOME/.asdf/completions/asdf.bash"' >> ~/.zshrc`  
`echo 'legacy_version_file = yes' >> ~/.asdfrc`  
`exec $SHELL`  
`asdf plugin add ruby`  
`asdf plugin add nodejs`  

Şimdi ise yolumuza **Ruby** kurmakla devam edelim.
**Ruby** kurmak için ilk önce kuracağınız sürümü bilmeniz gerekmektedir.  
Tavsiye olarak en güncel sürümü kurmanızı tavsiye ederim.   
<https://www.ruby-lang.org/en/downloads/> web sitesine gidip en güncel sürümü öğrenebilirsiniz.    
Şimdi kodumuzu yazmaya başlayalım.  
`asdf install ruby 3.2.2`  
`asdf global ruby 3.2.2`  
`gem update --system`  

Bunları yaptıktan sonra ruby kurmuş olacaksınız. Görmek için ise aşağıdaki komutları yazabilirsiniz.  
`which ruby`  
#=> /Users/username/.asdf/shims/ruby  
`ruby -v `  
#=> 3.2.2   

Daha sonra Rails projelerimizde Javascript'i eklemek için Node.js'yi kurabilirsiniz.  
`asdf install nodejs 18.16.1`  
`asdf global nodejs 18.16.1`  
`which node`  
#=> /Users/username/.asdf/shims/node  
`node -v`  
#=> 18.16.1   
`npm install -g yarn`  

Sırada **Rails** kurulumu var. **Rails** kurmak için ilk önce sürüm seçmeniz gerekmektedir.  
**Rails** En güncel sürümü öğrenmek için [buraya tıklayarak](https://rubyonrails.org/) gidebilirsiniz.  
Tavsiye olarak Ruby de olduğu gibi en güncel sürümü seçmenizi öneririm.  
Sürümünüzü seçtikten sonra aşağıdaki adımları yapmaya başlayalım.  
`gem install rails -v 7.0.6`  
**Rails**'i artık kurmuş bulunmaktayız. Kontrol etmek için aşağıdaki komutu çalıştırın  
`rails -v `  
#> Rails 7.0.6  
Çıktısını alabiliyorsanız bir sorun yok demektir.  

Sıradaki adım olarak veritabanı kuracağız veritabanı kurmak için ilk önce bir veritabanı belirlemeniz gerekmektedir.  
Kullanmadığınız veritabanını kurmanıza gerek yok. Veritabanları:

* MySQL  
**MySQL** kurmak için aşağıdaki komutu yazabilirsiniz.  
`brew install mysql`  
Bu komutu yazdığınızda size çalıştırmanız için bi kaç talimat vericek ordaki talimatları uygulayın.  
Uyguladıktan sonra aşağıdaki komutu çalıştırın.   
`brew services start mysql`  
Artık **MySQL** de kurmuş bulunmaktasınız.         

* PostgreSQL   
Eğer ki **PostgreSQL** kurmak istiyorsanız aşağıdaki adımları takip edebilirsiniz.  
`brew install postgresql`  
Bu komutu çalıştırdığınızda size bir kaç komut vericek. O komutları da yaptıktan sonra aşağıdaki komutu çalıştırın.  
`brew services start postgresql`  
Ve artık veritabanınızı da kurmuş bulunmaktasınız.  

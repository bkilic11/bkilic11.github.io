---
layout: post
title: Rails Blog Uygulaması
cover-img: assets/img/rails3.png
subtitle: Rails uygulması nasıl açılır ve uygulamada neler öğrendim
---
Burada Rails ile kendi yaptığım blog uygulamasını bulabilirsiniz. Örnek olarak bazı gemleri kullanarak blog uygulaması yaptım.  
Kendi github adresimde kodları bulabilirsiniz.  

### Rails Uygulaması nasıl açılır  
Terminalizi açın  
`cd Desktop` yazın.  
Daha sonra aşağıdaki adımları takip ederek Rails projesi oluşturun.
- **rails new myapp** "veritabanı kullanmadan oluşturmak için"
- **rails new myapp -d postgresql** veya **rails new myapp -d mysql** "hangi veritabanını kullanmak istiyorsanız onu yazabilirsiniz.  
- **cd myapp** "yazarak projenizin içine gidin"
- **rake db:create** "yazarak veritabanınızı oluşturabilirsiniz."    
- **rails server** "yazdığınızda artık serverınız çalıştırdığınız anlamına gelmektedir."
- tarayıcınızı açtıktan sonra http://localhost:3000 adresine giderek rails projenizi çalıştırdığınızı görebilirsiniz.       

#### Blog Uygulamasını Yaparken Neler öğrendim      

Rails blog uygulaması başlangıçta yapabilceniz uygulamalardan bir tanesidir. Rails yazmaya başlayan kişilerin genellikle ilk başladığı uygulamalardan bir tanesidir. Burada bu uygulamayı yazarken neler öğrendim. Bunlardan bahsedeyim.  

1. Resources komutu ile birlikte CRUD işlemlerini routes'a tek tek yazmaktan kurtuldum ve tek bir satırda bütün işlemleri halletim.  
2. Rails koduma resim eklemek için "gem image_processing" kütüphanesini ekledim ve kolayca resim ekleyebildim.
3. Resimi ekranımda göstermek için image_tag komutunu nasıl kullanacağımı öğrendim.
4. Resimi yüklemek için ise file_field komutu olduğunu öğrendim.
5. Arama filtresi ekledim bunun için Rails kütüphanesi olan "gem ransack" ekledim. 
6. Byebug gemini kurdum ve neden ve nasıl kullanıldığını öğrendim.
7. Daha sonra nasıl hata mesajı ekrana yazdırılır bunu öğrendim flash[:alert] komutunu kullanarak.
8. has_many ve belongs_to yapısını öğrendim.
9. Attığım posta nasıl yorum eklenir ve nasıl silinir. Bunları öğrendim.
10. Silme işlemlerini yaparken button_to kullanıldığını öğrendim.
11. Attığım postun yorumun ne zaman atıldığını gösteren kod <%= comment.created_at.strftime('%d-%m-%Y %H:%M:%S) %>
12. DRY Don't Repeat Yourself (Kendini Tekrar Eden) kod yazarken tekrara düşmemek için temiz bir kod olması için söylenen bir hatadır.
13. Dependent: :destroy sahibi yok edildiğinde ona ait olan herşeyi siler.

##### Blog Uygulamasını Görmek İçin  
<https://github.com/bkilic11/Blog>

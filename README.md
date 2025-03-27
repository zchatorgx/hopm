HOPM (Hybrid Open Proxy Monitor) Kurulum ve Yapılandırma Kılavuzu

1️⃣ Giriş

Bu belge, HOPM (Hybrid Open Proxy Monitor) botunun nasıl yapılandırılacağını anlatır. Bot, IRC sunucularında açık proxy taraması yapmak için kullanılır.

Bu kılavuz, özellikle IP adresinin ve oper şifresinin nasıl değiştirileceğini vurgular.

2️⃣ Ön Koşullar

HOPM'yi çalıştırmadan önce sisteminizin aşağıdaki gereksinimleri karşıladığından emin olun:

Bir IRC sunucusu (UnrealIRCd, InspIRCd vb.)

GCC ve gerekli kütüphaneler

Bir shell (Linux sunucu önerilir)

HOPM kaynak kodu

3️⃣ Kurulum

HOPM'yi aşağıdaki adımları takip ederek kurabilirsiniz:

# Kaynak kodu klonlayın veya indirin
git clone https://github.com/xyz/hopm.git
cd hopm

# Yapılandırmayı başlatın
./configure --prefix=$HOME/hopm

# Derleyin ve yükleyin
make && make install

Kurulum tamamlandıktan sonra yapılandırma ayarlarını güncellemeniz gerekir.

4️⃣ Yapılandırma (hopm.conf)

HOPM'nin çalışabilmesi için hopm.conf dosyasındaki şu ayarları güncelleyin.

1️⃣ IP Adresinizi Güncelleyin

HOPM'nin bağlanması gereken IRC sunucusunu tanımlamak için server ayarını değiştirin:

🚫 Örnek (Değiştirmeniz Gereken Yer):

server = "irc.example.com";

✅ Doğrusu (Kendi IRC Sunucunuz ile değiştirin):

server = "irc.seninircadresin.com";

2️⃣ Oper Şifrenizi Değiştirin

HOPM'nin oper olarak giriş yapabilmesi için oper_password değerini güncelleyin:

🚫 Örnek (Değiştirmeniz Gereken Yer):

oper_password = "123456";

✅ Doğrusu (Kendi Güçlü Şifreniz ile değiştirin):

oper_password = "GucluSifreniz";

5️⃣ HOPM'yi Çalıştırma

HOPM'yi başlatmak için şu komutu kullanabilirsiniz:

~/hopm/bin/hopm

Eğer arka planda çalışmasını istiyorsanız:

nohup ~/hopm/bin/hopm &

Yapılandırmanın doğruluğunu kontrol etmek için:

hopm -t

Eğer hata alırsanız, hopm.conf dosyanızda eksik veya yanlış bir yapılandırma olup olmadığını kontrol edin.

daha fazla bilgi için https://cadde.org & https://zchat.org chat sohbet odaları 

Tabii ki, `dbURI` değişkeninin kullanıcı tarafından değiştirilmemesi önemli. Aşağıda, README dosyanızı bu durumu dikkate alacak şekilde düzenlemiş bir örnek bulunmaktadır:

# MongoDB ile Backend Projesi

Bu proje, MongoDB veritabanını kullanarak basit bir backend uygulamasını içermektedir. Aşağıdaki adımları takip ederek projeyi kullanabilirsiniz.

## Kurulum

1. **Node.js ve npm Kurulumu:**
   Bilgisayarınızda Node.js ve npm yüklü olmalıdır. [Node.js indirme sayfası](https://nodejs.org/) üzerinden indirebilirsiniz.

2. **Proje İndirme:**
   Bu depoyu bilgisayarınıza klonlayın veya ZIP olarak indirin.

   ```bash
   git clone https://github.com/kullanici_adi/proje.git
   cd proje
   ```

3. **Bağımlılıkların Yüklenmesi:**
   Ana dizinde aşağıdaki komutu çalıştırarak bağımlılıkları yükleyin.

   ```bash
   npm install
   ```

4. **MongoDB Bağlantısı:**
   `db.js` dosyasındaki `dbURI` değişkenini **değiştirmeyin**, çünkü bu önceden yapılandırılmış bir MongoDB'ye yönlendirmektedir.

## Veritabanını Başlatma

1. Terminal veya komut istemcisinde aşağıdaki komutu çalıştırarak MongoDB veritabanına bağlanın:

   ```bash
   node db.js
   ```

## Veri Eklemek

1. `venue.js` dosyasında tanımlanan veri modeline uygun olarak, `db.js` içine yeni veri ekleyen komutları ekleyebilirsiniz. Örnek:

   ```javascript
   const Venue = mongoose.model("venue");
   
   const yeniVenue = new Venue({
     // Yeni veri detayları
   });

   yeniVenue.save((err) => {
     if (err) throw err;
     console.log("Yeni venue başarıyla eklendi.");
   });
   ```

## Uygulamayı Çalıştırma

1. Terminal veya komut istemcisinde aşağıdaki komutu çalıştırarak uygulamayı başlatın:

   ```bash
   npm start
   ```

2. Tarayıcınızı açın ve `http://localhost:3000` adresine giderek uygulamayı görebilirsiniz.

Bu kadar! Şimdi projenizi kendi verilerinizle kullanmaya hazırsınız. İyi çalışmalar!

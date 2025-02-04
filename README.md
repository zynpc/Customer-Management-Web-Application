# ASP.NET Core 8 MVC Müşteri Uygulaması

Bu proje, **ASP.NET Core 8 MVC** kullanarak bir **Müşteri Yönetim Sistemi** oluşturmayı amaçlamaktadır. Uygulama, **CRUD (Create, Read, Update, Delete)** işlemlerini gerçekleştirerek SQL Server ile veri yönetimi sağlar.

## Proje İçeriği

- **ASP.NET Core 8 MVC** kullanılarak geliştirildi.
- **Entity Framework Core** ile SQL Server'a bağlantı sağlandı.
- **Müşteri Kayıt Yönetimi** için temel CRUD işlemleri uygulandı.
- **Razor View Engine** ile sayfalar oluşturuldu.
- **Dependency Injection (Bağımlılık Enjeksiyonu)** prensibi kullanıldı.

## Kurulum

### 1. **Gereksinimler**
- .NET 8 SDK
- Visual Studio 2022 (veya daha yeni bir IDE)
- SQL Server (veya Azure SQL)
- Git (opsiyonel)

### 2. **Projeyi Klonlama**
```bash
 git clone <repository-url>
 cd WebApplication1
```

### 3. **Bağımlılıkları Yükleme**
Proje klasöründe bu komutu çalıştırın: dotnet restore


### 4. **Veritabanı Yapılandırması**
Projede **appsettings.json** dosyası içindeki `DefaultConnection` ayarını kendi SQL Server bağlantı dizesine göre güncelleyin.

**appsettings.json:**

"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=CustomerDB;Trusted_Connection=True;"
}


Ardından, veritabanını oluşturmak için şu komutu çalıştırın: dotnet ef database update


### 5. **Projeyi Çalıştırma**
 dotnet run

Veya Visual Studio üzerinden **F5** tuşuna basarak projeyi çalıştırabilirsiniz.

## Kullanım

1. **Müşterileri Listeleme**: `/customer/index` sayfasında tüm müşterileri görebilirsiniz.
2. **Yeni Müşteri Ekleme**: `/customer/create` sayfasında yeni bir müşteri ekleyebilirsiniz.
3. **Müşteri Güncelleme**: `/customer/edit/{id}` sayfasından mevcut bir kayıt güncellenebilir.
4. **Müşteri Silme**: `/customer/delete/{id}` sayfasından bir kayıt silinebilir.

## Kullanılan Teknolojiler

- **ASP.NET Core 8 MVC**
- **Entity Framework Core 6**
- **SQL Server**
- **Bootstrap & Razor Pages**

## Sorun Giderme

Eğer paketler eksikse: dotnet restore


Eğer bağlantı hatası alırsanız, SQL Server bağlantı dizesini kontrol edin ve sunucunun çalıştığından emin olun.

## Lisans
Bu proje **MIT Lisansı** altında sunulmuştur.



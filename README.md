Bu uygulama, MongoDB veritabanı kullanarak kategori yönetimini sağlayan bir sistemdir ve CRUD (Oluşturma, Okuma, Güncelleme, Silme) işlemleri ile veri yönetimini etkin bir şekilde gerçekleştirir. Uygulama aşağıdaki bileşenleri içerir:

Modüller:
Status Enum: Kategorilerin durumlarını tanımlar (Active, Modified, Passive).
BaseEntity Sınıfı: Veritabanı belgeleri için ortak özellikler sunar, örneğin durum, oluşturulma tarihi, makine adı ve IP adresi gibi bilgileri yönetir.
Category Sınıfı: Kategoriye ait temel özellikleri (isim, açıklama) tanımlar ve BaseEntity sınıfını miras alarak ortak bilgileri alır.
BaseService Sınıfı: CRUD işlemleri için temel metodları tanımlar (create, get_all, get_by_id, update).
CategoryService Sınıfı: BaseService sınıfını miras alarak, kategorilerle ilgili tüm işlemleri gerçekleştirir (kategori ekleme, listeleme, güncelleme ve silme).
MongoDB Bağlantısı: MongoDB veritabanına bağlanarak, kategori verilerinin bulunduğu categories koleksiyonuna erişim sağlar.

Kullanıcı Etkileşimi: Kullanıcı, terminal üzerinden aşağıdaki işlemlerden birini seçerek veri ile etkileşime geçebilir.
create: Yeni bir kategori ekler.
read all: Veritabanındaki tüm aktif ve modifiye olmuş kategorileri listeler.
read by id: Belirli bir kategori ID’sine göre kategori bilgilerini getirir.
update: Mevcut bir kategorinin bilgilerini günceller.
delete: Kategoriyi "Passive" durumuna getirerek etkisizleştirir.
Özet: Bu uygulama, MongoDB ile entegre çalışan ve kullanıcıların kategori verilerini yönetmesini sağlayan etkileşimli bir sistemdir. CategoryService sınıfı, kategori verilerini oluşturma, okuma, güncelleme ve silme gibi temel işlemleri gerçekleştirerek kullanıcıya esneklik ve verimlilik sunar.

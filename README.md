# Admin Ayarları

### Kimlik Doğrulama Yönetimi

#### Ek Kimlik Doğrulama kaynakları ekleme

Mangle, Active Directory'nin ek bir kimlik doğrulama kaynağı olarak kullanılmasını destekler.
Ayarlar için aşağıdaki adımları takip ediniz:

1. Mangle'a yönetici kullanıcı olarak giriş yapın.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc) -----> Auth Management -----> Auth Source .
3. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacUUjSyzEtnTn8YES%2FAuthSourceButton.png?alt=media&token=293d3f41-b50e-4f8b-94a0-5a8414741f42) tıkla.
4. URL, Domain bilgisi girin ve Submit'e tıklayın.
5. Başarılı mesaj "Auth sources will be updated with the new entry."
6. Desteklenen işlemleri görmek için tablo girişine ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-Lead2bNkR2AZju-PTuh%2FSupportedActionsButton.png?alt=media&token=b99be285-99bb-42ed-b6b9-9100d4664a4c) tıklayın.

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen Mangle Kullanıcı Arabiriminden -----> API Belgeleri bağlantısına gidin veya https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/user-management-controller

### Kullanıcı Ekleme/İçe Aktarma (Adding/Importing Users)

Mangle, yeni yerel kullanıcıların eklenmesini veya ek kimlik doğrulama kaynakları olarak eklenen Active Directory kaynaklarından kullanıcıların içe aktarılmasını destekler.
Ayarlar için aşağıdaki adımları takip ediniz:

1. Mangle'a yönetici kullanıcı olarak giriş yapın.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc) -----> Auth Management -----> Users .
3. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacNaxtg1iNbB1FcFT%2FAddUserButton.png?alt=media&token=aa913a92-fd20-401e-8e0c-4b3634701a03) tıklayın.
4. Seçilen Kimlik Doğrulama Kaynağı "mangle.local" ise Kullanıcı Adını, Kimlik Doğrulama Kaynağını ve Parolayı girin, uygun bir rol ve Gönder'e tıklayın.
5. Başarılı mesaj "Users will be updated with the new entry."
6. Desteklenen işlemleri görmek için bir tablo girişinin karşısındaki ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-Lead2bNkR2AZju-PTuh%2FSupportedActionsButton.png?alt=media&token=b99be285-99bb-42ed-b6b9-9100d4664a4c) işaretine tıklayın.

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen Mangle Kullanıcı Arabiriminden -----> API Documentation from the Mangle UI or access https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/user-management-controller

### Varsayılan ve Özel Roller

Mangle aşağıdaki varsayılan Rollere ve Ayrıcalıklara sahiptir.
| Varsayılan Rol | Varsayılan Ayrıcalıklar | İzin Verilen İşlemler |
|----------|:-------------:|------:|
| ROLE_READONLY | READONLY | Tüm uç noktalara, hatalara, isteklere, dayanıklılık puanı sorgularına ve hizmetlere Okuma Erişimi. Yönetici ayarlarına veya etkinliklerine erişim yok. |
| ROLE_ADMIN | ADMIN_READ_WRITE, USER_READ_WRITE | Tüm özelliklere ve Yönetici ayarlarına erişim |
| ROLE_USER | ADMIN_READ, USER_READ_WRITE | Tüm uç noktalara, hatalara, isteklere, dayanıklılık puanı sorgularına ve hizmetlere Ekleme, Düzenleme, Silme ve Çalıştırma ayrıcalıkları. Yönetici ayarlarına veya etkinliklerine erişim yok. |

Mangle, mevcut olan varsayılan ayrıcalıklardan özel rollerin oluşturulmasını destekler.
Ayar düzenlemeleri için adımları takip edin:

1. Mangle'a yönetici kullanıcı olarak giriş yapın.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc) -----> Auth Management -----> Roles gidin.
3. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-Lead-oNq_aUxqb48NTE%2FCustomRoleButton.png?alt=media&token=2030c4bf-ddf9-489e-b55f-0e0881602759) tıklayın.
4. Role Name, Privileges bilgisi girin ve onaylayın.
5. Başarılı mesaj: "Roles will be updated with the new entry"
6. Desteklenen işlemleri görmek için bir tablo girişinin karşısındaki ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-Lead2bNkR2AZju-PTuh%2FSupportedActionsButton.png?alt=media&token=b99be285-99bb-42ed-b6b9-9100d4664a4c) işaretine tıklayın.

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen bağlantıya gidin -----> API Documentation from the Mangle UI or access https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/role-controller

### Konfigürasyon

**Loglama**
**Log Seviyeleri**
Mangle, uygulama için log seviyelerinin değiştirilmesini destekler.
Düzenlemeler için adımları takip edin:

1. Mangle'a yönetici kullanıcı olarak giriş yapın.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc)-----> Configuration -----> Logging gidin.
3. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Lepw3Cs0ncVRHDzl2qz%2F-LepxSe1P-Be6pMvVAzD%2FLoggerButton.png?alt=media&token=897c22d6-4541-4442-bdf3-406febd61f67) tıklayın.
4. Logger name, Configured Level, Effective Level bilgisi girin ve işlemleri onaylayın.
5. Başarılı mesaj "displayed and the table for Log levels will be updated with the new entry."
6. Desteklenen işlemleri görmek için bir tablo girişinin karşısındaki ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-Lead2bNkR2AZju-PTuh%2FSupportedActionsButton.png?alt=media&token=b99be285-99bb-42ed-b6b9-9100d4664a4c) işaretine tıklayın.

![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRQ949udVzp2CIDU-09%2F-MRUSm5P8NxiNzzFpA2a%2FApplication_Log.png?alt=media&token=74d3dcf7-f442-4cea-849c-2e88e28c6e38) kullanıcı arabiriminde günlüğü açar ve periyodik olarak otomatik olarak yenilenir.
![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRQ949udVzp2CIDU-09%2F-MRUT-1ZIzoMAGJRgtJx%2FDownload_Bundle.png?alt=media&token=51cfae6b-706a-48b2-afe1-53b3c5a7eb44) destek paketini mangle sunucusundan yerel bir dosya dizinine indirmenize ve kaydetmenize izin verecektir. Kümelenmiş bir Mangle kurulumu durumunda, destek paketini tüm düğümlerden almak için kümedeki her düğüm için eylem tekrarlanmalıdır.

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen bağlantıya gidin-----> API Documentation from the Mangle UI or access https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/operation-handler

### Cluster Config

Cluster config bölümü, Mangle deployment modu ve kümelenmiş bir Mangle dağıtımı durumunda kurulumu oluşturan çeşitli nodes hakkında ayrıntılar sağlar. Kullanıcı arabirimi aracılığıyla çekirdek ayarlarını değiştirebilir ve dağıtım türleri arasında geçiş yapabilirsiniz.

Düzenlemeler için adımları takip edin:

1. Mangle'a yönetici kullanıcı olarak giriş yapın.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc)-----> Configuration -----> Cluster Config.

Sayfa cluster name, the validation token, members, quorum and deployment mode bilgilerini tablo formunda görüntülenir. Quorum and deployment mode arayüz ile düzenlenebilir.

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen bağlantıya gidin-----> API Documentation from the Mangle UI or access https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/cluster-config-controller

### Hata Eklentileri (Fault Plugins)

Bu bölüm, Mangle Github reposunda zaten mevcut olan özel hataları veya Kullanıcı Kılavuzunun Custom Faults bölümünde belirtilen adımları kullanarak oluşturduğunuz yeni bir hatayı, çalışan mevcut bir Mangle örneğine yüklemenizi sağlar.

Düzenlemeler için adımları takip edin:

1. Mangle'a yönetici kullanıcı olarak giriş yapın.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc) -----> Configuration -----> Fault Plugins.
3. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRQ949udVzp2CIDU-09%2F-MRUsRFiVzDFUVHIFq-H%2FLoad_Plugin.png?alt=media&token=3d8dded6-a420-48ab-99ff-800ee1746e4c) Tıklayın
4. Kullanım Kılavuzunun **Custom Faults** bölümünde belirtilen adımları izledikten sonra oluşturulan eklenti zip dosyasını seçin.
5. Onaylayın.
6. Başarılı Mesaj "Plugins will be updated with the new entry."
7. Desteklenen işlemleri görmek için bir tablo girişinin karşısındaki ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-Lead2bNkR2AZju-PTuh%2FSupportedActionsButton.png?alt=media&token=b99be285-99bb-42ed-b6b9-9100d4664a4c) işaretine tıklayın.

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen bağlantıya gidin -----> API Documentation from the Mangle UI or access https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/plugin-controller

### Esneklik Puan Metrik Yapılandırması (Resiliency Score Metric Configuration)

Esneklik Puanı, test edilen uygulamanın veya sistemin esnekliğini veya hataya dayanıklılık kapasitesini ölçmenizi sağlayan ilgi çekici yeni bir özelliktir. Puan, hata yerleştirme sırasında kullandığınız izleme aracından seçtiğiniz uygulama ölçümleri alınarak hesaplanır. Puan daha sonra, belirli bir süre boyunca izlenebilen ve takip edilebilen bir metrik olarak izleme aracına geri gönderilir.
Esneklik puanı hesaplamalarını etkinleştirmek için gereken yapılandırma, Yönetici ayarları aracılığıyla yapılmalıdır.
Düzenlemeler için adımları takip edin:

1. Mangle'a yönetici kullanıcı olarak giriş yapın.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc)-----> Configuration -----> Resiliency Score Metric Configuration.
3. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) Tıklayın.
4. Aşağıdaki girişleri sağlayın:
   4.1. Yapılandırma için bir ad
   4.2. Metrik Adı - Esneklik puanı metrikleri, izleme aracında bu ad kullanılarak saklanacaktır, örneğin: mangle.resiliency.score),
   4.3. Metrik kaynak adı - Kaynak, izleme aracında dayanıklılık puanı metriklerini kolayca filtrelemek için kullanılabilir.
   4.4. Test Referans Penceresi - Bu, sistemin testten önceki ve sonraki durumu için bir referans görevi görecek olan bir hata yerleştirme olayından önceki ve sonraki zaman penceresini ifade eder. Bu değer dakika cinsinden belirtilmelidir.
   4.5. Hesaplama Penceresi - Mangle, yapılandırılan hesaplama penceresine göre izleme sisteminden zaman serisi verilerini alacaktır. Bu değer saat cinsinden belirtilmelidir.
   4.6. Zaman serisi verilerinin ayrıntı düzeyi(Granularity of the time series data) - Bu, izleme sisteminden alınan verilerin ayrıntı düzeyini belirlemek içindir. Saniye, dakika, saat ve gün cinsinden olabilir.
5. Onaylayın.
6. Başarılı mesaj "Resiliency Metric Configuration will be updated with the new entry."
7. Desteklenen işlemleri görmek için bir tablo girişinin karşısındaki ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-Lead2bNkR2AZju-PTuh%2FSupportedActionsButton.png?alt=media&token=b99be285-99bb-42ed-b6b9-9100d4664a4c) işaretine tıklayın.

> **LÜTFEN AKLINIZDA BULUNDURUN:
> Esneklik puanı hesaplaması için yalnızca bir yapılandırma oluşturulabilir.
> Bu özellik hala değerlendirme aşamasındadır ve yalnızca VMware Wavefront tarafından desteklenir. Diğer izleme sistemleri için destek sağlaması için Mangle'a ihtiyacınız varsa, lütfen Mangle Github altında bir özellik isteği oluşturun. https://github.com/vmware/mangle/issues **

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen bağlantıya gidin-----> API Documentation from the Mangle UI or access https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/resiliency-score-controller

### Entegrasyonlar (Integrations)

**Metric Sağlayıcıları**
Mangle, ölçüm sağlayıcılar olarak Wavefront, Datadog veya Dynatrace'in eklenmesini destekler. Bu, hata enjeksiyonu ve düzeltme hakkındaki bilgilerin bu araçlara olaylar olarak yayınlanmasını sağlar ve böylece bunların izlenmesini kolaylaştırır.
Düzenlemeler için adımları takip edin:

1. Mangle'a yönetici kullanıcı olarak giriş yapın.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc) -----> Integrations -----> Metric Providers gidin.
3. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Lepw3Cs0ncVRHDzl2qz%2F-Leq2UFQ2fnvUel-5KVt%2FMonitoringToolButton.png?alt=media&token=b952ff39-0bfd-48b9-af28-266f70e99f74) Tıklayın.
4. Wavefront, Datadog or Dynatrace seçin, kimlik bilgilerini sağlayın ve işlemi onaylayın.
5. Başarılı Mesaj "Monitoring tools will be updated with the new entry."
6. Desteklenen işlemleri görmek için bir tablo girişinin karşısındaki ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-Lead2bNkR2AZju-PTuh%2FSupportedActionsButton.png?alt=media&token=b99be285-99bb-42ed-b6b9-9100d4664a4c) işaretine tıklayın.

Bir metrik sağlayıcı eklendiğinde Mangle, enjekte edilen ve düzeltilen her hata için olayları otomatik olarak etkin sağlayıcıya gönderir. Gereksinim, Mangle'ı bir uygulama olarak metriklerine bakarak izlemekse, Mangle uygulama metriklerinin ilgili metrik sağlayıcıya gönderilmesini etkinleştirmek için ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRQ949udVzp2CIDU-09%2F-MRUxyKWvzIJNKYcGLfr%2FSend_Metrics.png?alt=media&token=f017707e-9265-4f85-8158-d3114f2792fc) düğmesine tıklayın.

> **Dynatrace Entegrasyonu hakkında notlar:
> Cihaz Kimliği: Dynatrace'in kullanıcı arayüzünde görünecek olan özel cihazın adı. Özel cihaz, Dynatrace'te yalnızca Mangle'da "Send Metric" seçeneği etkinleştirilerek oluşturulacaktır. Mangle'ın uygulama ölçümleri, Mangle'da "Send Metric" seçeneğini etkinleştirdikten sonra,
> Dynatrace'te belirtilen cihaz kimliği altında görünür olacaktır.
> Dynatrace, bir uygulama tarafından raporlanan metrikler için aynı boyutları bekler. Bu nedenle, birden fazla Mangle örneği dağıtımınız varsa, Mangle metrik sağlayıcısını yapılandırırken lütfen aynı "key" "tags" seçeneğinin altına ekleyin (değerler farklı olabilir).**

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen bağlantıya gidin -----> API Documentation from the Mangle UI or access https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/operation-handler

### Bildirici (Notifier)

Mangle, hatalar uç noktalara enjekte edilirken Slack'i bir bildirim olarak destekler.
Düzenlemeler için adımları takip edin:

1. Mangle'a yönetici kullanıcı olarak giriş yapın. 2.![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacRGnZgE8i-v4kGwo%2FSettings.png?alt=media&token=8d4c0478-f36e-4369-a3bf-068f716763fc) -----> Integrations -----> Notifier gidin.
2. ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRQ949udVzp2CIDU-09%2F-MRUwEYBcU5Z0FDN1ZxS%2FNotifier.png?alt=media&token=df52ad13-bd7a-45a4-b22b-d37017548c4a) Tıklayın.
3. Bir Ad, Slack OAuth Token ve yayınlanacak uygun kanal adlarını sağlayın.
4. Bağlantıyı test edin ve işlemi onaylayın.
5. Başarılı mesaj "the table for Notifiers will be updated with the new entry."
6. Edit and Delete ayarları desteklenir.

Bu konfigürasyondan sonra, hata yürütme sırasında uygun bir bildirim seçebileceksiniz. Uygun bitiş noktasına bir hata enjekte edildiğinde, Slack'e aşağıdakine benzer bir bildirim gönderilir.

![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRQ949udVzp2CIDU-09%2F-MRUzhNc4cYXu1a18k0R%2FSlack_Notification.png?alt=media&token=a88b2e24-bd06-45ab-be62-5b1b4adda967)

> **İlgili API listesi**
> Swagger belgelerine erişim için lütfen bağlantıya gidin -----> API Documentation from the Mangle UI or access https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/notifier-controller

# OCP üzerinde Mangle kurulumu

İlgili tüm YAML dosyaları, aşağıdaki Mangle git deposunda mevcuttur. [Github](https://github.com/vmware/mangle/tree/master/mangle-support/kubernetes)

1- mangle adlı bir namespace oluşturun

    oc new-project mangle --description="description" --display-name="mangle"
    veya
    oc create namespace mangle

2- Cassandra pod ve service'i oluşturun
oc create -f https://github.com/vmware/mangle/blob/master/mangle-support/kubernetes/cassandra.yaml

    oc create -f https://github.com/vmware/mangle/blob/mastermangle-support/kubernetes/cassandra-service.yaml

3- Mangle pod ve service'i oluşturun

    oc create -f https://github.com/vmware/mangle/blob/master/mangle-support/kubernetes/mangle.yaml

    oc create -f https://github.com/vmware/mangle/blob/master/mangle-support/kubernetes/mangle-service.yaml

# Mangle Kullanım Kılavuzu

Bu Mangle Kullanım Kılavuzu, uç noktaların nasıl ekleneceği(endpoints), hataların nasıl çalıştırılacağı(faults), dayanıklılık puanının(resiliency score) nasıl oluşturulacağı ve raporların(reports) nasıl görüntüleneceği hakkında bilgi sağlar.

##### Hedef kitle

Bu kılavuz, beklenmedik arızalara maruz kaldığında uygulamalarının dayanıklılığını değerlendirmek için altyapı veya uygulamalara karşı kaos deneyleri yapmak isteyen SRE, Developer ve Kaos Mühendislerine yöneliktir.

| Alt İçerik           | Tanım                                                                                                                                                            |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Endpoints Ekleme     | Hata enjeksiyonu için Endpoints Ekleme hakkında bilgi sağlar.                                                                                                    |
| Injecting Faults     | Belirli bir Endpoint'e enjekte edilebilecek hata türleri hakkında bilgi sağlar                                                                                   |
| Esneklik Puanı       | Dayanıklılık puanı metriklerinin nasıl oluşturulacağı ve Mangle kullanılarak otomatik olarak bir monitoring sistemine nasıl gönderileceği hakkında bilgi sağlar. |
| Talepler ve Raporlar | Enjeksiyonların ilerlemesi ve durumu hakkında bilgi sağlar                                                                                                       |

## Kimlik Bilgileri Ekleme (Adding Credentials)

### Neden kimlik bilgileri eklemeliyim?

Mangle, hataları çalıştırmak istediğiniz herhangi bir endpoint'e bağlanmak için kimlik bilgilerini(Credentials) kullanır. Böylece, Mangle'ın desteklediği endpoint için bir kimlik bilgisi türünüz olur ve kimlik bilgileri olmadan, Mangle herhangi bir hata çalıştıramaz.

Kimlik bilgileri, Mangle'da depolanmadan önce şifrelenir ve bu nedenle güvenlidir.

Kimlik bilgileri, aynı türden birden çok endpoint için uygun şekilde yapılandırılırsa, endpointler arasında yeniden kullanılabilir.

### Kimlik Bilgisi Türleri

Mangle'da desteklenen aşağıdaki endpointler, karşılık gelen bir kimlik bilgisinin sağlanmasını gerektirir.

**Uzak Makine:** SSH etkin bir username, password veya private key file kabul eder.
**Kubernetes (K8s) Cluster:** Bir K8s kubeconfig dosyasını kabul eder.
**VMware vCenter:** username ve password kabul eder.
**AWS:** Access key ID ve Secret Key kabul eder.
**Azure:** Client Application ID ve Client Application Secret Key kabul eder.
**Database:** Veritabanı türü, Veritabanı adı, kullanıcı adı, password ve port numarası kabul eder.

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Credentials `--->` Endpoint Credentials

- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJT9FoUJ1-Fx3FHZCV%2F-MRJXHvz-SnZj7fokMcC%2FAdd_Credentials.png?alt=media&token=b003eb7c-9428-467c-b816-4f1d21d010b7) tıklayın ve uygun endpoint türünü seçin.
- Uygun ayrıntıları girin ve **Submit** edin
- Bir başarı mesajı görüntülenir ve Credentials tablosu yeni girişle güncellenir.
- Kayıtlı tüm kimlik bilgileri için Düzenleme ve Silme işlemleri desteklenir.

## Adapter Ekleme (Adding Adapters)

Mangle, endpointlerin çoğunu destekler. Ancak, VMware vCenter gibi belirli tescilli endpointler, varsayılan olarak etkinleştirildiğinde CPU ve bellek kaynaklarını tüketen ek bağımlılıklar gerektirir. Mangle'ın varsayılan dağıtımını hafif hale getirmek ve VMware vCenter'ı desteklemek için gereken bağımlılıklar haricileştirildi ve **vCenter adapter** adı verilen ayrı bir konteynerde birleştirildi.

Mangle'ın vCenter'a karşı hatalar çalıştırmasını istiyorsanız, vCenter Adapter için ek bir konteyner deploy etmeli ve Adapter instance'ını Mangle altına eklemelisiniz.

### Mangle vCenter adapter konteyneri deploy etme

Mangle vCenter Adapter, vCenter'a özgü hataları enjekte etmek için bir hata enjeksiyon adaptörüdür. Mangle uygulamasından tüm vCenter işlemleri bu adaptör üzerinden gerçekleştirilecektir.

Aşağıdaki komutu çalıştırarak Mangle-vCenter konteyner loglarını Docker host'una bağlamak için dizinler oluşturun:

```sh
mkdir -p /var/opt/mangle-vc-adapter-tomcat/logs
```

Aşağıdaki komutu çalıştırarak, konteyner volume mounting(bağlama) için ana bilgisayar dizininde(Host Dir) izin verin:

Varsayılan kimlik bilgilerini kullanarak vCenter adapter konteynerini deploy etmek için docker hostunda aşağıdaki docker komutunu çalıştırın. Burada 8443 numaralı port, konteynerin mevcut olacağı dışa bakan port numarasıdır. Aşağıdaki komutu çalıştırmadan önce 8443 port numarasının başka bir uygulama tarafından kullanılmadığından emin olun. Aksi takdirde, boş bir port kullanmak için komutu değiştirin ve ardından çalıştırın.

```sh
docker run --name mangle-vc-adapter --log-opt max-size=10m --log-opt max-file=1 -v /var/opt/mangle-vc-adapter-tomcat/logs:/var/opt/mangle-vc-adapter-tomcat/logs -d -p <IP>:8080:8080 -p <IP>:8443:8443 mangleuser/mangle_vcenter_adapter:<VERSION>
```

Özel kimlik bilgilerini kullanarak vCenter adapter konteynerini deploy etmek için docker hostunda aşağıdaki docker komutunu çalıştırın. **< >** içindeki "new password"u kendi seçtiğiniz bir parolayla değiştirin. Burada 8443 numaralı port, konteynerin mevcut olacağı dışa bakan port numarasıdır. Lütfen aşağıdaki komutu çalıştırmadan önce 8443 port numarasının başka bir uygulama tarafından kullanılmadığından emin olun. Aksi takdirde, boş bir port kullanmak için komutu değiştirin ve ardından çalıştırın.

```sh
docker run --name mangle-vc-adapter --log-opt max-size=10m --log-opt max-file=1 -v /var/opt/mangle-vc-adapter-tomcat/logs:/var/opt/mangle-vc-adapter-tomcat/logs -d -p <IP>:8080:8080 -p <IP>:8443:8443 -e JAVA_OPTS="-DcustomAdminCred=<new password>" mangleuser/mangle_vcenter_adapter:<VERSION>
```

> **:warning:**
> vCenter adapter için API belgeleri şu adreste bulunabilir:
> `https://<NODE-IP>:<PORT>:/mangle-vc-adapter/swagger-ui.html`
> Bu URL erişilebilir ve ulaşılabilir durumdaysa, vCenter adapter beklendiği gibi deploy edildiği gibi çalışmaktadır.
> VCenter adapter, herhangi bir API çağrısına karşı kimlik doğrulaması gerektirir. Yalnızca bir kullanıcıyı destekler: **admin**.
> Konteyneri deploy ederken varsayılan kimlik bilgilerini kullandıysanız, `_password` `_admin`'dir. Aksi takdirde, parola deployment sırasında sağladığınız özel parola olacaktır. adapter tarafından desteklenen tüm post API'ler, vCenter bilgilerini bir request body olarak alacaktır.

### Adapter Çeşitleri

Şu anda vCenter Server için yalnızca tek bir adapter tipi desteklenmektedir. Ancak gelecekte, diğer VMware ürünleri için Adapterleri destekleme planları vardır.

#### vCenter Sunucu Adapter

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Adapters `--->` vCenter Adapter
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJY2jA5EWknbtl_DWn%2F-MRJcMvaWGn27t4CDF2I%2FCreate_Adapter.png?alt=media&token=2fb1b549-7045-4f31-9472-b421271e6857) tıklayın ve uygun endpoint türünü seçin.
- Bir ad, IP/Hostname, kimlik bilgileri(credentials), vCenter Adapter URL (format: "`https://<IP/Hostname>:<Port&gt;`", burada IP/Hostname, adapter konteynerinin kullanılan portuyla birlikte çalıştığı docker ana bilgisayarıdır), username, password ve tag (bu endpoint'teki hataları benzersiz bir şekilde tanımlamak için etkin metrik sağlayıcıya gönderilmesi gereken ek etiketlere atıfta bulunur) girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **submit** edin
- Bir başarı mesajı görüntülenir ve Adapters tablosu güncellenir.
- Düzenleme ve Silme işlemleri, kaydedilen tüm adapterler için desteklenir.

> **:warning:** vCenter adapter, Mangle'ın çalıştığı aynı makineye kurulursa, vCenter endpoint'i eklemek için kullanılan vCenter adapter IP'si şunlardan biri olabilir:
>
> - internal docker konteyner IP
> - docker host IP
>
> **mangle-vc-adapter için internal docker container IP yi bulurken:** > `docker inspect --format '{{.NetworkSettings.IPAddress}}' *mangle-vc-adapter`

## Endpoint Ekleme (Adding Endpoints)

### Desteklenen Endpointler

Mangle'da endpoint, kaos mühendisliği deneyleriniz için birincil hedef olacak bir altyapı bileşenini ifade eder.

**Version 1.0** için Mangle dört tür endpoint'i destekledi:

- Kubernetes
- Docker
- VMware vCenter
- Uzak Makine

  2.0 sürümünden itibaren, yukarıda listelenen dört endpoint dışında, destek aşağıdaki yeni endpoint ile genişletildi:

- AWS (Amazon Web Services)

  3.0 sürümünden itibaren, destek aşağıdaki yeni uç noktalara genişletildi:

- Azure
- Veritabanları (Postgres, Cassandra and Mongo)

#### Kubernetes Endpoint

Mangle, Kubernetes clusterlarını **injection** için, **Endpoint** veya **Target** olarak destekler. Cluster'a bağlanmak ve desteklenen hataları(faults) çalıştırmak için bir **kubeconfig** dosyasına ihtiyaç duyar. Bir kubeconfig dosyası sağlanmazsa Mangle, bunun bir K8s cluster ile çalıştığını varsayar ve fault injection için aynı cluster'ı hedefler.

```
K8s Test Edilmiş Versiyonlar
v1.9.6, v1.9.9
```

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` Kubernetes Cluster
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Bir ad, credentials, namespace (**zorunlu**... namespace alanından emin değilseniz "**varsayılan**" olarak belirtin, aksi takdirde gerçek adı belirtin) ve tag (bu endpoint'deki hataları(faults) benzersiz bir şekilde tanımlamak için etkin metrik sağlayıcıya gönderilmesi gereken ek etiketleri ifade eder) alanı girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpointler için kullanılabilir.

#### Docker Endpoint

Mangle, **docker hostlarını** injection için **enpoint** veya **target** olarak destekler. Docker hostlarına bağlanmak ve desteklenen hataları(faults) çalıştırmak için IP/Hostname, port ayrıntıları ve sertifika ayrıntılarına (TLS **--tlsverify** seçeneği ile docker host için etkinleştirildiyse) ihtiyaç duyar. TLS etkinleştirilmişse Docker endpoint'i için bir sertifika oluşturmak üzere endpoint sekmesi altındaki Certificates bölümünü kullanın.

```
Docker Test Edilmiş Versiyonlar
1.13.1, build 092cba3
17.06.0-ce, build 02c1d87
18.09.3, build 774a1f4
```

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` Docker
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Bir ad, IP/Hostname, port ayrıntıları, tag (bu endpoint'deki hataları benzersiz bir şekilde tanımlamak için etkin metrik sağlayıcıya gönderilmesi gereken ek etiketlere atıfta bulunur) ve sertifika ayrıntıları (docker ana bilgisayarı için TLS etkinleştirilmişse) girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpointler için kullanılabilir.

#### VMware vCenter Endpoint

Mangle, VMware vCenter'ı injection için **enpoint** veya **target** olarak destekler. vCenter instance'ına bağlanmak ve desteklenen desteklenen hataları(faults) için IP/Hostname, credentials ve vCenter adapter URL gerekir. Henüz bir vCenter Adapter eklemediyseniz (vCenter Endpointleri eklemek için bir ön koşul), **Adapter Ekleme** yönergelerini gözden geçirin.

```
Test Edilmiş ve Desteklenen Versiyonlar VMware vCenter
vCenter 6.5 ve üstü
```

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` VMware vCenter.
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Bir ad, IP/Hostname, credentials, vCenter Adapter URL (format: `"https://<IP/Hostname>:<Port&gt;"`), username, password ve tag (bu uç noktadaki hataları benzersiz bir şekilde tanımlamak için etkin metrik sağlayıcıya gönderilmesi gereken ek etiketlere atıfta bulunur) girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpointler için kullanılabilir.

> **:warning:** vCenter adapter, Mangle'ın çalıştığı aynı makineye kurulursa, vCenter endpoint'i eklemek için kullanılan vCenter adapter IP'si şunlardan biri olabilir:
>
> - internal docker konteyner IP
> - docker host IP
>
> **mangle-vc-adapter için internal docker container IP yi bulurken:** > `docker inspect --format '{{.NetworkSettings.IPAddress}}' *mangle-vc-adapter`

#### Uzak Makine Endpoint (Remote Machine)

Mangle, injection için enpoint veya target olarak ssh'nin etkinleştirildiği herhangi bir uzak makineyi destekler. Uzak makineye bağlanmak ve desteklenen hataları(faults) çalıştırmak için IP/Hostname, credentials (şifre veya özel anahtar), ssh ayrıntılarına, işletim sistemi tipine ve tag(etketler)'e ihtiyaç duyar.

| İşletim Sistemi Uzak Makinelerin Test Edilen Sürümleri | Versionlar       |
| ------------------------------------------------------ | ---------------- |
| CentOS                                                 | 7, 7.7, 7.8, 8.2 |
| Debian                                                 | 7.8, 8, 9        |
| Photon OS                                              | 2, 3             |
| RHEL                                                   | 7.5, 8.2, 8.3    |
| Suse                                                   | 12, 15           |
| Ubuntu                                                 | 14, 16, 18       |

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` Remote Machine.
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Bir ad, IP/Hostname, credentials (parola veya özel anahtar), ssh port, ssh timeout, OS Tipi ve tag (bu uç noktadaki hataları benzersiz bir şekilde tanımlamak için etkin metrik sağlayıcıya gönderilmesi gereken ek etiketlere atıfta bulunur) girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpointler için kullanılabilir.

#### AWS (Amazon Web Services)

Mangle, injection için enpoint veya target olarak AWS'yi destekler. AWS'ye bağlanmak ve desteklenen hataları çalıştırmak için Region, credentials (Erişim anahtarı kimliği ve Gizli anahtar) ve taglere(Etiket) ihtiyaç duyar. Şu anda desteklenen tek hizmet EC2'dir. Ancak, bunu AWS'deki diğer önemli hizmetlere genişletme planları var.

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` AWS.
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Bir ad, Region, credentials (Access key ID ve Secret key), ssh port, ssh timeout, OS Type ve tag girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpointler için kullanılabilir.

#### Azure

Mangle, Azure'u injection için enpoint veya target olarak destekler. Azure'a bağlanmak ve desteklenen hataları çalıştırmak için Subscription ID, Tenant ID, credentials (Client application ID and Client application secret key) ve tag'e ihtiyaç duyar.

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` Azure.
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Bir ad, Subscription ID, Tenant ID, credentials (Client application ID ve Client application secret key) ve tag girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpointler için kullanılabilir.

#### Redis Proxy

Mangle, versiyon 3.0 ile birlikte ayrı bir açık kaynak projesi olan RedFI (Redis Fault Injection Proxy) ile entegre olarak Redis'e karşı hata çalıştırma(run faults) olanağı sağlamaktadır. Redis hatalarını denemek için, ortamınızda çalışır durumda bir Redis proxy'nizin olması zorunludur. RedisFI proxy'sini deploy etmek için belirtilen [talimatlara](https://github.com/openfip/redfi#usage) bakın. Proxy deploy edildikten ve çalıştırıldıktan sonra, onu Mangle'da endpoint olarak eklemek için aşağıdaki adımlarla ilerleyin.

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` Redis Proxy.
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Bir ad, Redis Proxy IP/Hostname, varsayılandan farklıysa alternatif bir controller port - 6380, ve tag girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpointler için kullanılabilir.

#### Veritabanları

Versiyon 3.0 ile Mangle, veritabanlarına karşı hatalar(faults) çalıştırma yeteneği sağlar. Desteklenen veritabanları Cassandra, Mongo ve Postgres'tir. Veritabanı endpointi'nin bir temel farkı vardır, çünkü bunlar bir hizmet olarak bir sanal makine/instance üzerinde, konteyner olarak Docker'da veya Pod olarak K8'lerde bulunabilmektedir. Bu nedenle, Mangle'da veritabanı endpointlerini tanımlarken, uzak makine, Docker veya K8s cluster olabilecek üst endpointi de(parent endpoint) belirtmeniz gerekir.

##### Takip edilecek adımlar:

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` Databases.
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Veritabanı uç noktası için bir ad, database credentials (Database Tipi, Database Username ve Password, Database Port, Database Name ve SSL Enabled status), parent endpoint (uzak makine, Docker veya Mangle'a önceden eklenmiş K8s endpointi olabilir) ve tag girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpointler için kullanılabilir.

### İlgili API Referansı

> 📝 Swagger dokümantasyonuna erişim için:
> Mangle kullanıcı arayüzünden ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Leac8tB-KodjFhsg2Zs%2F-LeacYoaMEsURLcmrZyl%2FHelp.png?alt=media&token=e28a8f10-207c-4ae0-a803-2949ee85c749) `--->` API Dokümantasyon bağlantısına gidin veya erişim sağlayın.
>
> `https://<Mangle IP or Hostname>/mangle-services/swagger-ui.html#/endpoint-controller`
>
> ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-Lf4J8nIngzw1Yrwg0f0%2F-Lf4MWbZt2a1LP9vjChy%2FEndpointController.png?alt=media&token=b1b9b451-acc0-43d8-a710-36564afe7ee7) <

## Endpoint Groups Ekleme

### Neden Endpoint Groups eklemeliyiz?

Mangle'ın, özellikle ürünün yüksek kullanılabilirlik(high availability) için bir düğüm kümesi (cluster of nodes) olarak dağıtıldığı durumlarda, hata yürütme sırasında endpoint kümesini single group olarak düşünmesine ihtiyacınız varsa, o zaman bir Endpoint group oluşturmanız ve bunu hata yürütme(time of fault execution ) veya planlama(scheduling) sırasında kullanmanız gerekir.

Bu:

- Hata yürütme sırasında endpoint cluster'daki nodelardan birini Rastgele seçmenize
  veya
- Endpoint cluster'daki tüm nodelarda aynı hatayı aynı anda(simultaneously) çalıştırmanıza izin verecektir.

### Endpoint Groups

- Mangle'a okuma ve yazma yetkilerine sahip bir kullanıcı olarak giriş yapın.
- Endpoint Sekmesi `--->` Endpoints `--->` Endpoint Groups.
- ![alt text](https://983585930-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LcVKiIEQZ_SDz8uqA0g%2F-MRJQDr0vAs1A5X-B_MF%2F-MRJRNuvfJHJt2vcCP3o%2FAdd_Button.png?alt=media&token=d9e50746-0c20-4648-923f-23b847f00b99) tıklayın.
- Bir ad, group type (şu anda yalnızca uzak makineler desteklenmektedir), bir liste veya iki veya daha fazla mevcut endpoint ve tag(etiket) girin.
- Test Connection'a tıklayın.
- Test başarılı olursa **Submit** edin
- Bir başarı mesajı görüntülenir ve Endpoints tablosu yeni girişle güncellenir.
- Edit, Delete, Enable and Disable aksiyonları, eklenen tüm Endpoint Groups için kullanılabilir.

Artık, hata yürütme(time of fault execution) sırasında bir endpoint yerine endpoint grup seçme seçeneğiniz olacak.

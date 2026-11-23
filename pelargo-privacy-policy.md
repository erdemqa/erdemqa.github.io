# Pelargo Privacy Policy

**Last updated: 23 November 2026**

This Privacy Policy explains how Pelargo, its iOS application, and the services used to provide city packs and app functionality process information about users.

**Data controller and publisher:** Erdem Özdemir (individual developer)  
**Privacy contact:** [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com)

This Policy applies to Pelargo and its related content-delivery, feedback, and support services. It does not replace the privacy policies of Apple or other third-party providers.

## 1. At a glance

- Pelargo does not require you to create an account or sign in.
- Saved places, user-created lists and notes, app preferences, and downloaded city content are stored on your device for app functionality.
- Product analytics is optional. Pelargo sends analytics to PostHog only after you opt in. You can withdraw that permission at any time in **Profile → Privacy & Analytics**.
- Declining analytics does not restrict app features, city-pack access, or purchases.
- Pelargo does not display third-party advertising, use the advertising identifier (IDFA), or track you across other companies' apps and websites.
- Pelargo does not request access to your device's precise location in the current version. Map screens display place coordinates included in city content; they do not need your live GPS location.

## 2. Information processed by Pelargo

### 2.1 Information stored on your device

Pelargo stores information locally to provide its features. Depending on how you use the app, this may include:

- Your selected app language and other app preferences.
- Onboarding and coach-mark completion status.
- Saved places, user-created lists, list ordering, and notes you add to those lists.
- Audio playback preferences and related app state.
- Downloaded city packs and audio assets.
- Analytics events waiting in a local queue until they can be sent over Wi-Fi, if you have enabled analytics.

Pelargo does not operate a user-account or cloud-sync service for your saved lists and notes. These items are not sent to Pelargo's servers as part of normal list use. Device backups, if enabled in iOS, are controlled by your device and Apple settings.

### 2.2 Optional product analytics

If you choose **Allow optional analytics**, Pelargo sends defined product-usage events to its PostHog Cloud project hosted in the European Union. Analytics is disabled unless you opt in.

Events may describe actions such as:

- App start and onboarding completion.
- City selection, city-pack activation, downloads, updates, and deletion.
- Opening a content item and using in-app search.
- Adding or removing an item from a list, and creating or deleting a list.
- Starting or completing a route and starting or ending an audio guide.
- Viewing a paywall and the outcome of a purchase attempt.
- Submitting a feedback, city request, or content-report form.

Depending on the event, the information sent may include:

- A pseudonymous RevenueCat App User ID, used as the PostHog event identifier.
- Event name and time, a session identifier, app version/build, iOS version, platform, network type, device language, and the language selected inside Pelargo.
- City IDs, canonical content identifiers, route identifiers, pack versions, and opaque list identifiers.
- For searches, the search-field length and number of results, **not the text you searched for**.
- For list activity, the list type and an opaque list ID, **not the title of your list or its notes**.
- For purchase events, the outcome and relevant city/product identifier, **not payment-card details or StoreKit receipt contents**.

Pelargo's custom analytics events do not include your name, email address, search text, user-created list titles or notes, free-form feedback text, precise GPS coordinates, payment-card details, or IDFA.

A RevenueCat App User ID may be generated anonymously by RevenueCat and is pseudonymous rather than a name or email address. It can still be treated as personal data because events associated with the same identifier can be linked together.

PostHog receives the IP address used to make the network request as part of normal internet communication. Pelargo does not add your IP address as a custom event property or use it to determine your precise location. The app sends an event-level instruction to disable GeoIP enrichment. In the PostHog project, the setting to discard client IP data is enabled; GeoIP enrichment is disabled for events, and no GeoIP transformation is configured. These settings are intended to prevent client IP addresses and GeoIP-derived location data from being retained in analytics events. PostHog may still process connection information transiently as necessary to provide and secure its service.

### 2.3 Purchases and entitlements

City-pack purchases are made through Apple's App Store purchase system (StoreKit). Apple processes the transaction and payment. Pelargo does not receive your payment-card number or bank details.

Pelargo uses RevenueCat to validate transactions and manage city-pack entitlements. RevenueCat may process transaction or receipt information supplied by StoreKit, product identifiers, entitlement status, technical app/device information, and the RevenueCat App User ID. Pelargo receives the purchase and entitlement results needed to unlock the relevant content.

If analytics is enabled, Pelargo may also send a purchase outcome and city/product identifier to PostHog. It does not send StoreKit receipt contents or payment-card details through its custom analytics events.

### 2.4 Feedback, city requests, and content reports

If you voluntarily send general feedback or request a new city, the text you enter is sent to Pelargo's feedback service hosted on Cloudflare. A free-text message may contain personal information if you choose to include it. Please do not include passwords, payment details, or sensitive personal information unless it is necessary for your request.

When you report a content item or image, the app sends the relevant canonical content ID or in-app asset name, together with the city-pack ID, pack version, and app version. The image-report function identifies an image asset in Pelargo; it does not upload a photo from your personal photo library.

Feedback text and report details are sent to Cloudflare for review and resolution. They are not included in Pelargo's custom PostHog event payloads. The feedback service stores submission and review details such as the submission type, reported image asset name or content identifier, city-pack and app-version information, status, and any review or resolution note. The feedback records do not contain your direct email address, RevenueCat App User ID, device ID, or raw IP address. A free-text message may nevertheless contain personal information if you choose to include it.

### 2.5 Private city-pack delivery and app security

Some city packs or audio packages may be delivered through a private download service. To verify an app installation, check access to content, prevent abuse, and issue a temporary download link, Pelargo may send the following to its Cloudflare-hosted authorization API:

- Your pseudonymous RevenueCat App User ID; a hash derived from this identifier may be stored in access records.
- An App Attest key identifier associated with this app installation and the public-key material used to verify the installation.
- Challenge identifiers, challenge data, and signed App Attest attestation or assertion data.
- The requested city ID, pack version, asset type, and language.

The App Attest key identifier and public-key material are used for app-installation verification. They are not IDFA and are not used for advertising or cross-app tracking. The Cloudflare access database may also store technical authorization and audit details, including the app bundle and version, platform and environment, device-key identifier, requested asset and city-pack details, timestamp, authorization outcome, and reason code. A record that a temporary download link was issued means the request was authorized and a link was generated; it does not establish that the file download completed.

To apply rate limits, the authorization service stores a hash of the requesting IP address in its rate-limit records; the raw IP address is not stored in those database records. Cloudflare may separately process IP addresses, request times, and technical request headers at the network or service layer to operate and protect the API.

The relevant Cloudflare object-storage buckets are private and are not exposed through public r2.dev or public custom-domain access. Authorized files are delivered using temporary URLs after the access check. No automatic object-lifecycle deletion rule is currently configured for the inspected private buckets; city-pack versions are managed manually.

### 2.6 Maps and location

In the current version, Pelargo does not request permission to access your device's precise location and does not send live GPS coordinates to Pelargo's analytics service. Map screens display coordinates for places contained in the city pack. Apple MapKit may process technical connection information and map requests when map content is displayed, in accordance with Apple's terms and privacy information.

If Pelargo introduces a feature that accesses device location in a future version, this Policy and the in-app disclosures will be updated before that processing begins, and the relevant iOS permission will be requested where required.

## 3. Why we process information

Depending on the information and the feature, Pelargo processes information for these purposes:

| Purpose | Information involved | Basis or user choice |
|---|---|---|
| Provide app features and offline content | Local preferences, saved lists, city packs, playback state | Necessary to provide the features you request; stored locally where possible |
| Process purchases and unlock city packs | StoreKit transaction data, RevenueCat App User ID, product and entitlement information | Purchase/contract and related service delivery |
| Authorize private downloads and protect the service | App Attest data, pseudonymous app user identifier, requested pack details, technical request data | Deliver purchased content and protect the service against misuse or fraud |
| Respond to feedback, city requests, and reports | Text or report identifiers you submit, app/content version details | Your voluntary request and the handling of that request |
| Understand and improve Pelargo | Optional product-usage events and app/device metadata | Your opt-in consent; you can withdraw it at any time |
| Meet legal obligations and handle disputes | Relevant transaction, support, or security records | Applicable legal obligations and, where permitted, legitimate interests |

Declining optional analytics does not affect your ability to use Pelargo or purchase or access city packs.

## 4. Analytics consent and your choices

Analytics is off until you opt in. You can choose **Continue without analytics** and keep using Pelargo.

You can change your choice at any time under **Profile → Privacy & Analytics**:

- When you turn analytics off, Pelargo stops collecting new analytics events, stops pending uploads, and deletes analytics events that are still waiting in the local SQLite queue.
- Events already delivered to PostHog are not automatically removed when you withdraw consent.
- You can request deletion of previously sent analytics data using the deletion-request option in **Profile → Privacy & Analytics**, or by emailing [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com). The request is reviewed and processed in the relevant service; it is not an instant automatic deletion. We will confirm when the request has been completed.

## 5. Who receives information

Pelargo does not sell or rent personal information. Information is shared with service providers only to the extent needed to provide the app, process purchases, deliver content, respond to requests, or conduct optional analytics.

| Provider | How it is used |
|---|---|
| **PostHog (EU Cloud)** | Receives optional product-analytics events after you opt in. The EU Cloud service is hosted in Frankfurt, Germany. |
| **RevenueCat** | Helps validate App Store transactions and manage purchase entitlements and the pseudonymous App User ID. |
| **Apple** | Provides App Store/StoreKit purchase processing, App Attest, iOS services, and Apple MapKit map display. |
| **Cloudflare** | Hosts Pelargo's feedback and content-report API and its database, private-pack authorization API and access records, and private object storage and file-delivery services. |

These providers process information under their own service terms and privacy documentation, and under the arrangements applicable to Pelargo's use of their services. Their policies are available here:

- [PostHog Privacy](https://posthog.com/privacy)
- [RevenueCat Privacy Policy](https://www.revenuecat.com/privacy-policy)
- [Apple Privacy](https://www.apple.com/legal/privacy/)
- [Cloudflare Privacy Policy](https://www.cloudflare.com/privacypolicy/)

## 6. International data processing

PostHog analytics is sent to Pelargo's EU Cloud project. Apple, RevenueCat, and Cloudflare may process information in the countries where they or their service providers operate. This may include countries outside your country of residence. Where applicable law requires safeguards for an international transfer, the transfer must be made under an appropriate legal transfer mechanism and the provider arrangements applicable to the service.

## 7. Retention and deletion

Retention methods differ by data type. Some information is stored locally or by service providers, while certain feedback, device-verification, and access-audit records are retained without a fixed automatic expiry. The following describes the current configuration reviewed for Pelargo as of the date of this Policy.

- **Local app data:** Saved lists, notes, preferences, and downloaded content remain on your device until you delete them, remove the relevant city pack, or remove the app, subject to any device backup managed by iOS.
- **Unsent analytics events:** The local analytics queue is kept only while events are waiting to be sent. It is purged when you withdraw analytics consent.
- **Analytics sent to PostHog:** The PostHog project is currently configured to retain analytics events for one year (up to 12 months). This event-retention setting does not necessarily delete pseudonymous Person Profiles or their properties; those may be subject to separate settings and may remain until separately deleted. You can submit a deletion request as described above. The project configuration and provider plan may change, so this setting will be reviewed when the service configuration changes.
- **Feedback and content reports:** Submission and review records are stored in Cloudflare D1. The current implementation does not have an automatic time-based deletion schedule or scheduled cleanup for these records. They are retained for review and resolution, content-curation history, service protection, and handling related questions or disputes. A deletion request is assessed individually under applicable law; records are not automatically purged after a stated period.
- **App Attest and access-security records:** Cloudflare D1 stores app-installation verification records, device-key and public-key information, and related authorization metadata. Expired or consumed challenge records and old rate-limit windows are cleaned up opportunistically when a new challenge is issued; this is not a guaranteed fixed deletion schedule. Registered-device records are not currently subject to automatic time-based deletion.
- **Private-download audit records:** Download-event records in Cloudflare D1 are retained as access-history records. No automatic retention period, scheduled cleanup, or time-based deletion is currently configured for them. These records cover authorization decisions for private city-pack and audio access. An “issued” outcome means that a temporary download link was authorized and generated, not that the file was successfully downloaded. Access records use hashed pseudonymous identifiers, and the rate-limit table stores a hash of the requesting IP address rather than the raw IP address.
- **Private object storage:** The inspected private Cloudflare R2 buckets do not have automatic lifecycle rules that expire or delete objects. City-pack versions are managed manually; objects remain stored until they are manually replaced or deleted.
- **Purchase records:** Apple and RevenueCat may retain transaction and entitlement information under their own policies and applicable legal or accounting requirements.

For more information about PostHog event and profile storage, see [PostHog's data-storage documentation](https://posthog.com/docs/privacy/data-storage).

To request access to or deletion of information that Pelargo controls, contact us at [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com). We may need to verify the request before acting. Some information may be retained where required by law or where necessary to establish, exercise, or defend legal claims.

## 8. International privacy rights

Depending on where you live and the law that applies, you may have the right to:

- Ask whether we process personal information about you and request a copy of it.
- Request correction of inaccurate or incomplete information.
- Request deletion of information or restriction of certain processing.
- Object to certain processing or request data portability, where applicable.
- Withdraw consent at any time where processing is based on consent. Withdrawal does not affect processing that took place before withdrawal.
- Complain to the competent data-protection authority.

### Users in Türkiye

For purposes of Türkiye's Personal Data Protection Law No. 6698 (KVKK), the data controller is **Erdem Özdemir**. You may submit requests concerning your rights under Article 11 of the KVKK, including learning whether your personal data are processed, requesting information about processing, asking for correction or deletion where the legal conditions apply, and exercising other rights provided by law, by emailing [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com).

We will respond within the period and using the procedure required by applicable law. If you are not satisfied with the response, you may apply to the Personal Data Protection Authority in accordance with the KVKK procedure.

### Users in the EEA, United Kingdom, or Switzerland

Where the GDPR or equivalent local law applies, you may also have rights to access, rectification, erasure, restriction, objection, and data portability, and the right to lodge a complaint with your local supervisory authority. The availability of a particular right depends on the legal basis and circumstances of the processing.

## 9. Security

Pelargo uses reasonable technical and organizational measures intended to protect information, including local storage for user lists and preferences, encrypted network connections, purchase-entitlement checks, and App Attest verification for protected content delivery. No method of transmission or storage is completely secure, and absolute security cannot be guaranteed.

## 10. Children

Pelargo is not designed specifically for children and does not intentionally collect children's personal information. If you believe a child has provided personal information through a feedback or support form, please contact us so we can review the request and take appropriate action.

## 11. Changes to this Policy

We may update this Policy when the app, its service providers, or applicable legal requirements change. The updated version will be published at this URL with a revised "Last updated" date. If a material change affects optional analytics purposes, data types, or recipients, Pelargo may request a new analytics choice before continuing that processing.

## 12. Contact

For privacy questions, access or deletion requests, or other concerns about Pelargo's data practices, contact:

**Erdem Özdemir**  
**Email:** [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com)

---

# Pelargo Gizlilik Politikası

**Son güncelleme: 23 Kasım 2026**

Bu Gizlilik Politikası, Pelargo iOS uygulamasının ve şehir paketlerini, uygulama özelliklerini ve destek hizmetlerini sunmak için kullanılan ilişkili servislerin bilgileri nasıl işlediğini açıklar.

**Veri sorumlusu ve yayıncı:** Erdem Özdemir (bireysel geliştirici)  
**Gizlilik iletişim adresi:** [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com)

Bu Politika Pelargo uygulaması ile ilişkili içerik dağıtım, geri bildirim ve destek hizmetleri için geçerlidir. Apple veya diğer üçüncü taraf hizmet sağlayıcıların kendi gizlilik politikalarının yerine geçmez.

## 1. Kısaca

- Pelargo'yu kullanmak için hesap oluşturmanız veya giriş yapmanız gerekmez.
- Kaydedilen yerler, kullanıcı listeleri ve notları, uygulama tercihleri ve indirilen şehir içerikleri uygulamanın çalışması için cihazınızda saklanır.
- Ürün kullanım analitiği isteğe bağlıdır. Pelargo analitik verilerini yalnızca açıkça izin vermenizden sonra PostHog'a gönderir. İzninizi istediğiniz zaman **Profil → Gizlilik ve Analitik** bölümünden geri çekebilirsiniz.
- Analitiği reddetmeniz uygulama özelliklerini, şehir paketi erişimini veya satın alımları kısıtlamaz.
- Pelargo üçüncü taraf reklam göstermez, reklam kimliği (IDFA) kullanmaz ve sizi başka şirketlerin uygulama veya internet siteleri arasında takip etmez.
- Mevcut sürümde Pelargo cihazınızın kesin konumuna erişim izni istemez. Harita ekranları şehir içeriğinde bulunan yer koordinatlarını gösterir; canlı GPS konumunuza ihtiyaç duymaz.

## 2. Pelargo tarafından işlenen bilgiler

### 2.1. Cihazınızda saklanan bilgiler

Pelargo, özelliklerini sunmak için bazı bilgileri cihazınızda yerel olarak saklar. Uygulamayı nasıl kullandığınıza bağlı olarak bu bilgiler şunları içerebilir:

- Seçtiğiniz uygulama dili ve diğer uygulama tercihleri.
- Onboarding ve coach mark tamamlama durumları.
- Kaydettiğiniz yerler, oluşturduğunuz listeler, liste sıralaması ve liste notlarınız.
- Sesli oynatma tercihleri ve ilgili uygulama durumu.
- İndirdiğiniz şehir paketleri ve ses dosyaları.
- Analitiği etkinleştirdiyseniz, Wi-Fi üzerinden gönderilmeyi bekleyen yerel analitik event'leri.

Pelargo, kullanıcı listeleri ve notları için bir kullanıcı hesabı veya bulut senkronizasyonu hizmeti işletmez. Normal liste kullanımı sırasında bu veriler Pelargo sunucularına gönderilmez. iOS cihaz yedeklemesi açıksa cihaz yedeklerinin kapsamı Apple ve iOS ayarlarına bağlıdır.

### 2.2. İsteğe bağlı ürün kullanım analitiği

**İsteğe bağlı analitiğe izin ver** seçeneğini tercih ederseniz Pelargo, tanımlanmış ürün kullanım event'lerini Avrupa Birliği'nde barındırılan PostHog Cloud projesine gönderir. Siz izin vermedikçe analitik kapalıdır.

Gönderilebilecek event'ler şunları içerebilir:

- Uygulamanın açılması ve onboarding'in tamamlanması.
- Şehir seçimi, şehir paketinin etkinleştirilmesi, indirilmesi, güncellenmesi ve silinmesi.
- Bir içerik öğesinin açılması ve uygulama içi arama kullanımı.
- Bir içeriğin listeye eklenmesi veya listeden çıkarılması; liste oluşturulması veya silinmesi.
- Rota başlatılması veya tamamlanması; sesli rehberin başlatılması veya bitirilmesi.
- Satın alma ekranının görüntülenmesi ve satın alma girişiminin sonucu.
- Geri bildirim, şehir isteği veya içerik bildirimi formunun gönderilmesi.

Event'e bağlı olarak gönderilen bilgiler şunları içerebilir:

- PostHog event kimliği olarak kullanılan takma adlı RevenueCat App User ID.
- Event adı ve zamanı, oturum kimliği, uygulama sürümü/build numarası, iOS sürümü, platform, ağ türü, cihaz dili ve Pelargo içinde seçtiğiniz uygulama dili.
- Şehir kimlikleri, canonical içerik kimlikleri, rota kimlikleri, paket sürümleri ve opak liste kimlikleri.
- Aramalar için arama alanının uzunluğu ve sonuç sayısı; **aradığınız metnin kendisi gönderilmez**.
- Liste hareketleri için liste türü ve opak liste kimliği; **listenizin adı veya notları gönderilmez**.
- Satın alma event'leri için sonuç ve ilgili şehir/ürün kimliği; **ödeme kartı bilgisi veya StoreKit makbuz içeriği gönderilmez**.

Pelargo'nun özel analitik event'leri adınızı, e-posta adresinizi, arama metinlerinizi, oluşturduğunuz listelerin adlarını veya notlarını, serbest metin geri bildirimlerinizi, kesin GPS koordinatlarınızı, ödeme kartı bilgilerinizi veya IDFA'yı içermez.

RevenueCat App User ID, RevenueCat tarafından anonim olarak oluşturulabilen, ad veya e-posta adresi niteliğinde olmayan takma adlı bir tanımlayıcıdır. Aynı kimlikle ilişkili event'lerin birbiriyle ilişkilendirilmesini sağladığından kişisel veri olarak değerlendirilebilir.

PostHog, normal ağ iletişiminin bir parçası olarak bağlantı kurmak için kullanılan IP adresini alır. Pelargo IP adresinizi özel event özelliği olarak eklemez ve kesin konumunuzu belirlemek için kullanmaz. Uygulama, event düzeyinde GeoIP zenginleştirmesini kapatma talimatı gönderir. PostHog projesinde istemci IP verilerini silme ayarı etkindir; event'ler için GeoIP zenginleştirmesi kapalıdır ve herhangi bir GeoIP dönüşümü yapılandırılmamıştır. Bu ayarlar, istemci IP adreslerinin ve GeoIP kaynaklı konum bilgilerinin analitik event'lerinde saklanmasını önlemek üzere yapılandırılmıştır. PostHog, hizmetini sunmak ve güvenliğini sağlamak için bağlantı bilgilerini gerektiğinde geçici olarak yine de işleyebilir.

### 2.3. Satın alımlar ve erişim hakları

Şehir paketi satın alımları Apple App Store satın alma sistemi (StoreKit) üzerinden yapılır. İşlemi ve ödemeyi Apple gerçekleştirir. Pelargo ödeme kartı numaranızı veya banka bilgilerinizi almaz.

Pelargo, işlemleri doğrulamak ve şehir paketi erişim haklarını yönetmek için RevenueCat kullanır. RevenueCat, StoreKit tarafından sağlanan işlem veya makbuz bilgilerini, ürün kimliklerini, erişim hakkı durumunu, uygulama/cihazla ilgili teknik bilgileri ve RevenueCat App User ID'yi işleyebilir. Pelargo, ilgili içeriğin kilidini açmak için gerekli satın alma ve entitlement sonuçlarını alır.

Analitik açıksa Pelargo satın alma sonucunu ve şehir/ürün kimliğini PostHog'a da gönderebilir. Özel analitik event'leri StoreKit makbuz içeriğini veya ödeme kartı bilgilerini içermez.

### 2.4. Geri bildirim, şehir istekleri ve içerik bildirimleri

Genel geri bildirim gönderir veya yeni şehir talep ederseniz girdiğiniz metin Cloudflare üzerinde barındırılan Pelargo geri bildirim servisine gönderilir. Serbest metin alanına kendi tercihinizle kişisel bilgi yazarsanız bu bilgi tarafımıza ulaşabilir. Talebiniz için gerekli olmadıkça şifre, ödeme bilgisi veya hassas kişisel bilgi yazmayın.

Bir içerik veya görsel bildirdiğinizde uygulama ilgili canonical içerik kimliğini veya uygulama içindeki görsel varlık adını; şehir paketi kimliği, paket sürümü ve uygulama sürümüyle birlikte gönderir. Görsel bildirim işlevi Pelargo içindeki görsel varlığını tanımlar; kişisel fotoğraf arşivinizden bir fotoğraf yüklemez.

Geri bildirim metni ve bildirim ayrıntıları incelenmek ve sonuçlandırılmak üzere Cloudflare'a gönderilir. Bunlar Pelargo'nun özel PostHog event içeriğine dahil edilmez. Geri bildirim servisi; bildirim türü, bildirilen görsel varlığının adı veya içerik kimliği, şehir paketi ve uygulama sürümü bilgileri, durum ve varsa inceleme/sonuçlandırma notu gibi başvuru ve inceleme ayrıntılarını saklar. Geri bildirim kayıtlarında doğrudan e-posta adresiniz, RevenueCat App User ID, cihaz kimliğiniz veya ham IP adresiniz tutulmaz. Bununla birlikte serbest metin alanına kendi tercihinizle kişisel bilgi yazarsanız bu bilgi kayda girebilir.

### 2.5. Özel şehir paketi dağıtımı ve uygulama güvenliği

Bazı şehir paketleri veya ses paketleri özel indirme hizmeti üzerinden dağıtılabilir. Uygulama kurulumunu doğrulamak, içeriğe erişimi kontrol etmek, kötüye kullanımı önlemek ve geçici indirme bağlantısı oluşturmak için Pelargo, Cloudflare üzerinde barındırılan yetkilendirme API'sine şunları gönderebilir:

- Takma adlı RevenueCat App User ID; bu tanımlayıcıdan türetilen bir hash erişim kayıtlarında saklanabilir.
- Bu uygulama kurulumuna bağlı App Attest anahtar kimliği ve kurulumu doğrulamak için kullanılan açık anahtar bilgileri.
- Challenge kimlikleri, challenge verileri ve imzalı App Attest attestation/assertion verileri.
- İstenen şehir kimliği, paket sürümü, varlık türü ve dil.

App Attest anahtar kimliği ve açık anahtar bilgileri uygulama kurulumunun doğrulanması için kullanılır. IDFA değildir; reklam veya uygulamalar arası takip amacıyla kullanılmaz. Cloudflare erişim veritabanında uygulama bundle kimliği ve sürümü, platform ve ortam, cihaz anahtarı kimliği, istenen varlık ve şehir paketi bilgileri, zaman damgası, yetkilendirme sonucu ve neden kodu gibi teknik yetkilendirme ve denetim ayrıntıları da saklanabilir. Geçici indirme bağlantısının oluşturulduğunu gösteren “issued” kaydı, isteğin yetkilendirildiği ve bağlantının üretildiği anlamına gelir; dosyanın başarıyla indirildiğini kanıtlamaz.

Yetkilendirme servisi, istek hızını sınırlamak için IP adresinin hash'lenmiş halini rate-limit kayıtlarında saklar; ham IP adresi bu veritabanı kayıtlarında tutulmaz. Cloudflare, API'yi işletmek ve korumak için ağ veya servis katmanında IP adreslerini, istek zamanlarını ve teknik istek başlıklarını ayrıca işleyebilir.

İlgili Cloudflare nesne depolama bucket'ları özeldir; public r2.dev veya public custom-domain erişimine açık değildir. Yetkilendirilmiş dosyalar erişim kontrolünden sonra geçici URL'ler kullanılarak sunulur. İncelenen özel bucket'larda otomatik nesne yaşam döngüsü silme kuralı yapılandırılmamıştır; şehir paketi sürümleri manuel olarak yönetilir.

### 2.6. Haritalar ve konum

Mevcut sürümde Pelargo cihazınızın konumuna erişim izni istemez ve canlı GPS koordinatlarınızı Pelargo analitik servisine göndermez. Harita ekranları şehir paketlerinde bulunan yerlere ait koordinatları gösterir. Harita içeriği görüntülenirken Apple MapKit, Apple'ın koşulları ve gizlilik açıklamaları doğrultusunda teknik bağlantı bilgilerini ve harita isteklerini işleyebilir.

Pelargo gelecekte cihaz konumuna erişen bir özellik sunarsa bu işlem başlamadan önce Politika ve uygulama içi bilgilendirmeler güncellenecek ve gerekli durumlarda ilgili iOS izni istenecektir.

## 3. Bilgileri hangi amaçlarla işliyoruz?

Pelargo, bilgi türüne ve kullanılan özelliğe bağlı olarak bilgileri şu amaçlarla işler:

| Amaç | İlgili bilgiler | Hukuki sebep veya kullanıcı tercihi |
|---|---|---|
| Uygulama özelliklerini ve çevrimdışı içeriği sunmak | Yerel tercihler, kaydedilen listeler, şehir paketleri, oynatma durumu | Talep ettiğiniz özelliği sunmak için gerekli; mümkün olduğunda cihazda yerel saklama |
| Satın alımları işlemek ve şehir paketlerinin kilidini açmak | StoreKit işlem bilgileri, RevenueCat App User ID, ürün ve entitlement bilgileri | Satın alma/sözleşme ve ilgili hizmetin sunulması |
| Özel indirmeleri yetkilendirmek ve hizmeti korumak | App Attest verileri, takma adlı uygulama kullanıcı kimliği, talep edilen paket ayrıntıları, teknik istek verileri | Satın alınan içeriğin teslimi ve kötüye kullanım/dolandırıcılığın önlenmesi |
| Geri bildirim, şehir talebi ve bildirimlere yanıt vermek | Gönderdiğiniz metin veya bildirim kimlikleri, uygulama/içerik sürüm bilgileri | Gönüllü talebiniz ve bu talebin sonuçlandırılması |
| Pelargo'yu anlamak ve geliştirmek | İsteğe bağlı ürün kullanım event'leri ve uygulama/cihaz üst verileri | Açık rızanız; istediğiniz zaman geri çekebilirsiniz |
| Yasal yükümlülükleri yerine getirmek ve uyuşmazlıkları ele almak | İlgili işlem, destek veya güvenlik kayıtları | Uygulanabilir yasal yükümlülükler ve izin verilen durumlarda meşru menfaat |

İsteğe bağlı analitiği reddetmeniz Pelargo'yu kullanmanızı, şehir paketi satın almanızı veya içeriğe erişmenizi engellemez.

## 4. Analitik izni ve tercihleriniz

Analitik siz izin verene kadar kapalıdır. **Analitik olmadan devam et** seçeneğini tercih ederek Pelargo'yu kullanmaya devam edebilirsiniz.

Tercihinizi istediğiniz zaman **Profil → Gizlilik ve Analitik** bölümünden değiştirebilirsiniz:

- Analitiği kapattığınızda Pelargo yeni analitik event'leri toplamayı durdurur, bekleyen yüklemeleri durdurur ve yerel SQLite kuyruğunda gönderilmeyi bekleyen event'leri siler.
- Daha önce PostHog'a iletilmiş event'ler, izni geri çekmenizle otomatik olarak silinmez.
- Daha önce gönderilmiş analitik verilerinin silinmesini **Profil → Gizlilik ve Analitik** bölümündeki silme talebi seçeneğinden veya [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com) adresine e-posta göndererek isteyebilirsiniz. Talep ilgili serviste incelenip işleme alınır; anında ve otomatik silme değildir. İşlem tamamlandığında size bilgi verilir.

## 5. Bilgileri kimlerle paylaşıyoruz?

Pelargo kişisel bilgileri satmaz veya kiralamaz. Bilgiler yalnızca uygulamayı sunmak, satın alımları işlemek, içerik dağıtmak, taleplere yanıt vermek veya isteğe bağlı analitik yürütmek için gerekli olduğu ölçüde hizmet sağlayıcılarla paylaşılır.

| Hizmet sağlayıcı | Kullanım amacı |
|---|---|
| **PostHog (EU Cloud)** | İzin verdikten sonra isteğe bağlı ürün analitiği event'lerini alır. EU Cloud hizmeti Almanya'nın Frankfurt şehrinde barındırılır. |
| **RevenueCat** | App Store işlemlerinin doğrulanmasına, satın alma erişim haklarının ve takma adlı App User ID'nin yönetilmesine yardımcı olur. |
| **Apple** | App Store/StoreKit satın alma işlemleri, App Attest, iOS servisleri ve Apple MapKit harita gösterimini sağlar. |
| **Cloudflare** | Pelargo'nun geri bildirim ve içerik bildirimi API'sini ve veritabanını, özel paket yetkilendirme API'sini ve erişim kayıtlarını, özel nesne depolama ve dosya dağıtım servislerini barındırır. |

Bu sağlayıcılar bilgileri kendi hizmet koşulları ve gizlilik dokümanları ile Pelargo'nun hizmet kullanımına ilişkin düzenlemeler kapsamında işler. Politikalarına aşağıdan ulaşabilirsiniz:

- [PostHog Gizlilik](https://posthog.com/privacy)
- [RevenueCat Gizlilik Politikası](https://www.revenuecat.com/privacy-policy)
- [Apple Gizlilik](https://www.apple.com/legal/privacy/)
- [Cloudflare Gizlilik Politikası](https://www.cloudflare.com/privacypolicy/)

## 6. Uluslararası veri işleme

PostHog analitiği Pelargo'nun EU Cloud projesine gönderilir. Apple, RevenueCat ve Cloudflare bilgileri kendilerinin veya hizmet sağlayıcılarının faaliyet gösterdiği ülkelerde işleyebilir. Bu ülkeler ikamet ettiğiniz ülkenin dışında olabilir. Uygulanabilir mevzuat uluslararası veri aktarımı için güvence gerektiriyorsa aktarım, uygun hukuki aktarım mekanizması ve hizmet sağlayıcıya ilişkin düzenlemeler çerçevesinde yapılmalıdır.

## 7. Saklama süreleri ve silme

Saklama yöntemleri veri türüne göre değişir. Bazı bilgiler cihazda veya hizmet sağlayıcılarda saklanırken, belirli geri bildirim, cihaz doğrulama ve erişim denetim kayıtları sabit bir otomatik sona erme süresi olmadan tutulur. Aşağıdaki açıklamalar, bu Politikanın tarihi itibarıyla Pelargo için incelenen mevcut yapılandırmayı yansıtır.

- **Yerel uygulama verileri:** Kaydedilen listeler, notlar, tercihler ve indirilen içerikler siz silene, ilgili şehir paketini kaldırana veya uygulamayı kaldırana kadar cihazınızda kalır. iOS cihaz yedekleri bu kapsamın dışında olabilir.
- **Gönderilmemiş analitik event'leri:** Yerel analitik kuyruğu yalnızca event'ler gönderilmeyi beklerken tutulur. Analitik iznini geri çektiğinizde kuyruk temizlenir.
- **PostHog'a gönderilmiş analitik:** PostHog projesi şu anda analitik event'leri için bir yıllık (en fazla 12 ay) saklama süresine göre yapılandırılmıştır. Bu event saklama ayarı, takma adlı Person Profile kayıtlarını veya bunların özelliklerini mutlaka silmez; bunlar ayrı ayarlara tabi olabilir ve ayrıca silinene kadar tutulabilir. Yukarıda açıklanan yöntemle silme talebinde bulunabilirsiniz. Proje yapılandırması ve hizmet planı değişebileceğinden, servis ayarları değiştiğinde bu süre yeniden kontrol edilir.
- **Geri bildirim ve içerik bildirimleri:** Başvuru ve inceleme kayıtları Cloudflare D1'de saklanır. Mevcut uygulamada bu kayıtlar için otomatik, zamana bağlı bir silme takvimi veya zamanlanmış temizlik işlemi bulunmamaktadır. Kayıtlar inceleme ve sonuçlandırma, içerik kürasyonu geçmişi, hizmetin korunması ve ilgili soru veya uyuşmazlıkların ele alınması amacıyla tutulur. Silme talepleri geçerli mevzuat kapsamında ayrı ayrı değerlendirilir; kayıtlar belirtilmiş bir sürenin sonunda otomatik olarak temizlenmez.
- **App Attest ve erişim güvenliği kayıtları:** Cloudflare D1'de uygulama kurulumu doğrulama kayıtları, cihaz anahtarı ve açık anahtar bilgileri ile ilgili yetkilendirme üst verileri saklanır. Süresi dolmuş veya tüketilmiş challenge kayıtları ile eski rate-limit pencereleri, yeni bir challenge oluşturulurken fırsat bulundukça temizlenir; bu işlem garantili ve sabit bir silme takvimi değildir. Kayıtlı cihaz bilgileri şu anda otomatik zamana bağlı silmeye tabi değildir.
- **Özel indirme denetim kayıtları:** Cloudflare D1'deki download-event kayıtları erişim geçmişi olarak tutulur. Bu kayıtlar için şu anda otomatik saklama süresi, zamanlanmış temizlik veya zamana bağlı silme yapılandırılmamıştır. Kayıtlar özel şehir paketi ve ses içeriği erişimine ilişkin yetkilendirme kararlarını kapsar. “Issued” sonucu geçici indirme bağlantısının yetkilendirilip oluşturulduğunu ifade eder; dosyanın başarıyla indirildiğini göstermez. Erişim kayıtlarında hash'lenmiş takma adlı tanımlayıcılar, rate-limit tablosunda ise ham IP adresi yerine isteğin IP adresinin hash'i kullanılır.
- **Özel nesne depolama:** İncelenen özel Cloudflare R2 bucket'larında nesneleri otomatik olarak sona erdiren veya silen yaşam döngüsü kuralları bulunmamaktadır. Şehir paketi sürümleri manuel olarak yönetilir; nesneler manuel olarak değiştirilene veya silinene kadar saklanır.
- **Satın alma kayıtları:** Apple ve RevenueCat işlem ve entitlement bilgilerini kendi politikaları ve geçerli yasal/muhasebe yükümlülükleri kapsamında saklayabilir.

PostHog event ve profil saklama hakkında daha fazla bilgi için [PostHog veri saklama dokümantasyonuna](https://posthog.com/docs/privacy/data-storage) bakabilirsiniz.

Pelargo'nun kontrol ettiği bilgilere erişmek veya bunların silinmesini istemek için [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com) adresinden bize ulaşabilirsiniz. Talebi işleme almadan önce kimliğinizi veya talebin size ait olduğunu doğrulamamız gerekebilir. Kanunen saklanması gereken veya hukuki taleplerin oluşturulması, kullanılması ya da savunulması için gerekli bazı bilgiler tutulabilir.

## 8. Gizlilik haklarınız

İkamet ettiğiniz yere ve uygulanabilir mevzuata bağlı olarak şu haklara sahip olabilirsiniz:

- Kişisel verilerinizin işlenip işlenmediğini öğrenme ve bir kopyasını isteme.
- Hatalı veya eksik bilgilerin düzeltilmesini isteme.
- Bilgilerin silinmesini veya belirli işlemlerin sınırlandırılmasını isteme.
- Uygulanabildiği durumlarda belirli işlemlere itiraz etme veya veri taşınabilirliği talep etme.
- İşleme açık rızaya dayanıyorsa rızanızı istediğiniz zaman geri çekme. Geri çekme, öncesinde yapılan işlemenin hukuka uygunluğunu etkilemez.
- Yetkili veri koruma kurumuna şikâyette bulunma.

### Türkiye'deki kullanıcılar

6698 sayılı Kişisel Verilerin Korunması Kanunu (KVKK) bakımından veri sorumlusu **Erdem Özdemir**'dir. KVKK'nın 11. maddesi kapsamındaki; kişisel verilerinizin işlenip işlenmediğini öğrenme, işlenmişse bilgi talep etme, hukuki şartları oluştuğunda düzeltme veya silme isteme ve kanunda yer alan diğer haklarınızı kullanma taleplerinizi [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com) adresine e-posta göndererek iletebilirsiniz.

Talepleriniz uygulanabilir mevzuatta öngörülen süre ve yöntemle yanıtlanır. Yanıtımızı yeterli bulmamanız halinde KVKK'da belirtilen usule uygun olarak Kişisel Verileri Koruma Kurumuna başvurabilirsiniz.

### Avrupa Ekonomik Alanı, Birleşik Krallık veya İsviçre'deki kullanıcılar

GDPR veya eşdeğer yerel mevzuatın uygulandığı durumlarda erişim, düzeltme, silme, işlemenin sınırlandırılması, itiraz ve veri taşınabilirliği haklarına; ayrıca yerel denetim kurumunuza şikâyette bulunma hakkına sahip olabilirsiniz. Belirli bir hakkın kullanılabilirliği, işlemenin hukuki sebebine ve koşullarına bağlıdır.

## 9. Güvenlik

Pelargo; kullanıcı listeleri ve tercihleri için yerel saklama, şifreli ağ bağlantıları, satın alma erişim kontrolleri ve korumalı içerik dağıtımı için App Attest doğrulaması dahil, bilgileri korumaya yönelik makul teknik ve organizasyonel önlemler kullanır. Hiçbir aktarım veya saklama yöntemi tamamen güvenli değildir; mutlak güvenlik garanti edilemez.

## 10. Çocukların gizliliği

Pelargo özellikle çocuklara yönelik tasarlanmamıştır ve çocukların kişisel bilgilerini bilerek toplamaz. Bir çocuğun geri bildirim veya destek formu aracılığıyla kişisel bilgi gönderdiğini düşünüyorsanız, talebi inceleyebilmemiz ve uygun işlemi yapabilmemiz için bizimle iletişime geçin.

## 11. Bu Politikadaki değişiklikler

Uygulama, hizmet sağlayıcılar veya geçerli yasal gereklilikler değiştiğinde bu Politikayı güncelleyebiliriz. Güncel sürüm bu URL'de, yenilenmiş "Son güncelleme" tarihiyle yayımlanır. İsteğe bağlı analitiğin amaçları, veri türleri veya alıcıları önemli ölçüde değişirse Pelargo bu işlem devam etmeden önce yeni bir analitik tercihi isteyebilir.

## 12. İletişim

Pelargo'nun veri işleme uygulamalarıyla ilgili gizlilik soruları, erişim veya silme talepleri ve diğer konular için:

**Erdem Özdemir**  
**E-posta:** [erdemsupports@gmail.com](mailto:erdemsupports@gmail.com)

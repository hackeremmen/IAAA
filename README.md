# IAAA
Identity and Access Management


																		TryHackMe - Identity and Access Management
																		==========================================


Task 2  IAAA Model
==================

İdentifikasiya, Doğrulama, Səlahiyyət və Hesabatlılıq (IAAA) informasiya təhlükəsizliyinin dörd sütunudur. Bu elementlərin hər biri məxfi məlumat və resursların məxfiliyinin, bütövlüyünün və əlçatanlığının təmin edilməsində mühüm rol oynayır.


IAAA Modelində IAAA identifikasiya, autentifikasiya, avtorizasiya və hesabatlılığı ifadə edir. IAAA modelinin dörd mərhələsi aşağıdakılardır:



1. Identification -  istifadəçinin kim olduğunu yoxlamaq prosesidir. Bu, istifadəçinin müəyyən bir şəxsiyyət iddiası ilə başlayır. Şəxsiyyət e-poçt ünvanı, istifadəçi adı və ya ID nömrəsi kimi unikal identifikatorla təmsil oluna bilər. Müvafiq mühitdə unikal olan istənilən identifikator etibarlı seçimdir; buna görə də, bir çox veb-saytlar istifadəçidən unikal istifadəçi adı yaratmağı xahiş etmək əvəzinə identifikasiya üçün e-poçt ünvanına etibar edərlər.

2. Authentication - istifadəçinin iddia etdiyi şəxs olmasını təmin etmək prosesidir. Başqa sözlə, bu addım iddia edilən şəxsiyyətin təsdiqlənməsi ilə bağlıdır. Doğrulamanın bir yolu düzgün parol təqdim etməkdir. Potensial parol zəiflikləri səbəbindən istifadəçilərdən e-poçtlarına göndərilən kodu yazmağı xahiş etmək kimi bir çox başqa üsullar populyarlıq qazanır.


3. Authorisation -  istifadəçinin nəyə daxil olmasına icazə verildiyini müəyyən edir. Başqa sözlə, onlara hesab imtiyazları əsasında xüsusi əməliyyatlar aparmaq səlahiyyəti veriləcək. Bu proses adətən istifadəçinin iş funksiyasına və ya icazə səviyyəsinə əsasən rolların və icazələrin təyin edilməsi ilə həyata keçirilir. İcazəsiz giriş və ya məlumatların pozulması riski yalnız istifadəçinin öz vəzifələrini yerinə yetirməsi üçün zəruri olan resurslara girişi məhdudlaşdırmaqla azaldılır.

4. Accountability -  öz hərəkətlərinə görə məsuliyyət daşıdıqlarını təmin etmək üçün istifadəçi fəaliyyətini izləyir. İstifadəçiyə sistemə giriş icazəsi verildikdən sonra hər kəsi öz hərəkətlərinə görə məsuliyyət daşıyan mexanizmlərə malik olmaq vacibdir. Bu proses bütün istifadəçi fəaliyyətini qeyd etməklə və onu mərkəzləşdirilmiş yerdə saxlamaqla əldə edilir. Təhlükəsizliklə bağlı insident baş verdikdə, bu məlumat problemin mənbəyini müəyyən etmək və müvafiq tədbirlər görmək üçün istifadə edilə bilər.


You are granted access to read and send an email. What is the name of this process?
Answer: Authorisation 

Which process would require you to enter your username?
Answer: Identification 

Although you have write access, you should only make changes if necessary for the task. Which process is required to enforce this policy?
Answer: Accountability 


Task 3  Identification
======================

İdentifikasiya istifadəçinin (və ya prosesin və ya sistemin) konkret şəxsiyyəti necə iddia etməsidir. Gündəlik həyatımızdan bir neçə nümunə nəzərdən keçirək. Tutaq ki, sizi bir məclisə dəvət etdilər və ünsiyyət qurmağa başladılar, sonra kimsə səndən soruşdu: "Adın nədir?" Və çox güman ki, onlara əsl adınızı deyəcəksiniz. Axı siz yaxşı vaxt keçirmək və yeni dostlar qazanmaq üçün oradasınız. Bir dəqiqə gözlə; siz həmçinin bir ad qoya və ya sevimli filminizdən bir şey seçə və "Tomas Anderson" kimi bir şeylə cavab verə bilərsiniz! İstənilən halda, digər şəxs şəxsiyyətinizi təsdiqləmək üçün şəxsiyyət vəsiqənizi istəməz; bu, yüksək təhlükəsizlik zonasına daxil olmaq deyil, sadəcə sosiallaşma hadisəsidir.

İdentifikasiya istifadəçi adı vasitəsilə ola bilər. İstifadəçi adı müxtəlif formalarda ola bilər. Məsələn, Tomas Anderson tanderson, thomasa, thomas01, ta001 və ya hətta ola bilər. a>neo. Hamısı təşkilatdan və platformadan asılıdır.

Eyniləşdirmə aşağıdakı kimi bir nömrə ilə də əldə edilə bilər:

National ID number
Student ID number
Passport number
Mobile phone number

Identifikasiya üçün istifadəçiyə xas olan istənilən nömrə istifadə oluna bilər. Bir çox veb-saytlar qeydiyyat üçün e-poçt ünvanı tələb edir, çünki istifadəçinin e-poçtunun unikal olacağına zəmanət verilir; bu, istifadəçini unikal istifadəçi adı tapmaqdan və onu yadda saxlamaqdan xilas edir.

Kompüterdən kənar başqa bir nümunəyə baxaq. İdman zalına getməyə yenicə başladınız və resepsiyonist sizdən adınızı soruşdu. Siz sevimli filminizdən adla cavab verə bilərsiniz; lakin resepsiyonist bu dəfə sizdən şəxsiyyət vəsiqənizi istəyə bilər. Niyə belə etsinlər? İddia etdiyiniz şəxs olduğunuzu təsdiqləmək üçün bu, identifikasiyadır. Təsadüfi bir oğlanın idman salonuna girməsinə və pullu abunəçilərindən birinin adını elan etməsinə icazə vermək istəmirlər. Hər kəs daxil olub abunəçi olduğunu iddia edə bilsə, idman zalı sahibləri qazanclı bir işə sahib ola bilməyəcəklər.

Müvafiq autentifikasiya olmadan ciddi ziyan dəyə bilər; bankdan kredit götürərkən saxta kimlik iddia edən kiminsə işinə nəzər salın. İT dünyasında autentifikasiya olmadan hər kəs e-poçt ünvanınızı bilsəydi, e-poçtunuza daxil ola bilərdi. Əksər sistemlər düzgün autentifikasiya olmadan düzgün işləyə bilməz; sistemlər kompüter sistemləri ilə məhdudlaşmır və bir çox başqaları arasında bank sistemləri, otel rezervasiya sistemləri və uçuş sistemlərini əhatə edir. Növbəti tapşırıqda autentifikasiyanı daha ətraflı əhatə edirik.






Which of the following cannot be used for identification?

1. Email address
2. Mobile number with international code
3. Year of birth
4. Passport number
Answer: 3




Which of the following cannot be used for identification?

1. Landline phone number
2. Street number
3. Health insurance card number
4. Student ID number
Answer: 2


Task 4  Authentication
======================


Autentifikasiya istifadəçinin və ya sistemin şəxsiyyətinin yoxlanılması prosesidir. İdman zalı nümunəmizə qayıdaq. İdman zalındakı resepsiyonist yalnız abunə olan üzvlərə icazə verir. Analoq dünyada buna necə nail olunur? Onlar sizdən idman zalı üzvlük kartınızı istəyə bilərlər (fərz edək ki, idman zalı hər abunəçi üçün bir kart təqdim edir). Fotoşəkiliniz və müvafiq idman zalı abunə məlumatları olan idman zalı üzvlük kartına sahib olmalısınız. Resepşn kartınızı yoxlayaraq şəxsiyyətinizi təsdiq edə bilər; autentifikasiya problemi həll olundu (kimsə kartı saxtalaşdırmağın bir yolunu tapmasa, lakin bu başqa problemdir).

İdentifikasiya və identifikasiya istənilən informasiya sisteminin və şəbəkəsinin əsas komponentləridir. İdentifikasiya və identifikasiya arasındakı fərqi başa düşmək vacibdir.

İdentifikasiya zamanı istifadəçi (və ya sistem və ya proses) müvafiq parametrlərdə spesifik (unikal) şəxsiyyətə iddia edir. Doğrulama istifadəçinin (və ya sistemin və ya prosesin) şəxsiyyətini sübut edir. Bu proses adətən aşağıdakı yollardan biri ilə həyata keçirilir:

1. Something you know
2. Something you have
3. Something you are

Daha az dərəcədə olsa da, daha iki üsul istifadə olunur:

* Somewhere you are (logical/physical location)
* Something you do (behaviour)


Answer the following questions using the correct item number from the numbered list below.

1. Something you know
2. Something you have
3. Something you are
4. 2FA

When you want to check your email, you enter your username and password. What kind of authentication is your email provider using?
Answer: 1

Your bank lets you finish most of your banking operations using its app. You can log in to your banking app by providing a username and a password and then entering the code received via SMS. What kind of authentication is the banking app using?
Answer: 4

Your new landline phone system at home allows callers to leave you a message when the call is not picked up. You can call your home number and enter a secret number to listen to recorded messages. What kind of authentication is being used here?
Answer: 1

You have just started working at an advanced research centre. You learned that you need to swipe your card and enter a four-digit PIN whenever you want to use the elevator. Under which group does this authentication fall?
Answer: 4





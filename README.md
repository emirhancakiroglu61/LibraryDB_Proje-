LibraryDB SQL Sorguları
Bu depo, bir kütüphane veritabanı (LibraryDB) için oluşturulmuş temel SQL sorgularını içerir. Dosyalar, bir books tablosunun oluşturulmasını, bu tabloya veri eklenmesini ve çeşitli sorgulama senaryolarını gösterir.

Dosyalar
LibraryDB.sql: books tablosunu oluşturan ve başlangıç verilerini ekleyen ana SQL dosyasıdır.

SQL sorguları.txt: books tablosu üzerinde gerçekleştirilen 10 farklı sorguyu ve bu sorguların açıklamalarını içerir.

Tablo Yapısı
books tablosu aşağıdaki sütunları içermektedir:

book_id: Kitap için benzersiz kimlik numarası (PRIMARY KEY).

title: Kitabın başlığı.

author: Kitabın yazarı.

genre: Kitabın türü (örn. 'roman', 'tarih', 'bilim').

price: Kitabın fiyatı (negatif olamaz).

stock_qty: Stoktaki kitap adedi (negatif olamaz).

published_year: Kitabın yayınlanma yılı (1800-2025 aralığında).

added_at: Kitabın veritabanına eklendiği tarih.

Kullanım
Veritabanınızı oluşturun ve USE LibraryDB; komutunu çalıştırın.

LibraryDB.sql dosyasını kullanarak books tablosunu oluşturun ve başlangıç verilerini ekleyin.

SQL sorguları.txt dosyasındaki sorguları inceleyebilir ve kendi veritabanınızda çalıştırarak sonuçları görebilirsiniz. Dosya, her bir sorgunun amacını açıklayan yorumlar içerir.

Örnek Sorgular
SQL sorguları.txt dosyasından bazı örnekler:

Tüm kitapları fiyata göre artan sırada listeleme:

SQL

SELECT title, author, price
FROM books
ORDER BY price ASC;
Türü 'roman' olan kitapları başlığa göre sıralama:

SQL

SELECT *
FROM books
WHERE genre = 'roman'
ORDER BY title ASC;
Fiyatı 80 ile 120 arasında olan kitapları bulma:

SQL

SELECT *
FROM books
WHERE price BETWEEN 80 AND 120;
Başlığında 'zaman' geçen kitapları filtreleme:

SQL

SELECT *
FROM books
WHERE title LIKE '%zaman%';

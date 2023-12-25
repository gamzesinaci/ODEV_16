# ODEV_16
**Pytest**
Geliştiricilerin birim testlerini hızlı bir şekilde yazıp yürütmesine olanak tanıyan Python için popüler bir test çerçevesidir. Test yazmak için basit ve kullanımı kolay bir sözdizimi sağlar ve işlevler, sınıflar ve modüller dahil her türlü Python kodunu test etmek için kullanılabilir.

**Dekoratör nedir? O nasıl çalışır?**
Bir dekoratör işlevi, argümanı olarak başka bir işlevi alır ve genellikle orijinal işlevin davranışını geliştiren veya değiştiren yeni bir işlev döndürür. Bu, işlevlerin kaynak kodlarını doğrudan değiştirmeden işlevlere işlevsellik katabilir ve bu da onu kodun yeniden kullanımı ve soyutlaması için güçlü bir araç haline getirir.

@pytest.mark.parametrize decorator'ü geliştiricinin aynı testi farklı değerler üzerinde tekrar tekrar çalıştırmasına olanak tanır.
import pytest 

def  add ( a, b ): 
    return a + b 

@pytest.mark.parametrize( "a, b, bekleniyor" , [ 
    ( 2 , 3 , 5 ), 
    ( 5 , 7 , 12 ), 
    ( - 2 , 2 , 0 ), 
] ) 
def  test_addition ( a, b, beklenen ): 
    asset add(a, b) == beklenen 

@pytest.mark.parametrize( "a, b" , [ 
    ( 2 , 3 ), 
    ( 5 , 7 ), 
    ( - 2 , 2 ), 
] ) 
def  test_positive_numbers ( a, b ): 
    iddia a > 0 
    iddia b > 0



@pytest.fixture verileri testlerimize hazırlamak için kullanılır. Fikstürler, gerçek test işlevlerinden önce (ve bazen sonra) pytest tarafından çalıştırılan işlevlerdir.
import pytest 

@pytest.fixture 
def  hazır_veri (): # Test verileri yazdırmasını 
    hazırlamak için kod ( "Test verileri hazırlanıyor..." ) verim # Test verileri yazdırmasını temizlemek için kod ( "Test verileri temizleniyor..." ) def test_database_operations ( kurulum_veritabanı, hazır_veri ): # Veritabanını ve hazırlanmış veri çıktısını gerektiren test kodu ( "Test çalıştırılıyor..." ) iddia 1 + 1 == 2

    
@pytest.mark.skip, belirtilen yerin atlanmasını sağlar.






















    

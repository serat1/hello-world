# Bir tane "Bilgisayar" sınıfı oluşturarak bu sınıfa metodlar ve özellikler ekleyin ve bu class'ı kullanmaya çalışın.

# Bu sınıfı yazarken öğrendiğimiz özel metodların hepsini tanımlamaya çalışın.

class Bilgisayar():

    def __init__(self,toplam_urun = []):
        self.toplam_urun = toplam_urun

    def urun_ekle(self, yeni_urun):
        self.toplam_urun.append(yeni_urun)
        print("Ürününüz eklendi. Yeni ürün listesi: ", envanter.toplam_urun)

    def ozellik_gir(self):
        pass


    def ozellik_degistir(self):
        pass

    def urun_listesi(self):
        print(self.toplam_urun)
        print(len(self.toplam_urun),"Adet urununuz bulunmakta.")

    def __len__(self):
        return len(self.toplam_urun)




envanter = Bilgisayar()



print("""
ENVANTER
--------
Yapılabilecekler
1. Yeni ürün ekle
2. Ürün özelliklerini gir
3. Ürün özelliklerini değiştir
4. Ürün listesi sorgula
5. Ürün sorgula
6. Ürün sayısını öğren
7. Bir ürünün özelliklerini öğren

** Yapmak istediğiniz işlem numarasını giriniz, çıkış için 'q' ya basınız.""")

while True:
    soru = input("Hangi işilemi yapmak istiyorsunuz: ")

    if (soru == "q"):
        break

    elif (soru == "1"):
        urun = input("Eklemek istediğiniz ürün ismini giriniz: ")
        envanter.urun_ekle(urun)

    elif (soru == "4"):
        envanter.urun_listesi()

    elif (soru == "5"):

        soru2 = input("Sorgulamak istediginiz urunu giriniz: ")

        if soru2 in envanter.toplam_urun:
            print("Ürün mevcut.")
            print(envanter.toplam_urun)

    elif (soru == "6"):
        print(len(envanter),"Adet ürün bulunmakta.")




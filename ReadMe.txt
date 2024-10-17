Genel Commit için
    git checkout master
    git pull origin master
    git add . 
    git commit -m "aciklama"
    git push origin master

Proje klasörünün içinde, her yazılımcı için ayrı klasör varsa;
-------------------------
Branch Kullanma:
Her yazılımcı kendi branch’inde çalışabilir. 

Branch oluşturmak için:
    git checkout -b yazilimci1-branch

-------------------------
Commit İşlemi:
Yazılımcılar kendi klasörlerindeki değişiklikleri commit edebilirler. Örneğin:
    git add yazilimci1/
    git commit -m "Yazılımcı 1 değişiklikleri"

-------------------------
Merge İşlemi:
Her yazılımcı kendi branch’inde çalıştıktan sonra, kodlarını ana branch'e (genellikle main veya master) birleştirebilir.
1. Merge yapmadan önce, ana branch'ten güncellemeleri almak için:
    git checkout main
    git pull origin main
    git checkout yazilimci1-branch
    git merge main
2. Eğer merge sırasında çatışma çıkmazsa, değişiklikleri ana branch'e merge edebilirsiniz:
    git checkout main
    git merge yazilimci1-branch

-------------------------
Push İşlemi:
Değişiklikleri GitHub’a göndermek için:
    git push origin main



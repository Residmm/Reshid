# Reshid
#list in python (very simple)
n = 0
print("\033[1mSiyahı\033[0m")
isler = []

while True:
    dovr = input("Davam etmək üçün - 1, Dayandırmaq üçün - 2, Siyahını görmək üçün - 3             ")

    if dovr == "2":
        break

    elif dovr == "3":
        if not isler:
            print("Siyahı boşdur!")
            continue

        for i, element in enumerate(isler, start=1):
            print(f"{i}. {element}")

        while True:
            sualb = input("silmək istədiyiniz var? Bəli-1 Xeyr-2    ")
            if sualb == "2":
                print("Oldu!")
                break
            elif sualb == "1":
                sualc = int(input("Neçəncini? "))
                if sualc > len(isler) or sualc == 0:
                    print("Düzgün qeyd edin")
                else:
                    del isler[sualc - 1]
                    if isler == []:
                        print("Bütün elementləri sildiniz")
                        break
                    else:
                        print("Nəticə belədir :")
                        for i, element in enumerate(isler, start=1):
                            print(f"{i}. {element}")
            else:
                print("Düzgün qeyd edin")
        if not isler:
            continue
    elif dovr=="1":
        n=len(isler)+1
        iş=input(f"Qeyd {n} :")
        isler.append(iş)
    else:
        print("Düzgün qeyd edin")
if isler !=[]:
    while True:
        sual=input("Yazdıqlarınızı yaddaşda saxlayaq?       Bəli-1 Xeyr-2                            ")        
        if sual=="2":
            print("Yazdıqlarınız yaddaşdan silindi")
            isler=[]
            break
        elif sual=="1":
            print("Yaddaşda saxlanıldı")
            suala=input("Yazdıqlarınızı görmək istəyirsiniz?     Bəli-1 Xeyr-2                            ")
            if suala=="1":
                for i,element in enumerate(isler,start=1):
                    print(f"{i}. {element}")
                while True:
                    sualb=input("silmək istədiyiniz var? Bəli-1 Xeyr-2    ")
                    if sualb=="2":
                        print("Oldu!")
                        break
                    elif sualb=="1":
                        while True:
                            sualc=int(input("Neçəncini? "))
                            if sualc>len(isler) or sualc==0:
                                print("Düzgün qeyd edin")
                            else:    
                                del isler[sualc-1]
                                print("Nəticə belədir :")
                                for i,element in enumerate(isler,start=1):
                                     print(f"{i}. {element}")
                                break     
                break    
            elif suala=="2":
                print("Oldu")
                break 
            else:
                print("Düzgün qeyd edin")       
        else: 
            print("Düzgün qeyd edin")

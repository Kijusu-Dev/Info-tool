#coding:utf-8

# Import et couleur pris de internet (Pas encore appris)
import os

os.system("cls")

COLORS = {\
"black":"\u001b[30;1m",
"red": "\u001b[31;1m",
"green":"\u001b[32m",
"yellow":"\u001b[33;1m",
"blue":"\u001b[34;1m",
"magenta":"\u001b[35m",
"cyan": "\u001b[36m",
"white":"\u001b[37m",
"yellow-background":"\u001b[43m",
"black-background":"\u001b[40m",
"cyan-background":"\u001b[46;1m",
"light-magenta":"\u001b[95m",
}

def colorText(text):
    for color in COLORS:
        text = text.replace("[[" + color + "]]", COLORS[color])
    return text

# Création de l'accés normal
colorall = "[[blue]] [[cyan]]"
print(colorText(colorall))

identifiant = "root"
mot_de_passe = "root"

user_id = input("Veuillez entrez votre identifiant : ")
user_password = input ("Veuillez entrez votre mot de passe : ")

if user_id == identifiant and user_password == mot_de_passe:
    print("")
    print("Vous êtes bien connecter en temps que", identifiant)
    print("")

    py_prog = True

    send_txt = True

    if send_txt == True:	
        command = "\t[[blue]]Les commandes[[cyan]]"
        print(colorText(command))
        print("")
        print("[1] Liens pour apprendre python")
        print("[2] Lien de mon IA")
        print("[3] Convertisseur binaire")
        print("[4] Encrypt & Décrypt & Identifier Hashes")
        print("[dev] Informations du développeur")
        print("")

    while py_prog:
        # Fonctions du programme
        py_prog = input("> ")
        if py_prog == "again":
            continue
        elif py_prog == "quit":
            break
        elif py_prog == "1":
            app_python = "\t[[blue]]Apprentissage python[[cyan]]"
            print(colorText(app_python))
            print("")
            print("[•] https://www.youtube.com/watch?v=HWxBtxPBCAc&list=RDCMUCS2e0hEJMhwd6bNscS60xTg&index=2")
            print("[•] https://www.youtube.com/watch?v=psaDHhZ0cPs&list=PLMS9Cy4Enq5JmIZtKE5OHJCI3jZfpASbR")
            print("[•] https://openclassrooms.com/fr/courses/235344-apprenez-a-programmer-en-python")
            print("")
        elif py_prog == "2":
            link_ia = "\t[[blue]]Lien de mon IA[[cyan]]"
            print(colorText(link_ia))
            print("")
            endev = "[[red]]En cours de développement...[[cyan]]"
            print(colorText(endev))
            print("")
        elif py_prog == "3":
            conv_binaire = "\t[[blue]]Convertisseur binaire[[cyan]]"
            print(colorText(conv_binaire))
            print("")
            print("[•] https://www.dcode.fr/code-binaire")
            print("")
        elif py_prog == "4":
            hashes = "\t[[blue]]Encrypt & Décrypt & Identifier Hashes[[cyan]]"
            print(colorText(hashes))
            print("")
            print("[•] https://md5decrypt.net/en/")
            print("[•] https://hashes.com/en/decrypt/hash")
            print("[•] https://md5decrypt.net/Detecteur/")
            print("[•] https://www.md5.fr/")
            print("")
        elif py_prog == "dev":
            devinfo = "\t[[red]]Informations du développeur[[red]]"
            print(colorText(devinfo))
            print("")
            print("Développeur : Kijusu")
            print("Prénom : Maxence")
            print("Age : 16")
            print("Profession : Bac pro sn")
            print("Avenir : Ingénieur informatique, Développeurs")
            colorall = "[[blue]] [[cyan]]"
            print(colorText(colorall))
            print("")
        else:
            print("Command inconnue")

else:
    print("")
    print("Mot de passe ou identifiant incorrect")
    print("")

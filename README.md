# Lab-7
def calculer_moyenne(notes):
    if not notes:
        return 0
    return sum(notes) / len(notes)

def obtenir_mention(moyenne):
    if moyenne >= 16:
        return "Très Bien"
    elif moyenne >= 14:
        return "Bien"
    elif moyenne >= 12:
        return "Assez Bien"
    elif moyenne >= 10:
        return "Passable"
    else:
        return "Insuffisant"

def main():
    nom = input("Entrez le nom de l'étudiant : ")
    notes_input = input("Entrez les notes séparées par des espaces : ")
    
    try:
        notes = [float(n) for n in notes_input.split()]
        moyenne = calculer_moyenne(notes)
        mention = obtenir_mention(moyenne)
        
        print(f"\nRésultat final :")
        print(f"Étudiant : {nom}")
        print(f"Moyenne  : {moyenne:.2f}")
        print(f"Mention  : {mention}")
        
    except ValueError:
        print("Erreur : Veuillez entrer des nombres valides.")

if __name__ == "__main__":
    main()

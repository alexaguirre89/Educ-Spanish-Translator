# Educ-Spanish-Translator
A Spanish translator that focuses on the educational purposes of translating in the classroom and will guide students instead of giving them the direct translation.
# Profe-Trans: Educational Spanish Translator Concept
def educational_translator(phrase, hint_mode=False):
    # Dictionary of specific Castilian rules for this demo
    # In a full app, this would be handled by a Small Language Model (SLM)
    rules = {
        "you": "In Castilian Spanish, use 'vosotros' for informal plural 'you', unlike 'ustedes' in Latin America.",
        "computer": "In Spain, we use 'el ordenador', whereas 'la computadora' is used elsewhere.",
        "car": "In Spain, use 'el coche' instead of 'el carro'."
    }

    print(f"--- Student Input: '{phrase}' ---")

    if hint_mode:
        print("💡 [HINT MODE ACTIVE]")
        if "you" in phrase.lower():
            print("Clue: You are talking to a group of friends in Madrid. Think of the 'vosotros' form!")
        print("Clue: Check if your verb needs to be in the Present Indicative or Subjunctive.")
        return "Can you try translating it now?"

    else:
        # Simplified translation logic for demonstration
        translation = "Vosotros coméis manzanas." # Example for 'You all eat apples'
        
        print(f"Translation: {translation}")
        print("\n--- Grammar Callout ---")
        print("1. Verb: 'Coméis' is the vosotros form of 'Comer'.")
        print(f"2. Regional Note: {rules['you']}")
        
        return translation

# Testing the script
educational_translator("You all eat apples", hint_mode=True)
print("\n" + "="*30 + "\n")
educational_translator("You all eat apples", hint_mode=False)

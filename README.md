import random

def guess_number():
    # Generer et tilfældigt tal mellem 1 og 100
    secret_number = random.randint(1, 100)
    attempts = 0

    print("Velkommen til Gæt et Tal!")

    while True:
        guess = int(input("Gæt et tal mellem 1 og 100: "))
        attempts += 1

        if guess < secret_number:
            print("Dit gæt er for lavt. Prøv igen.")
        elif guess > secret_number:
            print("Dit gæt er for højt. Prøv igen.")
        else:
            print(f"Fantastisk! Du gættede det rigtige tal ({secret_number}) på {attempts} forsøg!")
            break

if __name__ == "__main__":
    guess_number()

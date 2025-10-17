import requests
import pandas as pd

#Colunas: Title,Year,Rated,Released,Runtime,Genre,Director,Writer,Actor,Plot,Language,Country,Awars,Poster,Ratings,Metascore,
#imdbRating,imdbVotes,imdbId,Type,DVD,BoxOffice,Production,Website,Response

titulos_filme = {"Spider-Man",
                 "Spider-Man 2",
                 "Spider-Man 3",
                 "The Amazing Spider-Man",
                 "The Amazing Spider-Man 2",
                 "Captain America: Civil War",
                 "Spider-Man: Homecoming",
                 "Avengers: Infinity War",
                 "Avengers: Endgame",
                 "Spider-Man: Far From Home",
                 "Spider-Man: No Way Home",
                 "Spider-Man: Into the Spider-Verse",
                 "Spider-Man: Across the Spider-Verse"
                 }

lista_dados = []

for titulo in titulos_filme:

    url = f"http://www.omdbapi.com/?apikey=[KEY]&t={titulo}"

    request = requests.get(url)
    data = request.json()

    info_filme = {
        "Title": data.get("Title"),
        "Year": data.get("Year"),
        "Genre": data.get("Genre"),
        "Country": data.get("Country"),
        "Metascore": data.get("Metascore"),
        "imdbRating": data.get("imdbRating"),
        "BoxOffice": data.get("BoxOffice")
    }

    lista_dados.append(info_filme)

df = pd.DataFrame(lista_dados)

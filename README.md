# Ramme for API-spørring
# Lim inn spørring fra API-konsoll i PostContents
# Fyll inn tabellnummer i kilde URL

let
	PostContents = "...",
	Kilde = Web.Contents("https://data.ssb.no/api/v0/no/table/.../", [Content=Text.ToBinary(PostContents)]),
	Data=Csv.Document(Kilde, [Encoding=1252])
in
	Data

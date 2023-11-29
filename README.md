## Playing cards classification
Oznaczenia 52 klas 
'10C', '10D', '10H', '10S', '2C', '2D', '2H', '2S', '3C', '3D', '3H', '3S', '4C', '4D', '4H', '4S', '5C', '5D', '5H', '5S', '6C', '6D', '6H', '6S', '7C', '7D', '7H', '7S', '8C', '8D', '8H', '8S', '9C', '9D', '9H', '9S', 'AC', 'AD', 'AH', 'AS', 'JC', 'JD', 'JH', 'JS', 'KC', 'KD', 'KH', 'KS', 'QC', 'QD', 'QH', 'QS'
składają się z numeru lub figury karty oraz jej koloru.

Kolory:
- H - (Hearts) kier
- D - (Dimonds) karo
- C - (Clubs) trefl
- S - (Spades) pik


Figury:
- A - As
- K - Król
- Q - Dama
- J - Walet

### Trenowanie 

Z uwagi na problemy z uruchomieniem trenowania posługując się ścieżkami względnymi użyto ścieżek bezwzględnych dlatego trzeba zadbać o poprawne ścieżki w poniższych miejscach.
- W pliku ".\dataset\data.yaml" należy podać ścieżki do folderów ze zbiorem danych treningowych, walidacyjnych i testowych
- W wywołaniu komendy w folderze ".\yolov5":

    python .\train.py --img 416 --epochs 3 --data C:\Users\brosz\PycharmProjects\playingCardsClassification\dataset\data.yaml --weights yolov5s.pt

### Walidacja 
Również należy zadbać o odpowiednie ścieżki do plików.
- W wywołaniu komendy w folderze ".\yolov5":

    python .\val.py --weights C:\Users\brosz\PycharmProjects\playingCardsClassification\yolov5\runs\train\exp7\weights\best.pt --data C:\Users\brosz\PycharmProjects\playingCardsClassification\dataset\data.yaml --img 416 

### Detekcja
Również należy zadbać o odpowiednie ścieżki do plików.
- W wywołaniu komendy w folderze ".\yolov5":

    python ./detect.py --weights C:\Users\brosz\PycharmProjects\playingCardsClassification\yolov5\runs\train\exp7\weights\best.pt  --conf 0.25 --source C:\Users\brosz\PycharmProjects\playingCardsClassification\imgs_to_predict\1.jpeg

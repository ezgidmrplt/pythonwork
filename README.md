# pythonwork
import math

# 1. Noktaları Tanımlama
points = [(1, 2), (4, 6), (7, 8), (2, 1)]

# 2. Öklid Mesafesi Hesaplayan Fonksiyon Tanımı
def euclideanDistance(point1, point2):
    x1, y1 = point1
    x2, y2 = point2
    return math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2)

# 3. Mesafeleri Hesaplama ve Saklama
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# 4. Minimum Mesafenin Bulunması
min_distance = min(distances)
print("Minimum Öklid Mesafesi:", min_distance)

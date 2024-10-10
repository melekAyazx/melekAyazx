

import math

# Öklid mesafesini hesaplayan fonksiyon
def euclideanDistance(point1, point2):
    return math.sqrt((point2[0] - point1[0])**2 + (point2[1] - point1[1])**2)

# 2D uzaydaki noktalar
points = [(1, 2), (4, 6), (5, 1), (8, 3)]

# Noktalar arasındaki mesafeleri tutan liste
distances = []

# Her nokta çifti arasındaki mesafeyi hesaplayan döngü
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)

# Minimum mesafeyi bulma
min_distance = min(distances)

distances, min_distance

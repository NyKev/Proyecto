# Lista de nombres de los alumnos
nombres_alumnos = ["Nicole", "Jessica", "Andy", "Angel", "Oswaldo", "Kevin", "Paola", "Eliu"]

# Definir una lista vacía para almacenar los promedios de los alumnos
promedios_alumnos = []

# Función para calcular el promedio de 3 calificaciones
def calcular_promedio(calificaciones):
    return sum(calificaciones) / len(calificaciones)

# Ciclo para obtener las calificaciones de los alumnos
for nombre in nombres_alumnos:
    print(f"Alumno: {nombre}")
    calificaciones = []
    
    # Ciclo para obtener 3 calificaciones de cada alumno
    for j in range(3):
        calificacion = float(input(f"Ingresa la calificación del parcial {j+1}: "))
        calificaciones.append(calificacion)
    
    # Calcular y almacenar el promedio del alumno
    promedio = calcular_promedio(calificaciones)
    promedios_alumnos.append((nombre, promedio))

# Mostrar los promedios de los alumnos
print("\nPromedios de los alumnos:")
for nombre, promedio in promedios_alumnos:
    print(f"{nombre}: {promedio:.2f}")

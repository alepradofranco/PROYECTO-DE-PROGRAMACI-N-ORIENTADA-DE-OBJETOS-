# PROYECTO-DE-PROGRAMACI-N-ORIENTADA-DE-OBJETOS-
ACEPTACION DE CUPOS


class Aspirante:
    def __init__(self, nombre, apellido, edad):
        self.nombre = nombre
        self.apellido = apellido
        self.edad = edad

    def iniciar(self):
        print(f"Inscripción para {self.nombre} {self.apellido} de {self.edad} años de edad.")

    def actualizar_datos(self, nuevo_nombre=None, nuevo_apellido=None, nueva_edad=None):
        if nuevo_nombre:
            self.nombre = nuevo_nombre
        if nuevo_apellido:
            self.apellido = nuevo_apellido
        if nueva_edad:
            self.edad = nueva_edad
        print(f"Datos actualizados: {self.nombre} {self.apellido}, {self.edad} años.")

    def mostrar_info(self):
        print(f"Inscripción de {self.nombre} {self.apellido} de {self.edad} años de edad.")


class Evaluacion:
    def __init__(self, tipoEvaluacion, fecha, nota):
        self.tipoEvaluacion = tipoEvaluacion
        self.fecha = fecha
        self.nota = nota

    def registroEvaluacion(self):
        print(f"Evaluación de tipo {self.tipoEvaluacion} registrada el {self.fecha} con nota {self.nota}.")

    def realizar(self):
        print(f"Evaluación de tipo {self.tipoEvaluacion} realizada el {self.fecha}.")

    def resultado(self):
        print(f"Resultado de la evaluación {self.tipoEvaluacion}: Nota {self.nota}.")


class Cupos:
    # Atributo de clase
    estado_cupo = "Disponible"

    def __init__(self, numero_cupos, tipo_cupo):
        self.numero_cupos = numero_cupos
        self.tipo_cupo = tipo_cupo

    def mostrar_info(self):
        print(f"Cupo: {self.numero_cupos} de tipo {self.tipo_cupo}")

    def actualizar_cupo(self, nuevo_numero_cupos):
        self.numero_cupos = nuevo_numero_cupos
        print(f"Cupo actualizado a {self.numero_cupos}")

    def eliminar_cupo(self):
        print(f"Cupo {self.numero_cupos} de tipo {self.tipo_cupo} eliminado")


class SegmentoPoblacional:
    def __init__(self, genero, etnia, edad):
        self.genero = genero
        self.etnia = etnia
        self.edad = edad

    def actualizar_genero(self, nuevo_genero):
        self.genero = nuevo_genero
        print(f"Género actualizado a {self.genero}")

    def actualizar_etnia(self, nueva_etnia):
        self.etnia = nueva_etnia
        print(f"Etnia actualizada a {self.etnia}")

    def actualizar_edad(self, nueva_edad):
        self.edad = nueva_edad
        print(f"Edad actualizada a {self.edad}")


class Periodo:
    def __init__(self, año, semestre, fecha_inicio):
        self.año = año
        self.semestre = semestre
        self.fecha_inicio = fecha_inicio
        print(f"Creando el periodo {año}, semestre {semestre} con fecha de inicio {fecha_inicio}")

    def mostrar_info(self):
        print(f"Periodo: Año = {self.año}, Semestre = {self.semestre}, Fecha de inicio = {self.fecha_inicio}")

    def actualizar_periodo(self, nuevo_año, nuevo_semestre, nueva_fecha_inicio):
        self.año = nuevo_año
        self.semestre = nuevo_semestre
        self.fecha_inicio = nueva_fecha_inicio
        print(f"Periodo actualizado a {self.año}, Semestre {self.semestre} con fecha {self.fecha_inicio}")

    def generar_codigo_periodo(self):
        codigo = f"{self.año}-S{self.semestre}"
        print(f"El código del periodo es: {codigo}")


# ============================
# Ejemplos de uso
# ============================

# Aspirante
aspirante1 = Aspirante("Leyker", "Prado", 19)
aspirante1.iniciar()
aspirante1.actualizar_datos(nuevo_apellido="Prado Franco")

# Evaluación
evaluacion1 = Evaluacion("Computadora", "2025-07-05", 70)
evaluacion1.registroEvaluacion()
evaluacion1.resultado()

# Cupos
cupos1 = Cupos(50, "General")
cupos1.mostrar_info()
cupos1.actualizar_cupo(45)

# Segmento poblacional
segmento1 = SegmentoPoblacional("Masculino", "Mestizo", 19)
segmento1.actualizar_genero("Masculino")
segmento1.actualizar_edad(20)

# Periodo
periodo1 = Periodo(2025, 1, "2025-01-15")
periodo1.mostrar_info()
periodo1.generar_codigo_periodo()

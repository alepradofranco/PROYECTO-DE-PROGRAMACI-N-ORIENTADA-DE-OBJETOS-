# PROYECTO-DE-PROGRAMACI-N-ORIENTADA-DE-OBJETOS-
ACEPTACION DE CUPOS

#definir la clase aspirante
class Aspirante:
    #atributo de clase
    status= 'aspirante'

    def __init__(self, nombre, apellido, edad):
        print(f"Se ha creado un nuevo aspirante {nombre} {apellido} de {edad} años") 
        self.nombre = nombre
        self.apellido = apellido
        self.edad = edad   
#definir metodos de la clase aspirante
    def inscribir(self, carrera):
        return f"El {Aspirante.status} se ha inscrito en la carrera {carrera}"
    def ingresar(self,):
        return f"EL {Aspirante.status} {self.nombre} ingreso al sistema"
    def salir(self,):
        return f"EL {Aspirante.status} {self.nombre } salio del sistema"
       
#Instanciar la clase aspirante, creando un objeto llamado aspirante1
aspirante1 = Aspirante("Bartolo", "Saberes", 19)
#atributos de instancia
print(aspirante1.nombre)
print(aspirante1.apellido)  
print(aspirante1.edad)

#llamar metodos
print(aspirante1.inscribir("TI"))
print(aspirante1.ingresar())
print(aspirante1.salir())

#leyker
#definir la clase segmento poblacional
class Segmentopoblacional:
    def __init__(self, leveleducativo, ingresos,intereses):
        print(f"Se ha creado un nuevo segmento poblacional con nivel educativo {leveleducativo} e ingresos mensuales de {ingresos} y con intereses en {intereses}") 
        self.leveleducativo = leveleducativo
        self.ingresos = ingresos
        self.intereses = intereses
    #definir metodos de la clase segmento poblacional
    def actualizar_ingresos(self,newingreso):
        self.ingresos=newingreso
        return(f"Los ingresos mensuales fueron actualizados correctamente: {self.ingresos}")
    def resumensegmento(self):
        return (f"Nivel educativo: {self.leveleducativo}, Ingresos: {self.ingresos}, Intereses: {self.intereses}")
    
#Instanciar la clase aspirante , creando un objeto llamado aspirante1
Segmentopoblacional1 = Segmentopoblacional("Universitario", 520, "Tecnología")

#atributo de instancia
print(Segmentopoblacional1.leveleducativo)
print(Segmentopoblacional1.ingresos)   
print(Segmentopoblacional1.intereses)

#llamar metodos
print(Segmentopoblacional1.resumensegmento())

# Actualizando ingresos
Segmentopoblacional1.actualizar_ingresos(650)
print(Segmentopoblacional1.resumensegmento())

#definir la clase universidad
class Universidad:
    uni = 'Universidad'
    
    def __init__(self,nameUni,direccion,contacto):
        print(f"Se ha creado la universidad {nameUni} su direccion es: {direccion} sus contactos son: {contacto} ")
        self.nameUni = nameUni
        self.direccion =direccion
        self.contacto=contacto
        
        #definir metodos de la clase universidad
    def agregarestudiante(self,agregar):
        return(f"La {Universidad.uni} {self.nameUni} agrego  {agregar} {Aspirante.status}" )
    def obtener_num_Aspirantes (self,numero_de_aspirantes):
        return(f"La {Universidad.uni} tiene un total de {numero_de_aspirantes} {Aspirante.status}")
    def mostrarinformacion(self):
        return (f"Nombre: {self.nameUni}\n" 
                f"Ubicación: {self.direccion}\n"
                f"{universidad1.obtener_num_Aspirantes(999)}\n")
    

 #instanciar la clase universidad ,creando un objeto llamado universidad1
 
universidad1 = Universidad("Uleam","Avn. Circunvalacion", "1234567890")
print(universidad1.agregarestudiante(1))
print(universidad1.mostrarinformacion())


#Leslie
#definir la clase Asignacion
class Asignacion:
    
    def __init__(self,estado,fecha_asignacion,nombre_de_carrera_asignada):
        print(f"Se generaro un reporte de asignacion: {estado}/ su fecha: {fecha_asignacion} /carrera:{nombre_de_carrera_asignada} ")
        self.estado = estado 
        self.fecha_asignacion =fecha_asignacion
        self.nombre_de_carrera_asignada = nombre_de_carrera_asignada
        
    #definir metodos de la clase aspirante 
    def asignar_cupo(self,cupo):
        return f"Se ha {self.estado} {cupo} cupo al {Aspirante.status} en la carrera {self.nombre_de_carrera_asignada}"
    def cupo_aceptado(self,aceptado):
        return f"El {Aspirante.status} {aspirante1.nombre} ha {aceptado} su cupo "
    def cupo_rechazado (self, rechazado):
        return f" El {Aspirante.status} {aspirante1.nombre} ha {rechazado} su cupo "
        
#instanciar la clase Asignacion ,creando objeto llamado Asignacion1

asignacion1=Asignacion("Asignado","25/25/2025","TI")
print(asignacion1.estado)
print(asignacion1.fecha_asignacion)
print(asignacion1.nombre_de_carrera_asignada)
print(asignacion1.asignar_cupo(1))
print(asignacion1.cupo_rechazado("Rechazado"))
print(asignacion1.cupo_aceptado("Aceptado"))


#definir la clase cupos
class Cupos:
    
    
    def __init__(self,totalcupos,numero_de_asignados,numero_de_no_asignados):
        print(f"cupos existentes: {totalcupos} asignados: {numero_de_asignados} no asignados: {numero_de_no_asignados}")
        self.totalcupos = totalcupos
        self.numero_de_asignados = numero_de_asignados
        self.numero_de_no_asignados = numero_de_no_asignados
        
    def mostrar_cupos_totales(self):
        return f"La {Universidad.uni} {universidad1.nameUni} tiene un total de {self.totalcupos} cupos "
    def Agregar_cupos(self,agregar_cupos):
        return f"La {Universidad.uni} {universidad1.nameUni} agrego {agregar_cupos} cupos "
    def eliminar_cupos(self,eliminar_cupos):
        return f"La {Universidad.uni} {universidad1.nameUni} elimino {eliminar_cupos} cupos"
        
    
#instanciando clase cupos ,creando objeto llamado cupos

cupos1=Cupos("800","650","150") 
print(cupos1.numero_de_asignados)
print(cupos1.numero_de_no_asignados)
print(cupos1.totalcupos)   
print(cupos1.mostrar_cupos_totales())
print(cupos1.Agregar_cupos(100))
print(cupos1.eliminar_cupos(30))

#imprimimos el status de aspirante 1
print (Aspirante.status)
#cambiamos es status a studiante
Aspirante.status = "estudiante"
#imprimimimos el nuevo status para instanciar el objeto aspirante2
print (Aspirante.status)

#instanciamos el nuevo objeto con  otro status
aspirante2 = Aspirante("Bartolo", "Saberes", 19)
print(aspirante2.nombre)
print(aspirante2.apellido)  
print(aspirante2.edad)

#llamar metodos

print(aspirante2.inscribir("TI"))
print(aspirante2.ingresar())
print(aspirante2.salir())


# Ejemplos de uso

# ----------------------------
# Aspirante
aspirante1 = Aspirante("Bartolo", "Saberes", 19)
print(aspirante1.inscribir("Tecnologías de la Información"))
print(aspirante1.ingresar())
print(aspirante1.salir())

# ----------------------------
# Segmento Poblacional
segmento1 = Segmentopoblacional("Universitario", 520, "Tecnología")
print(segmento1.resumensegmento())
print(segmento1.actualizar_ingresos(650))
print(segmento1.resumensegmento())

# ----------------------------
# Universidad
universidad1 = Universidad("Uleam", "Av. Circunvalación", "1234567890")
print(universidad1.agregarestudiante(1))
print(universidad1.obtener_num_Aspirantes(999))
print(universidad1.mostrarinformacion())

# ----------------------------
# Asignación
asignacion1 = Asignacion("Asignado", "25/05/2025", "Tecnologías de la Información")
print(asignacion1.asignar_cupo(1))
print(asignacion1.cupo_aceptado("aceptado"))
print(asignacion1.cupo_rechazado("rechazado"))

# ----------------------------
# Cupos
cupos1 = Cupos(800, 650, 150)
print(cupos1.mostrar_cupos_totales())
print(cupos1.Agregar_cupos(100))
print(cupos1.eliminar_cupos(30))

# ----------------------------
# Cambio de estado del aspirante
print("Estado actual:", Aspirante.status)
Aspirante.status = "estudiante"
print("Nuevo estado:", Aspirante.status)

aspirante2 = Aspirante("Carla", "Mendoza", 20)
print(aspirante2.inscribir("Derecho"))
print(aspirante2.ingresar())
print(aspirante2.salir())

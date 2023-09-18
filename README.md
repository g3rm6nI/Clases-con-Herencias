# Clases-con-Herencias
Ejercicio Clases con Herencias

# Clase Curso
class Curso:
def __init__(self, fecha_comienzo, titulo, descripcion,
objetivos, programa, costo, duracion_meses, foto, estado,
categoria):
self.__fecha_comienzo = fecha_comienzo
self.__titulo = titulo
self.__descripcion = descripcion
self.__objetivos = objetivos
self.__programa = programa
self.__costo = costo
self.__duracion_meses = duracion_meses
self.__foto = foto
self.__estado = estado
self.__categoria = categoria
self.__clases = []
def agregar_clase(self, fecha, titulo, contenido, URLDrive):
clase = Clase(fecha, titulo, contenido, URLDrive)
self.__clases.append(clase)

# Getter y Setter de Curso
def get_fecha_comienzo(self):
return self.__fecha_comienzo
def set_fecha_comienzo(self, fecha_comienzo):
self.__fecha_comienzo = fecha_comienzo
def get_titulo(self):
return self.__titulo
def set_titulo(self, titulo):
self.__titulo = titulo
def get_ descripcion (self):
return self.__ descripcion
def set_ descripcion (self, descripcion):
self.__ descripcion = descripcion
def get_ objetivos (self):
return self.__ objetivos
def set_ objetivos (self, objetivos):
self.__ objetivos = objetivos
def get_ programa (self):
return self.__ programa
def set_ programa (self, programa):
self.__ programa = programa
def get_ costo (self):
return self.__ costo
def set_ costo (self, costo):
self.__ costo = costo
def get_ duracion_meses (self):
return self.__ costo
def set_ duracion_meses (self, duracion_meses):
self.__ duracion_meses = duracion_meses
def get_ foto (self):
return self.__ foto
def set_ foto (self, foto):
self.__ foto = foto
def get_ estado (self):
return self.__ estado
def set_ estado (self, estado):
self.__ estado = estado
def get_ categoria (self):
return self.__ categoria
def set_ categoria (self, categoria):
self.__ categoria = categoría

# Clase Usuario
class Usuario:
    def __init__(self, nombre, apellido, dni, direccion, fecha_nacimiento, localidad, codigo_postal, provincia, telefono_celular, email, clave):
        self.__nombre = nombre
        self.__apellido = apellido
        self.__dni = dni
        self.__direccion = direccion
        self.__fecha_nacimiento = fecha_nacimiento
        self.__localidad = localidad
        self.__codigo_postal = codigo_postal
        self.__provincia = provincia
        self.__telefono_celular = telefono_celular
        self.__email = email
        self.__clave = clave
        self.__activo = False
    
# Método para activar la cuenta del usuario
    def activar_cuenta(self):
        self.__activo = True

# Herencia de la clase Docente heredando de la clase Usuario
class Docente(Usuario):
def __init__(self, apellido, nombre, dni, fecha_nacimiento,
direccion, localidad, codigo_postal, provincia, telefono_celular,
email, clave):
super().__init__(apellido, nombre, dni, direccion, fecha_nacimiento,
localidad, codigo_postal, provincia, telefono_celular, email, clave)

# Clase Compra
class Compra:
def __init__(self, id_compra, id_carrito_compra, id_medios_pago,
id_usuario, fecha, monto_total):
self.__id_compra = id_compra
self.__id_carrito_compra = id_carrito_compra
self.__id_medios_pago = id_medios_pago
self.__id_usuario = id_usuario
self.__fecha = fecha
self.__monto_total = monto_total

# Clase Medios de Contacto
class MediosDeContacto:
def __init__(self, id_mediocontacto, fecha, email, telefono,
direccion, nombre):
self.__id_mediocontacto = id_mediocontacto
self.__fecha = fecha
self.__email = email
self.__telefono = telefono
self.__direccion = direccion
self.__nombre = nombre

# Enumeración Tipos de Medio de Contacto
class TiposDeMedioDeContacto(enum.Enum):
whatsapp = "whatsapp"
correo_electronico = "correo electrónico"
call_center = "call center"
referido_interno = "referido interno"

# Clase TiposMedioContacto heredando de MediosDeContacto
class TiposMedioContacto(MediosDeContacto):
    def __init__(self, id_medio_contacto, fecha, email, telefono, direccion, nombre, tipo):
        super().__init__(id_medio_contacto, fecha, email, telefono, direccion, nombre)
        self.tipo = tipo

# Ejemplo de uso
usuario1 = Usuario("NombreUsuario", "ApellidoUsuario", "87654321", "DirecciónUsuario", "01/01/1990", "LocalidadUsuario", "1234", "ProvinciaUsuario", "1234567890", "usuario@example.com", "clave")
usuario1.activar_cuenta()

docente1 = Docente("NombreDocente", "ApellidoDocente", "78901234", "10/10/1980", "DirecciónDocente", "LocalidadDocente", "5678", "ProvinciaDocente", "9876543210", "docente@example.com")

compra1 = Compra(1, 123, 456, usuario1, "01/09/2023", 500.0)

medio_contacto1 = TiposMedioContacto(1, "01/09/2023", "contacto@example.com", "1234567890", "DirecciónContacto", "NombreContacto", TiposMedioContacto.WhatsApp)

print(f"Usuario: {usuario1.get_nombre()} {usuario1.get_apellido()} - Cuenta activa: {usuario1._Usuario__activo}")
print(f"Docente: {docente1.get_nombre()} {docente1.get_apellido()} - Cuenta activa: {docente1._Usuario__activo}")
print(f"Compra realizada el {compra1.fecha} por un total de ${compra1.monto_total}")
print(f"Medio de contacto: {medio_contacto1.tipo} - Email: {medio_contacto1.email} - Teléfono: {medio_contacto1.telefono}")






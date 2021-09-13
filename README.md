"# flaskapi" 
votaciones.sql es la base de datos escrita MYSQL
la base de datos contiene triguer para almacenar log de registros de nuevos votantes 
la tabla que almacena esta informacion se llama historialvotante
el archivo modelovotaciones es el modelo relacional de la base de datos
![modelovotaciones](https://user-images.githubusercontent.com/33339574/133038161-1a15bd9b-5d54-4e37-b42b-dd918f77f8c8.png)

a continucion encontrara los servicios con las rutas creadas
api.add_resource(Loguin,'/api/v1/loguin')
api.add_resource(Departamentos,'/api/v1/departamentos/<int:user>/<int:idd>','/api/v1/guardadepartamento','/api/v1/deletedepartamento/<int:user>/<int:id>','/api/v1/actualizardepartamento')
api.add_resource(Departamento,'/api/v1/departamentos/<int:user>')

api.add_resource(Municipios,'/api/v1/<int:user>/municipios')
api.add_resource(Municipio,'/api/v1/<int:user>/municipios/<int:idm>','/api/v1/guardamunicipio','/api/v1/<int:user>/deletemunicipio/<int:idm>','/api/v1/actualizarmunicipio')

api.add_resource(Comunas,'/api/v1/<int:user>/comunas')
api.add_resource(Comuna,'/api/v1/<int:user>/comunas/<int:idco>','/api/v1/guardacomuna','/api/v1/<int:user>/deletecomuna/<int:idc>','/api/v1/actualizarcomuna')

api.add_resource(Barrios,'/api/v1/<int:user>/barrios')
api.add_resource(Barrio,'/api/v1/<int:user>/barrios/<int:idba>','/api/v1/guardabarrio','/api/v1/<int:user>/deletebarrio/<int:idba>','/api/v1/actualizarbarrio')

api.add_resource(Personas,'/api/v1/<int:user>/personas')
api.add_resource(Persona,'/api/v1/<int:user>/personas/<int:cc>','/api/v1/guardapersona','/api/v1/<int:user>/deletepersona/<int:cc>','/api/v1/actualizarpersona')

api.add_resource(Usuarios,'/api/v1/<int:user>/usuarios')
api.add_resource(Usuario,'/api/v1/<int:user>/usuarios/<int:cc>','/api/v1/guardausuario','/api/v1/<int:user>/deleteusuario/<int:cc>')

api.add_resource(Puestos,'/api/v1/<int:user>/puestos')
api.add_resource(Puesto,'/api/v1/<int:user>/puestos/<int:idp>','/api/v1/guardapuesto','/api/v1/<int:user>/deletepuesto/<int:idp>','/api/v1/actualizarpuesto')

api.add_resource(Votantes,'/api/v1/<int:user>/votantes')
api.add_resource(VotantesXlider,'/api/v1/<int:user>/votantes/lider/<int:idli>')
api.add_resource(VotantesXthislider,'/api/v1/<int:user>/votantes/thislider')
api.add_resource(VotantesXmunicipios,'/api/v1/<int:user>/votantes/municipio/<int:idmu>')
api.add_resource(VotantesXpuesto,'/api/v1/<int:user>/votantes/puesto/<int:idp>')
api.add_resource(Votante,'/api/v1/guardavotante')

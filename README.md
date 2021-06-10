# Desafio Spring de Emanuel Flores

### Proceso de desarrollo

Se plantearon una serie de requerimientos a cumplir para que Meli tenga una version beta de Social Meli

Primero, en grupo, se plantearon las bases del proyecto
Establecimos que era necesario contar con las siguientes capas:
- Capa Controlador
- Capa de Servicios
- Capa de Repositorio

A modo personal comence con el desarrollo de los controladores para cada endpoint:

Controlador usuarios:

    POST -> /{userId}/follow/{userIdToFollow}

    POST -> /{userId}/unfollow/{userIdToUnfollow}

    GET -> /{userId}/followers/count

    GET -> /{userId}/followers/list

    GET -> /{userId}/followed/list


Controlador posteos:


    POST -> /products/newpost
    
    GET -> /products/followed/{userId}/list

    POST -> /products/newpromopost

    GET -> /products/{userId}/countPromo/

    GET -> /products/{userId}/list/


A partir de esto se desarrollaron los servicios:

    UserService
    PostService
    PermissionService
    
Y Finalmente los repositorios:

    UserRepository
    PostRepository
    PermissionRepository
    


# Diagrama UML de clases principales

A continuacion se mostraran las principales entidades de este diseño

![alt text1](https://i.imgur.com/OUUb816.jpg)


Cabe destacar que como eleccion de diseño se establecio que todos son usuarios dentro del sistema, pero cada uno tiene un o unos roles
Los roles establecidos son: Comprador (Buyer) y Vendedor(Seller)
En el repositorio de usuarios se crearon 2 compradores, y un vendedor
Un vendedor por defecto puede ser comprador (se le asigna ese rol) 
Un comprador puede ser vendedor si publica algo
Esto llevo a establecer un servicio de permisos para establecer que solo se puede seguir a usuarios que contengan el perfil de vendedor


# Probar la API Rest

Se sugieren descargar un programa como Postman para probar los endpoints
[Esta coleccion] dispone de los diferentes url para probar el funcionamiento

[Esta coleccion]: https://www.getpostman.com/collections/3ca6aeda4597e5957409


----
Mi Github: [ema-flores] <br>
Mi Workplace: [Emanuel Flores]

[ema-flores]: https://github.com/ema-flores
[Emanuel Flores]: https://meli.workplace.com/profile.php?id=100067929857930































# Spring && Futuros aprendizajes

#### ¿Que te trae por aqui? 
Las nuevas actividades se llevaran a cabo en la rama asignada en este [repositorio]

[repositorio]: https://github.com/extanantone/meli_bootcamp_w8/tree/main

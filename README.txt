

> ng -v

------------------------------------

> ng new front-gmenu
> cd front-gmenu

npm install --save @angular/material @angular/cdk @angular/animations @angular/flex-layout


> cd front-gmenu
> ng serve --open –-port=4201 --host=0.0.0.0

----------------------------------------
CRIAR NOSSA PALETA DE CORES:
Ver no site a paleta criada:
http://mcg.mbitson.com/#!?myprimarycolor=%23006068&myaccentcolor=%233d85c6&mywarncolor=%23cc0000

1º) Criar um ficheiro my-styles.scss dentro da pasta: src/assets/css/
2º) Ficheiro angular.json (na raiz do projecto) adicionar esse caminho (src/assets/css/my-styles.scss) no atributo "styles".
3º) Apagar: "./node_modules/@angular/material/prebuilt-themes/indigo-pink.css"

----------------------------------------
ADICIONAR FONTES:
1º) Adicionar as fontes na pasta assets/fontes
2º) No ficheiro my-styles.css adicionar o caminho para as fontes, ex:
@font-face {
  font-family: AllerLt;
  src: local('Aller_Std_Lt.ttf'), url('../fontes/aller/Aller_Std_Lt.ttf');
}

ADICIONAR Material Icons
No index.html file:
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">

_____________________________________________________MODULOS:

ng generate module my-shared/modules/material-shared --module app.module
ng generate module my-shared/modules/web-shared --module app.module
ng generate module my-shared/modules/components-shared --module app.module
ng generate module my-core --module app.module


ng generate module modules/guest --route guest --module app.module
ng generate module modules/admin --route oa-admin --module app.module

ng generate module modules/admin/login --route login --module modules/admin/admin.module
ng generate module modules/admin/gestao --route gestao --module modules/admin/admin.module
ng generate module modules/admin/consulta --route consulta --module modules/admin/admin.module
ng generate module modules/admin/entidades --route entidades --module modules/admin/admin.module

ng generate module modules/guest/hotels/porto-grande --route portogrande --module modules/guest/guest.module
ng generate module modules/guest/hotels/praiamar --route praiamar --module modules/guest/guest.module
ng generate module modules/guest/hotels/belorizonte --route belorizonte --module modules/guest/guest.module
ng generate module modules/guest/hotels/salinas-sea --route salinassea --module modules/guest/guest.module


ng generate module modules/admin/entidades/hotel --route hotel --module modules/admin/entidades/entidades.module
ng generate module modules/admin/entidades/item --route item --module modules/admin/entidades/entidades.module
ng generate module modules/admin/entidades/restaurante --route restaurante --module modules/admin/entidades/entidades.module
ng generate module modules/admin/entidades/cardapio --route cardapio --module modules/admin/entidades/entidades.module
ng generate module modules/admin/entidades/titem --route titem --module modules/admin/entidades/entidades.module
ng generate module modules/admin/entidades/user --route user --module modules/admin/entidades/entidades.module
ng generate module modules/admin/entidades/role --route role --module modules/admin/entidades/entidades.module


_____________________________________________________END MODULOS

_____________________________________________________PARTILHADO

COMPONENTES:
ng g c my-shared/modules/components-shared/pagina-nao-encontrado
ng g c my-shared/modules/components-shared/inicio
ng g c my-shared/modules/components-shared/dialogo-confirmacao
ng g c my-shared/modules/components-shared/dialogo-alerta

SERVICES:
ng g service my-core/services/api-crud
ng g service my-core/services/http-interceptor
ng generate service my-core/services/login
ng generate service my-core/services/dialog
ng generate service my-core/services/oa-pdf
ng generate service my-core/services/oa-file-upload
ng generate service my-core/services/oa-exel
GUARDAS:
> ng g guard  my-core/guards/auth 

MODELS:
ng g class my-shared/models/login
ng g class my-shared/models/response-pageable

INTERFACES:

ng generate interface my-shared/interfaces-shared/my-pages

ng generate interface my-shared/interfaces-shared/i-log

ng generate interface my-shared/interfaces-shared/i-confirm-dialog-data
ng generate interface my-shared/interfaces-shared/i-alert-dialog-data

_____________________________________________________END PARTILHADO

_____________________________________________________COMPONENTES/SERVICES/MODELS/INTERFACES:

ADMIN:
> ng g component modules/admin/components/header/main_header
> ng g component modules/admin/components/footer/main_footer

GESTAO
> ng g component gestao/components/logout

HOTEL:-------------------------------------------------------------------------------
CRUD-HOTEL:
ng g component modules/admin/entidades/hotel/components/main_menu --module modules/admin/entidades/hotel/hotel.module
ng g component modules/admin/entidades/hotel/components/crud/listar --module modules/admin/entidades/hotel/hotel.module
ng g component modules/admin/entidades/hotel/components/crud/apagar --module modules/admin/entidades/hotel/hotel.module
ng g component modules/admin/entidades/hotel/components/crud/criaralterar --module modules/admin/entidades/hotel/hotel.module
ng g component modules/admin/entidades/hotel/components/crud/detalhe  --module modules/admin/entidades/hotel/hotel.module

MODEL-HOTEL:
ng g class modules/admin/entidades/hotel/models/m-hotel

SERVICE-HOTEL:
ng generate service modules/admin/entidades/hotel/services/hotel-crud

INTERFACE-HOTEL:

ng generate interface modules/admin/entidades/hotel/interfaces/i-response-pageable-hotel
ng generate interface modules/admin/entidades/hotel/interfaces/i-hotel
ng generate interface modules/admin/entidades/hotel/interfaces/i-links-hotel
ng generate interface modules/admin/entidades/hotel/interfaces/i-req-hotel


RESTAURANTE:-------------------------------------------------------------------------------
CRUD-RESTAURANTE:
ng g component modules/admin/entidades/restaurante/components/main_menu --module modules/admin/entidades/restaurante/restaurante.module
ng g component modules/admin/entidades/restaurante/components/crud/listar --module modules/admin/entidades/restaurante/restaurante.module
ng g component modules/admin/entidades/restaurante/components/crud/apagar --module modules/admin/entidades/restaurante/restaurante.module
ng g component modules/admin/entidades/restaurante/components/crud/criaralterar --module modules/admin/entidades/restaurante/restaurante.module
ng g component modules/admin/entidades/restaurante/components/crud/detalhe  --module modules/admin/entidades/restaurante/restaurante.module

MODEL-RESTAURANTE:
ng g class modules/admin/entidades/restaurante/models/m-restaurante

SERVICE-RESTAURANTE:
ng generate service modules/admin/entidades/restaurante/services/restaurante-crud

INTERFACE-RESTAURANTE:
ng generate interface modules/admin/entidades/restaurante/interfaces/i-response-pageable-restaurante
ng generate interface modules/admin/entidades/restaurante/interfaces/i-restaurante
ng generate interface modules/admin/entidades/restaurante/interfaces/i-links-restaurante
ng generate interface modules/admin/entidades/restaurante/interfaces/i-req-restaurante

PIPE-RESTAURANTE:
ng generate pipe modules/admin/entidades/restaurante/pipes/get-hotel-by-url

CARDAPIO:-------------------------------------------------------------------------------
CRUD-CARDAPIO:
ng g component modules/admin/entidades/cardapio/components/main_menu --module modules/admin/entidades/cardapio/cardapio.module
ng g component modules/admin/entidades/cardapio/components/crud/listar --module modules/admin/entidades/cardapio/cardapio.module
ng g component modules/admin/entidades/cardapio/components/crud/apagar --module modules/admin/entidades/cardapio/cardapio.module
ng g component modules/admin/entidades/cardapio/components/crud/criaralterar --module modules/admin/entidades/cardapio/cardapio.module
ng g component modules/admin/entidades/cardapio/components/crud/detalhe  --module modules/admin/entidades/cardapio/cardapio.module

MODEL-CARDAPIO:
ng g class modules/admin/entidades/cardapio/models/m-cardapio

SERVICE-CARDAPIO:
ng generate service modules/admin/entidades/cardapio/services/cardapio-crud

INTERFACE-CARDAPIO:
ng generate interface modules/admin/entidades/cardapio/interfaces/i-response-pageable-cardapio
ng generate interface modules/admin/entidades/cardapio/interfaces/i-cardapio
ng generate interface modules/admin/entidades/cardapio/interfaces/i-links-cardapio
ng generate interface modules/admin/entidades/cardapio/interfaces/i-req-cardapio

PIPE-CARDAPIO:
ng generate pipe modules/admin/entidades/cardapio/pipes/get-hotel-by-url
ng generate pipe modules/admin/entidades/cardapio/pipes/get-restaurante-by-url


ITEM:-------------------------------------------------------------------------------
CRUD-ITEM:
ng g component modules/admin/entidades/item/components/main_menu --module modules/admin/entidades/item/item.module
ng g component modules/admin/entidades/item/components/crud/listar --module modules/admin/entidades/item/item.module
ng g component modules/admin/entidades/item/components/crud/apagar --module modules/admin/entidades/item/item.module
ng g component modules/admin/entidades/item/components/crud/criaralterar --module modules/admin/entidades/item/item.module
ng g component modules/admin/entidades/item/components/crud/detalhe  --module modules/admin/entidades/item/item.module

MODEL-ITEM:
ng g class modules/admin/entidades/item/models/m-item

SERVICE-ITEM:
ng generate service modules/admin/entidades/item/services/item-crud

GUARDAS-ITEM:

ng generate guard modules/admin/entidades/item/guards/item
ng generate guard modules/admin/entidades/item/guards/item-desactivate

INTERFACE-ITEM:
ng generate interface modules/admin/entidades/item/interfaces/i-response-pageable-item
ng generate interface modules/admin/entidades/item/interfaces/i-item
ng generate interface modules/admin/entidades/item/interfaces/i-links-item
ng generate interface modules/admin/entidades/item/interfaces/i-req-item

TIPO ITEM:-------------------------------------------------------------------------------
CRUD-TITEM:
ng g component modules/admin/entidades/titem/components/main_menu --module modules/admin/entidades/titem/titem.module
ng g component modules/admin/entidades/titem/components/crud/listar --module modules/admin/entidades/titem/titem.module
ng g component modules/admin/entidades/titem/components/crud/apagar --module modules/admin/entidades/titem/titem.module
ng g component modules/admin/entidades/titem/components/crud/criaralterar --module modules/admin/entidades/titem/titem.module
ng g component modules/admin/entidades/titem/components/crud/detalhe  --module modules/admin/entidades/titem/titem.module

MODEL-TITEM:
ng g class modules/admin/entidades/titem/models/m-titem

SERVICE-TITEM:
ng generate service modules/admin/entidades/titem/services/titem-crud

INTERFACE-TITEM:
ng generate interface modules/admin/entidades/titem/interfaces/i-response-pageable-titem
ng generate interface modules/admin/entidades/titem/interfaces/i-titem
ng generate interface modules/admin/entidades/titem/interfaces/i-links-titem
ng generate interface modules/admin/entidades/titem/interfaces/i-req-titem

USER:-------------------------------------------------------------------------------
CRUD-USER:
ng g component modules/admin/entidades/user/components/main_menu --module modules/admin/entidades/user/user.module
ng g component modules/admin/entidades/user/components/crud/listar  --module modules/admin/entidades/user.module
ng g component modules/admin/entidades/user/components/crud/apagar  --module modules/admin/entidades/user.module
ng g component modules/admin/entidades/user/components/crud/criaralterar --module modules/admin/entidades/user/user.module
ng g component modules/admin/entidades/user/components/crud/detalhe --module modules/admin/entidades/user.module

MODEL-USER:
ng g class modules/admin/entidades/user/models/m-user

SERVICE-USER:
ng generate service modules/admin/entidades/user/services/user-crud

INTERFACE-USER:
ng generate interface modules/admin/entidades/user/interfaces/i-response-pageable-user
ng generate interface modules/admin/entidades/user/interfaces/i-user
ng generate interface modules/admin/entidades/user/interfaces/i-req-user






GUEST:---------------------------------------------------------------------------
> ng g component guest/components/header
> ng g component guest/components/footer


_____________________________________________________END COMPONENTES/SERVICES/MODELS/INTERFACES:


PORTOGRANDE
ng g component modules/guest/hotels/porto-grande/lobby --module modules/guest/hotels/porto-grande/porto-grande.module
ng g component modules/guest/hotels/porto-grande/kalimba --module modules/guest/hotels/porto-grande/porto-grande.module
ng g component modules/guest/hotels/porto-grande/restaurante --module modules/guest/hotels/porto-grande/porto-grande.module










CONJUNTO
> ng g component conjunto/components/main_menu
> ng g component conjunto/components/crud/listar
> ng g component conjunto/components/crud/apagar
> ng g component conjunto/components/crud/criaralterar
> ng g component conjunto/components/crud/detalhe
> ng g component conjunto/components/resume

ng g class conjunto/models/conjunto

ng generate service conjunto/services/conjunto-crud

TIPO CONJUNTO
ng g component tipo-conjunto/components/main_menu
ng g component tipo-conjunto/components/crud/listar
ng g component tipo-conjunto/components/crud/apagar
ng g component tipo-conjunto/components/crud/criaralterar
ng g component tipo-conjunto/components/crud/detalhe
ng g component tipo-conjunto/components/resume

ng g component tipo-conjunto/components/listarfilhos


ng g class tipo-conjunto/models/tipo-conjunto

ng generate service tipo-conjunto/services/tipo-conjunto-crud

LOGIN 


APP:



























PARTILHADO:
> ng generate service partilhado/services/dropdown
> ng g i partilhado/models/ilhaCV


LOGIN:




FUNCIONARIO:
> ng g component funcionario/components/main_menu
> ng g component funcionario/components/crud/listar
> ng g component funcionario/components/crud/apagar
> ng g component funcionario/components/crud/criaralterar
> ng g component funcionario/components/resume

ESTABELECIMENTO
> ng g component estabelecimento/components/main_menu
> ng g component estabelecimento/components/crud/listar
> ng g component estabelecimento/components/crud/apagar
> ng g component estabelecimento/components/crud/criaralterar
> ng g component estabelecimento/components/crud/detalhe
> ng g component estabelecimento/components/resume

> ng g class estabelecimento/models/estabelecimento
> ng g class estabelecimento/models/email
> ng g class estabelecimento/models/telefone
> ng g class estabelecimento/models/contacto

> ng generate service estabelecimento/services/estabelecimento-crud

UNIDADE ATOMICA
> ng g component unidade-atomica/components/main_menu
> ng g component unidade-atomica/components/crud/listar
> ng g component unidade-atomica/components/crud/apagar
> ng g component unidade-atomica/components/crud/criaralterar
> ng g component unidade-atomica/components/crud/detalhe
> ng g component unidade-atomica/components/resume

> ng g class unidade-atomica/models/unidade-atomica

> ng generate service unidade-atomica/services/unidade-atomica-crud

UNIDADE MULTIPLAS
> ng g component unidade-multipla/components/main_menu
> ng g component unidade-multipla/components/crud/listar
> ng g component unidade-multipla/components/crud/apagar
> ng g component unidade-multipla/components/crud/criaralterar
> ng g component unidade-multipla/components/crud/detalhe
> ng g component unidade-multipla/components/resume

> ng g class unidade-multipla/models/unidade-multipla

> ng generate service unidade-multipla/services/unidade-multipla-crud

IVA
> ng g class iva/models/iva
> ng generate service iva/services/iva-crud

CATEGORIA-PRODUTO
> ng g class categoria-produto/models/categoria-produto
> ng generate service categoria-produto/services/categoria-produto-crud

MESA
> ng g class mesa/models/mesa
> ng generate service mesa/services/mesa-crud

PRODUTO
> ng g component produto/components/main_menu
> ng g component produto/components/crud/listar
> ng g component produto/components/crud/apagar
> ng g component produto/components/crud/criaralterar
> ng g component produto/components/crud/detalhe
> ng g component produto/components/resume

> ng g class produto/models/produto
> ng generate service produto/services/produto-crud

> ng g component header/login
> ng g component admin/components/footer/main_footer
> ng g component topimg/main_topimg
> ng g component submenu/main_submenu
> ng g component admin
> ng g component menupesquisa


END COMPONENTES

SERVICES:

> ng g service services/api-crud
> ng g service services/auth

> ng g service gesta-cartaz/services/estabelecimento-crud

END SERVICES

GUARDAS:

> ng g guard guards/auth 

> ng generate guard estabelecimento/guards/estabelecimento
> ng generate guard estabelecimento/guards/estabelecimento-desactivate
> ng generate service estabelecimento/guards/estabelecimento-detalhe-resolver (depois tirar "service" no nome do ficheiro)


> ng generate guard admin/guards/admin

END GUARDAS


INTERFACE

> ng g interface interface/IFormCanDesactivate

END INTERFACE


Cartaz
> ng g component gesta-cartaz/cartaz_home
> ng g component gesta-cartaz/cartaz_header
> ng g component gesta-cartaz/hoje/cartaz_hoje
> ng g component gesta-cartaz/semana/cartaz_semana
> ng g component gesta-cartaz/embreve/cartaz_embreve
> ng g component gesta-cartaz/arquivo/cartaz_arquivo
> ng g component gesta-cartaz/cartaz_desporto
> ng g component gesta-cartaz/cartaz_musica
> ng g component gesta-cartaz/teste/http_observable
> ng g component gesta-cartaz/cartaz-crud/cartaz_read
> ng g component gesta-cartaz/cartaz-crud/cartaz_creater
> ng g component gesta-cartaz/cartaz-crud/cartaz_delete
> ng g component gesta-cartaz/cartaz-crud/cartaz_detalhe
> ng g component gesta-cartaz/cartaz-crud/cartaznaoencontrado

Publicidade
> ng g component gestao-publicidades/horizontal/pub_h01
> ng g component gestao-publicidades/horizontal/pub_h02
> ng g component gestao-publicidades/horizontal/pub_h03

> ng g component gestao-publicidades/virtical/pub_v01
> ng g component gestao-publicidades/virtical/pub_v02
> ng g component gestao-publicidades/virtical/pub_v03

TV:
> ng g component gesta-tv/tv_home
> ng g component gesta-tv/show/tv_show
> ng g component gesta-tv/noticia/tv_noticia
> ng g component gesta-tv/live/tv_live
> ng g component gesta-tv/entrevista/tv_entrevista
> ng g component gesta-tv/arquivo/tv_arquivo

END COMPONENTES

SERVICES:

> ng g service services/api
> ng g service services/auth

> ng g service gesta-cartaz/services/estabelecimento-crud


Guarda de rotas

> ng g guard guards/auth 

> ng generate guard estabelecimento/guards/estabelecimento

> ng g service guards/cartaz-guard  //renomear, tirar palavra "Service"
> ng g service guards/cartaz-deactivate  //renomear, tirar palavra "Service"

> ng g guard guards/cartaz-detalhe.resolver


END SERVICES:

MODELS

> ng g cl gesta-cartaz/models/cartaz
> ng g cl gestao-users/models/user

END MODELS

INTERFACE

> ng g interface interface/IFormCanDesactivate

END INTERFACE
----
Adding ngx-translate in Angular 9 App
> npm i @ngx-translate/core --save
> npm i @ngx-translate/http-loader --save

The @ngx-translate/core package includes the essential services, pipe, and directives, to convert the content in various languages.

The @ngx-translate/http-loader service helps in fetching the translation files from a webserver.
----

Criar o serviço de gerenciamento de experience:
 > ng g service experience/shared/experience

Criar componente para listar experience
> ng g component experience/listar-experience

Criar directivas
> ng g d experience/fundo-amarelo

Criar Router guard
> ng generate guard auth

Criar classe
> ng g cl model/Employee
Create src > model > employee.ts file.




------------------------------------
Para utilizar modulos devemos => import { NgModule } from '@angular/core';
ngModel pertence a FormsModule (import { FormsModule } from '@angular/forms';)
ElementRef e Renderer(recomendado) , permitem aceder e modificar ao elemento do DOM


https://youtu.be/rtfj6UPhbcE
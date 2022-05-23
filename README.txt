

> ng -v

------------------------------------

> ng new front-gmenu
ng add @angular/material

> cd front-gmenu
> ng serve --open –-port=4201 --host=0.0.0.0


(VER FICHEIRO INDEX:HTML, TEM AS ENTRADAS DE JQUERY; BOOTSTRAP E POPPER)

_____________________________________________________MODULOS:



ng generate module conjunto --route conjunto --module app.module

ng generate module tipo-conjunto --route tipo-conjunto --module app.module

ng generate module item --route item --module app.module

ng generate module tipo-item --route tipo-item --module app.module


ng generate module guest --route guest --module app.module

ng generate module admin --route admin --module app.module

ng generate module login --route login --module admin/admin.module

ng generate module gestao --route gestao --module admin/admin.module

ng generate module consulta --route consulta --module app.module

ng generate module my-shared/modules/material-shared --module app.module
ng generate module my-shared/modules/web-shared --module app.module
ng generate module my-core --module app.module




_____________________________________________________END MODULOS

_____________________________________________________COMPONENTES:
Criar componentes:

ADMIN:
> ng g component admin/components/header/main_header
> ng g component admin/components/footer/main_footer

GESTAO
> ng g component gestao/components/logout


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
> ng g c components/pagina-nao-encontrado
> ng g c components/inicio

SERVICES:

> ng g service my-core/services/api-crud
> ng g service my-core/services/http-interceptor

ng generate service my-core/services/login
ng g class my-core/models/login























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
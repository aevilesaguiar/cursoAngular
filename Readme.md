Faz toda parte do bootstrap : <app-root></app-root>
O que é o Angular CLI? interface de linha de comando para angular. O angular CLI é uma ferramenta open source.
Uma Aplicação Angular é baseada em componentes, podemos encapsular comportamentos e regras de interface, tornando a criação de aplicações algo mais simples. Inclusive um componente pode encapsular outro componente.
lifecycle Hook->eventos de ciclo de vida,  que ocorrem quando um componente é criado, renderizado, tem o valor de suas propriedades alteradas ou é destruído. o Angular invoca uma séries de métodos (hooks), que são executados no momento em que esses eventos são acionados.
Os métodos do lifecycle hooks possuem uma nomeclatura própria que utiliza o nome da interface junto do prefixo ng
HOOK METHOD	PURPOSE (propósito)	TIMING
ngOnInit()	Inicialize a diretiva ou o componente após o Angular exibir primeiro as propriedades vinculadas a dados e definir as propriedades de entrada da diretiva ou do componente. Utilizado principalmente para inicializar dados de um componente.	Chamado uma vez, após o primeiro ngOnChanges(). ngOnInit()ainda é chamado mesmo quando ngOnChanges()não é (que é o caso quando não há entradas vinculadas ao modelo).
ngOnChanges()	Responda quando o Angular define ou redefine as propriedades de entrada vinculadas a dados. O método recebe um Simple Changes objeto de valores de propriedade atuais e anteriores. Este evento é executado sempre que um valor de um controle de entrada dentro do componente é alterado.
Sempre que um componente recebe  um dado do @input(recebe dados externos) o ngOnchanges() é invocado.	Chamado antes ngOnInit()(se o componente tiver entradas vinculadas) e sempre que uma ou mais propriedades de entrada vinculadas a dados forem alteradas.
ngDoCheck()


algumas funções:
     ngAfterContentInit()



     ngAfterContentCheched()



     ngAfterViewInit()


     ngAfterViewChecked()

	Este evento é disparado sempre que as propriedades de entrada de um componente são verificadas.


Este método de ciclo de vida é executado quando o Angular realiza qualquer projeção de conteúdo nas visualizações do componente

Este método de gancho de ciclo de vida é executado sempre que o conteúdo do componente é verificado pelo mecanismo de detecção de alteração do Angular.

Este método de gancho de ciclo de vida é executado quando a visualização do componente foi totalmente inicializada

Ele é executado toda vez que a visualização de um determinado componente foi verificado pelo algoritmo de detecção de alterações do Angular	Chamado imediatamente após ngOnChanges()cada execução de detecção de alterações e imediatamente após ngOnInit()na primeira execução.
ngOnDestroy()	Limpeza logo antes de Angular destruir a diretiva ou componente. Cancele a assinatura de Observables e desvincule manipuladores de eventos para evitar vazamentos de memória.	Chamado imediatamente antes de Angular destruir a diretiva ou componente.

Data Binding:é uma forma de exibir dados em seu componente html, nada mais que trabalhar com dados.
Interpolation { }	A interpolação de texto permite que seja incorporado valores dinâmicos em seus modelos html	Html:<h1>{{title}}</h1>

Ts:public title:string=”olá, Gafanhoto”

Property Binding[ ]	Ajuda a definir valores de elementos ou diretivas html -> [  ] colchetes.	html:<button[disabled]=”disableButton”>Button</button>

<img [src]=”itemImagemUrl”>
<img src={{itemImageUrl}}> (com interpolation)
Event Binding	É a associação de eventos que permite você escutar e responder as ações do usuário, como pressionamentos de tecla, movimentos do mouse, cliques e toques.	
<button (click)=”calc()”>Button</button>
Two-way binding	É a união do property-binding com event-binding.

Usado para  ouvir eventos e atualizar valores simultaneamente entre componentes pai e filho.	Html:<input [(ngModel)]=”nome”>
<span>{{nome}}</span>

Ts: public nome=”Dener”













O Angular CLI é uma ferramenta open source desenvolvida pelo próprio time do Angular e é utilizado para facilitar a criação de componentes, classes, services e outros.
Comando para instalar	npm install -g @angular/cli
Comando para criar um projeto	ng new NOME-DO-PROJETO
Comando para testar o app localmente	ng serve ou ng s
Comando para criar componentes	ng g component <nome>  ou ng g c <nome>
Comando para criar uma classe	ng g class NOME-DA-MINHA-CLASSE
Comando para criar um service	ng g service NOME-DO-MEU-SERVIÇO
	
	
	
	
	
	
Comando para gerar a aplicação para produção/desenvolvimento
Build em produção	ng build --prod
Build em desenvolvimento	ng build --dev
	
	
	
	
	

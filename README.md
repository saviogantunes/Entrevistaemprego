# Entrevistaemprego
O codigo tem como objetivo selecionar candidatos para diferentes areas, porém com abilidades gerais. Nesse sentido, perguntas diversas deverão ser respondidas a fim avaliar seu potencial e entao o resultado sera mostrado.

#include <stdio.h>
#include <locale.h>
#include <math.h>
void chamaMenu();
void chamaCadastro();
void chamaPerguntas();


int  main () {
    chamaMenu ();
    system("pause");
    return 0;
    }
    void chamaMenu () {
int escolha;
setlocale(LC_ALL, "Portuguese");
do{
    printf("********************************************************************************************************************************************************************************************************************************\n\n");
    printf("                                                                                                INSTITUTO  BPGS \n\n ");
    printf("*********************************************************************************************************************************************************************************************************************************\n\n");
    printf("1- Cadastrar Candidato\n\n ");
    printf("2- Consultar resultados\n\n");
    printf("3- Sair\n\n");
    printf("Digite o numero da opção desejada:  ");
    scanf("%d", &escolha);
    switch( escolha) {
        case 1:   chamaCadastro();
        break;
        case 2:  /*chamaConsulta*/;
        break;
        case 3: printf("FIM DO PROGRAMA");
        break;
        }
    system ("cls");

}while(escolha!=3);
printf("                              \n\n                       OBRIGADO PELA SUA ATENÇÃO                              \n\n");
    }

void chamaPerguntas () {
    int alternativa;
    float notaFinal=0;
    printf("************************************************QUESTIONÁRIO********************************************************\n\n");
    printf("\n***********************POR FAVOR, RESPONDA SOMENTE COM O NÚMERO DA ALTERNATIVA ESCOLHIDA***************************\n\n\n");
    printf("**************OBSERVAÇAO: SERÃO APROVADOS AQUELES QUE OBTIVEREM NOTAS SUPERIORES A 6");
    printf("A-O processo de comunicação é o método pelo qual um emissor alcança um receptor.");
    printf("\nConsiste em seis etapas. A etapa 1 é desenvolver a ideia ou pensamento;");
    printf("\na 2 é codificar a ideia em palavras adequadas; a 3 é a transmissão;");
    printf("\na 4 é permitir que a outra pessoa receba a mensagem; a 5 é a decodificação ");
    printf ("\nda mensagem pelo receptor e a etapa 6 refere-se ao: \n\n");
    printf("1. Uso da mensagem pelo receptor.\n");
    printf("2. Emoção emitida pelo receptor.\n");
    printf("3. Pensamento emitido pelo emissor..\n");
    printf("4. Código utilizado pelo receptor.\n");
    printf("5. Código utilizado pelo emissor.\n\n");
    printf("\n digite sua resposta/alternativa escolhida:  ");
    scanf("%d", &alternativa);
    if (alternativa ==1) {
        notaFinal = notaFinal + 1.67;
    }
    system ("cls");
    printf("B-Um Técnico Judiciário precisa mudar o nome e a senha da rede wireless");
    printf("\ndo escritório onde trabalha, que ela está sendo utilizada por pessoas não ");
    printf("\nautorizadas. Para isso, ele deve entrar na área de configuração do modem que ");
    printf("\nrecebe a internet e que também é roteador. Para acessar essa área, no computador ");
    printf(" \nligado ao modem-roteador, deve abrir o navegador web e, na linha de endereço, ");
    printf("\ndigitar o: \n\n");
    printf("1. Comando http://ipconfig.");
    printf("\n2. Endereço de memória do roteador.");
    printf("\n3. Comando http://setup.");
    printf("\n4. Comando http://settings.");
    printf("\n5. IP de acesso ao roteador\n\n");
    printf("digite sua resposta/alternativa escolhida:  ");
    scanf ("%d", &alternativa);
    if (alternativa == 5) {
        notaFinal = notaFinal + 1.67;
    }
    system ("cls");
    printf("C-Uma empresa que esteja considerando a concessão sucessiva de descontos");
    printf("\ncomo forma de alavancar suas vendas deverá levar em conta que esse tipo ");
    printf("\nde estratégia: \n\n");
    printf("1. Significará forte diferencial competitivo em relação à concorrência.\n");
    printf("2. Aumentará necessariamente os lucros da organização.\n");
    printf("3. Servirá como instrumento eficiente de relações públicas.\n");
    printf("4. Terá influência nula sobre o resultado das vendas quando não houver a concessão de descontos.\n");
    printf("5. Poderá comprometer a percepção de valor da marca no longo prazo.\n\n");
    printf("digite sua resposta/alternativa escolhida: ");
    scanf("%d", &alternativa);
     if (alternativa == 5 ) {
        notaFinal = notaFinal + 1.67;
    }
    system ("cls");
    printf("D- Os consumidores reagem de diferentes formas quando procuram um produto numa");
    printf("\nloja ou supermercado e não o encontram. A situação na qual o consumidor NÃO ");
    printf("\nsofre impacto em sua decisão de compra, em virtude da falta do produto, ");
    printf("\né denominada:\n\n");
    printf("1. Neutra;");
    printf("\n2. Situacional;");
    printf("\n3. De consumidor específico;");
    printf("\n4. Indiferente;");
    printf("\n5. De oportunidade.\n\n");
    printf("Digite sua resposta/alternativa escolhida");
     scanf ("%d", &alternativa);
   if (alternativa == 2) {
        notaFinal = notaFinal + 1.67;
    }
    system ("cls");
    printf("E- Acerca dos tipos de memória de computador, assinale");
    printf("\na alternativa que apresenta um tipo de memória primária: ");
    printf("\n\n1. CACHE.\n");
    printf("2. Disco Rígido.\n");
    printf("3. Pendrive.\n");
    printf("4. DVD.\n");
    printf("5. HD-Externo.\n\n");
    printf("digite sua resposta/alternativa escolhida");
     scanf("%d", &alternativa);
    if (alternativa == 1) {
        notaFinal = notaFinal + 1.67;
    }
    system ("cls");
    printf("F- Publicidade e Marketing é o levantamento de informações contendo as diversas");
    printf("\ninstruções que o cliente fornece à agência para orientar seu trabalho de planejamento. ");
    printf("\nAssinale a alternativa à qual o conceito apresentado acima refere-se:\n\n ");
    printf("\n1. Rough.");
    printf("\n2. Briefing");
    printf("\n3. Follow-up");
    printf("\n4. Missão");
    printf("\n5. Feedback\n\n");
    printf("digite sua resposta/alternativa escolhida");
     scanf("%d", &alternativa);
    if (alternativa == 2) {
        notaFinal = notaFinal + 1.67;
    }
if(notaFinal>=6){
printf("SUA NOTA FOI %.1f \n\n PARABENS VOCE PASSOU NO TESTE\n\n", notaFinal);
system("pause\n");
}
else{
printf("SUA NOTA FOI %.1f",notaFinal);
printf("\nREPROVADO.\n FIM DO PROGRAMA.");
system ("pause");
}

}

void chamaCadastro() {
    char sexo , nome[20], email[30];
    int nasc , telefone , continua, novamente, area, sair;
    do {

        fflush(stdin);
        printf ("\nNome Completo: \n");
        scanf("%s", &nome[20] );
        fflush(stdin);
        printf("\nData de nascimento(DDMMAAAA): \n");
        scanf("%d", &nasc);
        printf("\nDigite seu sexo (F ou M): \n" );
        scanf ("%c", &sexo);
            while ((sexo != 'F') && (sexo != 'M')) {
                printf ("\nSexo deve ser F ou M: ");
                scanf ("%c", &sexo);
          }
        printf ("\nTelefone(DDD+NUM): \n");
        scanf("%d", &telefone);
        printf ("\nDigite seu email: ");
        scanf("%s", &email);
        printf ("\n\nDigite---->\n0 -PRÓXIMA ETAPA \n1 - REVER INFORMAÇÕES  \n---->");
        scanf ("%d", &continua);
        if (continua == 0) {
        novamente = 1;
        printf("\n\nFIM DA PRIMEIRA ETAPA\n");
        system ("pause");
        }else {
            novamente = 0;
        }
    } while (novamente == 0);
    system ("cls");
    printf("--------------ÁREA DE ATUAÇÃO--------------\n\n");
    printf(" 1- Marketing\n\n");
    printf(" 2- Tecnologia da Informação \n\n");
    printf(" 3- Admnistração \n\n");
    printf("\nDigite o número da opção desejada ----> ");
    scanf("%d", &area);
    system ("cls");
    switch (area){
        case 1:
              chamaPerguntas ();
            break;
        case 2:
              chamaPerguntas ();
            break;
        case 3:
             chamaPerguntas ();
            break;
    }
    system ("cls");

}



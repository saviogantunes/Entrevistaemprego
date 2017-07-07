# Entrevistaemprego
O codigo tem como objetivo selecionar candidatos para diferentes areas, porém com abilidades gerais. Nesse sentido, perguntas diversas deverão ser respondidas a fim avaliar seu potencial e entao o resultado sera mostrado.

#include<stdio.h>
#include<locale.h>
void ChamaMenu();
void ChamaPerguntas();
void ChamaCadastro();
void ChamaPontilhado();
void ChamaQuestionario();
float notaCandidatos[3];
char sexo , nome[20], email[30];
int nasc[3] , telefone[3], continua, novamente,codigo[3], sair, area, i=0,codigo[3],areas[3];
int main () {
    ChamaMenu();
    system("pause");
    return 0;
}
void ChamaMenu() {
    int escolha;
    setlocale(LC_ALL, "Portuguese");
    do{
        system("cls");
        ChamaPontilhado();
        printf("                                                                      RH INSTITUTO BPGS \n\n");
        ChamaPontilhado();
        printf(" 1- Cadastrar Candidato \n\n");
        printf(" 2- Consultar Relatório \n\n");
        printf(" 3- Sair \n\n");
        printf("Digite o número da opção desejada ----> ");
        scanf("%d", &escolha);
        switch (escolha){
            case 1:
                system("cls");
                ChamaCadastro();
                break;
            case 2:
                // consulta da pontuação final
                break;
        }
    }while (escolha != 3);
    system("cls");
    ObrigadoFinal();
}
void ChamaCadastro() {

    do {
        system("cls");
        fflush(stdin);
        printf ("Nome Completo: \n----> ");
        scanf("%s", &nome[20]);
        fflush(stdin);
        printf("\nData de nascimento(DDMMAAAA): \n----> ");
        scanf("%d", &nasc[i]);
        printf("\nSexo (F ou M): \n----> " );
        scanf("%s", &sexo);
        printf ("\nTelefone(DDD+NUM): \n----> ");
        scanf("%d", &telefone);
        printf ("\nEmail: \n----> ");
        scanf("%s", &email);
        system("cls");
        printf ("0 -PRÓXIMA ETAPA \n1 - ANULAR E CADASTRAR NOVAMENTE \n\n----> ");
        scanf ("%d", &continua);
        if (continua == 0) {
            novamente = 1;
            system("cls");
            ChamaPontilhado();
            printf("                                                                   FIM DA PRIMEIRA ETAPA\n\n");
            ChamaPontilhado();
            printf("\n\n");
            system ("pause");
        }else {
            novamente = 0;
        }
    } while(novamente == 0);
    system("cls");
    printf("------------------------------------------------------------------------ÁREA DE ATUAÇÃO");
    printf("---------------------------------------------------------------------------------\n\n");
    printf(" 1- Marketing\n\n");
    printf(" 2- Tecnologia da Informação \n\n");
    printf(" 3- Admnistração \n\n");
    printf("Digite o número da opção desejada ----> ");
    scanf("%d", &area);
    system ("cls");
    switch (area){
        case 1:
            ChamaPerguntas ();
            break;
        case 2:
            ChamaPerguntas ();
            break;
        case 3:
            ChamaPerguntas ();
            break;
    }
    system ("cls");
}
void ChamaPerguntas () {
    int alternativa;
    float notaFinal=0;
    ChamaQuestionario();
    printf("A-  O processo de comunicação é o método pelo qual um emissor alcança um receptor.");
    printf("\nConsiste em seis etapas. A etapa 1 é desenvolver a ideia ou pensamento;");
    printf("\na 2 é codificar a ideia em palavras adequadas; a 3 é a transmissão;");
    printf("\na 4 é permitir que a outra pessoa receba a mensagem; a 5 é a decodificação ");
    printf("\nda mensagem pelo receptor e a etapa 6 refere-se ao: \n\n");
    printf("1. Uso da mensagem pelo receptor.\n");
    printf("2. Emoção emitida pelo receptor.\n");
    printf("3. Pensamento emitido pelo emissor..\n");
    printf("4. Código utilizado pelo receptor.\n");
    printf("5. Código utilizado pelo emissor.\n\n");
    printf("RESPOSTA: ");
    scanf("%d", &alternativa);
    if ((alternativa == 1) && (area == 1)){
        notaFinal = notaFinal + 3;
    } else {
        if (alternativa == 1) {
        notaFinal = notaFinal + 1;
        }
    }
    system ("cls");
    ChamaQuestionario();
    printf("B-  Um Técnico Judiciário precisa mudar o nome e a senha da rede wireless");
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
    printf("RESPOSTA: ");
    scanf ("%d", &alternativa);
    if ((alternativa == 5) && (area == 2)){
        notaFinal = notaFinal + 3;
    } else {
        if (alternativa == 5) {
        notaFinal = notaFinal + 1;
        }
    }
    system ("cls");
    ChamaQuestionario();
    printf("C-  Uma empresa que esteja considerando a concessão sucessiva de descontos");
    printf("\ncomo forma de alavancar suas vendas deverá levar em conta que esse tipo ");
    printf("\nde estratégia: \n\n");
    printf("1. Significará forte diferencial competitivo em relação à concorrência.\n");
    printf("2. Aumentará necessariamente os lucros da organização.\n");
    printf("3. Servirá como instrumento eficiente de relações públicas.\n");
    printf("4. Terá influência nula sobre o resultado das vendas quando não houver a concessão de descontos.\n");
    printf("5. Poderá comprometer a percepção de valor da marca no longo prazo.\n\n");
    printf("RESPOSTA: ");
    scanf("%d", &alternativa);
    if ((alternativa == 5) && (area == 3)){
        notaFinal = notaFinal+ 3;
    } else {
        if (alternativa == 5) {
        notaFinal = notaFinal + 1;
        }
    }
    system ("cls");
    ChamaQuestionario();
    printf("D-  Os consumidores reagem de diferentes formas quando procuram um produto numa");
    printf("\nloja ou supermercado e não o encontram. A situação na qual o consumidor NÃO ");
    printf("\nsofre impacto em sua decisão de compra, em virtude da falta do produto, ");
    printf("\né denominada:\n\n");
    printf("1. Neutra;");
    printf("\n2. Situacional;");
    printf("\n3. De consumidor específico;");
    printf("\n4. Indiferente;");
    printf("\n5. De oportunidade.\n\n");
    printf("RESPOSTA: ");
    scanf ("%d", &alternativa);
    if ((alternativa == 2) && (area == 3)){
        notaFinal = notaFinal + 3;
    } else {
        if (alternativa == 2) {
        notaFinal = notaFinal + 1;
        }
    }
    system ("cls");
    ChamaQuestionario();
    printf("E-  Acerca dos tipos de memória de computador, assinale");
    printf("\na alternativa que apresenta um tipo de memória primária: ");
    printf("\n\n1. CACHE.\n");
    printf("2. Disco Rígido.\n");
    printf("3. Pendrive.\n");
    printf("4. DVD.\n");
    printf("5. HD-Externo.\n\n");
    printf("RESPOSTA: ");
    scanf("%d", &alternativa);
    if ((alternativa == 1) && (area == 2)){
        notaFinal = notaFinal + 3;
    } else {
        if (alternativa == 1) {
        notaFinal = notaFinal+ 1;
        }
    }
    system ("cls");
    ChamaQuestionario();
    printf("F-  Publicidade e Marketing é o levantamento de informações contendo as diversas");
    printf("\ninstruções que o cliente fornece à agência para orientar seu trabalho de planejamento. ");
    printf("\nAssinale a alternativa à qual o conceito apresentado acima refere-se:\n\n ");
    printf("\n\n1. Rough.");
    printf("\n2. Briefing");
    printf("\n3. Follow-up");
    printf("\n4. Missão");
    printf("\n5. Feedback\n\n");
    printf("RESPOSTA: ");
    scanf("%d", &alternativa);
    if ((alternativa == 2) && (area == 1)){
        notaFinal = notaFinal + 3;
    } else {
        if (alternativa == 2) {
        notaFinal = notaFinal+ 1;
        }
    }
    if (notaFinal > 6) {
        system ("cls");
        ChamaPontilhado();
        printf ("                                  PARABÉNS, VOCÊ PASSOU NO TESTE E A BPGS ENTRARÁ EM CONTATO COM VOCÊ EM BREVE\n\n");
        ChamaPontilhado();
        printf("-----> NOTA EXIGIDA: 6\n-----> SUA NOTA: %.2f\n\n\n", notaFinal);
        codigo[i] = i+1001;
        notaCandidatos[i]=notaFinal;
        areas[i] = area;
        printf("\n\n------------------------------------------------------------SEU CÓDIGO DE CADASTRO: %d",codigo[i]);
        printf("--------------------------------------------------------------------------------\n\n\n\n\n");
    } else {
        system ("cls");
        ChamaPontilhado();
        printf ("                                          INFELIZMENTE VOCÊ NÃO FOI APROVADO, AGRADECEMOS PELO SEU TEMPO \n\n\n");
        ChamaPontilhado();
        printf("-----> NOTA EXIGIDA: 6\n-----> SUA NOTA: %.2f\n\n\n", notaFinal);
        codigo[i] = i+1001;
        notaCandidatos[i]=notaFinal;
        areas[i] = area;
        printf("\n\n------------------------------------------------------------SEU CÓDIGO DE CADASTRO: %d",codigo[i]);
        printf("--------------------------------------------------------------------------------\n\n\n\n\n");
    }
    i++;
    system("pause");
}
void ChamaPontilhado(){
   printf("*******************************************************************************************");
   printf("*****************************************************************************\n\n");
}
void ChamaQuestionario() {
    printf("**************************************************************************QUESTIONÁRIO****************************");
    printf("******************************************************\n\n");
    printf("\n**********************************************************RESPONDA SOMENTE COM O NÚMERO DA ALTERNATIVA ");
    printf("ESCOLHIDA********************************************************\n\n\n");
}
void ObrigadoFinal() {
    printf("*******************************************************************************************");
    printf("*******************************************************************************************");
    printf("*******************************************************************************************");
    printf("*******************************************************************************************");
    printf("*******************************************************************************************");
    printf("************************************************");
    printf("\n\n\n\n\n\n                                                                            OBRIGADO\n\n\n\n\n\n");
    printf("*******************************************************************************************");
    printf("*******************************************************************************************");
    printf("*******************************************************************************************");
    printf("*******************************************************************************************");
    printf("*******************************************************************************************");
    printf("*************************************************\n\n\n\n\n");
}


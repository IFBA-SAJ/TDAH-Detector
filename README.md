# TDAH-Detector

# Projeto da Disciplina Engenharia de Software I 

# Equipe do sistema TDAH Detector
Pedro Jorge pedjorcal :    Gerente de projetos /Analista de sistema

Alisson A.Divino alisso19n:  Engenheiro de Requisitos / Programador

João Herick Jottatest: Arquiteto de Sistema / Analista de Requisitos

# Descrição:
Este documento tem como objetivo apresentar a organização , práticas e métricas, objetivos e marcos para criação do projeto TDAH DETECTOR, aplicativo 
para detecção de sinais do transtorno de déficitc com hiperatividade.

# Justificativa:
cotidianamente , encontra-se no mercado diversas opções de aplicativos e testes que contribuem na detecção do TAE(Transtorno do Espectro Autista), porém pouco 
se fala sobre a detecção do TDAH ( Transtorno de Déficit com Hiperatividade).
Diante deste contexto , foi lançada a proposta de criação de um aplicativo composto por jogos e testes relacionais a atenção que será responsável por detectar 
possiveis sinais dos sintomas do TDAH, gerando um resultado com porcentagem de probabilidade de o usuário submetido ao teste , ter o déficit ou não.

Código Java 

import java.util.Scanner;

public class DetecaoTDAH {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Bem-vindo ao aplicativo de detecção de TDAH!");
        System.out.println("Responda às seguintes perguntas para avaliar a atenção da criança:");

        int pontuacao = 0;
        int totalPerguntas = 15; // Reduzido para metade

        // Perguntas e respostas
        String[] perguntas = {
                "1. A criança tem dificuldade em prestar atenção a detalhes ou comete erros por descuido em atividades escolares?",
                "2. A criança tem dificuldade em manter a atenção em tarefas ou atividades lúdicas?",
                "3. A criança frequentemente parece não prestar atenção quando alguém está falando diretamente com ela?",
                "4. A criança frequentemente evita ou é relutante em se envolver em tarefas que exijam esforço mental constante?",
                "5. A criança costuma perder objetos necessários para tarefas ou atividades?",
                "6. A criança facilmente se distrai por estímulos externos?",
                "7. A criança parece não ouvir quando falada diretamente?",
                "8. A criança tem dificuldade em seguir instruções até o final, sem interrupções?",
                "9. A criança tem dificuldade em organizar tarefas e atividades?",
                "10. A criança evita ou reluta em se envolver em tarefas que exigem esforço mental prolongado?",
                // Adicione mais perguntas aqui
                "11. A criança tem dificuldade em manter a atenção em atividades de lazer, como assistir a um filme ou jogar?",
                "12. A criança costuma se perder em pensamentos e ignorar o que está acontecendo ao seu redor?",
                "13. A criança tem dificuldade em se concentrar em tarefas por longos períodos de tempo?",
                "14. A criança costuma esquecer as coisas do dia a dia, como compromissos ou tarefas?",
                "15. A criança frequentemente deixa de prestar atenção a detalhes e comete erros em atividades escolares ou em outras atividades?"
        };

        String[] respostas = {
                "a", // Resposta correta para a pergunta 1
                "a", // Resposta correta para a pergunta 2
                "a", // Resposta correta para a pergunta 3
                "a", // Resposta correta para a pergunta 4
                "a", // Resposta correta para a pergunta 5
                "a", // Resposta correta para a pergunta 6
                "a", // Resposta correta para a pergunta 7
                "a", // Resposta correta para a pergunta 8
                "a", // Resposta correta para a pergunta 9
                "a", // Resposta correta para a pergunta 10
                // Adicione mais respostas aqui
                "a", // Resposta correta para a pergunta 11
                "a", // Resposta correta para a pergunta 12
                "a", // Resposta correta para a pergunta 13
                "a", // Resposta correta para a pergunta 14
                "a"  // Resposta correta para a pergunta 15
        };

        // Apresentar as perguntas e obter as respostas
        for (int i = 0; i < perguntas.length; i++) {
            System.out.println(perguntas[i]);
            System.out.println("a) Sim");
            System.out.println("b) Não");
            String resposta = scanner.nextLine();
            if (resposta.equalsIgnoreCase(respostas[i])) {
                pontuacao += 5; // Atribui 5 pontos para cada resposta correta
            }
        }

        // Calcular a porcentagem de acerto
        double porcentagem = (double) pontuacao / (totalPerguntas * 5) * 100;

        // Avaliação do resultado
        System.out.println("\nPontuação total: " + pontuacao);
        if (porcentagem >= 50) {
            System.out.println("Baseado nas respostas, é recomendado que a criança seja avaliada por um especialista para possíveis sintomas de TDAH.");
        } else {
            System.out.println("Baseado nas respostas, parece que a criança está indo bem, mas é importante consultar um especialista para uma avaliação mais precisa.");
        }System.out.println("\nLembre-se, a detecção precoce do TDAH é essencial para o desenvolvimento saudável da criança. Consulte um especialista para obter mais informações e orientações.");

        scanner.close();
    }
}



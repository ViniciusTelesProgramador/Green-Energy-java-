package App;

import java.time.DayOfWeek; //biblioteca para trabalhar com os dias da semana 
import java.time.LocalDate; //biblioteca fornece métodos para manipular datas, como obter a data atual
import java.time.LocalTime; // biblioteca fornece métodos para manipular horários, como obter o horário atual
import java.util.ArrayList; // biblioteca implementa uma lista dinâmica que pode armazenar objetos. Ela fornece métodos para adicionar, remover, pesquisar e manipular elementos na lista
import java.util.HashMap; // biblioteca implementa uma tabela de hash que mapeia chaves a valores.
import java.util.List; // 
import java.util.Map;
import java.util.Scanner;
import java.awt.Desktop; //  biblioteca fornece métodos para interagir com o ambiente de desktop do sistema operacional. Ela permite abrir arquivos, URLs 
import java.net.URI; // biblioteca fornece métodos para analisar, construir e manipular URIs.


public class Green {



    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        // Variáveis de controle de usuário      
        
        int regiao = 0;
        double bandeira = 0;
        int consumoAlto = 0;
        
       
        // Criação do objeto da classe Objetos
        Objetos objetos = new Objetos();

        // HashMap para armazenar os eletrodomésticos selecionados e seus consumos
        Map<String, Integer> eletrodomesticosSelecionados = new HashMap<>();
        
        List<Lembrete> lembretes = new ArrayList<>();

        
        boolean isUserRegistered = false;
        User user = null;

        // Loop do menu principal
        boolean sair = false;
        while (!sair) {
            System.out.println("---------------------------------------------------------");
            System.out.println("BEM-VINDO AO GREEN ENERGY");
            System.out.println("---------------------------------------------------------");
            System.out.println("[1] LOGIN");
            System.out.println("[2] CADASTRAR");
            System.out.println("[3] SAIR ");

            int opc = scan.nextInt();

            switch (opc) {
            case 1:
                    
            	// variável usada para indicar se um usuário está registrado ou não em algum sistema ou aplicativo.
            	if (isUserRegistered) {
                    System.out.println("Por favor, faça o login para continuar:");
                    System.out.print("Username: ");
                    String inputUsername = scan.next();
                    System.out.print("Password: ");
                    String inputPassword = scan.next();

                    if (user != null && inputUsername.equals(user.getNome()) && inputPassword.equals(user.getSenha())) {
                        System.out.println("Login bem-sucedido!");
                  
                            
                            //MENU 2
                            boolean menu2 = false;
                            boolean exibirConsumoTotal = false;
                            while (!menu2)
                            {
                            System.out.println("------------------------------------");	
                            System.out.println("----------------MENU----------------");
                            System.out.println("SELECIONE A OPÇÃO DESEJADA");
                            System.out.println("[1] ADICIONAR ELETRODOMESTICO");
                            System.out.println("[2] VERIFICAR CONSUMO ");
                            System.out.println("[3] ADICIONAR LEMBRETES");
                            System.out.println("[4] SUPORTE");
                            System.out.println("[5] SAIR");
                            System.out.println("------------------------------------");
                            int opc2 = scan.nextInt();
                            
                  
                            switch (opc2) {
                            case 1:                                
                            	//Essa estrutura de código permite que o usuário selecione um eletrodoméstico a partir das opções exibidas e continue dentro do loop enquanto o valor de eletroValido for falso. A lógica para validar a seleção do eletrodoméstico e atualizar o valor de eletroValido não está presente no trecho de código fornecido, mas pode ser adicionada posteriormente.
                            	if (regiao == 1) {
                            		Case1_Norte caso1 = new Case1_Norte(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso1.executar();
                                     break;
                            	}// IF REGIAO 1 
                                     
                            	if(regiao ==2) {
                            		Case2_Nordeste caso2 = new Case2_Nordeste(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso2.executar();
                                      break;
                            	}// IF REGIAO 2 
                            	
                            	if(regiao==3) {
                            		Case3_CentroOeste caso3 = new Case3_CentroOeste(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso3.executar();
                                      break;
                            	}// IF REGIAO 3 
                            	
                            	if(regiao==4) {
                            		Case4_Sudeste caso4 = new Case4_Sudeste(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso4.executar();
                                     break;
                            	}// IF REGIAO 4
                            	
                            	if(regiao==5) {
                            		Case5_Sul caso5 = new Case5_Sul(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso5.executar();
                                     break;

                            	}// IF REGIAO 5 
                       
                            case 2:
                                // Verifica o consumo total dos eletrodomésticos selecionados e printa a lista com os eletrodomésticos selecionados
                                double consumoTotal = 0;
                                System.out.println("Eletrodomésticos selecionados:");
                                for (Map.Entry<String, Integer> entry : eletrodomesticosSelecionados.entrySet()) {
                                    String eletrodomestico = entry.getKey();
                                    int consumo = entry.getValue();
                                    consumoTotal += consumo;
                                    System.out.println(eletrodomestico + ": " + consumo + " kWh");
                                }// LISTA A TABELA DE ELETRODOMESTICOS E SEUS RESPECTIVOS CONSUMOS 

                                if (consumoTotal > 0) {
                                    // Cálculo do valor total em reais 
                                    double valorTotalReais = consumoTotal * bandeira;
                                    System.out.println("Consumo total: " + consumoTotal + " kWh");
                                    System.out.println("Valor total em reais: " + valorTotalReais + " R$");

                                    if (consumoTotal > 685) {
                                        // Mensagem que será exibida caso o consumo em reais do usuário esteja maior que 685,00 reais
                                        System.out.println("--------------------------------------------------------------------------------------------------------");
                                        System.out.println("Descubra como o Green Energy pode ajudar você a economizar na conta de energia!");
                                        System.out.println("Seu consumo atual está acima da média brasileira! Nós temos a solução para reduzir seus gastos");
                                        System.out.println("e tornar sua casa mais sustentável. Venha conhecer nosso projeto inovador e descubra como calcular");
                                        System.out.println("o consumo de cada eletrodoméstico, economizando e contribuindo para um futuro mais verde!");
                                        System.out.println("[1] - SIM  /    [2] - NÃO ");
                                        consumoAlto = scan.nextInt();
                                        if (consumoAlto == 1) {
                                            try {
                                                URI link = new URI("https://www.mixo.io/site/green-energy-f77ys/index.html");
                                                Desktop.getDesktop().browse(link);
                                            } catch (Exception erro) {
                                                System.out.println(erro);
                                            }
                                       
                                        }// REDIRECIONAMENTI PARA CAPTAÇÃO DE EMAIL DO USUARIO 
                                    if (consumoAlto==2) {
                                    	System.out.println("MESMO ASSIM, DESDE JÁ AGRADECEMOS, SÓ DEPENDE DE VOCÊ.");
                                    }
                                    
                                    } // IF DO CONSUMO TOTAL MAIOR QUE 685
                                
                                }// IF DO CONSUMO TOTAL MAIOR QUE 0 
                               
                                else {
                                    System.out.println("Nenhum eletrodoméstico selecionado.");
                                }
                                break;


                            case 3:
                                System.out.println("Selecione o tipo de lembrete:");
                                System.out.println("[1] - LEMBRETE DIÁRIO");
                                System.out.println("[2] - LEMBRETE SEMANAL");
                                System.out.println("[3] - VERIFICAR LEMBRETES ");
                                int tipoLembrete = scan.nextInt();

                                switch (tipoLembrete) {
                                case 1:// ADICIONA UM LEMBRETE DIÁRIO 
                                    System.out.println("Digite o horário para o lembrete diário (formato HH:MM):");
                                    String horarioDiario = scan.next();
                                    System.out.println("Digite a mensagem do lembrete diário:");
                                    scan.nextLine(); // Consumir a quebra de linha pendente
                                    String mensagemDiario = scan.nextLine();
                                    Lembrete lembreteDiario = new Lembrete("Diário", horarioDiario, mensagemDiario);
                                    lembretes.add(lembreteDiario);
                                    System.out.println("Lembrete diário adicionado com sucesso!");
                                
                                    break;
								
								case 2:// ADICIONA UM LEMBRETE SEMANAL 
								    System.out.println("Digite o dia da semana para o lembrete semanal (1-7, onde 1 = domingo, 2 = segunda, etc.):");
								    int diaSemana = scan.nextInt();
								    System.out.println("Digite o horário para o lembrete semanal (formato HH:MM):");
								    String horarioSemanal = scan.next();
								    System.out.println("Digite a mensagem do lembrete semanal:");
								    scan.nextLine(); // Consumir a quebra de linha pendente
								    String mensagemSemanal = scan.nextLine();
								    Lembrete lembreteSemanal = new Lembrete("Semanal", horarioSemanal, diaSemana, mensagemSemanal);
								    lembretes.add(lembreteSemanal);
								    System.out.println("Lembrete semanal adicionado com sucesso!");
								    break;
								    
								case 3:
								    System.out.println("[1] VERIFICAR LEMBRETE DIÁRIO");
								    System.out.println("[2] VERIFICAR LEMBRETE SEMANAL");
								    int verificalembrete = scan.nextInt();

								    if (verificalembrete == 1) {
								        // Verificar lembretes diários
								        LocalTime currentTime = LocalTime.now();
								        for (Lembrete lembrete : lembretes) {
								            if (lembrete.getTipo().equals("Diário")) {
								                String lembreteHorario = lembrete.getHorario();
								                if (currentTime.getHour() == Integer.parseInt(lembreteHorario.substring(0, 2)) &&
								                        currentTime.getMinute() == Integer.parseInt(lembreteHorario.substring(3, 5))) {
								                    System.out.println("Lembrete diário: " + lembrete.getMensagem());
								                    // Realize a ação desejada para o lembrete diário
								                }
								            }
								        }  
								    
								    } // VERIFICA LEMBRETE DIÁRIO 
								    
								    else if (verificalembrete == 2) {
								        // Verificar lembretes semanais
								        LocalDate currentDate = LocalDate.now();
								        DayOfWeek currentDayOfWeek = currentDate.getDayOfWeek();

								        for (Lembrete lembrete : lembretes) {
								            if (lembrete.getTipo().equals("Semanal")) {
								                int diadaSemana = lembrete.getDiaSemana();

								                if (currentDayOfWeek.getValue() == diadaSemana) {
								                    String lembreteHorario = lembrete.getHorario();
								                    LocalTime currentTime = LocalTime.now();
								                    if (currentTime.getHour() == Integer.parseInt(lembreteHorario.substring(0, 2)) &&
								                            currentTime.getMinute() == Integer.parseInt(lembreteHorario.substring(3, 5))) {
								                        System.out.println("Lembrete semanal: " + lembrete.getMensagem());
								                        break; // Adicionando o break para sair do loop após exibir o lembrete
								                    }
								                }
								            }
								        }
								     
								    } // VERIFICA OS LEBRETES SEMANAL 
								    
                            	} //SWICH DO LEMBRETE 
                      
                            break; // Adicionando o break para sair do switch-case após executar o caso 3
                            
                            
                            case 4:
							    System.out.println("Ligue para o nosso suporte em: (98) 9 8228-1027");
							    break;
							
							
                            case 5:
                                System.out.println("OBRIGADO POR USAR O GREEN ENERGY, VOLTE SEMPRE!");
                                menu2 = true; // Atualização para sair do loop
                                sair = true; // Atualização para finalizar o programa
                                break;
                            default:
                                System.out.println("Opção inválida.");
                                break;
                        
                            }// SWITCH OPC DO MWNU 2 

                        if (sair) {
                            break; // Saída do loop principal
                        }
                            }
                    }/// LOGIN BEM SUCEDIDO, ENTRA NO SISTEMA 
                        
                        
                        else {
                            System.out.println("Usuário ou senha inválidos.");
                        }
                    
                    break;
                    } // if do login para continuar 
            	
                    

            case 2:
                // Cadastro do usuário
                System.out.println("Bem-vindo ao sistema de cadastro.");

                user = new User();
                System.out.print("Username: ");
                String username = scan.next();
                user.setNome(username);

                System.out.print("Password: ");
                String password = scan.next();
                user.setSenha(password);

                System.out.print("Digite o seu CPF: ");
                String cpf = scan.next();
                user.setCpf(cpf);

                System.out.print("Digite o seu Telefone: ");
                String telefone = scan.next();
                user.setTelefone(telefone);

                System.out.println("Usuário cadastrado com sucesso!");
                isUserRegistered = true;
               
                    System.out.println("QUAL REGIÃO VOCÊ MORA ?");
                    System.out.println("[1] NORTE");
                    System.out.println("[2] NORDESTE");
                    System.out.println("[3] CENTRO-OESTE");
                    System.out.println("[4] SUDESTE");
                    System.out.println("[5] SUL");
                    regiao = scan.nextInt();
                    if (regiao >5) {
                    	System.out.println("SELECIONE UMA REGIAO VÁLIDA");
                    	break;
                    }
                    
                    System.out.println("Usuário cadastrado com sucesso!");
                    break;

                case 3:
                    System.out.println("Obrigado por utilizar o Green Energy.");
                    sair = true;
                    break;

                default:
                    System.out.println("Opção inválida.");
                    break;
                    
                    
              	} // case do login do usuario 
            
            // Verificar lembretes diários
            LocalTime currentTime = LocalTime.now();
            for (Lembrete lembrete : lembretes) {
                if (lembrete.getTipo().equals("Diário")) {
                    String lembreteHorario = lembrete.getHorario();
                    if (currentTime.getHour() == Integer.parseInt(lembreteHorario.substring(0, 2)) &&
                            currentTime.getMinute() == Integer.parseInt(lembreteHorario.substring(3, 5))) {
                        System.out.println("Lembrete diário: Hora de realizar a tarefa!");
                        // Realize a ação desejada para o lembrete diário
                    }
                }
                
            }// lembretes
        
        }// menu 1 
    
    }//public static void main(String[] args)

	public void executar() {
		// TODO Auto-generated method stub
		
	}

}// public class Green
    


package App;

import java.time.DayOfWeek; //biblioteca para trabalhar com os dias da semana 
import java.time.LocalDate; //biblioteca fornece métodos para manipular datas, como obter a data atual
import java.time.LocalTime; // biblioteca fornece métodos para manipular horários, como obter o horário atual
import java.util.ArrayList; // biblioteca implementa uma lista dinâmica que pode armazenar objetos. Ela fornece métodos para adicionar, remover, pesquisar e manipular elementos na lista
import java.util.HashMap; // biblioteca implementa uma tabela de hash que mapeia chaves a valores.
import java.util.List; // 
import java.util.Map;
import java.util.Scanner;
import java.awt.Desktop; //  biblioteca fornece métodos para interagir com o ambiente de desktop do sistema operacional. Ela permite abrir arquivos, URLs 
import java.net.URI; // biblioteca fornece métodos para analisar, construir e manipular URIs.


public class Green {



    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        // Variáveis de controle de usuário      
        
        int regiao = 0;
        double bandeira = 0;
        int consumoAlto = 0;
        
       
        // Criação do objeto da classe Objetos
        Objetos objetos = new Objetos();

        // HashMap para armazenar os eletrodomésticos selecionados e seus consumos
        Map<String, Integer> eletrodomesticosSelecionados = new HashMap<>();
        
        List<Lembrete> lembretes = new ArrayList<>();

        
        boolean isUserRegistered = false;
        User user = null;

        // Loop do menu principal
        boolean sair = false;
        while (!sair) {
            System.out.println("---------------------------------------------------------");
            System.out.println("BEM-VINDO AO GREEN ENERGY");
            System.out.println("---------------------------------------------------------");
            System.out.println("[1] LOGIN");
            System.out.println("[2] CADASTRAR");
            System.out.println("[3] SAIR ");

            int opc = scan.nextInt();

            switch (opc) {
            case 1:
                    
            	// variável usada para indicar se um usuário está registrado ou não em algum sistema ou aplicativo.
            	if (isUserRegistered) {
                    System.out.println("Por favor, faça o login para continuar:");
                    System.out.print("Username: ");
                    String inputUsername = scan.next();
                    System.out.print("Password: ");
                    String inputPassword = scan.next();

                    if (user != null && inputUsername.equals(user.getNome()) && inputPassword.equals(user.getSenha())) {
                        System.out.println("Login bem-sucedido!");
                  
                            
                            //MENU 2
                            boolean menu2 = false;
                            boolean exibirConsumoTotal = false;
                            while (!menu2)
                            {
                            System.out.println("------------------------------------");	
                            System.out.println("----------------MENU----------------");
                            System.out.println("SELECIONE A OPÇÃO DESEJADA");
                            System.out.println("[1] ADICIONAR ELETRODOMESTICO");
                            System.out.println("[2] VERIFICAR CONSUMO ");
                            System.out.println("[3] ADICIONAR LEMBRETES");
                            System.out.println("[4] SUPORTE");
                            System.out.println("[5] SAIR");
                            System.out.println("------------------------------------");
                            int opc2 = scan.nextInt();
                            
                  
                            switch (opc2) {
                            case 1:                                
                            	//Essa estrutura de código permite que o usuário selecione um eletrodoméstico a partir das opções exibidas e continue dentro do loop enquanto o valor de eletroValido for falso. A lógica para validar a seleção do eletrodoméstico e atualizar o valor de eletroValido não está presente no trecho de código fornecido, mas pode ser adicionada posteriormente.
                            	if (regiao == 1) {
                            		Case1_Norte caso1 = new Case1_Norte(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso1.executar();
                                     break;
                            	}// IF REGIAO 1 
                                     
                            	if(regiao ==2) {
                            		Case2_Nordeste caso2 = new Case2_Nordeste(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso2.executar();
                                      break;
                            	}// IF REGIAO 2 
                            	
                            	if(regiao==3) {
                            		Case3_CentroOeste caso3 = new Case3_CentroOeste(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso3.executar();
                                      break;
                            	}// IF REGIAO 3 
                            	
                            	if(regiao==4) {
                            		Case4_Sudeste caso4 = new Case4_Sudeste(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso4.executar();
                                     break;
                            	}// IF REGIAO 4
                            	
                            	if(regiao==5) {
                            		Case5_Sul caso5 = new Case5_Sul(bandeira, objetos, eletrodomesticosSelecionados, scan);
                                    caso5.executar();
                                     break;

                            	}// IF REGIAO 5 
                       
                            case 2:
                                // Verifica o consumo total dos eletrodomésticos selecionados e printa a lista com os eletrodomésticos selecionados
                                double consumoTotal = 0;
                                System.out.println("Eletrodomésticos selecionados:");
                                for (Map.Entry<String, Integer> entry : eletrodomesticosSelecionados.entrySet()) {
                                    String eletrodomestico = entry.getKey();
                                    int consumo = entry.getValue();
                                    consumoTotal += consumo;
                                    System.out.println(eletrodomestico + ": " + consumo + " kWh");
                                }// LISTA A TABELA DE ELETRODOMESTICOS E SEUS RESPECTIVOS CONSUMOS 

                                if (consumoTotal > 0) {
                                    // Cálculo do valor total em reais 
                                    double valorTotalReais = consumoTotal * bandeira;
                                    System.out.println("Consumo total: " + consumoTotal + " kWh");
                                    System.out.println("Valor total em reais: " + valorTotalReais + " R$");

                                    if (consumoTotal > 685) {
                                        // Mensagem que será exibida caso o consumo em reais do usuário esteja maior que 685,00 reais
                                        System.out.println("--------------------------------------------------------------------------------------------------------");
                                        System.out.println("Descubra como o Green Energy pode ajudar você a economizar na conta de energia!");
                                        System.out.println("Seu consumo atual está acima da média brasileira! Nós temos a solução para reduzir seus gastos");
                                        System.out.println("e tornar sua casa mais sustentável. Venha conhecer nosso projeto inovador e descubra como calcular");
                                        System.out.println("o consumo de cada eletrodoméstico, economizando e contribuindo para um futuro mais verde!");
                                        System.out.println("[1] - SIM  /    [2] - NÃO ");
                                        consumoAlto = scan.nextInt();
                                        if (consumoAlto == 1) {
                                            try {
                                                URI link = new URI("https://www.mixo.io/site/green-energy-f77ys/index.html");
                                                Desktop.getDesktop().browse(link);
                                            } catch (Exception erro) {
                                                System.out.println(erro);
                                            }
                                       
                                        }// REDIRECIONAMENTI PARA CAPTAÇÃO DE EMAIL DO USUARIO 
                                    if (consumoAlto==2) {
                                    	System.out.println("MESMO ASSIM, DESDE JÁ AGRADECEMOS, SÓ DEPENDE DE VOCÊ.");
                                    }
                                    
                                    } // IF DO CONSUMO TOTAL MAIOR QUE 685
                                
                                }// IF DO CONSUMO TOTAL MAIOR QUE 0 
                               
                                else {
                                    System.out.println("Nenhum eletrodoméstico selecionado.");
                                }
                                break;


                            case 3:
                                System.out.println("Selecione o tipo de lembrete:");
                                System.out.println("[1] - LEMBRETE DIÁRIO");
                                System.out.println("[2] - LEMBRETE SEMANAL");
                                System.out.println("[3] - VERIFICAR LEMBRETES ");
                                int tipoLembrete = scan.nextInt();

                                switch (tipoLembrete) {
                                case 1:// ADICIONA UM LEMBRETE DIÁRIO 
                                    System.out.println("Digite o horário para o lembrete diário (formato HH:MM):");
                                    String horarioDiario = scan.next();
                                    System.out.println("Digite a mensagem do lembrete diário:");
                                    scan.nextLine(); // Consumir a quebra de linha pendente
                                    String mensagemDiario = scan.nextLine();
                                    Lembrete lembreteDiario = new Lembrete("Diário", horarioDiario, mensagemDiario);
                                    lembretes.add(lembreteDiario);
                                    System.out.println("Lembrete diário adicionado com sucesso!");
                                
                                    break;
								
								case 2:// ADICIONA UM LEMBRETE SEMANAL 
								    System.out.println("Digite o dia da semana para o lembrete semanal (1-7, onde 1 = domingo, 2 = segunda, etc.):");
								    int diaSemana = scan.nextInt();
								    System.out.println("Digite o horário para o lembrete semanal (formato HH:MM):");
								    String horarioSemanal = scan.next();
								    System.out.println("Digite a mensagem do lembrete semanal:");
								    scan.nextLine(); // Consumir a quebra de linha pendente
								    String mensagemSemanal = scan.nextLine();
								    Lembrete lembreteSemanal = new Lembrete("Semanal", horarioSemanal, diaSemana, mensagemSemanal);
								    lembretes.add(lembreteSemanal);
								    System.out.println("Lembrete semanal adicionado com sucesso!");
								    break;
								    
								case 3:
								    System.out.println("[1] VERIFICAR LEMBRETE DIÁRIO");
								    System.out.println("[2] VERIFICAR LEMBRETE SEMANAL");
								    int verificalembrete = scan.nextInt();

								    if (verificalembrete == 1) {
								        // Verificar lembretes diários
								        LocalTime currentTime = LocalTime.now();
								        for (Lembrete lembrete : lembretes) {
								            if (lembrete.getTipo().equals("Diário")) {
								                String lembreteHorario = lembrete.getHorario();
								                if (currentTime.getHour() == Integer.parseInt(lembreteHorario.substring(0, 2)) &&
								                        currentTime.getMinute() == Integer.parseInt(lembreteHorario.substring(3, 5))) {
								                    System.out.println("Lembrete diário: " + lembrete.getMensagem());
								                    // Realize a ação desejada para o lembrete diário
								                }
								            }
								        }  
								    
								    } // VERIFICA LEMBRETE DIÁRIO 
								    
								    else if (verificalembrete == 2) {
								        // Verificar lembretes semanais
								        LocalDate currentDate = LocalDate.now();
								        DayOfWeek currentDayOfWeek = currentDate.getDayOfWeek();

								        for (Lembrete lembrete : lembretes) {
								            if (lembrete.getTipo().equals("Semanal")) {
								                int diadaSemana = lembrete.getDiaSemana();

								                if (currentDayOfWeek.getValue() == diadaSemana) {
								                    String lembreteHorario = lembrete.getHorario();
								                    LocalTime currentTime = LocalTime.now();
								                    if (currentTime.getHour() == Integer.parseInt(lembreteHorario.substring(0, 2)) &&
								                            currentTime.getMinute() == Integer.parseInt(lembreteHorario.substring(3, 5))) {
								                        System.out.println("Lembrete semanal: " + lembrete.getMensagem());
								                        break; // Adicionando o break para sair do loop após exibir o lembrete
								                    }
								                }
								            }
								        }
								     
								    } // VERIFICA OS LEBRETES SEMANAL 
								    
                            	} //SWICH DO LEMBRETE 
                      
                            break; // Adicionando o break para sair do switch-case após executar o caso 3
                            
                            
                            case 4:
							    System.out.println("Ligue para o nosso suporte em: (98) 9 8228-1027");
							    break;
							
							
                            case 5:
                                System.out.println("OBRIGADO POR USAR O GREEN ENERGY, VOLTE SEMPRE!");
                                menu2 = true; // Atualização para sair do loop
                                sair = true; // Atualização para finalizar o programa
                                break;
                            default:
                                System.out.println("Opção inválida.");
                                break;
                        
                            }// SWITCH OPC DO MWNU 2 

                        if (sair) {
                            break; // Saída do loop principal
                        }
                            }
                    }/// LOGIN BEM SUCEDIDO, ENTRA NO SISTEMA 
                        
                        
                        else {
                            System.out.println("Usuário ou senha inválidos.");
                        }
                    
                    break;
                    } // if do login para continuar 
            	
                    

            case 2:
                // Cadastro do usuário
                System.out.println("Bem-vindo ao sistema de cadastro.");

                user = new User();
                System.out.print("Username: ");
                String username = scan.next();
                user.setNome(username);

                System.out.print("Password: ");
                String password = scan.next();
                user.setSenha(password);

                System.out.print("Digite o seu CPF: ");
                String cpf = scan.next();
                user.setCpf(cpf);

                System.out.print("Digite o seu Telefone: ");
                String telefone = scan.next();
                user.setTelefone(telefone);

                System.out.println("Usuário cadastrado com sucesso!");
                isUserRegistered = true;
               
                    System.out.println("QUAL REGIÃO VOCÊ MORA ?");
                    System.out.println("[1] NORTE");
                    System.out.println("[2] NORDESTE");
                    System.out.println("[3] CENTRO-OESTE");
                    System.out.println("[4] SUDESTE");
                    System.out.println("[5] SUL");
                    regiao = scan.nextInt();
                    if (regiao >5) {
                    	System.out.println("SELECIONE UMA REGIAO VÁLIDA");
                    	break;
                    }
                    
                    System.out.println("Usuário cadastrado com sucesso!");
                    break;

                case 3:
                    System.out.println("Obrigado por utilizar o Green Energy.");
                    sair = true;
                    break;

                default:
                    System.out.println("Opção inválida.");
                    break;
                    
                    
              	} // case do login do usuario 
            
            // Verificar lembretes diários
            LocalTime currentTime = LocalTime.now();
            for (Lembrete lembrete : lembretes) {
                if (lembrete.getTipo().equals("Diário")) {
                    String lembreteHorario = lembrete.getHorario();
                    if (currentTime.getHour() == Integer.parseInt(lembreteHorario.substring(0, 2)) &&
                            currentTime.getMinute() == Integer.parseInt(lembreteHorario.substring(3, 5))) {
                        System.out.println("Lembrete diário: Hora de realizar a tarefa!");
                        // Realize a ação desejada para o lembrete diário
                    }
                }
                
            }// lembretes
        
        }// menu 1 
    
    }//public static void main(String[] args)

	public void executar() {
		// TODO Auto-generated method stub
		
	}

}// public class Green
    



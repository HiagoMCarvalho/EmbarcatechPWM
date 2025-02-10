# PWM Control com Raspberry Pi Pico

## Descrição do Projeto
Este projeto implementa o controle de um servo motor e um LED utilizando PWM (Pulse Width Modulation) no Raspberry Pi Pico. O servo motor oscila entre 0º e 180º após um período de inicialização, enquanto o LED acompanha a intensidade do sinal PWM.

## Estrutura do Projeto

```
PWM/
├── .vscode/            # Configurações do VS Code (opcional)
├── build/              # Diretório de build (gerado pelo CMake)
├── .gitignore          # Arquivo para ignorar arquivos no controle de versão
├── CMakeLists.txt      # Configuração do CMake para compilação do projeto
├── diagram.json        # Diagrama do circuito (se aplicável)
├── pico_sdk_import.cmake # Importação do SDK do Raspberry Pi Pico
├── Pwm.c               # Código principal do projeto
├── wokwi.toml          # Arquivo de configuração do simulador Wokwi
```

## Dependências
Para compilar e rodar este projeto, você precisará de:
- Raspberry Pi Pico SDK
- CMake
- Um ambiente de desenvolvimento C (GCC ARM)

## Compilação e Execução
1. Configure o ambiente do SDK do Raspberry Pi Pico.
2. No terminal, navegue até o diretório do projeto:
   ```sh
   git clone https://github.com/HiagoMCarvalho/EmbarcatechPWM.git
   cd PWM
   ```
3. Crie um diretório de build e entre nele:
   ```sh
   mkdir build && cd build
   ```
4. Execute o CMake para configurar o projeto:
   ```sh
   cmake ..
   ```
5. Compile o projeto:
   ```sh
   make
   ```
6. Envie o arquivo `.uf2` gerado para o Raspberry Pi Pico.

## Simulação no Wokwi
1. Acesse [Wokwi](https://wokwi.com/) e importe os arquivos `diagram.json` e `wokwi.toml`.
2. Inicie a simulação para visualizar o funcionamento do projeto sem precisar de hardware físico.

## Funcionamento do Código
- O servo inicia em 180º, depois se move para 90º e em seguida para 0º, aguardando 5 segundos em cada posição.
- Após a inicialização, ele oscila continuamente entre 0º e 180º.
- O LED PWM acompanha o ciclo do servo.

## Autor
Desenvolvido por <https://github.com/HiagoMCarvalho>

## Vídeo
Assista ao vídeo explicação: <https://drive.google.com/file/d/1RNJSfUh5YhYdfH0CiT3AN539w-FR6nRD/view?usp=sharing>

## Licença
Este projeto está sob a licença MIT.


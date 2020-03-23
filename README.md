# Ventilador Pulmonar Open Source VPOS
VPOS V1.0
Parte eletrônica de equipamento de emergência para COVID19 para fabricação no Brasil.

## Objetivos:

1. Automatizar conceiros de balão de Ambu (balão de reanimação).
1. Sistema mais simples possível, somente com os componentes estritamente necessários e disponíveis na forma de um módulo, para evitar soldas e montagens complicadas.
1. Sistema com partes facilmente disponíveis em lojas on-line.

## Requisitos (eletrônica):

1. Possível disponibilidade de peças para fabricação de 500 unidades.
1. Ele deve funcionar continuamente sem falhas (ciclo de trabalho de 100%) por 14 dias - 24 horas por dia. Se necessário, pode ser substituída após 14 dias.
1. Forneça pelo menos duas configurações para mistura ar/O2 entregues em ciclos de respiração. As configurações são 450 ml +/- 10 ml por respiração e 350 ml +/- 10 ml por respiração.
1. Tenha uma taxa ajustável entre 12 e 20 ciclos (respirações por minuto).
1. Prevenção de pontos quentes.
1. Ser capaz de respirar para um paciente inconsciente que é incapaz de respirar por si mesmo. Capacidade de sentir quando um paciente está respirando e apoiar que a respiração é desejável, mas não essencial.
1. Fail SAFE. Gerar um alarme em caso de falha. Os modos de falha a serem alarmados incluem (mas não estão limitados a) perda de pressão e perda de O2.

## Ideias
### Controle, microcontrolador (MCU):
1. Kit de desenvolvimento Arduino Nano → O Ard. Nano tem o mesmo hardware do arduino Uno. Ele é barata e facilmente disponível.
1. Shield de parafusos → Conexões por apertos pode ser uma boa solução (aceitamos sugestões!).
### Interface homem-máquina (IHM):
1. Tela LCD 16x2 com módulo i2c para menu de configurações → Facilmente acessível.
1. Teclado matricial de membrana para configurar → O teclado pode ser configurado para confirar o VPOS.
1. Sirene 12V (+ módulo relé) para alarmes → Essa sirene serve de alerta de emergência. O buzzer é muito baixo para esse tipo de alerta.
1. Buzzer 5V → Usado para feedback do aperto de botões e configurações.
### Sistema de atuação:
1. Motores tipo NEMA (NEMA17 ou NEMA23) → Versátil e facilmente disponível.
1. Driver TB6600 para acionar os motores NEMA → Esse driver é genérico e permite uso com os mais diversos motores.
### Conversão de energia / sistema elétrico:
1. Fonte de alimentação de 24V @5A
1. Módulo DC/DC ajustado em 5V para alimentar o arduino.
1. Botão parada de emergência industrial.

## Esquema eletrônico
![Driver](/pics/Drawing_geral.jpg)


## Conteúdo

1. [Partes]

[Partes]: docs/HW-Parts.md

## Referências
1. [Artigo Ventilação mecânica: princípios, análise gráfica e modalidades ventilatórias]
1. [Grupo COVID-19 Air BRASIL]
1. [CoronaVirus Makers]
1. [Open hardware projects working to solve COVID-19]
1. [COVID-19 Ventilator Projects and Resources and FAQ]

[Artigo Ventilação mecânica: princípios, análise gráfica e modalidades ventilatórias]: http://www.scielo.br/pdf/jbpneu/v33s2/a02v33s2.pdf

[Grupo COVID-19 Air BRASIL]: https://www.facebook.com/groups/235476464265909/

[CoronaVirus Makers]: https://gitlab.com/coronavirusmakers

[Open hardware projects working to solve COVID-19]: https://opensource.com/article/20/3/open-hardware-covid19

[COVID-19 Ventilator Projects and Resources and FAQ]: https://github.com/PubInv/covid19-vent-list



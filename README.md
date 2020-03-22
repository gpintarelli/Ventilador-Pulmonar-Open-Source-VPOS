# Ventilador Pulmonar Open Source VPOS
VPOS V1.0

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
### Controle, microcontrolador (MCU)
1. Kit de desenvolvimento Arduino NANO
1. Shield de parafusos
### Interface homem-máquina (IHM):
1. Tela LCD 16x2 com módulo i2c para menu de configurações
1. Teclado matricial de membrana para configurar
1. Sirene 12V para alarmes
### Sistema de atuação:
1. Motores tipo NEMA (NEMA17 ou NEMA23)
1. Driver TB6600 para acionar os motores NEMA (esse driver é genérico e permite uso com os mais diversos motores)
### Conversão de energia / sistema elétrico:
1. Fonte de alimentação de 24V @5A
1. Módulo DC/DC ajustado em 5V para alimentar o arduino

## Conteúdo

1. [Partes]

[Partes]: docs/HW-Parts.md
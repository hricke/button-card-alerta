
############### COD DO BOTAO QUE MUDA COR AO TROCAR DE STATUS #####################

type: custom:button-card
entity: sensor.status_tomada_222   ############ ENTIDADE
icon: mdi:cctv ############### AQUI É O ICONE QUE FICA QUANDO TIVER DESLIGADO
name: Monitor Quarto ############## NMOME
tap_action:
  action: call-service
  service: input_select.select_next
  data:
    entity_id: input_select.cube_mode
show_state: true
state:
  - value: Ligado ########### COLOCAR O MESMO NOME DO STATUS DO SENSOR ON OU OFF TIPO CORRENDO OOU PARADO
    color: rgb(189, 255, 5)
    icon: mdi: ############## AQUI É O ICONE QUE FICA QUANDO TIVER LIGADO
  - value: Desligado ########### COLOCAR O MESMO NOME DO STATUS DO SENSOR ON OU OFF TIPO CORRENDO OOU PARADO
    color: var(--disabled-text-color)

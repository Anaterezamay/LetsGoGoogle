# LetsGoGoogle
Projeto final do curso Python para Jornalistas (Knight Center)
#Atualização 1
#não coloquei ainda como fazer o download auto da pasta com zip. #Vou começar a pinçar.
ESTADO = input ('Digite a sigla do Estado desejado: ')
ESTADO = ESTADO.upper()
estado_codigo = (f'bem_candidato_2014_{ESTADO}.txt') 
codigo_ler =(f'{estado_codigo}')
arquivo = open(f'{estado_codigo}')

planilha = arquivo.read()
print (planilha)
arquivo.close()

#Atualização 2
ESTADO = input ('Digite a sigla do Estado desejado: ')
ESTADO = ESTADO.upper()
estado_codigo = (f'consulta_cand_2014_{ESTADO}.txt') 
cod_ab = open(f'{estado_codigo}')



planilha = cod_ab.read()

planilha = planilha.replace(";",",")
planilha = planilha.replace("\"", "")

lista = estado_codigo.strip("\r\n")
lista = list(open(f'{estado_codigo}'))
lista = [_str.split(' ') for _str in lista]
print (lista)

cod_ab.close()

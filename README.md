# LetsGoGoogle
Projeto final do curso Python para Jornalistas (Knight Center)

#não coloquei ainda como fazer o download auto da pasta com zip. #Vou começar a pinçar.
ESTADO = input ('Digite a sigla do Estado desejado: ')
ESTADO = ESTADO.upper()
estado_codigo = (f'bem_candidato_2014_{ESTADO}.txt') 
codigo_ler =(f'{estado_codigo}')
arquivo = open(f'{estado_codigo}')

planilha = arquivo.read()
print (planilha)
arquivo.close()

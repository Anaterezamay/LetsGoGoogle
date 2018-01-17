#Escolha um ano. Só temos os dados disponíveis a partir de 2006
ano = input ('Qual ano de eleição, a partir de 2006, você deseja consultar?')

#Faz o Download e Unzip os arquivos txt dos candidatos
from io import BytesIO
from urllib.request import urlopen
from zipfile import ZipFile
zipurl = (f'http://agencia.tse.jus.br/estatistica/sead/odsele/consulta_cand/consulta_cand_{ano}.zip')
print('Estamos apenas começando!')

with urlopen(zipurl) as zipresp:
    with ZipFile(BytesIO(zipresp.read())) as zfile:
        zfile.extractall('Candidatos')
print('Calma, seus candidatos por ano já foram selecionados.')

#Faz o Download e Unzip os arquivos txt dos bens
from io import BytesIO
from urllib.request import urlopen
from zipfile import ZipFile
zipurl = (f'http://agencia.tse.jus.br/estatistica/sead/odsele/bem_candidato/bem_candidato_{ano}.zip')
print('Mais um pouquinho')
with urlopen(zipurl) as zipresp:
    with ZipFile(BytesIO(zipresp.read())) as zfile:
        zfile.extractall('Bens')
print('E agora os bens deles!')

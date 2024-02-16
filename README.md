# CODIGO-PYTHON
linguagem de programação em python
***********************************
import pyodbc

dados_conexao = (
    
    "Driver={SQL Server};"
    "Server={Petherson};"
    "Database={IGREJA};"
    "UID={};"
    "PWD={};"
    
)

conexao = pyodbc.connect(dados_conexao)
print(" Acessado com Sucesso ")

curso = conexao.cursor()

nome = input('Entre com seu nome completo: ')
endereco = input('Rua e numero: ')
emai = input('E-mail: ')
data_nascimento = input('Data de nascimento exe. dd/mes/nn: ')
ministerio = input('Seu misterio: ')
estado_civil =input('Estado cilvil: ')
sexo = input('Colocar somente M ou F: ')


comando = f"""INSERT INTO TB_CADASTRO (NOME,ENDEREÇO,EMAIL,DATA_DE_NASCIMENTO,MINISTERIO,ESTADO_CIVIL,SEXO)
VALUES
('{nome}', '{endereco}', '{emai}', '{data_nascimento}' ,'{ministerio}', '{estado_civil}','{sexo}')"""

pecurso.execute(comando)
curso.commit()

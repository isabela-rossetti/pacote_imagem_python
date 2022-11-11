# pacote_processamento_imagem

O processamento da imagem do pacote pode ser usado para:
	
		- Correspondencia de histograma
		- Semelhanca estrutural
		- Redimensionar imagem
		- Ler imagem
		- Salvar imagem
		- Plotar imagem
		- Resultado da trama
		- Plotar histograma

## Instalacao

```bash
pip install pacoteprocessamentoimagem
```

## Autor
Isabela Rossetti

## Licenca
[MIT](https://github.com/isabela-rossetti/pacote_imagem_python/blob/main/LICENSE.txt)

__________________________________________

<h2>Passo a passo para criacao do pacote</h2>

<h3>1. Criar conta no Test Pypi e Pypi</h3>

[Test Pypi](https://test.pypi.org/)

[Pypi](https://pypi.org/)

<h3> 2. Criar um projeto </h3>

Criar pastas e arquivos para submissao. Neste caso foi utilizado a seguinte estrutura:

```
/pacote_python
   └LICENSE
   └README.md
   └setup.py
   └/pacoteprocessamentoimagem
      └combinacao
      └io
      └plot
      └transformacao
```

<h3> 3. Editar o conteudo dos arquivos</h3>

<h5> LICENSE </h5>

Neste arquivo foi escolhida a licenca <i>MIT License</i>, retirada do site  https://choosealicense.com/.

```
MIT License

Copyright (c) [ano] [nome_do_pacote]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

<h5>README </h5>

O arquivo deve conter informacoes de instalação, uso, licenca etc. Neste caso, as instruções de uso estao no topo do arquivo.

<h5> setup.py </h5>

O arquivo é utilizado para construção do pacote.

```
from setuptools import setup

with open("README.md", "r") as fh:
    readme = fh.read()

setup(name='pacoteprocessamentoimagem',
    version='0.0.1',
    url='https://github.com/isabela-rossetti/pacote_python',
    license='MIT License',
    author='Isabela Rossetti',
    long_description=readme,
    long_description_content_type="text/markdown",
    author_email='isabelarossetti.ir@gmail.com',
    keywords='Imagem',
    description=u'Pacote de leitura e processamento de imagens em python',
    packages=['pacoteprocessamentoimagem'])
```

<h3>4. Acessar a raiz do projeto</h3>

Acessar a pasta raiz do projeto atraves do terminal.

<h3>5. Executar os comandos de instalação</h3>

Os seguintes comandos devem ser executados no terminal:

```
python -m pip install --upgrade pip
```

```
python -m pip install --user twine
```

```
python -m pip install --user setuptools
```

```
pip install wheel
```

<h3>6. Executar o comando para criar a distribuicao</h3>


```
python setup.py sdist bdist_wheel
```

<h3>7. Publicar o pacote no Test Pypi</h3>

Publicar primeiro no Test Pypi para testar o funcionamento do pacote sem atrapalhar o versionamento do repositorio oficial (Pypi) atraves do seguinte comando:

```
python -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*
```

Neste momento sera pedido o login e senha cadastradas no site TestPypi. Feito o login, o pacote devera ser instalado com sucesso. 

<h3>8. Testar o pacote</h3>

Apos acessar o pacote no site TestPypi, executar a instalacao do pacote atraves do seguinte comando:

```
pip install -i https://test.pypi.org/simple/ pacoteprocessamentoimagem
```

Para usar o pacote, executar:

```
from pacoteprocessamentoimagem import combinacao, transformacao, io, plot
```

<h3>9. Publicar o pacote no Pypi</h3>

Com o pacote funcionando, publicar no Pypi atraves do seguinte comando:

```
python -m twine upload --repository-url https://upload.pypi.org/legacy/ dist/*
```

Novamente sera pedido o login e senha (desta vez as cadastradas no site Pypi) e o pacote sera instalado.

<h3>10. Usar o pacote</h3>

Executar a instalacao do pacote atraves do codigo gerado no Pypi:

```
pip install pacoteprocessamentoimagem
```

Testar novamente com os 2 ultimos codigos apresentados no item 8.

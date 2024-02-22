# Prevision_model_Machine-Learn-AI-900-DIO

## Passo a passo

Primeiro criei uma conta na Azure pelo site: <https://portal.azure.com>

Depois de ter criado uma conta e assinatura for habilitada,o seguinte passo é clicar em "Create a Resourse".

Na proxima página pesquise por "Machine Learning" na barra de pesquisa, assim que aparecer os elementos filtrados na tela, procure por "Azure Machine Learning", clique em "Create" e então "Azure Machine Learning".

Na página que abrir, no campo "Resource group" clique no link "Create new" logo abaixo do campo, escolha um nome de sua preferência e clique em "OK".

Preencha o campo "Name", escolha a região no campo "Region", obs(Escolha qualquer outra Região proxima a você, pois o "Brasil South" não tem tantos recursos e é mais caro.

Feito isso clique em "Review + Create. Caso você tenha preenchido tudo direitinho na próxima página clique em "Create" e aguarde.

Quando finalizado e criado com sucesso, clique no "botão Go so Resource" e na próxima página clique em "Launch studio".

Se é sua primeira vez no Azure, talvez ele peça algumas informações para criar uma workspace.

Proximo passo agora é procurar no menu a sua esquerda o "Automated ML", clique nele, em seguida clique em "New Automated ML job".

Para fins didáticos preencha os campos desta forma:

Job name: mslearn-bike-automl
Experiment name: Create new
New experient name: mslearn-bike-rental
Description: Opcional

Clique em "Next"

Na próxima tela configure da seguinte forma:

Select task type: Regression

Clique em "Create"

Name: Sua escolha
Description: Sua escolha
Type: Tabular

Clique em "Next"

Selecione "From web files"

Clique em "Next"

No campo Web URL coloque: <https://aka.ms/bike-rentals>

Clique em "Next"

No campo Column headers escolha a opção: "Only first file has headers".

Clique em "Next", Clique em "Next" novamente e em seguita "Create".

Quando tudo estiver finalizado, selecione se dado criado e clique em "Next".

Faça as seguintes configurações:

No campo Target Column, selecione "rentals (Integer)"

Clique em "View additional configuration settings"

Desmarque todos checkbox

No campo Allowed models, selecione "RandomForest e "LightGBM" e clique em "Save" e "save" novamente.

Expanda a seção "Limits" e faça as seguintes configurações:

Max trials: 3
Max Concurrent trials: 3
Max nodes: 3
Metric sore threshold: 0.085
Experiment timeout: 15
Iteration timeout: 15
Marque a opção "Enable early termination".
Validation type: "Train-validation split".

Clique em "Next", "Next" novamente e "Submit training job".

Aguarde a tarefa ser complatada e prontinho. Seu modelo está criado.

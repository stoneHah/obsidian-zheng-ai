---
title: "MinerU"
owner: "opendatalab"
source: "https://github.com/opendatalab/mineru"
website: "https://mineru.net"
description: "A high-quality tool for convert PDF to Markdown and JSON.一站式开源高质量数据提取工具，将PDF转换成Markdown和JSON格式。"
stars: 30.6
tags:
  - "github"
  - "repo"
  - "python"
  - "pdf"
  - "parser"
  - "ocr"
  - "pdf-converter"
  - "extract-data"
  - "document-analysis"
  - "pdf-parser"
  - "layout-analysis"
  - "ai4science"
  - "pdf-extractor-rag"
  - "pdf-extractor-llm"
  - "pdf-extractor-pretrain"
created: 2025-04-15
---
## README

[![](https://github.com/opendatalab/MinerU/raw/master/docs/images/MinerU-logo.png)](https://github.com/opendatalab/MinerU/blob/master/docs/images/MinerU-logo.png)

[![stars](https://camo.githubusercontent.com/afc27e3f1f59f307c3a8d04566b579bdb3abab006edbd6a4573e6996e15e2f6c/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f6f70656e646174616c61622f4d696e6572552e737667)](https://github.com/opendatalab/MinerU) [![forks](https://camo.githubusercontent.com/c7e0d10c7571ff407489ef6026a3d3b21991a77e9f283b6a7b1d2068627cb830/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f666f726b732f6f70656e646174616c61622f4d696e6572552e737667)](https://github.com/opendatalab/MinerU) [![open issues](https://camo.githubusercontent.com/a8b818359f939addf54adc17bbfca4409414f23e403ba06d2e19ea47e419554b/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6973737565732d7261772f6f70656e646174616c61622f4d696e657255)](https://github.com/opendatalab/MinerU/issues) [![issue resolution](https://camo.githubusercontent.com/6afd6231712e8bb0d087d84390c797bcfa180ead2a3ed93455f065b3d9db4630/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6973737565732d636c6f7365642d7261772f6f70656e646174616c61622f4d696e657255)](https://github.com/opendatalab/MinerU/issues) [![PyPI version](https://camo.githubusercontent.com/25cc81a36fcb34f65a7165aa71423510c06a868f88b543a0955e1c8bde069fe0/68747470733a2f2f696d672e736869656c64732e696f2f707970692f762f6d616769632d706466)](https://pypi.org/project/magic-pdf/) [![PyPI - Python Version](https://camo.githubusercontent.com/36a227a62a5d83a5293c2333ca157dd72ee55e0bfcf727d86af98fa753eb00af/68747470733a2f2f696d672e736869656c64732e696f2f707970692f707976657273696f6e732f6d616769632d706466)](https://pypi.org/project/magic-pdf/) [![Downloads](https://camo.githubusercontent.com/a72a9d5d89658e8fb219e54a413eba7aab272fa7f59f6014020ff143bc98f6a5/68747470733a2f2f7374617469632e706570792e746563682f62616467652f6d616769632d706466)](https://pepy.tech/project/magic-pdf) [![Downloads](https://camo.githubusercontent.com/a09c60255fa5d195826a27104bddc64667380607a538b0c51c3467336a40494e/68747470733a2f2f7374617469632e706570792e746563682f62616467652f6d616769632d7064662f6d6f6e7468)](https://pepy.tech/project/magic-pdf)

[![OpenDataLab](https://camo.githubusercontent.com/7823e1efdb5fc27ca8bc72a464bf422be18f6ad3f3036c72217f21c1d1e641e3/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f44656d6f5f6f6e5f4f70656e446174614c61622d626c75653f6c6f676f3d646174613a696d6167652f7376672b786d6c3b6261736536342c50484e325a79423361575230614430694d544d304969426f5a576c6e61485139496a457a4e43496765473173626e4d39496d6830644841364c79393364336375647a4d7562334a6e4c7a49774d44417663335a6e496a3438634746306143426b50534a744d5449794c446c6a4d4377314c5451734f5330354c446c7a4c546b744e4330354c546b734e4330354c446b744f5377354c4451734f537735656949675a6d6c736244306964584a734b434e684b534976506a78775958526f49475139496d30784d6a49734f574d774c4455744e4377354c546b734f584d744f5330304c546b744f5377304c546b734f5330354c446b734e4377354c446c364969426d615778735053496a4d4445774d5441784969382b50484268644767675a44306962546b784c444534597a41734e5330304c446b744f537735637930354c5451744f5330354c4451744f5377354c546b734f5377304c446b734f586f6949475a7062477739496e56796243676a59696b694c7a3438634746306143426b50534a744f5445734d54686a4d4377314c5451734f5330354c446c7a4c546b744e4330354c546b734e4330354c446b744f5377354c4451734f537735656949675a6d6c7362443069497a41784d4445774d534976506a78775958526f49475a7062477774636e56735a5430695a585a6c626d396b5a43496759327870634331796457786c50534a6c646d56756232526b4969426b50534a744d7a6b734e6a4a6a4d4377784e6977344c444d774c4449774c444d344c4463744e6977784d6930784e6977784d6930794e6c59304f574d774c5451734d7930334c4459744f4777304e6930784d6d4d314c5445734d5445734d7977784d537734646a4d78597a41734d7a63744d7a41734e6a59744e6a59734e6a59744d7a63734d4330324e69307a4d4330324e6930324e6c59304e6d4d774c5451734d7930334c4459744f4777794d433032597a55744d5377784d53777a4c4445784c4468324d6a4636625330794f537732597a41734d5459734e69777a4d4377784e7977304d43777a4c4445734e5377784c4467734d5377314c4441734d5441744d5377784e53307a517a4d334c446b314c4449354c4463354c4449354c445979566a5179624330784f537731646a4977656949675a6d6c736244306964584a734b434e6a4b534976506a78775958526f49475a7062477774636e56735a5430695a585a6c626d396b5a43496759327870634331796457786c50534a6c646d56756232526b4969426b50534a744d7a6b734e6a4a6a4d4377784e6977344c444d774c4449774c444d344c4463744e6977784d6930784e6977784d6930794e6c59304f574d774c5451734d7930334c4459744f4777304e6930784d6d4d314c5445734d5445734d7977784d537734646a4d78597a41734d7a63744d7a41734e6a59744e6a59734e6a59744d7a63734d4330324e69307a4d4330324e6930324e6c59304e6d4d774c5451734d7930334c4459744f4777794d433032597a55744d5377784d53777a4c4445784c4468324d6a4636625330794f537732597a41734d5459734e69777a4d4377784e7977304d43777a4c4445734e5377784c4467734d5377314c4441734d5441744d5377784e53307a517a4d334c446b314c4449354c4463354c4449354c445979566a5179624330784f537731646a4977656949675a6d6c7362443069497a41784d4445774d534976506a786b5a575a7a506a78736157356c59584a48636d466b61575675644342705a4430695953496765444539496a6730496942354d5430694e44456949486779505349334e53496765544939496a45794d4349675a334a685a476c6c626e5256626d6c30637a306964584e6c636c4e7759574e6c5432355663325569506a787a6447397749484e3062334174593239736233493949694e6d5a6d59694c7a343863335276634342765a6d5a7a5a585139496a456949484e3062334174593239736233493949694d795a544a6c4d6d55694c7a34384c327870626d5668636b6479595752705a573530506a78736157356c59584a48636d466b61575675644342705a4430695969496765444539496a6730496942354d5430694e44456949486779505349334e53496765544939496a45794d4349675a334a685a476c6c626e5256626d6c30637a306964584e6c636c4e7759574e6c5432355663325569506a787a6447397749484e3062334174593239736233493949694e6d5a6d59694c7a343863335276634342765a6d5a7a5a585139496a456949484e3062334174593239736233493949694d795a544a6c4d6d55694c7a34384c327870626d5668636b6479595752705a573530506a78736157356c59584a48636d466b61575675644342705a4430695979496765444539496a6730496942354d5430694e44456949486779505349334e53496765544939496a45794d4349675a334a685a476c6c626e5256626d6c30637a306964584e6c636c4e7759574e6c5432355663325569506a787a6447397749484e3062334174593239736233493949694e6d5a6d59694c7a343863335276634342765a6d5a7a5a585139496a456949484e3062334174593239736233493949694d795a544a6c4d6d55694c7a34384c327870626d5668636b6479595752705a573530506a77765a47566d637a34384c334e325a7a343d266c6162656c436f6c6f723d7768697465)](https://mineru.net/OpenSourceTools/Extractor?source=github) [![HuggingFace](https://camo.githubusercontent.com/545f0fe2269e1589381626b5ba6a4c447c6c043290697784879410280c85a90b/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f44656d6f5f6f6e5f48756767696e67466163652d79656c6c6f772e7376673f6c6f676f3d646174613a696d6167652f706e673b6261736536342c6956424f5277304b47676f414141414e5355684555674141414638414141425943414d414141436b6c39742f414141416b31424d5645564863457a2f6e51762f6e51762f6e51722f6e51762f6e51722f6e51762f6e51762f6e51722f7752662f7478542f7067372f7952722f7242442f7a527a2f6e67762f6f417a2f7a687a2f6e77762f7478542f6e67762f3042332b7a427a2f6e51762f3068372f77786e2f7652622f7468586b7569542f7278482f7078442f6f677a637179662f6e5176546c537a2f637a43786b79372f536a6966646a542f4d6a332b4d6a33774d6a313561546e444e7a2b445344395254554273503046524f3051364f305779497845494141414147485253546c4d414442387a535746336b7244447738544a314e625835656676386666392f66784b444a3975414141474b6b6c45515652343275325a3633716a4f41794743345277434f6642324a41477172536232576e54772f316633556157635347594e4b5464662f502b6d4f6b5472452b794a42756c7666764c543241357275656e61564879496b7333336e706c2f364334732f5a4c414d3435534f692f3146745a5079467572314f596f66425833773764353442786d2b453864622b6e4472313274746d45535a347a6c75644a4547355337544f373259506c4b5a4679452b594359554a54425a734d694e53355364374e6c446d4b4d324567324a516738617762676c667167626841726a786b533764677032524836686339414d4c645a5955745a4e35444a72346d6f6c433842664b72456b504b456e45566a4c62675731664c7937375a564f4a61676f49634c496c2b497861515a476a6958353937486f704635436b6158564d444f395079697833414656336b77346c514c436248754d6f767a3846616c6c626351494a35546130766b7339526e6f6c62434b383442746a4b5253357541343368596f5a634f424749473245706276364376465651386d386c6f683636574e7953736e4e3768744c35384c4e702b4e5854382f506858694258504d6a4c5378747770385739662f31416e6752696572426b412b6b6b2f497055534f654b42797a6e3879336b41414166682f2f306f58675634726f486d2f6b7a3445327a2f2f7a5263332f6c6777427a624d326d4a7851456135707167583764314c306874726878374c4b784f5a6c4b627763415779454f577159534938595074674451566a7042356e76614861536e426151534436687765446938506f737844362f50543039595933785141374c5443544b6659582b5148704130474363716d454876722f6379664b5154457577676273326b50784a454230694e6a664a63435450796f63782b413067726948536d4144694339316f4e4756774a363952756459653635764a6d6f716670756c306c727158616457306a464b4835424b77416543712b44656e37732b337a66524a7a4136312f556a2f39482f567a4c4b5478396a46505064586565502b4c37574576444c414b41496f46386250544b54302b544d37573865506a33527a2f596e336b4f41703266314b663057656f6e7937706e2f6350796476685159562b65464f666d4f753756422f5669506533342f454e33524648592f7952755438646443744d50482f4d6342415435732b765264652f676632632f7350736a4c4b2b6d354942514635744f2b683274546c42476e50363639334a6473766f666a4f506e6e45486b6832546e562f583166426c3953357a7277757746384e467241564a567743415054653867614a6c6f6d716c7030707634506a6e3938744a2f742f664c2b2b36756e705231594743326e2f4b436f613074544c6f4b6945655550446c39346e6a2b352f5476332f6554357642513630583153306f5a722b49575252384c64687537416c4c6a5049536c4a634f397672466f746b793953707a446571756c7745697235626559416330523744394b533144587661306a68595244586f4578506463367977354753686b5a58653951644f2f754f76486f66786a72562f544e5336694d4a532b3454635354676b396e3561674a64425162422f2f4966462f48707650743354626937623649364b305237327036616a7279454a72454e57326262655655476a66676f616c73344c3434336337424545346d4a4f32537062526e67785172414b527564527a4751386a564f4c327144566a6a49384b3167633354494a354b69465a31712b67647341525042344e515334416a77565374373244536f584e794f57557255356d51396e5259796a703839586f376f52493642676139514e54316d512f7074614a7135542f37576367415a7977522f586c5047415544646574334c452b71533054492b672b614a55384d49716a6f304b78384c792b6d61784c6a4a6d6a51313872413059436b784c5162555a50315771646d7951474a4c556d37566e5146716f646d5853716d527264567071647a6b354c766d76677445635738504d476461533233454f577944566241435a7a554a5061714d626a44787041335172676c3041696b696d474462716d79543850384e4f596971726c64463872582b594e37546f705834556f4875534359593763675834674877636c514b6c317a6878305448662b7443415556616c7a6a493757673945687074726b496366494a6a41393465764f6e384232654861567a7642726e6c32696730536f36687650617a304947634f7654487655496c45322b70727141784c5351785a6c55327374716c314e7143434c644969494e2f693144424548556f456c4d3964427261766269416e4b716770693449426b772b75745350496f42696a44584a6970535656374d704f454a55416335516d6d33426e554e2b7733687465456965594b66525a53495563584b4d5666307535774434457773554e56765a4f745554374132476b6666486a42795770487176524259725456373261366a387a5a3657304454453836486e3034626d795758335269395748375a55365137682b5a486f306e4855416373517656685852445a484368776979692f686e50754f735345463645786b336f365939445431655a2b36634153586b3259396b2b36454f514d44476d3657424b3130774f514a43427772656e383663505057556352416e54566a476355314c4267733946555269582f6536343739795a634c7743426d54786961774577724f636c6575753132743374624c762f4e34524c594942685965786d3746636e344f4a636e302b7a632b73382f5666506564645a4841474e365454386547637a4864522f477473312f4d7a446b54687232337a71725666414d465433334e7831524a7378316b357a7557494c4c6e472f7673482b46763544344e5456637031477a6f384141414141456c46546b5375516d4343266c6162656c436f6c6f723d7768697465)](https://huggingface.co/spaces/opendatalab/MinerU) [![ModelScope](https://camo.githubusercontent.com/cefa3a0aa0b04b14356ea9c36d5556034602ff2e616f4699c7267cbbfaed783d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f44656d6f5f6f6e5f4d6f64656c53636f70652d707572706c653f6c6f676f3d646174613a696d6167652f7376672b786d6c3b6261736536342c50484e325a79423361575230614430694d6a497a4969426f5a576c6e61485139496a49774d43496765473173626e4d39496d6830644841364c79393364336375647a4d7562334a6e4c7a49774d44417663335a6e496a344b436941385a7a344b4943413864476c306247552b544746355a5849674d54777664476c306247552b43694167504842686447676761575139496e4e325a3138784e4349675a6d6c7362443069497a59794e47466d5a6949675a443069625441734f446b754f4452734d6a55754e6a55734d4777774c4449314c6a59304f546b35624330794e5334324e537777624441734c5449314c6a59304f546b356569497650676f67494478775958526f49476c6b50534a7a646d64664d54556949475a706247773949694d324d6a52685a6d596949475139496d30354f5334784e4377784d5455754e446c734d6a55754e6a55734d4777774c4449314c6a5931624330794e5334324e537777624441734c5449314c6a59316569497650676f67494478775958526f49476c6b50534a7a646d64664d54596949475a706247773949694d324d6a52685a6d596949475139496d30784e7a59754d446b734d5451784c6a4530624330794e5334324e446b354f537777624441734d6a49754d546c734e4463754f4451734d4777774c4330304e7934344e4777744d6a49754d546b734d4777774c4449314c6a59316569497650676f67494478775958526f49476c6b50534a7a646d64664d54636949475a706247773949694d7a4e6d4e6d5a44456949475139496d30784d6a51754e7a6b734f446b754f4452734d6a55754e6a55734d4777774c4449314c6a59304f546b35624330794e5334324e537777624441734c5449314c6a59304f546b356569497650676f67494478775958526f49476c6b50534a7a646d64664d54676949475a706247773949694d7a4e6d4e6d5a44456949475139496d30774c4459304c6a4535624449314c6a59314c4442734d4377794e5334324e5777744d6a55754e6a55734d4777774c4330794e5334324e586f694c7a344b4943413863474630614342705a44306963335a6e587a45354969426d615778735053496a4e6a493059575a6d4969426b50534a744d546b344c6a49344c4467354c6a6730624449314c6a59304f546b354c4442734d4377794e5334324e446b354f5777744d6a55754e6a51354f546b734d4777774c4330794e5334324e446b354f586f694c7a344b4943413863474630614342705a44306963335a6e587a49774969426d615778735053496a4d7a5a6a5a6d51784969426b50534a744d546b344c6a49344c4459304c6a4535624449314c6a59304f546b354c4442734d4377794e5334324e5777744d6a55754e6a51354f546b734d4777774c4330794e5334324e586f694c7a344b4943413863474630614342705a44306963335a6e587a49784969426d615778735053496a4e6a493059575a6d4969426b50534a744d5455774c6a51304c445179624441734d6a49754d546c734d6a55754e6a51354f546b734d4777774c4449314c6a5931624449794c6a45354c4442734d4377744e4463754f4452734c5451334c6a67304c4442364969382b43694167504842686447676761575139496e4e325a3138794d6949675a6d6c7362443069497a4d3259325a6b4d5349675a4430696254637a4c6a51354c4467354c6a6730624449314c6a59314c4442734d4377794e5334324e446b354f5777744d6a55754e6a55734d4777774c4330794e5334324e446b354f586f694c7a344b4943413863474630614342705a44306963335a6e587a497a4969426d615778735053496a4e6a493059575a6d4969426b50534a744e4463754f4451734e6a51754d546c734d6a55754e6a55734d4777774c4330794d6934784f5777744e4463754f4451734d4777774c4451334c6a6730624449794c6a45354c4442734d4377744d6a55754e6a56364969382b43694167504842686447676761575139496e4e325a3138794e4349675a6d6c7362443069497a59794e47466d5a6949675a443069625451334c6a67304c4445784e5334304f5777744d6a49754d546b734d4777774c4451334c6a6730624451334c6a67304c4442734d4377744d6a49754d546c734c5449314c6a59314c4442734d4377744d6a55754e6a56364969382b436941384c32632b436a777663335a6e50673d3d266c6162656c436f6c6f723d7768697465)](https://www.modelscope.cn/studios/OpenDataLab/MinerU) [![Colab](https://camo.githubusercontent.com/96889048f8a9014fdeba2a891f97150c6aac6e723f5190236b10215a97ed41f3/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/gist/myhloli/3b3a00a4a0a61577b6c30f989092d20d/mineru_demo.ipynb) [![Paper](https://camo.githubusercontent.com/43ff71669eb46d83f0260b7e6c66528f3d0439b2154bed4eefe9694baedd9906/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f50617065722d61725869762d677265656e)](https://arxiv.org/abs/2409.18839)

[![opendatalab%2FMinerU | Trendshift](https://camo.githubusercontent.com/0641f62e07680e8376ef15eb9294a1e5bc9dcf999b9a5beffd7891da5e9e3f84/68747470733a2f2f7472656e6473686966742e696f2f6170692f62616467652f7265706f7369746f726965732f3131313734)](https://trendshift.io/repositories/11174)

[English](https://github.com/opendatalab/MinerU/blob/master/README.md) | [简体中文](https://github.com/opendatalab/MinerU/blob/master/README_zh-CN.md)

[PDF-Extract-Kit: High-Quality PDF Extraction Toolkit](https://github.com/opendatalab/PDF-Extract-Kit)🔥🔥🔥  
  
[Easier to use: Just grab MinerU Desktop. No coding, no login, just a simple interface and smooth interactions. Enjoy it without any fuss!](https://mineru.net/client?source=github)🚀🚀🚀

👋 join us on [Discord](https://discord.gg/Tdedn9GTXq) and [WeChat](http://mineru.space/s/V85Yl)

# Changelog- 2025/04/12 1.3.2 released
	- Fixed the issue of incompatible dependency package versions when installing in Python 3.13 environment on Windows systems.
	- Optimized memory usage during batch inference.
	- Improved the parsing effect of tables rotated by 90 degrees.
	- Enhanced the parsing accuracy for large tables in financial report samples.
	- Fixed the occasional word concatenation issue in English text areas when OCR language is not specified.(The model needs to be updated)
- 2025/04/08 1.3.1 released, fixed some compatibility issues
	- Supported Python 3.13
	- Made the final adaptation for some outdated Linux systems (e.g., CentOS 7), and no further support will be guaranteed for subsequent versions. [Installation Instructions](https://github.com/opendatalab/MinerU/issues/1004)
- 2025/04/03 1.3.0 released, in this version we made many optimizations and improvements:
	- Installation and compatibility optimization
		- By removing the use of `layoutlmv3` in layout, resolved compatibility issues caused by `detectron2`.
		- Torch version compatibility extended to 2.2~2.6 (excluding 2.5).
		- CUDA compatibility supports 11.8/12.4/12.6/12.8 (CUDA version determined by torch), resolving compatibility issues for some users with 50-series and H-series GPUs.
		- Python compatible versions expanded to 3.10~3.12, solving the problem of automatic downgrade to 0.6.1 during installation in non-3.10 environments.
		- Offline deployment process optimized; no internet connection required after successful deployment to download any model files.
	- Performance optimization
		- By supporting batch processing of multiple PDF files ([script example](https://github.com/opendatalab/MinerU/blob/master/demo/batch_demo.py)), improved parsing speed for small files in batches (compared to version 1.0.1, formula parsing speed increased by over 1400%, overall parsing speed increased by over 500%).
		- Optimized loading and usage of the mfr model, reducing GPU memory usage and improving parsing speed (requires re-execution of the [model download process](https://github.com/opendatalab/MinerU/blob/master/docs/how_to_download_models_en.md) to obtain incremental updates of model files).
		- Optimized GPU memory usage, requiring only a minimum of 6GB to run this project.
		- Improved running speed on MPS devices.
	- Parsing effect optimization
		- Updated the mfr model to `unimernet(2503)`, solving the issue of lost line breaks in multi-line formulas.
	- Usability Optimization
		- By using `paddleocr2torch`, completely replaced the use of the `paddle` framework and `paddleocr` in the project, resolving conflicts between `paddle` and `torch`, as well as thread safety issues caused by the `paddle` framework.
		- Added a real-time progress bar during the parsing process to accurately track progress, making the wait less painful.
2025/03/03 1.2.1 released
- Fixed the impact on punctuation marks during full-width to half-width conversion of letters and numbers
- Fixed caption matching inaccuracies in certain scenarios
- Fixed formula span loss issues in certain scenarios
2025/02/24 1.2.0 released

This version includes several fixes and improvements to enhance parsing efficiency and accuracy:

- **Performance Optimization**
	- Increased classification speed for PDF documents in auto mode.
- **Parsing Optimization**
	- Improved parsing logic for documents containing watermarks, significantly enhancing the parsing results for such documents.
	- Enhanced the matching logic for multiple images/tables and captions within a single page, improving the accuracy of image-text matching in complex layouts.
- **Bug Fixes**
	- Fixed an issue where image/table spans were incorrectly filled into text blocks under certain conditions.
	- Resolved an issue where title blocks were empty in some cases.
2025/01/22 1.1.0 released

In this version we have focused on improving parsing accuracy and efficiency:

- **Model capability upgrade** (requires re-executing the [model download process](https://github.com/opendatalab/MinerU/blob/master/docs/how_to_download_models_en.md) to obtain incremental updates of model files)
	- The layout recognition model has been upgraded to the latest `doclayout_yolo(2501)` model, improving layout recognition accuracy.
	- The formula parsing model has been upgraded to the latest `unimernet(2501)` model, improving formula recognition accuracy.
- **Performance optimization**
	- On devices that meet certain configuration requirements (16GB+ VRAM), by optimizing resource usage and restructuring the processing pipeline, overall parsing speed has been increased by more than 50%.
- **Parsing effect optimization**
	- Added a new heading classification feature (testing version, enabled by default) to the online demo ([mineru.net](https://mineru.net/OpenSourceTools/Extractor)/[huggingface](https://huggingface.co/spaces/opendatalab/MinerU)/[modelscope](https://www.modelscope.cn/studios/OpenDataLab/MinerU)), which supports hierarchical classification of headings, thereby enhancing document structuring.
2025/01/10 1.0.1 released

This is our first official release, where we have introduced a completely new API interface and enhanced compatibility through extensive refactoring, as well as a brand new automatic language identification feature:

- **New API Interface**
	- For the data-side API, we have introduced the Dataset class, designed to provide a robust and flexible data processing framework. This framework currently supports a variety of document formats, including images (.jpg and .png), PDFs, Word documents (.doc and .docx), and PowerPoint presentations (.ppt and .pptx). It ensures effective support for data processing tasks ranging from simple to complex.
	- For the user-side API, we have meticulously designed the MinerU processing workflow as a series of composable Stages. Each Stage represents a specific processing step, allowing users to define new Stages according to their needs and creatively combine these stages to customize their data processing workflows.
- **Enhanced Compatibility**
	- By optimizing the dependency environment and configuration items, we ensure stable and efficient operation on ARM architecture Linux systems.
	- We have deeply integrated with Huawei Ascend NPU acceleration, providing autonomous and controllable high-performance computing capabilities. This supports the localization and development of AI application platforms in China. [Ascend NPU Acceleration](https://github.com/opendatalab/MinerU/blob/master/docs/README_Ascend_NPU_Acceleration_zh_CN.md)
- **Automatic Language Identification**
	- By introducing a new language recognition model, setting the `lang` configuration to `auto` during document parsing will automatically select the appropriate OCR language model, improving the accuracy of scanned document parsing.
2024/11/22 0.10.0 released

Introducing hybrid OCR text extraction capabilities:

- Significantly improved parsing performance in complex text distribution scenarios such as dense formulas, irregular span regions, and text represented by images.
- Combines the dual advantages of accurate content extraction and faster speed in text mode, and more precise span/line region recognition in OCR mode.
2024/11/15 0.9.3 released

Integrated [RapidTable](https://github.com/RapidAI/RapidTable) for table recognition, improving single-table parsing speed by more than 10 times, with higher accuracy and lower GPU memory usage.

2024/11/06 0.9.2 released

Integrated the [StructTable-InternVL2-1B](https://huggingface.co/U4R/StructTable-InternVL2-1B) model for table recognition functionality.

2024/10/31 0.9.0 released

This is a major new version with extensive code refactoring, addressing numerous issues, improving performance, reducing hardware requirements, and enhancing usability:

- Refactored the sorting module code to use [layoutreader](https://github.com/ppaanngggg/layoutreader) for reading order sorting, ensuring high accuracy in various layouts.
- Refactored the paragraph concatenation module to achieve good results in cross-column, cross-page, cross-figure, and cross-table scenarios.
- Refactored the list and table of contents recognition functions, significantly improving the accuracy of list blocks and table of contents blocks, as well as the parsing of corresponding text paragraphs.
- Refactored the matching logic for figures, tables, and descriptive text, greatly enhancing the accuracy of matching captions and footnotes to figures and tables, and reducing the loss rate of descriptive text to near zero.
- Added multi-language support for OCR, supporting detection and recognition of 84 languages. For the list of supported languages, see [OCR Language Support List](https://paddlepaddle.github.io/PaddleOCR/latest/en/ppocr/blog/multi_languages.html#5-support-languages-and-abbreviations).
- Added memory recycling logic and other memory optimization measures, significantly reducing memory usage. The memory requirement for enabling all acceleration features except table acceleration (layout/formula/OCR) has been reduced from 16GB to 8GB, and the memory requirement for enabling all acceleration features has been reduced from 24GB to 10GB.
- Optimized configuration file feature switches, adding an independent formula detection switch to significantly improve speed and parsing results when formula detection is not needed.
- Integrated [PDF-Extract-Kit 1.0](https://github.com/opendatalab/PDF-Extract-Kit):
	- Added the self-developed `doclayout_yolo` model, which speeds up processing by more than 10 times compared to the original solution while maintaining similar parsing effects, and can be freely switched with `layoutlmv3` via the configuration file.
	- Upgraded formula parsing to `unimernet 0.2.1`, improving formula parsing accuracy while significantly reducing memory usage.
	- Due to the repository change for `PDF-Extract-Kit 1.0`, you need to re-download the model. Please refer to [How to Download Models](https://github.com/opendatalab/MinerU/blob/master/docs/how_to_download_models_en.md) for detailed steps.
2024/09/27 Version 0.8.1 released

Fixed some bugs, and providing a [localized deployment version](https://github.com/opendatalab/MinerU/blob/master/projects/web_demo/README.md) of the [online demo](https://opendatalab.com/OpenSourceTools/Extractor/PDF/) and the [front-end interface](https://github.com/opendatalab/MinerU/blob/master/projects/web/README.md).

2024/09/09 Version 0.8.0 released

Supporting fast deployment with Dockerfile, and launching demos on Huggingface and Modelscope.

2024/08/30 Version 0.7.1 released

Add paddle tablemaster table recognition option

2024/08/09 Version 0.7.0b1 released

Simplified installation process, added table recognition functionality

2024/08/01 Version 0.6.2b1 released

Optimized dependency conflict issues and installation documentation

2024/07/05 Initial open-source release

## Table of Contents1. [MinerU](https://github.com/opendatalab/#mineru)
	- [Project Introduction](https://github.com/opendatalab/#project-introduction)
	- [Key Features](https://github.com/opendatalab/#key-features)
	- [Quick Start](https://github.com/opendatalab/#quick-start)
		- [Online Demo](https://github.com/opendatalab/#online-demo)
		- [Quick CPU Demo](https://github.com/opendatalab/#quick-cpu-demo)
		- [Using GPU](https://github.com/opendatalab/#using-gpu)
		- [Using NPU](https://github.com/opendatalab/#using-npu)
	- [Usage](https://github.com/opendatalab/#usage)
		- [Command Line](https://github.com/opendatalab/#command-line)
		- [API](https://github.com/opendatalab/#api)
		- [Deploy Derived Projects](https://github.com/opendatalab/#deploy-derived-projects)
		- [Development Guide](https://github.com/opendatalab/#development-guide)
2. [TODO](https://github.com/opendatalab/#todo)
3. [Known Issues](https://github.com/opendatalab/#known-issues)
4. [FAQ](https://github.com/opendatalab/#faq)
5. [All Thanks To Our Contributors](https://github.com/opendatalab/#all-thanks-to-our-contributors)
6. [License Information](https://github.com/opendatalab/#license-information)
7. [Acknowledgments](https://github.com/opendatalab/#acknowledgments)
8. [Citation](https://github.com/opendatalab/#citation)
9. [Star History](https://github.com/opendatalab/#star-history)
10. [Magic-doc](https://github.com/opendatalab/#magic-doc)
11. [Magic-html](https://github.com/opendatalab/#magic-html)
12. [Links](https://github.com/opendatalab/#links)

# MinerU## Project IntroductionMinerU is a tool that converts PDFs into machine-readable formats (e.g., markdown, JSON), allowing for easy extraction into any format. MinerU was born during the pre-training process of [InternLM](https://github.com/InternLM/InternLM). We focus on solving symbol conversion issues in scientific literature and hope to contribute to technological development in the era of large models. Compared to well-known commercial products, MinerU is still young. If you encounter any issues or if the results are not as expected, please submit an issue on [issue](https://github.com/opendatalab/MinerU/issues) and **attach the relevant PDF**.

pdf\_zh\_cn.mp4<video src="https://private-user-images.githubusercontent.com/11393164/351177226-4bea02c9-6d54-4cd6-97ed-dff14340982c.mp4?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDQ2NzQyMTIsIm5iZiI6MTc0NDY3MzkxMiwicGF0aCI6Ii8xMTM5MzE2NC8zNTExNzcyMjYtNGJlYTAyYzktNmQ1NC00Y2Q2LTk3ZWQtZGZmMTQzNDA5ODJjLm1wND9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTA0MTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwNDE0VDIzMzgzMlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTBkNGM3ZDI4ZjQ1MTU1NTliYmJhMzI1ZjE3OThlOTM4MDMxNmJiZmU5MjExYzU5MjhiMWQ1ZDdhZWY0ZjQwZjAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.MasRGGHQBjy8rtqcgbtDA88dvcySUfHOA4w40ygaf8Y" data-canonical-src="https://private-user-images.githubusercontent.com/11393164/351177226-4bea02c9-6d54-4cd6-97ed-dff14340982c.mp4?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDQ2NzQyMTIsIm5iZiI6MTc0NDY3MzkxMiwicGF0aCI6Ii8xMTM5MzE2NC8zNTExNzcyMjYtNGJlYTAyYzktNmQ1NC00Y2Q2LTk3ZWQtZGZmMTQzNDA5ODJjLm1wND9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTA0MTQlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwNDE0VDIzMzgzMlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTBkNGM3ZDI4ZjQ1MTU1NTliYmJhMzI1ZjE3OThlOTM4MDMxNmJiZmU5MjExYzU5MjhiMWQ1ZDdhZWY0ZjQwZjAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.MasRGGHQBjy8rtqcgbtDA88dvcySUfHOA4w40ygaf8Y" controls="controls" muted="muted" class="d-block rounded-bottom-2 border-top width-fit" style="max-height:640px; min-height: 200px"></video>

## Key Features- Remove headers, footers, footnotes, page numbers, etc., to ensure semantic coherence.
- Output text in human-readable order, suitable for single-column, multi-column, and complex layouts.
- Preserve the structure of the original document, including headings, paragraphs, lists, etc.
- Extract images, image descriptions, tables, table titles, and footnotes.
- Automatically recognize and convert formulas in the document to LaTeX format.
- Automatically recognize and convert tables in the document to HTML format.
- Automatically detect scanned PDFs and garbled PDFs and enable OCR functionality.
- OCR supports detection and recognition of 84 languages.
- Supports multiple output formats, such as multimodal and NLP Markdown, JSON sorted by reading order, and rich intermediate formats.
- Supports various visualization results, including layout visualization and span visualization, for efficient confirmation of output quality.
- Supports running in a pure CPU environment, and also supports GPU(CUDA)/NPU(CANN)/MPS acceleration
- Compatible with Windows, Linux, and Mac platforms.

## Quick StartIf you encounter any installation issues, please first consult the [FAQ](https://github.com/opendatalab/#faq).  
If the parsing results are not as expected, refer to the [Known Issues](https://github.com/opendatalab/#known-issues).  
There are three different ways to experience MinerU:

- [Online Demo (No Installation Required)](https://github.com/opendatalab/#online-demo)
- [Quick CPU Demo (Windows, Linux, Mac)](https://github.com/opendatalab/#quick-cpu-demo)
- Accelerate inference by using CUDA/CANN/MPS
	- [Linux/Windows + CUDA](https://github.com/opendatalab/#Using-GPU)
	- [Linux + CANN](https://github.com/opendatalab/#using-npu)
	- [MacOS + MPS](https://github.com/opendatalab/#using-mps)
> [!WARNING]
> Pre-installation Notice—Hardware and Software Environment Support

<table><tbody><tr><td colspan="3" rowspan="2">Operating System</td></tr><tr><td>Linux after 2019</td><td>Windows 10 / 11</td><td>macOS 11+</td></tr><tr><td colspan="3">CPU</td><td>x86_64 / arm64</td><td>x86_64(unsupported ARM Windows)</td><td>x86_64 / arm64</td></tr><tr><td colspan="3">Memory Requirements</td><td colspan="3">16GB or more, recommended 32GB+</td></tr><tr><td colspan="3">Storage Requirements</td><td colspan="3">20GB or more, with a preference for SSD</td></tr><tr><td colspan="3">Python Version</td><td colspan="3">&gt;=3.10</td></tr><tr><td colspan="3">Nvidia Driver Version</td><td>latest (Proprietary Driver)</td><td>latest</td><td>None</td></tr><tr><td colspan="3">CUDA Environment</td><td>11.8/12.4/12.6/12.8</td><td>11.8/12.4/12.6/12.8</td><td>None</td></tr><tr><td colspan="3">CANN Environment(NPU support)</td><td>8.0+(Ascend 910b)</td><td>None</td><td>None</td></tr><tr><td rowspan="2">GPU/MPS Hardware Support List</td><td colspan="2">GPU VRAM 6GB or more</td><td colspan="2">All GPUs with Tensor Cores produced from Volta(2017) onwards.<br>More than 6GB VRAM</td><td rowspan="2">apple slicon</td></tr></tbody></table>

### Online DemoSynced with dev branch updates:

[![OpenDataLab](https://camo.githubusercontent.com/7823e1efdb5fc27ca8bc72a464bf422be18f6ad3f3036c72217f21c1d1e641e3/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f44656d6f5f6f6e5f4f70656e446174614c61622d626c75653f6c6f676f3d646174613a696d6167652f7376672b786d6c3b6261736536342c50484e325a79423361575230614430694d544d304969426f5a576c6e61485139496a457a4e43496765473173626e4d39496d6830644841364c79393364336375647a4d7562334a6e4c7a49774d44417663335a6e496a3438634746306143426b50534a744d5449794c446c6a4d4377314c5451734f5330354c446c7a4c546b744e4330354c546b734e4330354c446b744f5377354c4451734f537735656949675a6d6c736244306964584a734b434e684b534976506a78775958526f49475139496d30784d6a49734f574d774c4455744e4377354c546b734f584d744f5330304c546b744f5377304c546b734f5330354c446b734e4377354c446c364969426d615778735053496a4d4445774d5441784969382b50484268644767675a44306962546b784c444534597a41734e5330304c446b744f537735637930354c5451744f5330354c4451744f5377354c546b734f5377304c446b734f586f6949475a7062477739496e56796243676a59696b694c7a3438634746306143426b50534a744f5445734d54686a4d4377314c5451734f5330354c446c7a4c546b744e4330354c546b734e4330354c446b744f5377354c4451734f537735656949675a6d6c7362443069497a41784d4445774d534976506a78775958526f49475a7062477774636e56735a5430695a585a6c626d396b5a43496759327870634331796457786c50534a6c646d56756232526b4969426b50534a744d7a6b734e6a4a6a4d4377784e6977344c444d774c4449774c444d344c4463744e6977784d6930784e6977784d6930794e6c59304f574d774c5451734d7930334c4459744f4777304e6930784d6d4d314c5445734d5445734d7977784d537734646a4d78597a41734d7a63744d7a41734e6a59744e6a59734e6a59744d7a63734d4330324e69307a4d4330324e6930324e6c59304e6d4d774c5451734d7930334c4459744f4777794d433032597a55744d5377784d53777a4c4445784c4468324d6a4636625330794f537732597a41734d5459734e69777a4d4377784e7977304d43777a4c4445734e5377784c4467734d5377314c4441734d5441744d5377784e53307a517a4d334c446b314c4449354c4463354c4449354c445979566a5179624330784f537731646a4977656949675a6d6c736244306964584a734b434e6a4b534976506a78775958526f49475a7062477774636e56735a5430695a585a6c626d396b5a43496759327870634331796457786c50534a6c646d56756232526b4969426b50534a744d7a6b734e6a4a6a4d4377784e6977344c444d774c4449774c444d344c4463744e6977784d6930784e6977784d6930794e6c59304f574d774c5451734d7930334c4459744f4777304e6930784d6d4d314c5445734d5445734d7977784d537734646a4d78597a41734d7a63744d7a41734e6a59744e6a59734e6a59744d7a63734d4330324e69307a4d4330324e6930324e6c59304e6d4d774c5451734d7930334c4459744f4777794d433032597a55744d5377784d53777a4c4445784c4468324d6a4636625330794f537732597a41734d5459734e69777a4d4377784e7977304d43777a4c4445734e5377784c4467734d5377314c4441734d5441744d5377784e53307a517a4d334c446b314c4449354c4463354c4449354c445979566a5179624330784f537731646a4977656949675a6d6c7362443069497a41784d4445774d534976506a786b5a575a7a506a78736157356c59584a48636d466b61575675644342705a4430695953496765444539496a6730496942354d5430694e44456949486779505349334e53496765544939496a45794d4349675a334a685a476c6c626e5256626d6c30637a306964584e6c636c4e7759574e6c5432355663325569506a787a6447397749484e3062334174593239736233493949694e6d5a6d59694c7a343863335276634342765a6d5a7a5a585139496a456949484e3062334174593239736233493949694d795a544a6c4d6d55694c7a34384c327870626d5668636b6479595752705a573530506a78736157356c59584a48636d466b61575675644342705a4430695969496765444539496a6730496942354d5430694e44456949486779505349334e53496765544939496a45794d4349675a334a685a476c6c626e5256626d6c30637a306964584e6c636c4e7759574e6c5432355663325569506a787a6447397749484e3062334174593239736233493949694e6d5a6d59694c7a343863335276634342765a6d5a7a5a585139496a456949484e3062334174593239736233493949694d795a544a6c4d6d55694c7a34384c327870626d5668636b6479595752705a573530506a78736157356c59584a48636d466b61575675644342705a4430695979496765444539496a6730496942354d5430694e44456949486779505349334e53496765544939496a45794d4349675a334a685a476c6c626e5256626d6c30637a306964584e6c636c4e7759574e6c5432355663325569506a787a6447397749484e3062334174593239736233493949694e6d5a6d59694c7a343863335276634342765a6d5a7a5a585139496a456949484e3062334174593239736233493949694d795a544a6c4d6d55694c7a34384c327870626d5668636b6479595752705a573530506a77765a47566d637a34384c334e325a7a343d266c6162656c436f6c6f723d7768697465)](https://mineru.net/OpenSourceTools/Extractor?source=github) [![HuggingFace](https://camo.githubusercontent.com/545f0fe2269e1589381626b5ba6a4c447c6c043290697784879410280c85a90b/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f44656d6f5f6f6e5f48756767696e67466163652d79656c6c6f772e7376673f6c6f676f3d646174613a696d6167652f706e673b6261736536342c6956424f5277304b47676f414141414e5355684555674141414638414141425943414d414141436b6c39742f414141416b31424d5645564863457a2f6e51762f6e51762f6e51722f6e51762f6e51722f6e51762f6e51762f6e51722f7752662f7478542f7067372f7952722f7242442f7a527a2f6e67762f6f417a2f7a687a2f6e77762f7478542f6e67762f3042332b7a427a2f6e51762f3068372f77786e2f7652622f7468586b7569542f7278482f7078442f6f677a637179662f6e5176546c537a2f637a43786b79372f536a6966646a542f4d6a332b4d6a33774d6a313561546e444e7a2b445344395254554273503046524f3051364f305779497845494141414147485253546c4d414442387a535746336b7244447738544a314e625835656676386666392f66784b444a3975414141474b6b6c45515652343275325a3633716a4f41794743345277434f6642324a41477172536232576e54772f316633556157635347594e4b5464662f502b6d4f6b5472452b794a42756c7666764c543241357275656e61564879496b7333336e706c2f364334732f5a4c414d3435534f692f3146745a5079467572314f596f66425833773764353442786d2b453864622b6e4472313274746d45535a347a6c75644a4547355337544f373259506c4b5a4679452b594359554a54425a734d694e53355364374e6c446d4b4d324567324a516738617762676c667167626841726a786b533764677032524836686339414d4c645a5955745a4e35444a72346d6f6c433842664b72456b504b456e45566a4c62675731664c7937375a564f4a61676f49634c496c2b497861515a476a6958353937486f704635436b6158564d444f395079697833414656336b77346c514c436248754d6f767a3846616c6c626351494a35546130766b7339526e6f6c62434b383442746a4b5253357541343368596f5a634f424749473245706276364376465651386d386c6f683636574e7953736e4e3768744c35384c4e702b4e5854382f506858694258504d6a4c5378747770385739662f31416e6752696572426b412b6b6b2f497055534f654b42797a6e3879336b41414166682f2f306f58675634726f486d2f6b7a3445327a2f2f7a5263332f6c6777427a624d326d4a7851456135707167583764314c306874726878374c4b784f5a6c4b627763415779454f577159534938595074674451566a7042356e76614861536e426151534436687765446938506f737844362f50543039595933785141374c5443544b6659582b5148704130474363716d454876722f6379664b5154457577676273326b50784a454230694e6a664a63435450796f63782b413067726948536d4144694339316f4e4756774a363952756459653635764a6d6f716670756c306c727158616457306a464b4835424b77416543712b44656e37732b337a66524a7a4136312f556a2f39482f567a4c4b5478396a46505064586565502b4c37574576444c414b41496f46386250544b54302b544d37573865506a33527a2f596e336b4f41703266314b663057656f6e7937706e2f6350796476685159562b65464f666d4f753756422f5669506533342f454e33524648592f7952755438646443744d50482f4d6342415435732b765264652f676632632f7350736a4c4b2b6d354942514635744f2b683274546c42476e50363639334a6473766f666a4f506e6e45486b6832546e562f583166426c3953357a7277757746384e467241564a567743415054653867614a6c6f6d716c7030707634506a6e3938744a2f742f664c2b2b36756e705231594743326e2f4b436f613074544c6f4b6945655550446c39346e6a2b352f5476332f6554357642513630583153306f5a722b49575252384c64687537416c4c6a5049536c4a634f397672466f746b793953707a446571756c7745697235626559416330523744394b533144587661306a68595244586f4578506463367977354753686b5a58653951644f2f754f76486f66786a72562f544e5336694d4a532b3454635354676b396e3561674a64425162422f2f4966462f48707650743354626937623649364b305237327036616a7279454a72454e57326262655655476a66676f616c73344c3434336337424545346d4a4f32537062526e67785172414b527564527a4751386a564f4c327144566a6a49384b3167633354494a354b69465a31712b67647341525042344e515334416a77565374373244536f584e794f57557255356d51396e5259796a703839586f376f52493642676139514e54316d512f7074614a7135542f37576367415a7977522f586c5047415544646574334c452b71533054492b672b614a55384d49716a6f304b78384c792b6d61784c6a4a6d6a51313872413059436b784c5162555a50315771646d7951474a4c556d37566e5146716f646d5853716d527264567071647a6b354c766d76677445635738504d476461533233454f577944566241435a7a554a5061714d626a44787041335172676c3041696b696d474462716d79543850384e4f596971726c64463872582b594e37546f705834556f4875534359593763675834674877636c514b6c317a6878305448662b7443415556616c7a6a493757673945687074726b496366494a6a41393465764f6e384232654861567a7642726e6c32696730536f36687650617a304947634f7654487655496c45322b70727141784c5351785a6c55327374716c314e7143434c644969494e2f693144424548556f456c4d3964427261766269416e4b716770693449426b772b75745350496f42696a44584a6970535656374d704f454a55416335516d6d33426e554e2b7733687465456965594b66525a53495563584b4d5666307535774434457773554e56765a4f745554374132476b6666486a42795770487176524259725456373261366a387a5a3657304454453836486e3034626d795758335269395748375a55365137682b5a486f306e4855416373517656685852445a484368776979692f686e50754f735345463645786b336f365939445431655a2b36634153586b3259396b2b36454f514d44476d3657424b3130774f514a43427772656e383663505057556352416e54566a476355314c4267733946555269582f6536343739795a634c7743426d54786961774577724f636c6575753132743374624c762f4e34524c594942685965786d3746636e344f4a636e302b7a632b73382f5666506564645a4841474e365454386547637a4864522f477473312f4d7a446b54687232337a71725666414d465433334e7831524a7378316b357a7557494c4c6e472f7673482b46763544344e5456637031477a6f384141414141456c46546b5375516d4343266c6162656c436f6c6f723d7768697465)](https://huggingface.co/spaces/opendatalab/MinerU) [![ModelScope](https://camo.githubusercontent.com/cefa3a0aa0b04b14356ea9c36d5556034602ff2e616f4699c7267cbbfaed783d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f44656d6f5f6f6e5f4d6f64656c53636f70652d707572706c653f6c6f676f3d646174613a696d6167652f7376672b786d6c3b6261736536342c50484e325a79423361575230614430694d6a497a4969426f5a576c6e61485139496a49774d43496765473173626e4d39496d6830644841364c79393364336375647a4d7562334a6e4c7a49774d44417663335a6e496a344b436941385a7a344b4943413864476c306247552b544746355a5849674d54777664476c306247552b43694167504842686447676761575139496e4e325a3138784e4349675a6d6c7362443069497a59794e47466d5a6949675a443069625441734f446b754f4452734d6a55754e6a55734d4777774c4449314c6a59304f546b35624330794e5334324e537777624441734c5449314c6a59304f546b356569497650676f67494478775958526f49476c6b50534a7a646d64664d54556949475a706247773949694d324d6a52685a6d596949475139496d30354f5334784e4377784d5455754e446c734d6a55754e6a55734d4777774c4449314c6a5931624330794e5334324e537777624441734c5449314c6a59316569497650676f67494478775958526f49476c6b50534a7a646d64664d54596949475a706247773949694d324d6a52685a6d596949475139496d30784e7a59754d446b734d5451784c6a4530624330794e5334324e446b354f537777624441734d6a49754d546c734e4463754f4451734d4777774c4330304e7934344e4777744d6a49754d546b734d4777774c4449314c6a59316569497650676f67494478775958526f49476c6b50534a7a646d64664d54636949475a706247773949694d7a4e6d4e6d5a44456949475139496d30784d6a51754e7a6b734f446b754f4452734d6a55754e6a55734d4777774c4449314c6a59304f546b35624330794e5334324e537777624441734c5449314c6a59304f546b356569497650676f67494478775958526f49476c6b50534a7a646d64664d54676949475a706247773949694d7a4e6d4e6d5a44456949475139496d30774c4459304c6a4535624449314c6a59314c4442734d4377794e5334324e5777744d6a55754e6a55734d4777774c4330794e5334324e586f694c7a344b4943413863474630614342705a44306963335a6e587a45354969426d615778735053496a4e6a493059575a6d4969426b50534a744d546b344c6a49344c4467354c6a6730624449314c6a59304f546b354c4442734d4377794e5334324e446b354f5777744d6a55754e6a51354f546b734d4777774c4330794e5334324e446b354f586f694c7a344b4943413863474630614342705a44306963335a6e587a49774969426d615778735053496a4d7a5a6a5a6d51784969426b50534a744d546b344c6a49344c4459304c6a4535624449314c6a59304f546b354c4442734d4377794e5334324e5777744d6a55754e6a51354f546b734d4777774c4330794e5334324e586f694c7a344b4943413863474630614342705a44306963335a6e587a49784969426d615778735053496a4e6a493059575a6d4969426b50534a744d5455774c6a51304c445179624441734d6a49754d546c734d6a55754e6a51354f546b734d4777774c4449314c6a5931624449794c6a45354c4442734d4377744e4463754f4452734c5451334c6a67304c4442364969382b43694167504842686447676761575139496e4e325a3138794d6949675a6d6c7362443069497a4d3259325a6b4d5349675a4430696254637a4c6a51354c4467354c6a6730624449314c6a59314c4442734d4377794e5334324e446b354f5777744d6a55754e6a55734d4777774c4330794e5334324e446b354f586f694c7a344b4943413863474630614342705a44306963335a6e587a497a4969426d615778735053496a4e6a493059575a6d4969426b50534a744e4463754f4451734e6a51754d546c734d6a55754e6a55734d4777774c4330794d6934784f5777744e4463754f4451734d4777774c4451334c6a6730624449794c6a45354c4442734d4377744d6a55754e6a56364969382b43694167504842686447676761575139496e4e325a3138794e4349675a6d6c7362443069497a59794e47466d5a6949675a443069625451334c6a67304c4445784e5334304f5777744d6a49754d546b734d4777774c4451334c6a6730624451334c6a67304c4442734d4377744d6a49754d546c734c5449314c6a59314c4442734d4377744d6a55754e6a56364969382b436941384c32632b436a777663335a6e50673d3d266c6162656c436f6c6f723d7768697465)](https://www.modelscope.cn/studios/OpenDataLab/MinerU)

### Quick CPU Demo#### 1\. Install magic-pdfconda create -n mineru 'python>=3.10' -y
conda activate mineru
pip install -U "magic-pdf\[full\]"

#### 2\. Download model weight filesRefer to [How to Download Model Files](https://github.com/opendatalab/MinerU/blob/master/docs/how_to_download_models_en.md) for detailed instructions.

#### 3\. Modify the Configuration File for Additional ConfigurationAfter completing the [2\. Download model weight files](https://github.com/opendatalab/#2-download-model-weight-files) step, the script will automatically generate a `magic-pdf.json` file in the user directory and configure the default model path. You can find the `magic-pdf.json` file in your 【user directory】.

> [!TIP]
> The user directory for Windows is "C:\Users\username", for Linux it is "/home/username", and for macOS it is "/Users/username".

You can modify certain configurations in this file to enable or disable features, such as table recognition:

> [!NOTE]
> If the following items are not present in the JSON, please manually add the required items and remove the comment content (standard JSON does not support comments).

{
    // other config
    "layout-config": {
        "model": "doclayout\_yolo" 
    },
    "formula-config": {
        "mfd\_model": "yolo\_v8\_mfd",
        "mfr\_model": "unimernet\_small",
        "enable": true  // The formula recognition feature is enabled by default. If you need to disable it, please change the value here to "false".
    },
    "table-config": {
        "model": "rapid\_table", 
        "sub\_model": "slanet\_plus",
        "enable": true, // The table recognition feature is enabled by default. If you need to disable it, please change the value here to "false".
        "max\_time": 400
    }
}

### Using GPUIf your device supports CUDA and meets the GPU requirements of the mainline environment, you can use GPU acceleration. Please select the appropriate guide based on your system:

- [Ubuntu 22.04 LTS + GPU](https://github.com/opendatalab/MinerU/blob/master/docs/README_Ubuntu_CUDA_Acceleration_en_US.md)
- [Windows 10/11 + GPU](https://github.com/opendatalab/MinerU/blob/master/docs/README_Windows_CUDA_Acceleration_en_US.md)
- Quick Deployment with Docker
> [!IMPORTANT]
> Docker requires a GPU with at least 6GB of VRAM, and all acceleration features are enabled by default.

wget https://github.com/opendatalab/MinerU/raw/master/docker/global/Dockerfile -O Dockerfile
docker build -t mineru:latest .
docker run -it --name mineru --gpus=all mineru:latest /bin/bash -c "echo 'source /opt/mineru\_venv/bin/activate' >> ~/.bashrc && exec bash"
magic-pdf --help

### Using NPUIf your device has NPU acceleration hardware, you can follow the tutorial below to use NPU acceleration:

[Ascend NPU Acceleration](https://github.com/opendatalab/MinerU/blob/master/docs/README_Ascend_NPU_Acceleration_zh_CN.md)

### Using MPSIf your device uses Apple silicon chips, you can enable MPS acceleration for your tasks.

You can enable MPS acceleration by setting the `device-mode` parameter to `mps` in the `magic-pdf.json` configuration file.

{
    // other config
    "device-mode": "mps"
}

## Usage### Command Line[Using MinerU via Command Line](https://mineru.readthedocs.io/en/latest/user_guide/usage/command_line.html)

> [!TIP]
> For more information about the output files, please refer to the Output File Description.

### API[Using MinerU via Python API](https://mineru.readthedocs.io/en/latest/user_guide/usage/api.html)

### Deploy Derived ProjectsDerived projects include secondary development projects based on MinerU by project developers and community developers,  
such as application interfaces based on Gradio, RAG based on llama, web demos similar to the official website, lightweight multi-GPU load balancing client/server ends, etc. These projects may offer more features and a better user experience.  
For specific deployment methods, please refer to the [Derived Project README](https://github.com/opendatalab/MinerU/blob/master/projects/README.md)

### Development GuideTODO

# TODO- [x] Reading order based on the model
- [x] Recognition of `index` and `list` in the main text
- [x] Table recognition
- [x] Heading Classification
- [ ] Code block recognition in the main text
- [ ] [Chemical formula recognition](https://github.com/opendatalab/MinerU/blob/master/docs/chemical_knowledge_introduction/introduction.pdf)
- [ ] Geometric shape recognition

# Known Issues- Reading order is determined by the model based on the spatial distribution of readable content, and may be out of order in some areas under extremely complex layouts.
- Vertical text is not supported.
- Tables of contents and lists are recognized through rules, and some uncommon list formats may not be recognized.
- Code blocks are not yet supported in the layout model.
- Comic books, art albums, primary school textbooks, and exercises cannot be parsed well.
- Table recognition may result in row/column recognition errors in complex tables.
- OCR recognition may produce inaccurate characters in PDFs of lesser-known languages (e.g., diacritical marks in Latin script, easily confused characters in Arabic script).
- Some formulas may not render correctly in Markdown.

# FAQ[FAQ in Chinese](https://github.com/opendatalab/MinerU/blob/master/docs/FAQ_zh_cn.md)

[FAQ in English](https://github.com/opendatalab/MinerU/blob/master/docs/FAQ_en_us.md)

# All Thanks To Our Contributors[![](https://camo.githubusercontent.com/f2f36dab4b87e401a086922c95bc34123aef3eee5dad301297395dfb0eb80bf6/68747470733a2f2f636f6e747269622e726f636b732f696d6167653f7265706f3d6f70656e646174616c61622f4d696e657255)](https://github.com/opendatalab/MinerU/graphs/contributors)

# License Information[LICENSE.md](https://github.com/opendatalab/MinerU/blob/master/LICENSE.md)

This project currently uses PyMuPDF to achieve advanced functionality. However, since it adheres to the AGPL license, it may impose restrictions on certain usage scenarios. In future iterations, we plan to explore and replace it with a more permissive PDF processing library to enhance user-friendliness and flexibility.

# Acknowledgments- [PDF-Extract-Kit](https://github.com/opendatalab/PDF-Extract-Kit)
- [DocLayout-YOLO](https://github.com/opendatalab/DocLayout-YOLO)
- [StructEqTable](https://github.com/UniModal4Reasoning/StructEqTable-Deploy)
- [RapidTable](https://github.com/RapidAI/RapidTable)
- [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)
- [RapidOCR](https://github.com/RapidAI/RapidOCR)
- [PaddleOCR2Pytorch](https://github.com/frotms/PaddleOCR2Pytorch)
- [PyMuPDF](https://github.com/pymupdf/PyMuPDF)
- [layoutreader](https://github.com/ppaanngggg/layoutreader)
- [fast-langdetect](https://github.com/LlmKira/fast-langdetect)
- [pdfminer.six](https://github.com/pdfminer/pdfminer.six)

# Citation@misc{wang2024mineruopensourcesolutionprecise,
      title\={MinerU: An Open-Source Solution for Precise Document Content Extraction}, 
      author\={Bin Wang and Chao Xu and Xiaomeng Zhao and Linke Ouyang and Fan Wu and Zhiyuan Zhao and Rui Xu and Kaiwen Liu and Yuan Qu and Fukai Shang and Bo Zhang and Liqun Wei and Zhihao Sui and Wei Li and Botian Shi and Yu Qiao and Dahua Lin and Conghui He},
      year\={2024},
      eprint\={2409.18839},
      archivePrefix\={arXiv},
      primaryClass\={cs.CV},
      url\={https://arxiv.org/abs/2409.18839}, 
}

@article{he2024opendatalab,
  title\={Opendatalab: Empowering general artificial intelligence with open datasets},
  author\={He, Conghui and Li, Wei and Jin, Zhenjiang and Xu, Chao and Wang, Bin and Lin, Dahua},
  journal\={arXiv preprint arXiv:2407.13773},
  year\={2024}
}

# Star History  ![Star History Chart](https://camo.githubusercontent.com/af489eff58355c5050a68fa265c6f5bf8ea810b04db14f2e095700001c832e59/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d6f70656e646174616c61622f4d696e65725526747970653d44617465)

# Magic-doc[Magic-Doc](https://github.com/InternLM/magic-doc) Fast speed ppt/pptx/doc/docx/pdf extraction tool

# Magic-html[Magic-HTML](https://github.com/opendatalab/magic-html) Mixed web page extraction tool

# Links- [LabelU (A Lightweight Multi-modal Data Annotation Tool)](https://github.com/opendatalab/labelU)
- [LabelLLM (An Open-source LLM Dialogue Annotation Platform)](https://github.com/opendatalab/LabelLLM)
- [PDF-Extract-Kit (A Comprehensive Toolkit for High-Quality PDF Content Extraction)](https://github.com/opendatalab/PDF-Extract-Kit)


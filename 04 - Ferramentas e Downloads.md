Com o tempo diversas ferramentas foram criadas para facilitar a vida de quem pretende construir um hackintosh seja leigos ou usuários avançados. Nessa seção estarei listando as ferramentas mais comuns com uma breve explicação.

## Bootloaders

Para usar o Mac OS X é necessário a instalação de um bootloader, que fará seu computador parecer com um Mac real.

[**Chimera**](http://www.tonymacx86.com/downloads.php?do=file&id=246) - É apenas uma ramificação supostamente aprimorada do Chameleon.

- **OBS**: Esse software é desenvolvido pelo pessoal do fórum Tonymac de forma fechada para a comunidade e só terá suporte no fórum de seus criadores.

---

**[Chameleon](http://www.insanelymac.com/forum/files/file/59-chameleon-23-svn/)** - É o bootloader mais amigavél aos usuários, seja pela sua simplicidade ou pela facilidade de configuração. Caso encontre algum problema, será extremamente mais fácil obter suporte em diversos fóruns, por ser amplamente utilizado.

= **OBS**: Indicado para placas-mãe antigas ou que não possuem suporte a UEFI.

[**Clover**](http://sourceforge.net/projects/cloverefiboot/) - Possui inúmeras funcionalidades e é de longe o bootloader mais rápido e seguro se comparado com os demais, além de poder ser instalado em modo UEFI ou Legacy. Sua única desvantagem seria as suas complexas configurações, que pode assustar muitos usuários acostumados com a simplicidade do Chameleon/Chimera.

Mesmo assim a comunidade tem migrado para o Clover a passos largos e o suporte tem aumentado cada vez mais.

- **OBS**: Indicado para placas-mãe que possuem suporte a UEFI

## Bootloaders Wizards

Após instalarmos o bootloader é necessário configurá-lo para que ele possa injetar a SMBIOS para identificação do seu computador, injetar a DSDT para que seu hardware funcione de forma eficiente, gerenciar o consumo de energia e logicamente carregar nosso Mac OS X.

**[Chameleon Wizard](http://www.hackintoshosx.com/files/file/4132-chameleon-wizard/)** - É um assistente bem inuítivo. Em uma única aba você poderá configurar a inicialização do seu bootloader e nas demais abas poderá editar sua SMBIOS, aplicar patchs na DSDT e instalar temas no bootloader. 

- **OBS**: Compatível com o Chimera.

**[Clover Configurator](http://www.hackintoshosx.com/files/file/49-clover-configurator/)** - Assistente bem complexo com suas várias seções de configurações. Pode ser complicado no início, principalmente a seção de Fixes para DSDT mas felizmente existe uma [Wiki em inglês](http://clover-wiki.zetam.org/Home), bem detalhada para ajudá-lo a configurar o bootloader.

Também oferece suporte a temas, edição de SMBIOS além da injeção de kexts na inicialização do bootloader, que na minha opinião, é um excelente recurso, na qual poderá reinstalar ou atualizar o Mac OS X, sem perder as configurações ou kexts instaladas.

## Instaladores de Kexts

Instalar kexts pode parecer fácil mas senão forem instaladas de forma correta, poderá causar problemas como Kernel Panic.

Não basta apenas arrastá-las para o pasta `/System/Library/Extensions`. É necessário abrir o Utilitário de Disco para reparar as permissões e só então o kernel poderá atualizar o  cache com as kexts instaladas.

Achou complicado? Por isso mesmo que os instaladores de kexts foram criados, para nos poupar de todo esse trabalho.

[Kext Utility](http://www.hackintoshosx.com/files/file/3640-kext-utility-for-mavericks/) - Instalador bem simples bastando apenas arrastar as kexts para o aplicativo e o mesmo fará a instalação das kexts, reparar as permissões e atualizar o cache.

[Kext Wizard](http://www.hackintoshosx.com/files/file/2136-kext-wizard-3-7-10/) - Funciona de forma parecida com o Kext Utility, porém lhes da opção de instalar as kexts no Sistema ou no Chameleon e além disso, permite que kexts sejam carregadas no sistema sem instalá-las.

[Kext Beast](http://www.tonymacx86.com/downloads.php?do=file&id=32) - O modo de instalação de kexts desse aplicativo é bem peculiar. Basta deixar as suas kexts na ‘Mesa’ e executar o aplicativo.

- **OBS**: Esse software é desenvolvido pelo pessoal do fórum Tonymac de forma fechada para a comunidade e só terá suporte no fórum de seus criadores.

## All in Ones

### Vantagens:

- Contém diversas kexts para áudio, rede, Wi-Fi, USB, teclados e mouses PS2;
- Muitas kexts já vem com o patch necessário para funcionarem bem;
- Diversas SMBIOS a escolha;
- Bootloader integrado;

### Desvantagens:

- Configurações Automáticas

*"Mas por que gerar as configurações é ruim? Não funciona?"*

Na verdade funciona, mas há coisas que ainda devem ser feitas manualmente e as configurações do bootloader é uma delas, pois o aprendizado tem mais importância e prioridade do que a zona de conforto.

----

[**Multibeast**](http://www.tonymacx86.com/downloads.php?do=cat&id=3) - É a ferramenta mais conhecida da comunidade. Ela trás consigo diversas kexts, além de gerar as configurações para o bootloader Chimera.

- OBS: Essa software é desenvolvido pelo pessoal do fórum Tonymac de forma fechada para a comunidade e só terá suporte no fórum de seus criadores.

[**Hackintosh Vietnam Tool**](http://www.insanelymac.com/forum/files/file/210-hackintosh-vietnam-ultimate-aio-tool/) - Funciona de forma semelhante ao Multibeast porém com alguns recursos a mais como dois bootloader como o Chameleon e o Clover,  gerador de arquivos SSDT e diversas ferramentas inclusas.

**[MacPois0n Yosemite](http://www.insanelymac.com/forum/files/file/359-macpois0n-yosemite/)** - Essa ferramenta é praticamente a mesma coisa que a anterior porém é dedicada exclusivamente para o Yosemite além de possuir alguns drivers a mais como os driver para as mais recentes placas de vídeo da AMD.

## Editores de DSDT

Editar a DSDT parece complicado a primeira vista, ainda mais quando não se possui o menor conhecimento para isso, mas a comunidade está sempre ativa para facilitar nossa vida.

[**MaciASL**](http://sourceforge.net/projects/maciasl/) - A comunidade em torno deste aplicativo já disponibilizou em seus repositórios diversas DSDT’s para os mais variados tipos de placas-mãe das marcas ASUS, Intel, Gigabyte, MSI, etc. Em bem provável que já exista uma DSDT para sua placa-mãe.

## Editores de arquivos .PLIST

As vezes precisamos alterar algumas informações de kexts ou configurações do bootloader e sempre editamos esses arquivos com o editor nativo do Mac. Porém muitos usuários inexperientes acabam quebrando a codificação desses arquivos e por isso foram criados duas ótimas ferramentas para esse fim, ambas tem o mesmo propósito então utilize aquela que mais lhes agradar.

- [PlistEdit Pro](http://www.fatcatsoftware.com/plisteditpro/)
- [Property List Editor](http://www.insanelymac.com/forum/topic/298787-editor-de-arquivos-plist-property-list-editor/)

## Ferramentas para Debug

Durante a construção de um hackintosh, podem haver alguns problemas e nem sempre temos experiência o suficiente para detectar onde esses problemas estão. Por esse motivo foram criadas ferramentas de debug para nos acudir em momentos como esse.

[**IORegistryExplorer**](http://www.hackintoshosx.com/files/file/4251-ioregistryexplorer/) - Talvez essa seja a ferramenta mais utilizada pelos usuários. Diversos fóruns especializados pedem o arquivo `.ioreg`, que contém toda a depuração do seu sistema, antes de dar qualquer suporte a seus usuários. É nesse momento que a ferramenta entra em ação.

## Ferramentas para Análise

Antes de pensar em construir um hackintosh é preciso avaliar a compatibilidade do seu hardware. Em posse dessas informações, você poderá pesquisar em fóruns especializados, se todos os componentes que compõem o seu hardware são compatíveis, se possuem kexts, que problemas eles podem apresentar, etc. Qualquer informação válida será de grande ajuda.

[**System Info**](http://olarila.com/forum/viewtopic.php?f=6&t=25) - Essa ferramenta além de dizer se os componentes são compatíveis ou não, exibe algumas informações como **DevID** e **VenID** que são amplamente utilizadas em kexts para reconhecimento de hardware.

- OBS: Para utilizar este aplicativo é necessário ter o **Java** instalado e também está **disponível para Windows**.

## Monitoramento de Temperaturas

Como em qualquer outro computador é preciso estar atento as temperaturas do seu hardware e em hackintoshes não é diferente. Alias é uma tarefa de extrema importância após terminar construir seu hackintosh. A monitoração deve ser feita durante alguns dias e se não apresentar sobreaquecimento, instabilidades ou travamentos significa que tudo está correndo as mil maravilhas. 

[**HWMonitor**](http://sourceforge.net/projects/hwsensors/) - Este aplicativo é fornecido no instalador **HWSensors** (FakeSMC), vital para o funcionamento do hackintosh. Os sensores de **CPU**, **GPU**, **LPC** (Chipset) funcionarão sem problemas, porém o sensor **ACPI** precisa de algumas edições na DSDT para funcionar.

---

Tutorial elaborado e editado por: **Samuel Cabral**. Links por: **Danilo Tavares**


---

<br/>

```md
A versão original deste documento pode ser acessada [aqui](https://docs.google.com/document/d/1hfviixDupf9K7QdvvIbtwwbc9vVQAg9fyiON3mB894g/edit).
Formatação em *Markdown* por [gabrguedes](https://github.com/gabrguedes).
```

<br/>

---

*Você pode solicitar uma nova alteração neste arquivo fazendo uma `pull request`. Inclua, na `pull request`, o link para o arquivo original no Google Drive apontando o que há de diferente entre o arquivo atual e o seu.*
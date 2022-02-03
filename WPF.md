# Projeto C#

O arquivo de extensão .csproj, de formato XML, define diversos aspectos de um projeto da linguagem C#, como parâmetros de depuração e compilação.

# XAML (eXtensible Application Markup Language)

É um arquivo XML usado para criar e inicializar objetos do .NET, como janelas e controles de uma aplicação WPF. Os elementos do XAML correspondem às classes de objetos do .NET e os atributos, às propriedades e eventos.

As *tags* e os atributos do XAML são sensíveis a maiúsuclas e minúsculas (*case sensitive*).

## Duas maneiras de escrever os atributos

Os atributos podem ser definidos dentro das *tags* dos controles ou em *tags* próprias com a notação Controle-Ponto-Atributo. Por exemplo:

```
<Button FontWeight="Bold">Botão</Button>
```

é equivalente a:

```
<Button>
    <Button.FontWeight>Bold</Button.FontWeight>
    Botão
</Button>
```

## App.xaml e App.xaml.cs

Os arquivos complementares App.xaml e App.xaml.cs são o ponto de partida de uma aplicação WPF, ou seja, onde se procuram as instruções iniciais.
## Estrutura da Janela (MainWindow)

```
\\ MainWindow.xaml
<Window x:Class="OlaMundoWPF.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:OlaMundoWPF"
        mc:Ignorable="d"
        Title="Olá, mundo!" Height="450" Width="800">
    <Grid>
        <Button x:Name="Btn_Clique_Aqui" Content="Clique aqui" Margin="0,0,0,0" VerticalAlignment="Center" HorizontalAlignment="Center" Width="100" Click="Btn_Clique_Aqui_Click"/>
    </Grid>
</Window>
```
No exemplo acima, o marcador Window é a raiz do arquivo responsável por definir a janela. A propriedade x:Class é o nome da classe que controla os aspectos lógicos da janela (no arquivo de formato **xaml.cs**). O termo "xmlns" significa Sintaxe do Espaço de Nomes (Namespace) do XML. No exemplo, o controle Button, incluído por meio do marcador de mesmo nome, encontra-se dentro do Grid, que é um controle de organização dos elementos da janela. O controle Button tem várias propriedades, como nome (x:Name) e texto (Content), e o evento Click, que é disparado pelo clique do usuário e processado pelo método Btn_Clique_Aqui_Click.

```
\\ MainWindow.xaml.cs
using System.Windows;

namespace OlaMundoWPF
{
    /// <summary>
    /// Interação lógica para MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }

        private void Btn_Clique_Aqui_Click(object sender, RoutedEventArgs e)
        {
            MessageBox.Show("Olá, mundo!");
        }
    }
}
```

O arquivo MainWindow.xaml.cs estabelece o comportamento lógico da aplicação. A classe é do tipo **partial** porque a sua definição se divide entre os arquivos MainWindow.xaml e MainWindow.xaml.cs. O método Btn_Clique_Aqui_Click é chamado quando o evento de clique do botão Btn_Clique_Aqui é disparado.

## Eventos

Em XAML, definimos os eventos como uma propriedade do controle. Por exemplo:

```
<Button x:Name="Botao" MouseUp="Botao_MouseUp">Clique aqui</Button>
```

O trecho de código acima relaciona o evento MouseUp com o método Botao_MouseUp, que poderia ter a seguinte assinatura:

```
private void Botao_MouseUp(object sender, MouseButtonEventArgs e)
```

Também é possível associar o evento de um controle a um método por meio de um [delegado (*delegate*)](https://docs.microsoft.com/pt-br/dotnet/csharp/programming-guide/delegates/using-delegates) deste:

```
public partial class MainWindow : Window {

    public MainWindow() {
        InitializeComponent();
        Botao.MouseUp += new MouseButtonEventHandler(Botao_MouseUp);
    }

    private void Botao_MouseUp(object sender, MouseButtonEventArgs e) {
    }
}
```
# Referências

WPF Tutorial: https://wpf-tutorial.com/

SELLS, C e GRIFFITHS, I. [Programming WPF](https://www.oreilly.com/library/view/programming-wpf-2nd/9780596510374/), 2a ed., O'Relly, 2007.

# Questões de prova

## Questão 1

*Ano: 2015 Banca: FGV Órgão: TCM-SP Prova: FGV - 2015 - TCM-SP - Agente de Fiscalização - Tecnologia da Informação*

No contexto da WPF (Windows Presentation Foundation), o controle que pode conter coleções de objetos de tipos variados (tais como image e panel) compartilhando o mesmo espaço da tela é conhecido como:

Alternativas

A. DataGrid;

B. GridView;

C. Slider;

D. TabControl;

E. TreeView.

### Comentários

A. INCORRETO. DataGrid é um controle do Windows Forms que exibe dados em linhas e colunas, no formato de uma tabela. Ver https://docs.microsoft.com/pt-br/dotnet/desktop/winforms/controls/datagrid-control-overview-windows-forms?view=netframeworkdesktop-4.8

B. INCORRETO. O controle GridView é uma classe para dispor itens em colunas dentro do controle ListView. Ver https://docs.microsoft.com/pt-br/dotnet/api/system.windows.controls.gridview?view=windowsdesktop-6.0

C. INCORRETO. Slider é um controle de seleção de valores por meio do deslizamento de um seletor sobre uma barra. Ver https://docs.microsoft.com/pt-br/dotnet/api/system.windows.controls.slider?view=windowsdesktop-6.0

D. CORRETO. TabControl é um controle que apresenta guias (ou abas) para alternância do conteúdo visível, o que permite compartilhar o mesmo espaço de tela para objetos distintos. Ver https://docs.microsoft.com/pt-br/dotnet/desktop/winforms/controls/tabcontrol-control-windows-forms?view=netframeworkdesktop-4.8

E. INCORRETO. TreeView é um controle do Windows Forms para mostrar itens em uma visão hierárquica, como a de pastas e arquivos no Explorador de Arquivos do Windows. Ver https://docs.microsoft.com/pt-br/dotnet/desktop/winforms/controls/tabcontrol-control-windows-forms?view=netframeworkdesktop-4.8

**Gabarito: D**

# Questão 2

*FGV - 2016 - Arquitetura de Software - Padrões de projeto (Design Patterns) - IBGE* 

O padrão de projeto MVVM foi proposto por John Grossman para simplificar o desenvolvimento de aplicações baseadas nas tecnologias WPF e Windows Phone. O MVVM foi desenvolvido como uma especialização do padrão:

Alternativas:

A - Model-View-Controller;

B - Mobile-Interator Model;

C - Presentation Model;

D - Singleton Model;

E - Decorator Model.

### Comentário

MVVM, Model-View-View-Model, é um padrão de projeto que separa o desenvolvimento da interface (visualização) de usuário da lógica de negócio (modelo). Baseia-se no padrão ["Presentation Model"](https://martinfowler.com/eaaDev/PresentationModel.html) de Martin Fowler. No WPF, a camada de visualização é escrita de forma declarativa em um arquivo XAML.

Referências: https://docs.microsoft.com/pt-br/windows/uwp/data-binding/data-binding-and-mvvm e https://docs.microsoft.com/en-us/archive/msdn-magazine/2009/february/patterns-wpf-apps-with-the-model-view-viewmodel-design-pattern 


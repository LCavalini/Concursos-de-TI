# Projeto C#

O arquivo de extensão .csproj, de formato XML, define diversos aspectos de um projeto da linguagem C#, como parâmetros de depuração e compilação.

# XAML

É um arquivo XML usado para criar e inicializar objetos do .NET, como janelas e controles de uma aplicação WPF. Os elementos do XAML correspondem às classes de objetos do .NET e os atributos, às propriedades e eventos.

## Estrutura

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
# AppliGestion
<Window x:Class="MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:WpfApplication5"
        mc:Ignorable="d"
        Title="MainWindow" Style="{DynamicResource WindowStyle1}" HorizontalAlignment="Center" Margin="-1,0,0,0" d:DesignWidth="1069.266" Height="1080" Width="1920">
    <Window.Resources>

        <ControlTemplate x:Key="WindowTemplateKey" TargetType="{x:Type Window}">
            <Border BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}" Background="{TemplateBinding Background}">
                <Grid>
                    <AdornerDecorator>
                        <ContentPresenter/>
                    </AdornerDecorator>
                    <ResizeGrip x:Name="WindowResizeGrip" HorizontalAlignment="Right" IsTabStop="false" Visibility="Collapsed" VerticalAlignment="Bottom"/>
                </Grid>
            </Border>
            <ControlTemplate.Triggers>
                <MultiTrigger>
                    <MultiTrigger.Conditions>
                        <Condition Property="ResizeMode" Value="CanResizeWithGrip"/>
                        <Condition Property="WindowState" Value="Normal"/>
                    </MultiTrigger.Conditions>
                    <Setter Property="Visibility" TargetName="WindowResizeGrip" Value="Visible"/>
                </MultiTrigger>
            </ControlTemplate.Triggers>
        </ControlTemplate>
        <Style x:Key="WindowStyle1" TargetType="{x:Type Window}">
            <Setter Property="Foreground" Value="{DynamicResource {x:Static SystemColors.WindowTextBrushKey}}"/>
            <Setter Property="Background" Value="{DynamicResource {x:Static SystemColors.WindowBrushKey}}"/>
            <Setter Property="Template">
                <Setter.Value>
                    <ControlTemplate TargetType="{x:Type Window}">
                        <Border BorderBrush="{TemplateBinding BorderBrush}" BorderThickness="{TemplateBinding BorderThickness}" Background="{TemplateBinding Background}">
                            <AdornerDecorator>
                                <ContentPresenter/>
                            </AdornerDecorator>
                        </Border>
                    </ControlTemplate>
                </Setter.Value>
            </Setter>
            <Style.Triggers>
                <Trigger Property="ResizeMode" Value="CanResizeWithGrip">
                    <Setter Property="Template" Value="{StaticResource WindowTemplateKey}"/>
                </Trigger>
            </Style.Triggers>
        </Style>
        <Color x:Key="Color1">#FF1D1D61</Color>
    </Window.Resources>
    <Window.Background>
        <ImageBrush ImageSource="H:\fleur.jpg"/>
    </Window.Background>

    <Menu x:Name="menu" Margin="11,10,12,9" RenderTransformOrigin="0.154,-5.009" OpacityMask="#FFD81313" BorderBrush="#FF1B1B1B" VerticalAlignment="Top" Height="28" FontSize="14" Foreground="White" TextOptions.TextFormattingMode="Display" FontWeight="Black" FontStyle="Italic" FontFamily="Swis721 Blk BT">
        <Menu.Background>
            <LinearGradientBrush EndPoint="0.5,1" StartPoint="0.5,0">
                <GradientStop Color="Black" Offset="0"/>
                <GradientStop Color="#FFB42121" Offset="1"/>
            </LinearGradientBrush>
        </Menu.Background>
        <Menu.Effect>
            <DropShadowEffect Color="#FF9E7474"/>
        </Menu.Effect>
        <Menu.RenderTransform>
            <TransformGroup>
                <ScaleTransform/>
                <SkewTransform AngleX="0.898"/>
                <RotateTransform/>
                <TranslateTransform X="-4.556"/>
            </TransformGroup>
        </Menu.RenderTransform>
        <MenuItem Header="Home" Click="MenuItem_Click" Margin="5,0"/>
        <MenuItem Header="Sécurité&#xD;&#xA;" Click="MenuItem_Click_1" Margin="5,0"/>
        <MenuItem Header="Environnement" Margin="5,0"/>
        <MenuItem Header="Habilité&#x9;" Click="MenuItem_Click_2" FontSize="13" Width="95" Margin="5,0"/>
        <MenuItem Header="Formation" Width="107" Margin="5,0"/>

        <Grid>
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="11*"/>
                <ColumnDefinition Width="14*"/>
            </Grid.ColumnDefinitions>
            <Button x:Name="button" Content="Répondre à une affaire" VerticalAlignment="Top" Margin="425,842,-614,-843" Height="24" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button1" Content="Rechercher une affaire" Margin="0,818,-614,-814" RenderTransformOrigin="-1.945,3.981" HorizontalContentAlignment="Center" VerticalContentAlignment="Center" Padding="4,-2,1,1" VerticalAlignment="Top" UseLayoutRounding="True" HorizontalAlignment="Right" Width="189" FontStyle="Normal" Grid.ColumnSpan="2"/>

            <TextBlock x:Name="textBlock" TextWrapping="Wrap" Text="Client" Height="24" Margin="464,488,-561,-489" RenderTransformOrigin="-2.587,1.886" VerticalAlignment="Top" FontSize="20" FontStyle="Normal" Padding="5,0,0,0" Grid.Column="1" Foreground="#FFFFF7F7" FontFamily="Swis721 BlkEx BT"/>
            <TextBlock x:Name="textBlock1" HorizontalAlignment="Left" TextWrapping="Wrap" Text="TextBlock" VerticalAlignment="Top" Height="150" Margin="443,531,-592,-658" Width="149" Grid.Column="1">
                <TextBlock.Background>
                    <ImageBrush ImageSource="H:\Client.jpg"/>
                </TextBlock.Background>
            </TextBlock>
            <Button x:Name="button2" Content="Etudier l'affaire" HorizontalAlignment="Right" VerticalAlignment="Top" Width="135" Margin="0,871,-587,-870" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button3" Content="Réaliser le chantier" HorizontalAlignment="Left" VerticalAlignment="Top" Width="189" Margin="425,898,-614,-899" FontStyle="Normal" Height="24" Grid.Column="1"/>
            <Button x:Name="button4" Content="Mise en service" HorizontalAlignment="Left" VerticalAlignment="Top" Width="135" Margin="452,927,-587,-926" Height="22" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button5" Content="Clore le chantier" HorizontalAlignment="Left" VerticalAlignment="Top" Width="135" Margin="452,954,-587,-953" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button6" Content="Gérer les ressources humaine" HorizontalAlignment="Left" VerticalAlignment="Top" Width="246" Margin="-194,570,-52,-569" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button7" Content="Achat" HorizontalAlignment="Left" VerticalAlignment="Top" Width="246" Margin="-194,528,-52,-527" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button8" Content="Gérer les ressources humaine" HorizontalAlignment="Left" VerticalAlignment="Top" Width="246" Margin="-194,570,-52,-569" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button9" Content="Qualité et Environnement" HorizontalAlignment="Left" VerticalAlignment="Top" Width="246" Margin="929,528,-1175,-527" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button10" Content="Prevention" HorizontalAlignment="Left" VerticalAlignment="Top" Width="246" Margin="929,570,-1175,-569" FontStyle="Normal" Grid.Column="1"/>
            <Button x:Name="button11" Content="Diriger la société" HorizontalAlignment="Left" VerticalAlignment="Top" Width="211" Margin="413,232,-624,-231" FontStyle="Normal" Grid.Column="1" RenderTransformOrigin="0.239,1.682"/>

        </Grid>




    </Menu>

</Window>

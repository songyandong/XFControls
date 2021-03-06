# RadioButtonGroup

## Sample
~~~
...
 <Page.Resources>
    <ResourceDictionary>
      ...
      <ControlTemplate x:Key="Selected">
        <ctrls:Border BackgroundColor="{DynamicResource AccentColor}"
                      Stroke="White"
                      CornerRadius="5"
                      Padding="5,5"
                      WidthRequest="80"
                      StrokeThickness="1"
                      >
          <ContentPresenter />
        </ctrls:Border>
      </ControlTemplate>

      <ControlTemplate x:Key="UnSelected">
        <ctrls:Border BackgroundColor="Transparent"
                      Stroke="White"
                      CornerRadius="5"
                      Padding="5,5"
                      WidthRequest="80"
                      StrokeThickness="1">
          <ContentPresenter />
        </ctrls:Border>
      </ControlTemplate>

    </ResourceDictionary>
  </Page.Resources>
  ...
  ...

<StackLayout>
<StackLayout>
    <Label Text="请选择大类" />

    <ctrls:RadioButtonGroup ItemsSource="{Binding Datas}"
                            SelectedItem="{Binding BigCat}"
                            DisplayPath="Data.Name"
                            SelectedItemControlTemplate="{StaticResource Selected}"
                            UnSelectedItemControlTemplate="{StaticResource UnSelected}"
                            />
</StackLayout>

<StackLayout IsVisible="{Binding CanShowSecondCategory}">
    <Label Text="请选择小类" />
    <ctrls:RadioButtonGroup ItemsSource="{Binding BigCat.Subs}"
                            SelectedItem="{Binding SecondCat}"
                            DisplayPath="Data.Name"
                            SelectedItemControlTemplate="{StaticResource Selected}"
                            UnSelectedItemControlTemplate="{StaticResource UnSelected}"
                            />

</StackLayout>
</StackLayout>
~~~

## Properties:
Name | Desc | Type | Default Value
|---|---|---|---|
ShowRadio | | bool | Horizontal
SelectedItemControlTemplate | | ControlTemplate |[DefaultRadioButtonSelectedControlTemplate](https://github.com/gruan01/XFControls/blob/master/XFControls/Src/AsNum.XFControls/Templates/DefaultRadioButtonSelectedControlTemplate.xaml)
UnSelectedItemControlTemplate | | ControlTemplate | [DefaultRadioButtonUnSelectedControlTemplate](https://github.com/gruan01/XFControls/blob/master/XFControls/Src/AsNum.XFControls/Templates/DefaultRadioButtonUnSelectedControlTemplate.xaml)
Other's please refer [RadioGroupBase](RadioGroupBase.md)

## ISSUE

# WPF MultiComboBox

`>= .NET Framework 4.7.2`

Based on https://www.codeproject.com/Articles/45782/A-WPF-Combo-Box-with-Multiple-Selection

## Examples

`SelectedItems` must be an instance of `IList`.

###DisplayMemberPath:

```xaml
<customControls:MultiComboBox ItemsSource="{Binding Items}"
                              SelectedItems="{Binding SelectedItems}"
                              SelectionMode="Multiple"
                              DisplayMemberPath="Label" />
```


### DataTemplate:

```xaml
<customControls:MultiComboBox ItemsSource="{Binding Items}"
                              SelectedItems="{Binding SelectedItems}"
                              SelectionMode="Multiple">
    <customControls:MultiComboBox.ItemTemplate>
        <DataTemplate>
            <Label Background="Red"
                   Content="{Binding Label}"
                   Margin="0"
                   Padding="2,0"/>
        </DataTemplate>
    </customControls:MultiComboBox.ItemTemplate>
</customControls:MultiComboBox>
```
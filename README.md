# POE
RecipeAppWPF: A recipe management app with filtering capabilities built on WPF. Easily add, display, and filter recipes. Developed in C# with Visual Studio.
<Window x:Class="RecipeAppWPF.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        Title="Recipe App" Height="600" Width="800">
    <Grid Margin="10">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="*"/>
        </Grid.RowDefinitions>
        
        <StackPanel>
            <TextBlock Text="Recipe Filter" FontSize="20" Margin="10"/>

            <StackPanel Orientation="Horizontal" Margin="10">
                <TextBlock Text="Ingredient: " VerticalAlignment="Center"/>
                <TextBox Name="IngredientTextBox" Width="200" Margin="5,0"/>
            </StackPanel>
            <StackPanel Orientation="Horizontal" Margin="10">
                <TextBlock Text="Food Group: " VerticalAlignment="Center"/>
                <ComboBox Name="FoodGroupComboBox" Width="200" Margin="5,0">
                    <ComboBoxItem Content="All" IsSelected="True"/>
                    <ComboBoxItem Content="Vegetables"/>
                    <ComboBoxItem Content="Fruits"/>
                    <ComboBoxItem Content="Grains"/>
                    <ComboBoxItem Content="Proteins"/>
                    <ComboBoxItem Content="Dairy"/>
                </ComboBox>
            </StackPanel>
            <StackPanel Orientation="Horizontal" Margin="10">
                <TextBlock Text="Max Calories: " VerticalAlignment="Center"/>
                <TextBox Name="MaxCaloriesTextBox" Width="200" Margin="5,0"/>
            </StackPanel>
            <Button Name="FilterButton" Content="Filter Recipes" Click="FilterButton_Click" Margin="10"/>

            <ListBox Name="RecipesListBox" Margin="10" Height="200"/>
        </StackPanel>

        <StackPanel Grid.Row="1">
            <TextBlock Text="Add Recipe" FontSize="20" Margin="10"/>
            <StackPanel Orientation="Horizontal" Margin="10">
                <TextBlock Text="Recipe Name: " VerticalAlignment="Center"/>
                <TextBox Name="RecipeNameTextBox" Width="200" Margin="5,0"/>
            </StackPanel>
            <StackPanel Orientation="Horizontal" Margin="10">
                <TextBlock Text="Number of Ingredients: " VerticalAlignment="Center"/>
                <TextBox Name="IngredientCountTextBox" Width="200" Margin="5,0"/>
            </StackPanel>
            <Button Name="AddRecipeButton" Content="Add Recipe" Click="AddRecipeButton_Click" Margin="10"/>
            <Button Name="DisplayRecipesButton" Content="Display Recipes" Click="DisplayRecipesButton_Click" Margin="10"/>
        </StackPanel>
    </Grid>
</Window>

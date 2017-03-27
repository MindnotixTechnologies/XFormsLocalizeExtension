# Xamarin.Forms Localization Library

HOW TO:

1. Install-Package Xamarin.Forms.Localization.Library via nuget, make sure that platform assemblies (i.e. XFormsLocalizeExtension.Android) are referenced.
2. Create resource directory under PCL project, i.e. Resx.
3. Create necessary resource files (*.resx) under resource directory.
	- one for default localization
		MainPageLocale.resx
	- and for other languages
		MainPageLocale.pl.resx
		MainPageLocale.en.resx
		and so on
4. Create sample page in Your PCL:
	
	    <ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:SampleApp"
             xmlns:xfl="clr-namespace:XFormsLocalizeExtension.MarkupExtensions;assembly=XFormsLocalizeExtension"
             x:Class="SampleApp.MainPage">

		<Label Text="{xfl:XFormsLocalizeExtension SampleApp.Resx.MainPageLocale:HelloWorldResx}" 
           	       VerticalOptions="Center" 
           	       HorizontalOptions="Center" />

		</ContentPage>
	
5. That's all, enjoy Your localized application:)

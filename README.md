# Onfido.Xamarin.Android
Onfido.Xamarin.Android Binding

@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
CSP Solutions https://www.cspsolutions.com/ Provides Software
- DevOps Services
- Integration Services
- Xamarin Binding Libraries
- AI DevOps
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

Note: ************* Add reference to "onfido-capture-sdk-14.0.0.aar" it is around 45 MB, Github did allow to upload it 
You can download this AAR Library and reference it in the solution under Jar folder

Download from Maven
https://repo1.maven.org/maven2/com/onfido/sdk/capture/onfido-capture-sdk/14.0.0/onfido-capture-sdk-14.0.0.aar
https://mvnrepository.com/artifact/com.onfido.sdk.capture/onfido-capture-sdk/14.0.0

// ONFIDO documentation https://documentation.onfido.com/sdk/android/

//The following example after you reference the  Onfido.Xamarin.Android Binding

        OnfidoConfig _config = null;
        IOnfido _onfido = null;

        protected void LaunchOnfido()
        {
            string token = "eyJhbGciOiJ..............."; // Generate https://documentation.onfido.com/sdk/android/

            this._config = OnfidoConfig.InvokeBuilder(this.ApplicationContext).WithSDKToken(token).Build();

            this._onfido = OnfidoFactory.Create(this.ApplicationContext).Client;

            this._onfido.StartActivityForResult(this, 1, this._config);
        }



@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

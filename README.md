# Onfido.Xamarin.Android
Onfido.Xamarin.Android Binding

@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
CSP Solutions https://www.cspsolutions.com/ Provides Software
- DevOps Services
- Integration Services
- Xamarin Binding Libraries
- AI DevOps
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

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

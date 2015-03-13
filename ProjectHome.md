A simple UI project built using WPF for creating SQL server Connection strings.

This small library is meant to be used in other applications where the user need to specify a connection string to a database.

It is built to be as easy as possible to integrate into your application.

How to use:
```

                    ConnectionStringCreatorGUI.SqlConnectionString initialConnStr;

                    try
                    {
                        initialConnStr = new ConnectionStringCreatorGUI.SqlConnectionString(connectionString);
                    }
                    catch (Exception)
                    {
                        // If the connectionstring that you provided is bad then start with a blank connstr
                        initialConnStr = new ConnectionStringCreatorGUI.SqlConnectionString();
                    }
                 
                    Window win = new ConnectionStringCreatorGUI.ConnectionStringBuilderWindow(initialConnStr, returnConnBuilder =>
                    {
                        ConnectionString = returnConnBuilder.ToString();
                    });

                    win.Show();

                

```
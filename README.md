# A sample Apama EPL App called "CorrelatorProcessTerminator" for use in Cumulocity

Sometimes it is useful to be able to "activate" a simple existing EPL App that is able to quickly cause the apama-ctrl microservice to restart.  No need for support tickets, or Ops assistance, or higher-level permissions.

Once deployed as a new EPL App, you just flick the activation switch and 10seconds later the microservice will restart.  After restart the EPLApp is recovered as "active", but the fail-safe ensures that it dies immediately with an explanation.  If the system was extremely heavily overloaded, then you might need to increase the failsafe beyond 2mins, but in my tests it was detecting uptime of around 1.8secs at the time it checked and then died. The app would appear to be active, but in reality has no live mthreads, so to use again just reactivate it.
Hope it is useful in your toolbox.

----
LICENSE

Anyone is free to use and modify these EPL files. They are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite, nor any part of the formal Apama Community assets provided by Software AG. Users are free to use, fork and modify them.

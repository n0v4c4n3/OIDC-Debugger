# OAuth 2.0 and OpenID Connect Debugger

:earth_americas: Live here: https://test.sso.bigcheese.uy

## What is this?

Getting an OAuth or OpenID Connect flow working properly can be tricky. There's a bunch of parameters you need to get right, and it's not always easy to capture or parse errors. I wrote this little web tool to make the process easier.

## How to use the debugger

All you need to do is temporarily set your OAuth client redirect URI to `https://test.sso.bigcheese.uy/debug`:

<img src="https://www.recaffeinate.co/img/post/introducing-openid-connect-debugger/temp-redirect-uri.png" alt="Temporarily change client redirect URI to debugger" title="Screenshot of Google developer console" width="550px">

Then, build a request to your authorization server using the debugger, and fire it off:

<img src="https://www.recaffeinate.co/img/post/introducing-openid-connect-debugger/switch-response-mode.gif" alt="Choose response mode and click Send Request" title="Screenshot of debugger form" width="550px">

The debugger will capture the callback and help you understand what happened (whether success or failure):

<img src="https://www.recaffeinate.co/img/post/introducing-openid-connect-debugger/error-and-success.gif" alt="Decode the error message, or view the successful callback information" title="Screenshot of error and success page" width="550px">

## Contributing

Issues and PRs are welcome! The project is built with ASP.NET Core and Vue.js.

To build and run locally,

```
git clone https://github.com/n0v4c4n3/oidc-debugger
cd oidc-debugger
snap install dotnet-sdk --classic
dotnet build
dotnet run
```

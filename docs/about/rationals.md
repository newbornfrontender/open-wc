# Rationals

Before we recommend anything it goes through a process of evaluations.
In short

1. We only recommend usage of a features/function if it is release in a stable version of a least ONE browser
2. We only recommend libraries if they offer an es module version

::: warning
We have ONE exception to this rule and that is 'bare modules'.
This is such a powerful an prominent feature in the current js ecosystem so if you don't use it you basically need to implement everything yourself.
We do not want you to do this so we need to embrace this as our only exeption for now.
There is already a spec in the works which will bring bare modules via [import maps](https://github.com/WICG/import-maps) to the browser.
So we hope this exeption will not stay forever.
:::

## Workflows

Following there rules we strive to provide you with three development workflows.

Each of the workflows tackles a specific task in your webcomponent/application.
You are encouraged to freely switch between them depending on what you are working on.

1. Developing workflow

Use an up to date browser and develop with 0 tools => any webserver should do.
We hope you spend most of your time in this envirorment.

When would you choose this workflow:
- while developing new stuff
- whenever possible

Why would you choose this:
- simple to setup
- as fast as it gets
- be sure to use only browser complient code
- auto reload

::: warning
Unfortunately we are not fully there yet, because of 'bare modules' exception you need to have a server that at least supports them.
We recommend our [Developing Setup](../developing/setup) => is still on our ToDo List.
:::


2. Bundling workflow

Chances are the webcomponents you are creating will need to run in more then just the latest browser.
In these cases it's time to open your toolbox and make sure everything works in all supported browsers.

When would you choose this workflow:
- to verify everything works in all supported browsers
- to debug not latest browsers

We recommend our [Open Web Component Bundling Setup](../bundling).

Why would you choose it:
- as good as it gets when you need to work with not latest browsers
- auto bundling + reloading


3. Production Bundling workflow

Once you are happy with your webcomponents it's time to put them somewhere more useful. 
Most likely a publicly available web server.
Before you do that let's apply all the optimizations magic we can cook up.

When would you use this:
- optimize your build
- publish

We recommend our [Open Web Component Bundling Setup](../bundling).

Why would you choose it:
- multiple bundling outputs
- conditional auto loader for those bundles (without a special server)

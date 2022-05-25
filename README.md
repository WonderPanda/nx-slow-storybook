# NX Slow Storybook

This repo demonstrates that the developer experience of using a Storybook configuraiton for a react library all generated through official @nrwl generators
`@nrwl/react:library` and `@nrwl/react:storybook-configuration` is extremely slow.

Even with an incredibly simple monorepo set up with a single react component library that has a storybook configuration it takes 1-2 full seconds for HMR to kick in and the UI to update.

In our actual project at work where there are a few more libs and apps the hot reload can take 10-15 seconds which makes it completely unusable

## Steps

1. Install the dependencies by running `yarn`
2. Run the storybook for the component library `yarn nx storybook components` and wait for it to become available
3. Make a change inside `components.tsx` and observe that it takes a very long time for changes to be reflected in the UI

## Notes

It feels like there is something going wrong with the setup here because I've seen in many other projects/setups that Storybook hot reloading should feel nearly instantaneous

Example output:

```
webpack built preview 629e33ca826bf35dc419 in 1504ms
webpack building...
webpack built preview e9f2d5d63a668308e3e0 in 1196ms
webpack building...
webpack built preview c4c4f47821c914339dbc in 1149ms
```


# Verida Javascript Library

This monorepo contains [Verida Client Library](packages/verida-ts) and a variety of utility packages that support that library.

There is a `#react-native` branch that maintains a slightly modified version of the `Verida Client Library` that is used to build the `@verida/client-rn` package.

## Developer Notes

### Linking dependencies

It's not possible to add dependencies between monorepo packages using yarn (ie: `yarn add @verida/3id-utils-node`) if that package hasn't been published to `npm`.

Unpublished dependencies betwen monorepo packages can be linked by:

- Manually adding the expected dependency to `package.json` (ie: `@verida/3id-utils-node`)
- Run `npx lerna bootstrap` in the root directory of this project

# Vestra Pulse

The separate mobile-client repository for Vestra.

**Planning scaffold only.** There is no implemented Expo/React Native app, application entry point, mobile build or deployed mobile API yet. The original two-file scaffold and its history were extracted from `apps/pulse` in [Vestra](https://github.com/amabee/Vestra). This repository does not require a sibling checkout or `workspace:*` dependencies.

## Repository layout

- [Vestra](https://github.com/amabee/Vestra): Nova desktop app, its backend/runtime, shared SDK and existing documentation.
- [Pulse](https://github.com/amabee/Pulse): future mobile-client implementation.
- [Foundry](https://github.com/amabee/Foundry): native extension sources and registry.

The Astra project is outside this extraction and remains unchanged.

## Next implementation work

1. Establish the mobile API and authentication contract. The old Atlas route suggestions in the historical scaffold are not an existing mobile backend.
2. Create the Expo/React Native application and mobile-native UI.
3. Add explicitly versioned shared contracts or API clients as needed, keeping this repository independently installable.
4. Add real type checks, device/emulator tests and mobile build CI once application code exists.

Provider credentials must stay on the backend; do not embed service secrets in a mobile bundle. The desktop DOM component library is not a React Native UI library.

Planned areas: home rows, search, watchlist, continue watching, playback and offline metadata caching. These are goals, not implemented features.

## Local setup

The repository uses pnpm 11.9.0 and Node 22 or newer. `pnpm install --frozen-lockfile` validates its standalone package setup; there is currently no app to start or build. Application scripts will be added with the implementation, rather than reporting successful placeholder builds.

MIT; see [LICENSE](LICENSE). Never commit account tokens, signing keys, generated app bundles or device credentials.

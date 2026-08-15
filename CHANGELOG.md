# Modern React Snippets Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-08-15

### Added
- Ported the entire snippet collection to native **Zed IDE extension format** (`extension.toml`).
- Added 180+ snippets for React, React Native, Redux, Hooks, PropTypes, TypeScript, testing, and JavaScript utilities across:
  - `snippets/javascript.json` (JavaScript / JSX)
  - `snippets/typescript.json` (TypeScript)
  - `snippets/tsx.json` (TSX / React TypeScript)
- Added direct hook trigger aliases (`useState`, `useEffect`, `useRef`, `useReducer`, `useMemo`, `useCallback`, `useContext`, `useLayoutEffect`, `useImperativeHandle`).
- Added linked tabstops (`$1`, `$2`, `$0`) allowing synchronized renaming of component names and state setters.

### Removed
- Removed legacy Java runtime and Gradle build system (no longer needed for Zed).

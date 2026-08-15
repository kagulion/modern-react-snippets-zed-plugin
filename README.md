# Modern React Snippets

Essential, modern React snippets for the [Zed](https://zed.dev) code editor. Includes comprehensive snippets for **React**, **React Native**, **Redux Toolkit**, **React Hooks**, **TypeScript**, **PropTypes**, **Jest Testing**, and modern **JavaScript / TS utilities**.

## Installation

### Via Zed Extensions
1. Open the Command Palette in Zed (`Ctrl+Shift+P` on Windows/Linux or `Cmd+Shift+P` on macOS).
2. Type **`zed: extensions`** and press <kbd>Enter</kbd>.
3. Search for **"Modern React Snippets"** and click **Install**.

### Manual / Local Dev Extension
1. Clone or download this repository:
   ```bash
   git clone https://github.com/kagulion/modern-react-snippets-zed-plugin.git
   ```
2. Open Zed and open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`).
3. Run **`zed: install dev extension`**.
4. Select the root folder of this repository (`modern-react-snippets-zed-plugin`).

## Supported Languages

- **JavaScript / JSX** (`.js`, `.jsx`)
- **TypeScript** (`.ts`)
- **TSX** (`.tsx`)

All snippets use native LSP tabstops (`$1`, `$2`, `$0`). When inserting component templates, typing the component name updates all occurrences (definition, JSX tags, and default export) simultaneously!

## Snippets Reference

### ⚛️ React Components (JavaScript / JSX)

| Trigger | Description | Output |
| :--- | :--- | :--- |
| `rfce` | React Functional Export Component | `function Component() { return (<div>Component</div>); } export default Component;` |
| `rfc` | React Functional Component | `export default function Component() { return (<div>Component</div>); }` |
| `rafce` | React Arrow Function Export Component | `const Component = () => { return (<div>Component</div>); }; export default Component;` |
| `rafc` | React Arrow Function Component | `export const Component = () => { return (<div>Component</div>); };` |
| `rfcp` | React Functional Component with PropTypes | Functional component with `PropTypes` declaration |
| `rmc` | React Functional Memo Component | `const Component = memo(() => { return (<div>Component</div>); }); export default Component;` |
| `rmcp` | React Memo Component with PropTypes | React memo component with `PropTypes` |
| `rcc` | React Class Component | `export default class Component extends Component { ... }` |
| `rce` | React Class Export Component | `class Component extends Component { ... }; export default Component;` |
| `rccp` | React Class Component with PropTypes | React class component with `static propTypes` |
| `rcep` | React Class Export with PropTypes | React class export with `static propTypes` |
| `rpc` | React Pure Class Component | `export default class Component extends PureComponent { ... }` |
| `rpce` | React Pure Class Export Component | `class Component extends PureComponent { ... }; export default Component;` |
| `rpcp` | React Pure Class with PropTypes | PureComponent with `static propTypes` |
| `rfcredux` | React Functional Component with Redux | Component with Redux `connect(mapStateToProps, mapDispatchToProps)` |
| `rfcreduxp` | React Functional Redux with PropTypes | Functional Component with Redux connect and PropTypes |
| `rcredux` | React Class Component with Redux | Class Component connected to Redux |
| `rcreduxp` | React Class Redux with PropTypes | Class Component connected to Redux with PropTypes |
| `rconst` | Class Constructor | `constructor(props) { super(props); this.state = { ... }; }` |
| `rcontext` | Create React Context | `const Context = React.createContext();` |

---

### 🔷 TypeScript React Components (`.ts`, `.tsx`)

| Trigger | Description | Output |
| :--- | :--- | :--- |
| `tsrfce` | TS React Functional Export Component | `type Props = {}; function Component({}: Props) { ... } export default Component;` |
| `tsrfc` | TS React Functional Component | `type Props = {}; export default function Component({}: Props) { ... }` |
| `tsrafce` | TS React Arrow Function Export Component | `type Props = {}; const Component = (props: Props) => { ... }; export default Component;` |
| `tsrafc` | TS React Arrow Function Component | `type Props = {}; const Component = (props: Props) => { ... };` |
| `tsrcc` | TS React Class Component | `export default class Component extends Component<Props, State> { ... }` |
| `tsrce` | TS React Class Export Component | `class Component extends Component<Props, State> { ... }; export default Component;` |
| `tsrpc` | TS React Pure Component | `export default class Component extends PureComponent<Props> { ... }` |
| `tsrpce` | TS React Pure Export Component | `class Component extends PureComponent<Props> { ... }; export default Component;` |
| `tsrcredux`| TS React Class with Redux | Class component connected to Redux with typed Props and State |
| `tsrnf` | TS React Native Functional Component | Typed functional component for React Native |
| `tsrnfs` | TS React Native Function with Styles | Typed React Native component with `StyleSheet.create({})` |
| `expint` | Export TypeScript Interface | `export interface Name { ... }` |
| `exptp` | Export TypeScript Type | `export type Name = { ... }` |

---

### 🪝 React Hooks

| Trigger / Alias | Description | Output |
| :--- | :--- | :--- |
| `useState` / `useStateSnippet` | State Hook | `const [state, setState] = useState(initialState);` |
| `useEffect` / `useEffectSnippet` | Effect Hook | `useEffect(() => { ... return () => { ... }; }, [deps]);` |
| `useRef` / `useRefSnippet` | Ref Hook | `const ref = useRef(initialValue);` |
| `useReducer` / `useReducerSnippet` | Reducer Hook | `const [state, dispatch] = useReducer(reducer, initialArg, init);` |
| `useMemo` / `useMemoSnippet` | Memo Hook | `useMemo(() => value, [deps]);` |
| `useCallback` / `useCallbackSnippet` | Callback Hook | `useCallback(() => { ... }, [deps]);` |
| `useContext` / `useContextSnippet` | Context Hook | `const context = useContext(MyContext);` |
| `useLayoutEffect` / `useLayoutEffectSnippet` | Layout Effect Hook | `useLayoutEffect(() => { ... }, [deps]);` |
| `useImperativeHandle` / `useImperativeHandleSnippet` | Imperative Handle Hook | `useImperativeHandle(ref, () => ({ ... }), [deps]);` |

---

### 📱 React Native

| Trigger | Description | Output |
| :--- | :--- | :--- |
| `rnf` | React Native Functional Component | `export default function Component() { return (<View><Text>Component</Text></View>); }` |
| `rnfe` | React Native Arrow Function Export | `const Component = () => { ... }; export default Component;` |
| `rnfs` | React Native Function with Styles | Functional component + `StyleSheet.create({})` |
| `rnfes` | React Native Arrow Function with Styles | Arrow function export + `StyleSheet.create({})` |
| `rnc` | React Native Class Component | `export default class Component extends Component { ... }` |
| `rnce` | React Native Class Export Component | `class Component extends Component { ... }; export default Component;` |
| `rncs` | React Native Class with Styles | Class component + `StyleSheet.create({})` |
| `rnpc` | React Native Pure Component | Pure class component for React Native |
| `rnpce` | React Native Pure Export Component | Pure class export component for React Native |
| `rnstyle` | React Native Stylesheet | `const styles = StyleSheet.create({ ... });` |

---

### 🔄 Redux & Redux Toolkit

| Trigger | Description | Output |
| :--- | :--- | :--- |
| `rxslice` | Redux Toolkit Slice | `createSlice({ name, initialState, reducers: {} })` |
| `rxselect` | Reselect Selector | `export const selector = state => state.property` |
| `rxreducer` | Redux Reducer Function | `export default (state = initialState, { type, payload }) => { ... }` |
| `rxaction` | Redux Action Creator | `export const action = (payload) => ({ type, payload })` |
| `rxconst` | Redux Action Type Constant | `export const ACTION_NAME = 'ACTION_NAME'` |
| `redux` | Import Redux Connect | `import { connect } from 'react-redux'` |
| `reduxmap` | MapStateToProps / MapDispatchToProps | `const mapStateToProps = (state) => ({}); const mapDispatchToProps = {};` |

---

### 📦 Import Snippets

| Trigger | Description | Output |
| :--- | :--- | :--- |
| `imr` | Import React | `import React from 'react'` |
| `imrd` | Import ReactDOM | `import ReactDOM from 'react-dom'` |
| `imrc` | Import React with Component | `import React, { Component } from 'react'` |
| `imrcp` | Import React with Component & PropTypes | `import PropTypes from 'prop-types'; import React, { Component } from 'react'` |
| `imrm` | Import React with memo | `import React, { memo } from 'react'` |
| `imrmp` | Import React with memo & PropTypes | `import PropTypes from 'prop-types'; import React, { memo } from 'react'` |
| `imrpc` | Import React with PureComponent | `import React, { PureComponent } from 'react'` |
| `imrpcp` | Import React with PureComponent & PropTypes | `import PropTypes from 'prop-types'; import React, { PureComponent } from 'react'` |
| `imrn` | Import React Native | `import { View, Text } from 'react-native'` |
| `impt` | Import PropTypes | `import PropTypes from 'prop-types'` |
| `imp` | Import Default | `import module from 'path'` |
| `imd` | Import Destructured | `import { item } from 'path'` |
| `ime` | Import Everything as Namespace | `import * as alias from 'path'` |
| `ima` | Import as Alias | `import { item as alias } from 'path'` |
| `imn` | Import without Module Name | `import 'path'` |
| `imbr` | Import Browser Router | `import { BrowserRouter as Router } from 'react-router-dom'` |
| `imrr` | Import Router with Route & NavLink | `import { BrowserRouter as Router, Route, NavLink } from 'react-router-dom'` |

---

### 🛡️ PropTypes Snippets

| Trigger | Output | Trigger | Output |
| :--- | :--- | :--- | :--- |
| `pts` | `PropTypes.string` | `ptsr` | `PropTypes.string.isRequired` |
| `ptn` | `PropTypes.number` | `ptnr` | `PropTypes.number.isRequired` |
| `ptb` | `PropTypes.bool` | `ptbr` | `PropTypes.bool.isRequired` |
| `pta` | `PropTypes.array` | `ptar` | `PropTypes.array.isRequired` |
| `pto` | `PropTypes.object` | `ptor` | `PropTypes.object.isRequired` |
| `ptf` | `PropTypes.func` | `ptfr` | `PropTypes.func.isRequired` |
| `ptnd` | `PropTypes.node` | `ptndr` | `PropTypes.node.isRequired` |
| `ptel` | `PropTypes.element` | `ptelr` | `PropTypes.element.isRequired` |
| `ptany` | `PropTypes.any` | `ptsh` | `PropTypes.shape({ ... })` |
| `ptshr` | `PropTypes.shape({ ... }).isRequired` | `ptex` | `PropTypes.exact({ ... })` |
| `ptexr` | `PropTypes.exact({ ... }).isRequired` | `ptao` | `PropTypes.arrayOf(...)` |
| `ptaor` | `PropTypes.arrayOf(...).isRequired` | `ptoo` | `PropTypes.objectOf(...)` |
| `ptoor` | `PropTypes.objectOf(...).isRequired` | `pte` | `PropTypes.oneOf([...])` |
| `pter` | `PropTypes.oneOf([...]).isRequired` | `ptet` | `PropTypes.oneOfType([...])` |
| `ptetr` | `PropTypes.oneOfType([...]).isRequired` | `pti` | `PropTypes.instanceOf(...)` |
| `ptir` | `PropTypes.instanceOf(...).isRequired` | | |

---

### 🔍 Console & Debugging

| Trigger | Description | Output |
| :--- | :--- | :--- |
| `clg` | Console Log | `console.log(variable)` |
| `clo` | Console Log Object | `console.log('variable', variable)` |
| `clj` | Console Log JSON Pretty | `console.log('variable', JSON.stringify(variable, null, 2))` |
| `cer` | Console Error | `console.error(error)` |
| `cwa` | Console Warn | `console.warn(warning)` |
| `cin` | Console Info | `console.info(info)` |
| `ctl` | Console Table | `console.table([data])` |
| `ctm` | Console Time | `console.time('label')` |
| `cte` | Console Time End | `console.timeEnd('label')` |
| `ctr` | Console Trace | `console.trace(error)` |
| `cgr` | Console Group | `console.group('label')` |
| `cge` | Console Group End | `console.groupEnd()` |
| `cco` | Console Count | `console.count(label)` |
| `ccl` | Console Clear | `console.clear()` |
| `cdi` | Console Dir | `console.dir(object)` |
| `cas` | Console Assert | `console.assert(assertion, message)` |

---

### 🧪 Testing (Jest / React Testing)

| Trigger | Description | Output |
| :--- | :--- | :--- |
| `desc` | Describe Block | `describe('suite', () => { ... })` |
| `test` | Test Block | `test('should ...', () => { ... })` |
| `testa` | Async Test Block | `test('should ...', async () => { ... })` |
| `tit` | It Block | `it('should ...', () => { ... })` |
| `tita` | Async It Block | `it('should ...', async () => { ... })` |
| `stest` | React Snapshot Test | Setup React snapshot test with `react-test-renderer` |
| `srtest` | React Redux Test | Setup React Component test wrapped in Redux `Provider` |
| `sntest` | React Native Test | Setup React Native snapshot test |
| `snrtest` | React Native Redux Test | Setup React Native test with Redux `Provider` |

---

### 🛠️ Helpers & JavaScript Utilities

| Trigger | Description | Output |
| :--- | :--- | :--- |
| `anfn` | Anonymous Function | `(params) => { ... }` |
| `nfn` | Named Arrow Function | `const func = (params) => { ... }` |
| `dob` | Destructure Object | `const { prop } = object;` |
| `dar` | Destructure Array | `const [item] = array;` |
| `prom` | Return New Promise | `return new Promise((resolve, reject) => { ... });` |
| `sto` | Set Timeout | `setTimeout(() => { ... }, delay);` |
| `sti` | Set Interval | `setInterval(() => { ... }, interval);` |
| `fre` | Array forEach | `array.forEach(item => { ... });` |
| `fof` | For...of Loop | `for (let item of iterable) { ... }` |
| `fin` | For...in Loop | `for (let prop in object) { ... }` |
| `exp` | Export Default | `export default item;` |
| `exd` | Export Destructured | `export { item } from 'path';` |
| `exa` | Export as Alias | `export { item as alias } from 'path';` |
| `enf` | Export Named Function | `export const func = (params) => { ... };` |
| `edf` | Export Default Arrow Function | `export default (params) => { ... };` |
| `ednf` | Export Default Named Function | `export default function func(params) { ... };` |
| `bnd` | Bind Method to `this` | `this.method = this.method.bind(this);` |
| `cp` | Destructure `this.props` | `const { prop } = this.props;` |
| `cs` | Destructure `this.state` | `const { state } = this.state;` |
| `sst` | Set State Object | `this.setState({ ... });` |
| `ssf` | Set State Function | `this.setState((state, props) => ({ ... }));` |
| `cref` | Create Ref | `this.myRef = React.createRef();` |
| `cmmb` | Comment Multi-line Block | Block JSDoc comment |

## Credits & Acknowledgements

- Ported to Zed by **[KAGU](https://github.com/kagulion)**.
- Based on the original WebStorm plugin [Modern React Snippets](https://github.com/anuragkanwar/modern-react-snippets-plugin) by [Anurag Kanwar](https://github.com/anuragkanwar).
- Inspired by [ES7+ React/Redux/React-Native snippets](https://github.com/ults-io/vscode-react-javascript-snippets) by [dsznajder](https://github.com/dsznajder) / ULTS.

## 📄 License

This project is licensed under the [MIT License](LICENSE.md) — see the [LICENSE.md](LICENSE.md) file for details.

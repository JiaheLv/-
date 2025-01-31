# 毕业设计代码流程记录

## 环境配置

- Ubuntu    24.04.1 LTS
- Geth      1.14.12-stable-293a300d
  
  ```bash
  sudo apt-get install software-properties-common
  sudo add-apt-repository -y ppa:ethereum/ethereum
  sudo apt-get update
  sudo apt-get install ethereum
  ```

- Solidity  0.8.28+commit.7893614a.Linux.g++

  ```bash
  sudo add-apt-repository -y ppa:ethereum/ethereum
  sudo apt-get update
  sudo apt-get install solc
  ```

- Nodejs    18.19.1
  
  ```bash
  sudo apt-get install -y nodejs
  ```

- Npm       9.2.0
  
  ```bash
  sudo apt-get install npm
  ```

- Truffle   v5.11.5 (core: 5.11.5)
  
  ```bash
  npm install -g truffle
  ```

### 问题记录

#### truffle 安装 warn

```bash
lvjiahe@LvJh:~$ sudo npm install -g truffle

npm WARN deprecated @ensdomains/resolver@0.2.4: Please use @ensdomains/ens-contracts
npm WARN deprecated rimraf@2.7.1: Rimraf versions prior to v4 are no longer supported
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated mkdirp-promise@5.0.1: This package is broken and no longer maintained. 'mkdirp' itself supports promises now, please switch to that.
npm WARN deprecated memdown@1.4.1: Superseded by memory-level (https://github.com/Level/community#faq)
npm WARN deprecated deferred-leveldown@5.3.0: Superseded by abstract-level (https://github.com/Level/community#faq)
npm WARN deprecated level-js@5.0.2: Superseded by browser-level (https://github.com/Level/community#faq)
npm WARN deprecated levelup@4.4.0: Superseded by abstract-level (https://github.com/Level/community#faq)
npm WARN deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm WARN deprecated leveldown@5.6.0: Superseded by classic-level (https://github.com/Level/community#faq)
npm WARN deprecated glob@7.2.0: Glob versions prior to v9 are no longer supported
npm WARN deprecated multibase@0.6.1: This module has been superseded by the multiformats module
npm WARN deprecated multicodec@0.5.7: This module has been superseded by the multiformats module
npm WARN deprecated cids@0.7.5: This module has been superseded by the multiformats module
npm WARN deprecated apollo-server-plugin-base@3.7.2: The `apollo-server-plugin-base` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated apollo-datasource@3.3.2: The `apollo-datasource` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated apollo-server-errors@3.3.1: The `apollo-server-errors` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated apollo-server-env@4.2.1: The `apollo-server-env` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/utils.fetcher` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated apollo-reporting-protobuf@3.4.0: The `apollo-reporting-protobuf` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/usage-reporting-protobuf` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated apollo-server-types@3.8.0: The `apollo-server-types` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated apollo-server-express@3.13.0: The `apollo-server-express` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated apollo-server-core@3.13.0: The `apollo-server-core` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated @truffle/interface-adapter@0.5.37: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated testrpc@0.0.1: testrpc has been renamed to ganache-cli, please use this package from now on.
npm WARN deprecated @truffle/promise-tracker@0.1.7: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/dashboard-message-bus-common@0.1.7: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/spinners@0.2.5: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/dashboard-message-bus-client@0.1.12: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/compile-common@0.9.8: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @ensdomains/ens@0.4.5: Please use @ensdomains/ens-contracts
npm WARN deprecated @truffle/events@0.1.25: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/source-map-utils@1.3.119: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/error@0.2.2: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated apollo-server@3.13.0: The `apollo-server` package is part of Apollo Server v2 and v3, which are now end-of-life (as of October 22nd 2023 and October 22nd 2024, respectively). This package's functionality is now found in the `@apollo/server` package. See https://www.apollographql.com/docs/apollo-server/previous-versions/ for more details.
npm WARN deprecated abstract-leveldown@7.2.0: Superseded by abstract-level (https://github.com/Level/community#faq)
npm WARN deprecated @truffle/codec@0.17.3: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/provider@0.3.13: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/config@1.3.61: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/code-utils@3.0.4: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/abi-utils@1.0.3: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/db-loader@0.2.36: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated @truffle/debugger@12.1.5: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated @truffle/db@2.0.36: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.
npm WARN deprecated abstract-leveldown@6.2.3: Superseded by abstract-level (https://github.com/Level/community#faq)
npm WARN deprecated abstract-leveldown@6.3.0: Superseded by abstract-level (https://github.com/Level/community#faq)
npm WARN deprecated abstract-leveldown@6.2.3: Superseded by abstract-level (https://github.com/Level/community#faq)
npm WARN deprecated multibase@0.7.0: This module has been superseded by the multiformats module
npm WARN deprecated abstract-leveldown@2.7.2: Superseded by abstract-level (https://github.com/Level/community#faq)
npm WARN deprecated abstract-leveldown@6.2.3: Superseded by abstract-level (https://github.com/Level/community#faq)
npm WARN deprecated uuid@2.0.1: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated multicodec@1.0.4: This module has been superseded by the multiformats module

added 1166 packages in 4m

100 packages are looking for funding
  run `npm fund` for details
```

#### flag provided but not defined: --rpc

> 版本更新导致的命令行参数变化  
> 使用`--http`代替`--rpc`  
> 使用`--http.api`代替`--rpcapi`  
> 使用`--http.cordomain`代替`--rpccorsdomain`  
> 参考：[https://github.com/ethereum/go-ethereum/wiki/Command-Line-Options](https://github.com/ethereum/go-ethereum/wiki/Command-Line-Options)

# waf.hook {#wafhook}

[Waf](https://waf.io) is a Python-based software building system.

In Nixpkgs, `waf.hook` overrides the default configure, build, and install phases.

## Variables controlling waf.hook {#variablesControllingWafHook}

### `wafPath` {#wafPath}

Location of the `waf` tool. It defaults to `./waf`, to honor software projects that include it directly inside their source trees.

If `wafPath` doesn't exist, then `waf.hook` will copy the `waf` provided from Nixpkgs to it.

### `wafConfigureFlags` {#wafConfigureFlags}

Controls the flags passed to waf tool during configure phase.

### `wafFlags` {#wafFlags}

Controls the flags passed to waf tool during build and install phases.

### `dontAddWafCrossFlags` {#dontAddWafCrossFlags}

When set to `true`, don't add cross compilation flags during configure phase.

### `dontUseWafConfigure` {#dontUseWafConfigure}

When set to true, don't use the predefined `wafConfigurePhase`.

### `dontUseWafBuild` {#dontUseWafBuild}

When set to true, don't use the predefined `wafBuildPhase`.

### `dontUseWafInstall` {#dontUseWafInstall}

When set to true, don't use the predefined `wafInstallPhase`.

### Variables honored by waf.hook {#variablesHonoredByWafHook}

The following variables commonly used by `stdenv.mkDerivation` are also honored by `waf.hook`.

- `prefixKey`
- `configureTargets`
- `enableParallelBuilding`
- `enableParallelInstalling`
- `buildFlags`
- `buildTargets`
- `installFlags`
- `installTargets`

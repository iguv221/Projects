
# R (via apt) (r-apt)

Installs the latest R, some R packages, and needed dependencies. Note: May require source code compilation for some R packages.

## Example Usage

```json
"features": {
    "ghcr.io/rocker-org/devcontainer-features/r-apt:0": {}
}
```

## Options

| Options Id | Description | Type | Default Value |
|-----|-----|-----|-----|
| vscodeRSupport | Install R packages to make vscode-R work. lsp means the `languageserver` package, full means lsp plus the `httpgd` package. | string | minimal |
| installDevTools | Install the `devtools` R package. | boolean | false |
| installREnv | Install the `renv` R package. | boolean | false |
| installRMarkdown | Install the `rmarkdown` R package. It is required for R Markdown or Quarto documentation. | boolean | false |
| installJupyterlab | Install and setup JupyterLab (via `python3 -m pip`). JupyterLab is a web-based interactive development environment for notebooks. | boolean | false |
| installRadian | Install radian (via `python3 -m pip`). radian is an R console with multiline editing and rich syntax highlight. | boolean | false |
| installVscDebugger | Install the `vscDebugger` R package from the GitHub repo. It is required for the VSCode-R-Debugger. | boolean | false |
| useTesting | For Debian, install packages from Debian testing. If false, the R package installed by apt may be out of date. | boolean | true |
| installBspm | Install and enable BSPM (Bridge to System Package Manager) to install R packages. This option is only working on Ubuntu now. | boolean | false |

## Customizations

### VS Code Extensions

- `REditorSupport.r`

<!-- markdownlint-disable MD041 -->

## Supported platforms

`linux/amd64` platform `debian`, `ubuntu:focal` and `ubuntu:jammy`.

If the `useTesting` is `true`, `linux/arm64` platform `debian` also supported.

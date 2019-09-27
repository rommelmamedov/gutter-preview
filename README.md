# Image Preview - Visual Studio Code Extension

Shows image preview in the gutter and on hover

## It looks like this

![Demonstrating svg image preview in a css file](https://raw.githubusercontent.com/kisstkondoros/gutter-preview/master/images/sample.png)

## Install

[How to install Visual Studio Code extensions](https://code.visualstudio.com/docs/editor/extension-gallery)

[Direct link to Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-gutter-preview)

### Change Log

-   0.23.0
    -   Added webp to acceptedExtensions (contribution by @Afsar-Pasha)
-   0.22.3
    -   Fix handling of special characters in URIs
-   0.22.2
    -   Fix file URI handling
-   0.22.1
    -   Remove unnecessary files from the package
-   0.22.0
    -   Use webpack to bundle the extension
    -   Update to vscode@1.37.0
    -   Check CancellationToken while collecting resource references
-   0.21.1
    -   Disable reference resolution by default
-   0.21.0
    -   Show images defined in constant classes
-   0.20.0
    -   Add currentColor configuration support for SVGs
-   0.19.5
    -   Fix data uri handling (contribution by @rafaelkendy)
-   0.19.4
    -   Prepend file protocol to image url in the hover preview (bug fix for Remote - WSL)
-   0.19.3
    -   Add special case extracting urls from between braces for latex
-   0.19.2
    -   Downgrade vscode-languageclient and -server to 5.21
-   0.19.1
    -   Update dependencies
-   0.19.0
    -   Add ico to accepted extensions
-   0.18.0
    -   Add "Reveal in Side Bar" link to hover message
-   0.17.5
    -   Fix processing of js/tsconfig path section
-   0.17.4
    -   Ensure loadPathsFromTSConfig always returns at least an empty object
    -   Update runtime dependencies
-   0.17.3
    -   Fix and adjust loading of path aliases from js/tsconfig
-   0.17.2
    -   Remove trailing wildcard from js/tsconfig path mappings
-   0.17.1
    -   Add typescript as runtime dependency
-   0.17.0
    -   Add support for path aliases defined by config property or by js/tsconfig
        -   see path mapping in the [typescript documentation](https://www.typescriptlang.org/docs/handbook/module-resolution.html#path-mapping) for further details
            Please note that a restart is necessary after changing the js/tsconfig.json.
-   0.16.5
    -   Replace probe-image-size with image-size
-   0.16.4
    -   Update dependencies
-   0.16.3
    -   Avoid repeated decorations when word wrapping is enabled
-   0.16.2
    -   Handle error explicitly when requesting resources from the network
-   0.16.1
    -   Fix typo in readme
-   0.16.0
    -   Fix image size calculation
    -   Fix image path handling under Windows
    -   Require vscode version 1.28.0
    -   Make use of ImageCache for faster image path verification
    -   Implement partial scan and proper cancellation token handling
-   0.15.3
    -   Skip lines longer than 20k when searching for potential links
    -   Fix runtime dependency issue (slash)
-   0.15.2
    -   Restore vscode.Uri based image handling for decorations
-   0.15.1
    -   Update dependencies
    -   Add scope for configuration properties
-   0.15.0
    -   Change casing of configuration options (by Orhan Sönmez)
    -   Add option (`gutterpreview.showUnderline`) to disable link like underline (by Orhan Sönmez)
    -   Use more flexible pattern for data url detection
    -   Fix path resolution for urls relative to the workspace folder
-   0.14.2
    -   Fix several windows compatiblity issues
-   0.14.1
    -   Add null checks around editor instances
-   0.14.0
    -   Remove onFileChange callback from ImageCache
    -   Fix throttledScan implementation
    -   Add recognizer for data Urls
    -   Reformat package json
    -   Add underline to recognized urls
    -   Dispose unused decorations
    -   Detect more than one url in a single line
    -   Use column metadata from recognizers
    -   Pass workspacefolder for the given document explicitly
    -   Remove superfluous recognizers
    -   Replace onLanguage activation events with '\*'
    -   Move link search logic off the extension host
    -   Add localLinkRecognizer
    -   Add workspace.rootPath as fallback to RelativeToWorkspaceRootFileUrlMapper
    -   Simplify recognizer execution
    -   Reorganize variables
    -   Move temporary file handling to imagecache
    -   Simplify disposable handling
    -   Extract ImageCache
    -   Extract mappers and recognizers from extension.ts
    -   Add prettier along with husky to ensure consistent formatting
    -   Remove unused variables
    -   Remove unused dependency: base64-img
    -   Remove unused imports
    -   Add linkRecognizer
    -   Support hover preview in output tab
    -   Reformat extension.ts
-   0.13.1
    -   Avoid NPE for invalid URL's
-   0.13.0
    -   Add new configuration property 'gutterpreview.imagepreviewmaxheight'
-   0.12.2
    -   Only consider path name in file system based url mappers
-   0.12.1
    -   Adjust file lookup and add multi root support
-   0.12.0
    -   Avoid file locks by using temp files
-   0.11.4
    -   Support lookup in template strings
-   0.11.3
    -   Add missing protocol check
-   0.11.2
    -   Updated the python regex to account for lines with multiple strings
-   0.11.1
    -   Remove path separator replacements
-   0.11.0
    -   Added a python image filename recognizer
-   0.10.2
    -   Provide fallback for http hosted images
-   0.10.1
    -   Attempt to fix path join on macOS Sierra
-   0.10.0
    -   Add info about image size to hover preview
    -   Show hover preview without file type restriction
-   0.9.1
    -   Ignore workspace relative url mapper when there is no workspace at all
-   0.9.0
    -   Support images in markdown files
-   0.8.0
    -   Change Extension name to Image Preview
    -   Add option ("showimagepreviewongutter") to disable image preview on the gutter
-   0.7.2
    -   Set image height on supported vscode versions
-   0.7.1
    -   Update changelog
-   0.7.0
    -   Add http scheme for // urls
-   0.6.2
    -   Run recognition also when the activeTextEditor is changed
    -   Fix image url detection RegExp
-   0.6.1
    -   Support old and new RenderOptions API
-   0.6.0
    -   Add image src recognizer
-   0.5.0
    -   Added "gutterpreview.sourcefolder" configuration variable
-   0.4.1
    -   Add image hover provider to scss files as well
-   0.4.0
    -   Add html to supported file types
    -   Dedupe recognized urls
    -   Format source code
    -   Add http/https url matcher
    -   Fix file url creation
-   0.3.0
    -   Support data URI's in hover widget
-   0.2.3
    -   VSCode engine dependency changed to allow further versions
-   0.2.2
    -   Hack is now unnecessary it was removed from the readme
-   0.2.1
    -   Readme updated
-   0.2.0
    -   code restricted to work on css/scss/less files
    -   hacks removed
-   0.1.0
    -   Image preview shown on hover as well
-   0.0.3
    -   Displayname fixed
-   0.0.2
    -   Sample image attached
-   0.0.1
    -   Initial project setup

### License

Licensed under MIT

## API Report File for "@momentum-design/token-builder"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { Config as Config_2 } from 'style-dictionary';
import { File as File_3 } from 'style-dictionary';
import { Format as Format_2 } from 'style-dictionary';
import { Formatter } from 'style-dictionary';
import type { Named } from 'style-dictionary';
import type { Platform as Platform_2 } from 'style-dictionary';
import type { Transform as Transform_2 } from 'style-dictionary';
import { TransformedToken } from 'style-dictionary';

// @public (undocumented)
export interface Config {
    // (undocumented)
    files: Array<ConfigFile>;
    // (undocumented)
    formats: Array<Format>;
    // (undocumented)
    prefix: string;
    // (undocumented)
    schemaFiles?: Array<string>;
    // (undocumented)
    strict?: boolean;
    // Warning: (ae-forgotten-export) The symbol "Transform" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    transforms?: Array<Transform>;
}

// @public (undocumented)
export interface ConfigFile {
    // (undocumented)
    cssSelector?: string;
    // (undocumented)
    destination: string;
    // (undocumented)
    filters?: Filters;
    // (undocumented)
    iosAccessControl?: string;
    // (undocumented)
    iosImport?: string | Array<string>;
    // (undocumented)
    iosObjectType?: string;
    // (undocumented)
    outputReferences?: boolean;
    // (undocumented)
    scssThemeable?: boolean;
    // (undocumented)
    showFileHeader?: boolean;
    // (undocumented)
    targets: Array<string>;
}

// @public (undocumented)
export const CONSTANTS: {
    FILE_ENCODING: "utf-8";
    FORMATS: {
        MD_JSON_MINIMAL: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        CSS_VARIABLES: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        SCSS_VARIABLES: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        WEB_JSON: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        ANDROID_RESOURCES: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        SWIFT_CLASS: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
    };
    LOCAL_FORMATS: {
        MD_JSON_MINIMAL: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
    };
    LOCAL_TRANSFORMS: {
        MD_ELEVATION: string;
    };
    SD_FORMATS: {
        CSS_VARIABLES: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        SCSS_VARIABLES: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        WEB_JSON: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        ANDROID_RESOURCES: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
        SWIFT_CLASS: {
            EXTENSION: string;
            FORMAT: string;
            GROUP: string;
            NAME: string;
            PATH: string;
        };
    };
    SD_TRANSFORMS: {
        ATTRIBUTE_CTI: string;
        NAME_CTI_KABAB: string;
    };
    TRANSFORMS: {
        MD_ELEVATION: string;
        ATTRIBUTE_CTI: string;
        NAME_CTI_KABAB: string;
    };
};

// @public (undocumented)
export class Dictionary {
    constructor(config: DictionaryConfig);
    // (undocumented)
    protected config: DictionaryConfig;
    // (undocumented)
    get formats(): Array<Format>;
    // (undocumented)
    get input(): string;
    // (undocumented)
    get output(): string;
    // (undocumented)
    get platforms(): Record<string, Platform>;
    // (undocumented)
    get prefix(): string | undefined;
    // (undocumented)
    get sdConfig(): Config_2;
    // (undocumented)
    get targets(): Array<string>;
}

// @public (undocumented)
export interface DictionaryConfig {
    // (undocumented)
    file: ConfigFile;
    // (undocumented)
    formats: Array<Format>;
    // (undocumented)
    input: string;
    // (undocumented)
    output: string;
    // (undocumented)
    prefix: string;
    // (undocumented)
    transforms?: Array<Transform>;
}

// @public (undocumented)
export class ElevationTransform {
    constructor(config?: ElevationTransformConfig);
    // (undocumented)
    protected config: ElevationTransformConfig;
    // Warning: (ae-forgotten-export) The symbol "CONSTANTS_3" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    static get CONSTANTS(): typeof CONSTANTS_3;
    // (undocumented)
    get matcher(): ElevationTransformMatcher;
    // (undocumented)
    get name(): string;
    // (undocumented)
    get sdConfig(): Named<Transform_2>;
    // (undocumented)
    get transformer(): ElevationTransformTransformer;
    // (undocumented)
    get transitive(): boolean | undefined;
    // (undocumented)
    get type(): ElevationTransformType;
}

// @public (undocumented)
export interface ElevationTransformConfig {
    // (undocumented)
    transitive?: boolean;
}

// @public (undocumented)
export type ElevationTransformMatcher = (token: ElevationTransformToken) => boolean;

// @public (undocumented)
export type ElevationTransformToken = TransformedToken;

// @public (undocumented)
export type ElevationTransformTransformer = (token: ElevationTransformToken) => any;

// @public (undocumented)
export type ElevationTransformType = 'attribute' | 'name' | 'value';

// @public
class File_2 {
    constructor(config: FileConfig);
    get categories(): Array<string>;
    // (undocumented)
    protected config: FileConfig;
    // (undocumented)
    get destination(): string;
    // (undocumented)
    get extension(): string;
    // (undocumented)
    get file(): string;
    // (undocumented)
    get filter(): (token: TransformedToken) => boolean;
    // (undocumented)
    get format(): string;
    // (undocumented)
    get iosAccessControl(): string | undefined;
    // (undocumented)
    get iosImport(): string | Array<String> | undefined;
    // (undocumented)
    get iosObjectType(): string | undefined;
    // (undocumented)
    get items(): Array<string>;
    // (undocumented)
    get references(): boolean;
    // (undocumented)
    get scssThemeable(): boolean;
    // (undocumented)
    get sdConfig(): File_3;
    // (undocumented)
    get selector(): string | undefined;
    // (undocumented)
    get showFileHeader(): boolean;
    // (undocumented)
    get types(): Array<string>;
}
export { File_2 as File }

// @public (undocumented)
export interface FileConfig {
    // (undocumented)
    cssSelector?: string;
    // (undocumented)
    destination: string;
    // (undocumented)
    filters?: Filters;
    // (undocumented)
    format: Format;
    // (undocumented)
    iosAccessControl?: string;
    // (undocumented)
    iosImport?: string | Array<string>;
    // (undocumented)
    iosObjectType?: string;
    // (undocumented)
    outputReferences?: boolean;
    // (undocumented)
    scssThemeable?: boolean;
    // (undocumented)
    showFileHeader?: boolean;
}

// @public (undocumented)
export type Filter = Array<string>;

// @public (undocumented)
export interface Filters {
    // (undocumented)
    categories?: Filter;
    // (undocumented)
    items?: Filter;
    // (undocumented)
    types?: Filter;
}

// @public (undocumented)
export type Format = keyof typeof CONSTANTS.FORMATS;

// @public (undocumented)
export class JsonMinimalFormat {
    // Warning: (ae-forgotten-export) The symbol "CONSTANTS_2" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    static get CONSTANTS(): typeof CONSTANTS_2;
    // (undocumented)
    get formatter(): Formatter;
    // (undocumented)
    get name(): string;
    // (undocumented)
    get sdConfig(): Format_2;
}

// @public (undocumented)
export class Platform {
    constructor(config: PlatformConfig);
    // (undocumented)
    protected config: PlatformConfig;
    // (undocumented)
    get file(): File_2;
    // (undocumented)
    get format(): Format;
    // (undocumented)
    get group(): string;
    // (undocumented)
    get output(): string;
    // (undocumented)
    get path(): string;
    // (undocumented)
    get prefix(): string | undefined;
    // (undocumented)
    get sdConfig(): Platform_2;
    // (undocumented)
    get transforms(): Array<string> | undefined;
}

// @public (undocumented)
export interface PlatformConfig {
    // (undocumented)
    file: ConfigFile;
    // (undocumented)
    format: Format;
    // (undocumented)
    output: string;
    // (undocumented)
    prefix?: string;
    // (undocumented)
    transforms?: Array<Transform>;
}

// @public (undocumented)
export class TokenBuilder {
    constructor(config: TokenBuilderConfig);
    // (undocumented)
    build(): Promise<this>;
    // (undocumented)
    static build(config: TokenBuilderConfig): Promise<TokenBuilder>;
    // (undocumented)
    protected config: TokenBuilderConfig;
    // (undocumented)
    initialize(): Promise<this>;
}

// @public (undocumented)
export interface TokenBuilderConfig {
    // (undocumented)
    config: Config | string;
    // (undocumented)
    input: string;
    // (undocumented)
    output: string;
}

// (No @packageDocumentation comment for this package)

```
# WooCommerce PHPCS Configuration Packages

This repository contains the PHPCS configuration packages for WooCommerce.

## Usage

First add phpcs.xml file to yor project root directory.

```xml
<?xml version="1.0"?>
<ruleset name="WordPress Coding Standards">
	<description>WooCommerce extension PHP_CodeSniffer ruleset.</description>

	<exclude-pattern>*/vendor/*</exclude-pattern>

	<config name="minimum_supported_wp_version" value="4.7" />
	<config name="testVersion" value="7.2-" />

	<rule ref="WordPress-Core">
		<exclude name="Generic.WhiteSpace.IncrementDecrementSpacing" />
		<exclude name="Modernize.FunctionCalls.Dirname" />
		<exclude name="PEAR.Files.IncludingFile" />
		<exclude name="PSR12.Traits.UseDeclaration" />
		<exclude name="PSR2.Classes.ClassDeclaration.CloseBraceAfterBody" />
		<exclude name="PSR2.Files.EndFileNewline.TooMany" />
		<exclude name="PSR2.Methods.FunctionClosingBrace.SpacingBeforeClose" />
		<exclude name="Squiz.Functions.FunctionDeclarationArgumentSpacing" />
		<exclude name="Universal.Constants.UppercaseMagicConstants" />
		<exclude name="Universal.Namespaces" />
		<exclude name="Universal.UseStatements.NoLeadingBackslash" />
	</rule>

	<rule ref="WordPress-Extra">
		<exclude name="Generic.Commenting.DocComment.SpacingAfter" />
		<exclude name="Generic.Files.LineEndings.InvalidEOLChar" />
		<exclude name="Generic.Functions.FunctionCallArgumentSpacing.SpaceBeforeComma" />
		<exclude name="PEAR.Functions.FunctionCallSignature" />
		<exclude name="Squiz.Commenting" />
		<exclude name="Squiz.PHP.DisallowSizeFunctionsInLoops.Found" />
		<exclude name="Squiz.WhiteSpace" />
		<exclude name="WordPress.Arrays" />
		<exclude name="WordPress.Files.FileName" />
		<exclude name="WordPress.NamingConventions" />
		<exclude name="WordPress.Security.EscapeOutput.ErrorNotEscaped" />
		<exclude name="WordPress.Security.EscapeOutput.ExceptionNotEscaped" />
		<exclude name="WordPress.Security.ValidatedSanitizedInput.MissingUnslash" />
		<exclude name="WordPress.WhiteSpace" />
		<exclude name="WordPress.WP.I18n.NonSingularStringLiteralText" />

		<exclude name="Universal.CodeAnalysis.NoEchoSprintf" />
		<exclude name="Universal.ControlStructures.DisallowLonelyIf" />
		<exclude name="Universal.Files.SeparateFunctionsFromOO" />
		<exclude name="WordPress.WP.I18n.EmptyTextDomain" />

		<exclude name="NormalizedArrays.Arrays.ArrayBraceSpacing" />
		<exclude name="NormalizedArrays.Arrays.CommaAfterLast" />

		<exclude name="Generic.WhiteSpace.LanguageConstructSpacing" />
		<exclude name="Squiz.Functions.MultiLineFunctionDeclaration" />
		<exclude name="Universal.WhiteSpace" />
	</rule>

	<rule ref="WooCommerce-Core">
		<exclude name="Core.Commenting.CommentTags.AuthorTag" />
		<exclude name="Generic.WhiteSpace.ScopeIndent.Incorrect" />
		<exclude name="Universal.Arrays.DisallowShortArraySyntax" />
		<exclude name="WooCommerce.Commenting.CommentHooks.HookCommentWrongStyle" />
		<exclude name="WooCommerce.Commenting.CommentHooks.MissingHookComment" />
		<exclude name="WooCommerce.Commenting.CommentHooks.MissingSinceComment" />
		<exclude name="WordPress.PHP.DontExtract" />
	</rule>

	<rule ref="PHPCompatibility">
		<exclude-pattern>tests/</exclude-pattern>
	</rule>
</ruleset>
```

```bash
git clone https://github.com/BeycanDeveloper/woocommerce-phpcs

# Run this command and install dependencies
cd phpcs-wp && composer install && cd ../phpcs-wc composer install && cd ../phpcs-compatibility-wp composer install && cd ../phpcs-utils composer install && cd ../phpcs-extra composer install && cd ../phpcs-compatibility-paragonie composer install && cd ../phpcs-compatibility composer install

# Run this command for phpcs know path

phpcs --config-set installed_paths C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-wp,C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-compatibility,C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-compatibility-paragonie,C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-compatibility-wp,C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-utils,C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-extra,C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-wc,C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-wc\\src\\WooCommerce,C:\\Users\\your-user-name\\Desktop\\woocommerce-phpcs\\phpcs-wc\\src\\WooCommerce-Core
```


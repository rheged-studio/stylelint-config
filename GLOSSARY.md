# Stylelint Config

The estate's shared Stylelint configuration, `@rheged-studio/stylelint-config`: one preset that every Rheged Studio project extends so CSS is linted the same way across the stack.

## Language

**Preset**:
The single exported Stylelint config object, compiled from `src/index.ts` to `dist/index.js` and extended by consumers as `@rheged-studio/stylelint-config`. The package has one entry point and no named variants.
_Avoid_: Ruleset, shared config, base config

**Consumer**:
A project that installs the preset and extends it from its own `stylelint.config.mjs` or `.stylelintrc.json`. Consumers supply `stylelint` itself as a peer dependency and own their ignore globs.
_Avoid_: Downstream, host project, user

**Standard layer**:
The first layer of the preset, `stylelint-config-standard`, supplying the community baseline of modern CSS conventions.
_Avoid_: Base layer, default rules

**Tailwind layer**:
The second layer of the preset, `stylelint-config-tailwindcss`, listed after the standard layer so it wins the `at-rule-no-unknown` and `function-no-unknown` overrides and Tailwind syntax lints cleanly.
_Avoid_: Tailwind plugin, Tailwind override

**Tailwind assumption**:
The house default that every consumer uses Tailwind, which is why the Tailwind layer is always on and cannot be opted out of by choosing a different preset.
_Avoid_: Tailwind mode, Tailwind flag

**Alphabetical property order**:
The preset's ordering rule, `order/properties-alphabetical-order`, supplied by `stylelint-order`: declarations within a rule appear in alphabetical order so diffs stay small and placement is never debated.
_Avoid_: Property sorting, declaration order

**Fixture**:
`fixtures/tailwind.css`, a small stylesheet that exercises Tailwind directives and ordered declarations and must lint clean under the preset.
_Avoid_: Test file, sample

**Self-test**:
The repo's dogfooding check, in which its own `stylelint.config.mjs` extends the built `dist/index.js` and lints the fixture via `pnpm lint:css`. It needs `pnpm build` first.
_Avoid_: Smoke test, dogfood run

**Override**:
A consumer's own `rules` entry, placed after extending the preset, that changes or disables a preset rule, for example setting `order/properties-alphabetical-order` to `null`.
_Avoid_: Exception, opt-out

**Ignore globs**:
The file patterns a consumer excludes from linting through `.stylelintignore` or `ignoreFiles`. The preset deliberately ships none, so scoping is always the consumer's decision.
_Avoid_: Ignore list, exclusions

# BEM

> Block Element Modifier

This page focuses on the BEM Methodology in the context of structuring CSS in your applications.

Pull Requests Welcome!

## Why BEM?

> Replace "can you build this?" with "can you maintain this without losing your minds?" ~ [@necolas](https://twitter.com/necolas/status/360170108028600320?ref_src=twsrc%5Etfw)

## Learning BEM

- [Get BEM](http://getbem.com/introduction/)
- [Why BEM? In a Nushell](https://blog.decaf.de/2015/06/24/why-bem-in-a-nutshell/)
- [MindBEMding – getting your head ’round BEM syntax](https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)
- [How to Scale and Maintain Legacy CSS with Sass and SMACSS](https://webuild.envato.com/blog/how-to-scale-and-maintain-legacy-css-with-sass-and-smacss/)
- [Building a modular My Health Skills with BEM and Sass](http://bluegg.co.uk/blog/building-my-health-skills-part-3)
- [BEM 101](https://css-tricks.com/bem-101/)
- [About HTML semantics and front-end architecture](http://nicolasgallagher.com/about-html-semantics-front-end-architecture/) by Nicolas Gallager

## SUIT is BEM

SUIT is a BEM-like convention that I prefer.

### Quick Primer on SUIT ([source](https://webdesign.tutsplus.com/tutorials/using-postcss-with-bem-and-suit-methodologies--cms-24592))

SUIT comprises Utilities and Components. Within components there can be Modifiers, Descendants and States.

SUIT uses a combination of pascal case (PascalCase), camel case (camelCase) and dashes. Its conventions enforce a limit on the sometimes confusing number of dashes and underscores that can appear in BEM. For example, the BEM class `.search-form__text-field` would be `.SearchForm-textField` in SUIT.

#### Utility
Utilities handle structure and positional styling, and are written in such a way that they can be applied anywhere in a component. They are prefixed with `u-` and written in camel case. For example, `.u-clearFix`.

#### Component
A component in SUIT takes the place of a block in BEM. Components are always written in pascal case and are only part of SUIT that uses pascal case, making them easy to identify. For example, `.SearchForm`.

#### Component Namespace

Components can optionally be prefixed with a namespace and single dash nmsp- to ensure conflicts are prevented, e.g. `.mine-SearchForm`.

#### Descendent
A descendent in SUIT replaces an element in BEM. It uses a single dash - and is written in camel case. For example `.SearchForm-heading`, `.SearchForm-textField` and `.SearchForm-submitButton`.

#### Modifier
SUIT uses modifiers as does BEM, however their role is more tightly controlled. A SUIT modifier is generally only applied directly to a component, not to a descendent. It should also not be used to represent state changes, as SUIT has a dedicated naming convention for states.

Modifiers are written in camel case and are preceded by two dashes `--`. For example,  `.SearchForm--advanced`.

#### State
State classes can be used to reflect changes to a component’s state. This allows them to be clearly differentiated from modifiers, which reflect modification of a component’s base appearance regardless of state. If necessary, a state can also be applied to a descendent.

States are prefixed with `is-` and are written in camel case. They are also always written as adjoining classes. For example  `.SearchForm.is-invalid`.

## SUIT CHEATSHEET

```
// Namespace can be used with the camelCase prefix `.name-`
.mine-ComponentName {}

// Components are PascalCase
.ComponentName {}

// Descendents are cascalCase with single dash
.ComponentName-descendentName {}

// Modifiers are cascalCase with double dash
// Modifiers are only applied to a Component, not a descendent
.ComponentName--modifierName {}

// State can be applied to descendents and components
// using the `.is-` prefix
.ComponentName.is-stateName {}
.ComponentName-descendentName.is-stateName {}

```


## Videos

- [Our CSS Best Practices are Killing Us](https://vimeo.com/72759139) by Nicole Sullivan

## Tools

- [Parker](https://github.com/katiefenn/parker) Stylesheet analysis tool
  - [Improving your CSS with Parker](https://csswizardry.com/2016/06/improving-your-css-with-parker/)

## CSS Wizards

The guys to follow when it comes to all things BEM.

- **Harry Roberts** [csswizardry.com](https://csswizardry.com) | [@CSSWizardry](https://twitter.com/csswizardry)
- **Nicolas Gallager** [nicolasgallagher.com](http://nicolasgallagher.com) | [@necolas](https://twitter.com/necolas)
- **Nicole Sullivan** [stubbornella.org](http://www.stubbornella.org/content/) | [@stubbornella](https://twitter.com/stubbornella)

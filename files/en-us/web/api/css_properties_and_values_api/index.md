---
title: CSS Properties and Values API
slug: Web/API/CSS_Properties_and_Values_API
page-type: web-api-overview
browser-compat:
  - api.CSSPropertyRule
  - api.CSS.registerProperty_static
---

{{DefaultAPISidebar("CSS Properties and Values API")}}

The **CSS Properties and Values API** — part of the [CSS Houdini](/en-US/docs/Web/API/Houdini) umbrella of APIs — allows developers to explicitly define their {{cssxref('--*', 'CSS custom properties')}}, allowing for property type checking, default values, and properties that do or do not inherit their value.

## Interfaces

- {{domxref('CSS/registerProperty_static', 'CSS.registerProperty')}}
  - : Defines how a browser should parse {{cssxref('--*', 'CSS custom properties')}}. Access this interface through {{domxref('CSS/registerProperty_static', 'CSS.registerProperty')}} in [JavaScript](/en-US/docs/Web/JavaScript).
- {{cssxref('@property')}}
  - : Defines how a browser should parse {{cssxref('--*', 'CSS custom properties')}}. Access this interface through {{cssxref('@property')}} [at-rule](/en-US/docs/Web/CSS/At-rule) in [CSS](/en-US/docs/Web/CSS).

## Examples

The following will register a {{cssxref('--*', 'CSS custom property')}} named `--my-prop` using {{domxref('CSS/registerProperty_static', 'CSS.registerProperty')}} in [JavaScript](/en-US/docs/Web/JavaScript). `--my-prop` will use the CSS color syntax, it will have a default value of `#c0ffee`, and it will not inherit its value:

```js
window.CSS.registerProperty({
  name: "--my-color",
  syntax: "<color>",
  inherits: false,
  initialValue: "#c0ffee",
});
```

The same registration can take place in [CSS](/en-US/docs/Web/CSS) using the {{cssxref('@property')}} [at-rule](/en-US/docs/Web/CSS/At-rule):

```css
@property --my-color {
  syntax: "<color>";
  inherits: false;
  initial-value: #c0ffee;
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [Using the CSS properties and values API](/en-US/docs/Web/API/CSS_Properties_and_Values_API/guide)
- [CSS Painting API](/en-US/docs/Web/API/CSS_Painting_API)
- [CSS Typed Object Model](/en-US/docs/Web/API/CSS_Typed_OM_API)
- [CSS Houdini](/en-US/docs/Web/API/Houdini)

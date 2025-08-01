# Accessibility Compat Data (ACD)

## What Is ACD?
Accessibility Compat Data (ACD) is a project to document
how web platform features are supported by assistive technologies (AT)
across different browsers. Inspired by the Browser Compatibility Data (BCD) project
which is integrated into developer resources like Mozilla Developer Network (MDN) and CanIUse,
ACD aims to bring accessibility interoperability data into the same developer ecosystem.

## Why It Matters
Currently, developers have no integrated way to check if a feature that 'works in a browser'
is also accessible to people using screen readers or other AT.
Tools like MDN show browser support, but not how screen readers interpret those features.

Web features can be visible and functional in a browser but unusable with assistive tech.

ACD addresses this by:

1. Tracking how features behave across browser + AT combinations
2. Surfacing this data in places developers already use
3. Helping teams spot issues earlier and avoid costly accessibility fixes later

## How is 'Accessible' Defined?
We will be using the WCAG 2.1 definition of
[accessibility-supported](https://www.w3.org/TR/WCAG21/#dfn-accessibility-supported).

> The way that the web content technology is used must be supported
> by users' assistive technology (AT). This means that the way that
> the technology is used has been tested for interoperability with
> users' assistive technology in the human language(s) of the content,
>
> AND
>
> The web content technology must have accessibility-supported
> user agents that are available to users. [...] The technology
> is supported natively in widely-distributed user agents
> that are also accessibility supported (such as HTML and CSS);

This means that the browser has to expose the web feature
to the accessibility tree **and** be supported by the AT.

## Key Goals
1. Define a machine-readable dataset to represent accessibility support for web features
2. Integrate accessibility data into MDN and other developer tooling
3. Support developers in building accessible experiences from the start
4. Reduce compliance burdens by making accessibility interoperability data more visible
5. Improve web experiences for users of assistive technologies

## What ACD Is Not
ACD is not an auditing tool and doesn’t evaluate entire websites. ACD does not define
a baseline, or mark features as accessible or inaccessible.

## Current Focus (Research Phase)
- Collaborating with browser vendors, documentation maintainers, and accessibility experts
- Scoping the dataset shape and testing methodology
- Running workshops and surveys to understand the needs of developers, accessibility
  professionals, and developer tooling maintainers.
- Identifying integration paths into existing resources like MDN

## Reading Material
- [Technical Gap & Scoping Report](/technical-gap-analysis-scope.md):
  Read the full report to explore what we’ve learned, what’s still unknown, and what's next.
- [Milestones](/milestones.md): Learn more about how we're measuring success for this
  phase of the project.  

## Get Involved

If your organisation cares about accessibility and better tooling for developers,
ACD is your chance to invest in infrastructure that makes the web work for everyone.

**Sponsor**: [Open Collective](https://give.lolaslab.co)
**Email**: lola@lolaslab.co

# Accessibility Compat Data (ACD)

**Note: For now, this repo documents the first phase of the Accessibility Compat Data project.**

## Background
The [Browser Compat Data](https://github.com/mdn/browser-compat-data) (BCD) project is a "machine-readable browser (and JavaScript runtime) compatibility data for Web technologies", this data is presented on MDN so that web developers can see the interoperability data for a given web feature, it's used in [Baseline](https://developer.mozilla.org/en-US/blog/baseline-unified-view-stable-web-features/) to measure what web features are "baseline", and many other developer tools. However, BCD doesn't give any information on the accessibility of a given feature, which means the tools that rely on BCD also don't take accessibility into consideration.

In 2024 the Interop Group made Accessibility a focus area and have carried that on into [2025](https://github.com/web-platform-tests/interop-accessibility/issues/148), part of the investigation area involves expanding the test suite to include expectations for various aria roles and attributes. However, this only tells part of the story, developers and tool maintainers want a way to know how web features are spoken or presented in AT-browser combinations. [aria-at](https://aria-at.w3.org) already does something similar to this, it provides interoperability reports for screen-reader-browser combinations however, it's been heavily focussed on APG. [a11ysupport.io](a11ysupport.io) also provides interoperability data but this is only for aria attributes.

## Proposal
This project, [Accessibility Compat Data](/proposal.md) (currently in the investigation phase), aims to create a dataset similar to BCD which includes AT-browser compatibility data for web features. The dataset will be machine-readable and show how web features are presented in various AT-browser combinations, developer resources like MDN and Baseline will be able to read and present the data to users which will hopefully lead to more informed web development and accessible web experiences. Have a read of the [proposal](/proposal.md) for more details and please don't hesitate to open an issue if you have questions.

## Funding

This project addresses a critical gap in the web platform: developers have no standardised, integrated way to understand how web features are supported by assistive technologies across different browsers. We know that developers already rely on tools like MDN and CanIUse to make decisions about browser support and this project extends that model to accessibility.

This initial phase is focused on research, scoping and strategic alignment. I'm working closely with standards bodies, browser vendors, documentation platforms and assistive technology stakeholders to define the scope, data model and methodology needed to make this project a reality.

To move this work forward, we’re seeking funding and support from organisations who understand the value of open-source infrastucture, developer enablement and the importance of accessible experiences. 

Your support will directly contribute to:
1. A shared, open dataset that helps developers understand real-world AT/browser interoperability
2. Better web experiences for users of screen-readers (& in the future, other assistive tech)
3. Accessibility interoperability data integrated into developer resources
4. Reduced compliance burden through earlier, evidence-based decision making
5. A more transparent and inclusive web ecosystem

If your organisation is committed to accessibility and improving the developer experience, this is an opportunity to support foundational work that has the potential to reshape how accessibility is implemented and understood on the web.
You can support by:
- Directly emailing me: lola@lolaslab.co
- [Sponsoring on Open Collective](https://give.lolaslab.co)
- ~~GitHub Sponsors~~



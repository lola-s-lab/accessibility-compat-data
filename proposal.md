# Proposal

*This first appeared on [lola's lab](https://lolaslab.co/blog/2025/accessibility-compat-data)*

Last year I ran an investigation into what it would take to add accessibility data into MDN. At the time I was focussed on including the interoperability reports for the W3C ARIA Authoring Practices Guide (APG) and the patterns themselves into MDN. Conversations on that are paused at the moment but it got me thinking more deeply about the kind of data web developers need when engaging with MDN and other web documentation.
Having been involved in the WebDX community group and various ARIA or ARIA-adjacent groups, when I speak or take part in workshops, people were saying variations of the same thing; "Baseline doesn't take accessibility into account", "How do I know how this web feature performs with X screen-reader in Y browser?". These complaints and questions all boil down to the same thing, something that many accessibility professionals and web developers have been asking about for years: screen-reader browser interoperability data for web features, aka the Accessibility Compat Dataset.

## The Idea
The Accessibility Compat Data (ACD) project addresses an important gap in web development, by collecting and integrating assistive technology (AT) and browser compatibility data for web features into widely used developer resources like MDN, Baseline and CanIUse, similar to the current Browser Compat Data (BCD).
Currently, there’s no central resource that shows how well web features are supported by screen readers in various browsers, leading to inaccessible experiences for users.
I want to work with AT & browser vendors, documentation sites, & accessibility experts to research the current landscape, and define a standardised dataset and methodology for collecting compatibility data.
The expected outcomes are:
1. A maintained open dataset
2. Better web experiences for users of screen-readers (& in the future, other assistive tech)
3. Accessibility compatibility data integrated into developer resources
4. Improved AT/browser interoperability
5. Better developer guidance for building accessible web experiences

This work aims to bridge the gap between specification and real-world implementation, empower developers to build more accessible web applications, and support compliance with digital accessibility regulations.

## The Current Landscape
Currently, there are two projects which provide accessibility interoperability data for web features:
1. a11ysupport.io, which provides data for ARIA attributes in AT/browser combinations. This data 
is very useful but not integrated into widely used developer documentation platforms, and is limited to only ARIA attributes.

2. The ARIA-AT project, which provides interoperability data for the patterns defined in the ARIA 
Authoring Practices Guide (APG). These patterns aren't web features but patterns defined by the APG task force making them also limited in scope.

The intention of ACD is to provide interoperability data for web features in general and present that data in an accessible way for web developers, browser vendors and AT vendors.

## Next Steps
Bringing the stakeholders together; as I mentioned earlier, I've already started talking to people in various groups about this project but will more formally bring the relevant stakeholders together. I'll be hosting a series of presentations in various groups, individual presentations and meetings with specific companies, etc.
Active fundraising; Currently, all the work I've put into this has been self-funded using my personal savings. I can't afford to continue to fund this work but the work is incredibly important, we have an opportunity to make a real impact across the web for both web users and web developers. I fundraise for all of my work through [Open Collective](https://opencollective.com/lolas-lab#category-CONTRIBUTE) which is a platform that provides a transparent ledger so sponsors can see how money is being spent. Funding I receive offline will also be logged in Open Collective.
Technical landscape and gap analysis report; the first phase of this project is to create a technical landscape and gap analysis. This report will help guide the solution and experiments we run, we know what's missing and what's needed but we also need to understand past endeavours, why solutions failed or didn't get wide adoption, how similar datasets function and integrate into various systems, etc. Thankfully, some of this work has already begun.


I'm really excited about this work, it's something various communities have been asking about for a long, long time. With the creation of Baseline and MDN, CanIUse, and Visual Studio integrating BCD into their resources, it's important that accessibility doesn't continue to be excluded.
I hope you'll join me on this journey!

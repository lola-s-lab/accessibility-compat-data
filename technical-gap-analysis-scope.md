# Technical Gap Analysis and Scope

## Background
Despite decades of progress in web standards and accessibility guidelines, real-world interoperability between assistive technologies and browsers remains inconsistent and undocumented in mainstream developer tools. Developers typically rely on resources like MDN and CanIUse to assess browser compatibility. However, these resources lack data on how assistive technologies interpret web features.

Accessibility Compat Data (ACD) is a project aimed at improving web accessibility 
by documenting browser and assistive tech support across the web platform. ACD will provide:
1. a structured way to track AT+browser support
2. integration with popular developer tooling & resources

Long-term, ACD could help identify patterns that inform spec clarifications, interoperability 
guidance, or implementation notes. As the European Accessibility Act comes into effect, 
many organisations are paying closer attention to their web presence and ensuring they are working within the legislation. Additionally, there's increased pressure from accessibility advocates, 
standards bodies, and legal professionals to ensure that assistive technology users have equitable access to the web.

In June 2025, I ran multiple workshops with representatives from Mozilla, Microsoft, Google, 
Tetralogical, Meta, Open Web Docs, and independent accessibility professionals. 
The consensus was that there is a need for ACD, and it should be researched further, 
especially since a major documentation platform reported receiving requests for accessibility compatibility data.

While the conversations and workshops have highlighted the need for ACD and surfaced alignment opportunities, 
some gaps remain, especially regarding understanding edge case interoperability behaviours 
and how this data should and can be displayed to developers.
This report shares what was learned, what's still unknown and immediate next steps.

## Technical Landscape & Gap Analysis
There are various accessibility interoperability datasets, including but not limited to aria-at, a11ysupport.io, 
HTML5 Accessibility, and Tetralogical's Screen-reader-HTML-support. However, for one reason or another, 
they only partially meet developer needs. None of the current offerings are integrated into popular 
developer tooling or resources. While Mozilla Developer Network (MDN) includes "accessibility considerations" 
on necessary pages, they have received requests for richer, more complete data on the interoperability 
of web features as it relates to accessibility. 

Having this data detached from popular developer resources undermines the importance 
and value of creating accessible web experiences. 
This forces developers to seek out accessibility compatibility data separately from general 
information on web features. In practice, only the developers who know to look for it 
will find it, leaving many users, who rely on assistive tech, unable to experience 
reliable or consistent functionality. Making accessibility compatibility data more 
visible also helps organisations meet legal obligations, an increasingly important 
factor, but not the only reason this work matters.

Some of the available data is poorly maintained or not maintained at all any more, 
leading to outdated and incorrect data. In other cases, such as Web Platform Tests 
and a11ysupport.io, the data doesn't tell the full story. WPT focuses on the browser and 
ensuring that the accessibility tree (the internal representation of the web page for 
assistive technologies) is properly constructed, where possible; however, this only tells 
half the story. What happens when one or more screen readers don't interpret what's in the 
accessibility tree? Similarly, a11ysupport.io shows data specifically for ARIA roles. 
ACD is working with browser vendors, developer tooling and resource owners and maintainers, 
and accessibility professionals to ensure that the data we provide is up-to-date, 
well-maintained, and properly integrated into existing systems.

Additionally, assistive technologies work on an operating system level (unlike browsers) 
and also have to interpret UI elements, prompts, and actions outside of the browser, 
which adds another layer of complexity. The decisions that assistive technologies make 
regarding how or if to interpret various components, happen internally, 
and don’t typically happen in standards organisations, which leads to varying user experiences.

## Scope
The workshops I ran surfaced concerns, needs and questions, which helped clarify the scope of the project.
Firstly, ACD is not a means to deem any website, web app or other service using web technologies 
as accessible or not. ACD is not designed to evaluate the accessibility of a full website or application, 
it focuses specifically on whether individual web platform features are reliably supported by 
assistive technologies in different browser environments.

Instead, ACD will be providing data on whether web features are accessibility supported, 
meaning they work reliably across a combination of browsers, assistive tech, 
and user agent settings, as defined by WCAG 2.1. ACD will show if a web feature is supported 
in the browser and/or assistive technology, i.e. can the web feature be displayed in the 
tested browser and can the web feature be interpreted by the tested assistive technology.

The data provided by ACD will help developers and web creators make more informed decisions. 
It will help them know which web features they may have to polyfill to make work in specific 
browser-AT combinations, which edge cases they need to consider, and will encourage them to 
pay closer attention to how they construct their websites and applications.
This data doesn't replace the role of an accessibility auditor or accessibility engineer, 
but complements their work by surfacing issues sooner.

To clarify priorities, here’s what ACD is focused on now, what’s on hold, and what’s explicitly out of scope.

### In Scope
1. **Collecting data on the accessibility-supported status of web features.**

   I will be working with the maintainers of Browser Compat Data and a host of
   stakeholders to figure out the best way to collect this data.
   This will include deciding the shape of the data, collection methodologies,
   and decision-making systems for the accessibility-supported status of a web feature.
   
2. **Integrating the data into developer tooling and resources.**

   Tooling owners and maintainers have expressed interest in integrating
   this data into their products and services.
   I'll be working with them as stakeholders to decide the best way
   the data should be integrated to best serve developers.

### Temporarily Out of Scope
These items are out of scope for now, during the research phase. 
They'll likely be included in the scope at a later date.
1. **Distinguishing between implementation bugs and deliberate AT/browser behaviour.**

   Sometimes, browser and AT vendors make decisions that lead to inconsistency across platforms;
   for now, we won't be distinguishing between either of these.

2. **Highlighting which part of the stack is responsible for the bug.**

   It's important for browser and AT vendors, as well as web developers, to understand where in the stack
   a potential inconsistency is so that the appropriate party can address it.

### Out of Scope
1. Fixing accessibility bugs or issues.
2. Providing website and application accessibility audits.

## Open Questions
The workshops surfaced a few key questions we’ll need to explore further:
1. What's the most intuitive and useful way to display this data to web developers?
2. What's the difference between a bug and a decision (sometimes ATs decide not to or to do
   things a certain way that may present as a bug)?
4. What known edge cases affect interoperability? E.g. some participants reported that
   the accessibility tree can expose incorrect or misleading information.

## Next Steps
1. Run a developer survey, ideally on MDN, to better understand what kind of data would be most useful
   and how best to present it. I'm working with the owners of MDN surveys to make this happen.
3. I will be working with Open Web Docs, which maintains Browser Compat Data (used by MDN and CanIUse),
   to understand how we can approach data collection and integration into third-party platforms.
5. Begin holding stakeholder meetings, bringing together relevant stakeholders for joint planning
   and feedback sessions.


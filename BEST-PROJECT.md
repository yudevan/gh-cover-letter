# James M. Greene [<img class="emoji" title="GitHub" alt=":octocat:" src="https://a248.e.akamai.net/assets.github.com/images/icons/emoji/octocat.png" height="20" width="20" align="absmiddle" />][me/gh] [<img class="emoji" title="Twitter" alt=":bird:" src="https://a248.e.akamai.net/assets.github.com/images/icons/emoji/bird.png" height="20" width="20" align="absmiddle" />][me/t] [<img class="emoji" title="Email" alt=":e-mail:" src="https://a248.e.akamai.net/assets.github.com/images/icons/emoji/e-mail.png" height="20" width="20" align="absmiddle" />][me/email] [<img class="emoji" title="Website" alt=":earth_americas:" src="https://a248.e.akamai.net/assets.github.com/images/icons/emoji/earth_americas.png" height="20" width="20" align="absmiddle" />][me/site]  

---

## Best Project

### New Feature: User Annotations
The best project that I have had the honor of spearheading was the prototyping, refining, and implementing of the "User Annotations" feature for my employer's latest flagship product for legal research, [WestlawNext][wlnext/product] (also, [its marketing site][wlnext/promo]). This feature enabled users to:
 1. Highlight text within our legal documents.
 2. Highlight text within our legal documents and attach a inline note to it.
 3. Attach document-level notes when no associated text needs to be highlighted.


### Why?
So why was this feature the best project I've worked on to date?  It was:
 - **"Impossible":** When our Information Architect originally brought the idea to me and my team on a Friday afternoon, we all thought it was impossible to achieve, especially cross-browser (IE >= 7, and friends). None of us had ever seen such functionality on the web at that point, only in desktop applications like Adobe Reader/Acrobat&mdash;and it is still quite rare even today. However, all of our biggest competitors have added since attempted to copy our functionality... some mostly successfully, some not.
 - **Agile:** As it happened, I was leaving on a family road trip the next day. Inspired by the  challenge, I brought my personal laptop along and was able to hammer out a basic but working prototype for IE and an especially buggy prototype for the other browsers. Additionally, although we were already practicing agile development as our SDLC, this particular project had an exceptionally tight feedback loop between the IA and myself, which made it simple to mold the functionality to be the exact implementation to match his idea.
 - **Unique Knowledge:** Even as seasoned web developers, what we didn't know during our IA's initial pitch was that the browsers did each offer _one of two_ Selection & Range DOM APIs: IE's proprietary model or the W3C standardized model. Both models have their pros and cons but were certainly not equivalent. As it turned out, a working prototype was much easier to achieve with IE's model but I was eventually able to achieve consistent cross-browser functionality over the next few weeks. The work I had to do to bridge the gaps was effectively a proprietary precursor to the [Rangy][rangy] JavaScript library.
 - **Challenging:** Even after working around the cross-browser compatibility issues, our product's content posed its own challenges:
     1. Our users' annotations are private data, so they couldn't be associated directly with a document.
     2. We have pedabytes of document content, so giving each user their own copy of the document wasn't a cost effective option.
     3. Our document content also gets updated occasionally, so our algorithm for placing the inline user annotations had to be very forgiving.
 - **Little Management Overhead:** For this project, I worked mostly independently with minor collaboration points when I wanted some unbiased design validation from my peers. Moreover, to my management's credit, they were primarily just "along for the ride" on this effort and the lack of micromanagement (_not_ the norm at the company) made it _so_ much easier to get some intense work done without any roadblocks.
 - **Successful:** Last but certainly not leas, the project originally thought impossible ended in a complete success. Not only did it go out with the initial release of our new product but it was also wildly popular with our customers: on an average day, more than 30000 new highlights and notes are added.


### Sharing
Unfortunately, I have never been able to acquire permission from my employer to open source the overall annotations workflow. However, I have been "allowed" to open source several smaller pieces of it by deciding that sharing them with the world was important enough to me to warrant the extra effort required to rewrite them from scratch. Thus, I have since released initial versions of the "jquery.textSelect" and "jWalker" JavaScript libraries (see [OPEN-SOURCE.md][cover-letter/open-source] for more details), though more work remains to get them up to par with the robustness and completeness of their proprietary counterparts.


[me/gh]: http://github.com/JamesMGreene "GitHub"
[me/t]: http://twitter.com/_JamesMGreene "Twitter"
[me/email]: mailto:james.m.greene@gmail.com "Email"
[me/site]: http://about.me/JamesMGreene "Website"
[wlnext/product]: http://next.westlaw.com
[wlnext/promo]: http://westlawnext.com
[rangy]: http://code.google.com/p/rangy
[cover-letter/open-source]: OPEN-SOURCE.md

SOTD: These are personal notes toward a comment on the challenge of "dual-use privacy" technolgies

# The privacy challenges of dual-use technology

Today's Web and Internet technologies are tremendously generative;
they can be leveraged for many purposes unanticipated by their
original developers.[[Zittrain]] Generativity is a core contributor to
the "permissionless innovation" that is a hallmark of the Net. Yet
this widely distributed generativity can also pose a challenge as we
try to innovate the Net's infrastructure -- how can we know that one
person's bug wasn't another's feature; that changes won't break one of
those unexpected but valued applications?

Privacy exhibits this pattern in spades, because privacy-enhancing
technologies are often dual-use, or their privacy-enhancing value is a
side-effect of other properties. 

For example, VPNs are used by many to provide transport-level
encryption of communications, to support geographically distributed
shared access to corporate network resources, to bypass local network
filtering, or to conceal geographic location, among others. Thus when
WebRTC/RTCWeb exposed the internal IP addresses of browser users in
order to facilitate peer routing of real-time audio and video, some
users were surprised and dismayed, while others were unfazed. RTC spec
contributors explained the choice as one of performance and simplicity
for end-users: their RTC connections should just work. 
TK: NEEDSREFS and further development

## Examples: 

* VPNs
* Middleboxes (SEMI, SPUD)
* Private browsing mode
* Fingerprinting / cookie-blocking
* ... 

## Goals and Principles

* Minimize surprise

* Users and tools shouldn't have to identify themselves as
  "privacy-seeking" or "privacy-protecting"

* Collateral privacy should be protected 

## Questions

* When can we infer intent, either to get or defeat privacy-protective
  measures? How do calls for regulatory action mesh with implicit
  privacy protection?

## References

IAB SEMI, IAB Workshop on Stack Evolution in a Middlebox Internet (SEMI), https://www.iab.org/activities/workshops/semi/
W3C TAG, Unsanctioned Web Tracking, http://www.w3.org/2001/tag/doc/unsanctioned-tracking/
Zittrain. Jonathan L. Zittrain, “The Generative Internet,” 119 Harv. L. Rev 1974 (2006) 

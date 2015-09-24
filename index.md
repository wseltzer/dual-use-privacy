SOTD: These are @wseltzer's personal notes toward a note on the challenge of "dual-use privacy" technolgies. I welcome comments/criticisms!

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
for end-users: their RTC connections should just work. Users who
relied on VPNs to keep their local IP addresses private were surprised
to find that this property no longer held. [[TK: NEEDSREFS and further
development]]

Privacy, like anonymity, loves company.[[DingledineMathewson]] The
more people using a given technology, especially if it has
non-privacy-specific purposes, the less its users stand out as
"privacy seekers." The use of privacy-specific technologies was used
as a selector in the NSA's XKeyscore system.[[XKeyscore]] It is
counterproductive if individuals trying to preserve privacy, whether
web browsers from advertisers or dissidents from repressive political
regimes, stand out from the crowd by virtue of the tools they use.

[[Does layering have any role here? How does it impact that IP
disclosure is a cross-layer issue? Sometimes, layering helps us to
avoid these problems. Interfaces between the layers are clearly
defined, and issues designated to one layer or delegated to
another. But the app layer could still do or mess up the permissions.]]

We don't want to ossify the Internet or Web by picking some subset of
properties and saying those must be preserved. We can't even say that
changes are permissible only in new protocols or with new semantics,
because of the "port 80" problem, that new ports and protocols don't
get through firewalls and middleboxes. How do we evolve new
technologies, change the behavior of existing ones that may have
unexpected privacy implications, without surprising or harming the
users who depend on some features of the old stack? Any answer
involving "notice" must account for the practice rolling software
updates, where users may barely be aware that software such as their
Web browser has changed.

Further, research into user "fingerprinting" and the analogy to covert
channels, as well as statistical analysis of differential privacy
suggest that nearly any element added to the platform may be used to
distinguish users or increase the linkability of their activity, and
thereby reduce privacy.[[TAG]] Even if privacy reviews describe these
entropy-reducing factors, they may not be able to recommend
eliminating all potential for privacy reduction; the fix may lie in
policy as well as technology.

Should we start looking at privacy-affecting changes more like
security risks? That could mean assessing the threats and mitigations,
and giving notice to affected users, as well as to developers and
advocates who can intervene on users' behalf.

Emerging privacy model of the web (with thanks to Nick Doty):
origin-bound storage; 
permissions
per-origin isolation
layer boundaries
...
meeting users' expectations, building out the details of this model. 

[[TK: Need much better guidance to spec developers and users!]]


## Examples: 

* VPNs
* Middleboxes (SEMI, SPUD)
* Private browsing mode
* Fingerprinting / cookie-blocking
* ... 

## Goals and Principles

* Minimize surprise to users and developers

* Users and tools shouldn't have to identify themselves as
  "privacy-seeking" or "privacy-protecting"

* Protect collateral privacy

* Preserve generativity

## Questions

* When can we infer intent, either to get or defeat privacy-protective
  measures? How do calls for regulatory action mesh with implicit
  privacy protection?

* Is a "flag day"/protocol change the only time we can make
  privacy-breaking changes? 

* Whose responsibility is it to watch for the impacts of protocol changes on
  privacy?

## References

Dingledine, R. and Mathewson, N., Anonymity Loves Company:
Usability and the Network Effect  http://freehaven.net/anonbib/cache/usability:weis2006.pdf

IAB SEMI, IAB Workshop on Stack Evolution in a Middlebox Internet (SEMI), https://www.iab.org/activities/workshops/semi/

W3C TAG, Unsanctioned Web Tracking, http://www.w3.org/2001/tag/doc/unsanctioned-tracking/

XKeyscore. Glenn Greenwald, XKeyscore: NSA tool collects 'nearly everything a user does on the internet, The Guardian, 31 July 2013  http://www.theguardian.com/world/2013/jul/31/nsa-top-secret-program-online-data

https://www.schneier.com/blog/archives/2014/07/nsa_targets_pri.html

Zittrain. Jonathan L. Zittrain, “The Generative Internet,” 119 Harv. L. Rev 1974 (2006) 

https://www.w3.org/TR/html-design-principles/#priority-of-constituencies

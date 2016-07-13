---
title: Disclosure policy
---

We at snyk value the security community and believe that responsible disclosure of security vulnerabilities helps us ensure the security and privacy of the users.
​
A responsible disclosure program includes a policy with clear and simple rules of engagement for security researchers to report vulnerabilities they discover. It protects both the developer and researcher, while allowing developers to safely benefit from vulnerabilities discovered by researchers.
​
Security vulnerabilities can be reported to us, and we will manage the responsible disclosure procedure, (1) receiving the report, (2) notifying the developer, (3) coordinating the fix and (4) publicly disclosing the vulnerability giving full credit to the researcher.

### 1. Report

Receiving the submitted vulnerability report from the researcher/reporter, sent to [report@snyk.io](mailto:report@snyk.io).
Snyk will verify and document each reported vulnerability prior to developer notification.

### 2. Developer Notification

The first phase of the public disclosure process, goal is to provide vulnerability details necessary for the developer to begin its internal resolution process.

If the developer has not acknowledged receipt within 30 business days of the original notification, Snyk will retransmit the vulnerability details to the original contact and at least one secondary contact, if a secondary contact is publicly available. If the developer allows an additional ten business days to elapse following the second notification (40 business days since original notification) without acknowledging the information, vulnerability details will be re-sent not only to the previous two contacts, but also to customers or other stakeholders at Snyk's discretion.

If the product developer does not respond to any of the three notification attempts within an additional ten days following the third notification (50 business days since original notification), or if the developer indicates that it does not wish to coordinate disclosure, Snyk may elect to issue a public advisory (Step 4).
Acknowledgement of the notification by the developer should include all of the following items:

a. developer confirms the vulnerability information is received and the schedule for investigation.  
b. developer provides a point of contact responsible for coordinating and tracking information on the issue from within its organization.  
c. developer provides an estimate as to when it expects to complete its initial investigation of the security issue provided in the notification.  

### 3. Developer Coordination

Upon successful acknowledgement of the notification, Snyk will work with the developer to determine how the security issue will be addressed. The following tasks are included within this phase:

a. At developer's request, Snyk will provide additional information to assist in the development of a solution.  
b. At developer's request, Snyk may review proposed solutions for effectiveness.  
c. The developer and Snyk will exchange proposed timing for public disclosure of the issue and related solution for mutual approval.  
​
If developer responses to all communications in this phase are not received within ten business days, Snyk may move directly to the Public Disclosure phase.

### 4. Public disclosure

Public Disclosure is the final phase of the disclosure process. During this phase, Snyk intent is to add the vulnerability to it's [public database (vulndb)](https://snyk.io/vuln/), provide information on the vulnerability and related solutions. Public Disclosure may be initiated either by completing the Developer Coordination phase or through a process failure in prior phases.

During the Public Disclosure phase Snyk, and optimally the developer, will disseminate information on the vulnerability and related solution to the public. Snyk may disseminate information through public e-mail lists, web pages or any other medium it deems appropriate to reach the intended audiences.

### 5. PGP Key

As mentioned above, you can report issues simply by emailing us at [report@snyk.io](mailto:report@snyk.io), and a member of the Snyk team will review your confidential report.

If possible, we recommend you encrypt such vulnerabiltiiy disclosures using the following PGP key:

``` language-markup
-----BEGIN PGP PUBLIC KEY BLOCK-----

mQINBFeF/s0BEADCn8LlbRrbKaKlrq1ss0nbfcs3mtRAAZeQFb1BAArCD5ycdJWM
bDdJfONdHC6kqrctCFKUj3gLi7cpzE8Cd8xbt+ieDNcX1uBFuYijpzPg9JQhzMt4
k24IDJf/Rrl4biQQKAbu4W77aNasvT13A/FiSW8ClPsiZzAfNMdEZSNPUJzVsGH/
TWuqbTd72RDENDIkrMxNEaebxHEES6GfmKkbIkNpBS7Rf2MAm7AFaGHlYcnHorjs
oBr9MrEOjiorpdhiQ8sRwdECBWp1cfVFLj9oLXJiS3kk0M2nJnM/yWZbiarFtzu3
3G5rS9Xua+yzQFWLaSyFx6KQGAiCFL035FA5IZ/w/Sm5+ZXZeDxGktAd4X7yaJBv
DDj0GEkAHjslXYMokm9jQTktDdxS78u5dH3Wyk8sftNTayg9w/21qlpxnlFz79WL
QKkf/PTjgccBmruZ3lMPlzSWLwCOWdDy2wUrFqMfOMjcKfo0clGOZK8DNBUPCdf+
0FcEBR1+jPqvFt7QoAEoqpl3fIjmuIqgWEuprDWVScDGJyCyw4pE1CJIaQtKgZf9
9e3xOgSDdhYOCIwIv14yfMVCXZ5nI5A8is8JP//ZAVC8ZJsYcqz4d6es5N9xIaI9
9u4+WaDcRjqTxTPBHJZLPsMy83TTOxPDxmB2Xa8Tno3cavSTzfRR44GXRQARAQAB
tCJTbnlrJ3MgRGlzY2xvc3VyZSA8cmVwb3J0QHNueWsuaW8+iQI9BBMBCgAnBQJX
hf7NAhsDBQkS0UkABQsJCAcDBRUKCQgLBRYCAwEAAh4BAheAAAoJEM9JPnxu3Fqm
C/4P/3uYerVrz8yXhrP9hYT98hX/1zST5AFM2FJ3+QK5Ir+6pAD3b11ggsAyXTqo
dr+VvyC04GRGNv8mMVfitSaJbkqUXupL++L2g4tftI1JbsFaS9qf/aIZKjCRtZti
iYj1hmZsNd2FMUvcDLuA6WqAoeLW6YeDflJu9PMJUNcK+bHHM75zj4FyX1WIRrQw
CA3oMzgE7vF9c41RSWEL5kqeOHIa4NXNTyUexa5jOe8W1gfRV6vC0ZObKnKTv/SH
Hau20mueObefGvapoMRqwZBgjzHyf1GIyKxd6qkdawNbVW+s4iF4L+LTzkXYmCtH
UsU6gCMuWn/KDp6armnhYZYvjcTk48gWFN/3JVyBr1s2dYL6MB7pfPth1kfLaVSI
bB5MfETHe2FVFcVFMW86sFN+HG8cY4i/SEdcV04jK/AqRmJbOPFPlPDAg3jRWK11
luMJ+0kCBV7y+AlI6jviNhxE3sgezZyTq0yEBj4/u8bG40TPUqrwwpbjXvYhREoV
grrYWKUljQOVyVoLSOBSJ7EQUcCVSYA59LTo7EY0yoMsO1tl8kUIu/Gu3khl5o4c
KKZvk/0EodWNJrflOtu0Qu0vghqSlXF3Fm+tLV1xKxal2d8S4RUdq0zuP24G6fGv
RQiDMzKEQy5jzt8L5x7wAg37qgYBVKhsH9M3O1u+U1xBcSafuQINBFeF/s0BEADA
N6kGL30pHnkgeQ4ORLd9g1z5R9glo+1OUqWqa7bTVCe+1WHT3yRUUU/kOKKldFBK
Dwrlqs0vgchLhj3oietYFaHo3eQ1TWpUv03Gv2KFszUoDnBrcTq5LP2IcfC8ek7E
ZuRlEAc5yXrLzrRCMgIt7wYIDZ+14/K/1H/c91ygryJU+C3SmNAvNBhiAbevCUSr
B290gVmQ0h/6v2plAD3yvv08jfwjYCTIftvpO6wMWCQt4Vz+8gRTwmSgrNKf26Fn
siT46ptaiK5rCpq1fOaBzBXVPNnzHT3iaNq+30brxQKBA8OxVc1VR9XPaHIXjBLY
/Kt2br8/dMsnLeJ/MJ9/Q7A7sm5syjnS8jMmf9yEJI7dQOcTLMz8pp8v3VHzyTng
ZcdJ4CePr/mrr7MrIIjALzXa7SuxUTTYMlYuP3fVT5pFoNsSB4BLyt4gs0XdBSFl
ozLG+VKlOTAClPhqczIAHMJ5k6JXzsPuEiBIkcvoaD+OhscaOXGS3/2i0L2QYUTO
iLTdOfoJvQSfmOA+2s1UYdypcOalurwvCHT5Le7AN3vaZx7DO7E0TtsNUuilX1VH
51sSWP9ZN23G91f9aZwLYbXVhEoTFujXzoSl45GHMFSSWxAQUQAMpzH2NcRPfjwG
Fu0p88ohEglJPFRz6QPRNtq7qXoG5oboDf+PI2OODQARAQABiQIlBBgBCgAPBQJX
hf7NAhsMBQkS0UkAAAoJEM9JPnxu3Fqm0jIP/Rx0ciIq+XWr3DVizjU4yxi4u2wn
fsq6WlZxWxsomn48/2ajIrE8MxGyKY5FGekyJk8VbcZloW6Oi1BoY39AnG9Lgxeh
IIqFU/6kWk+azGnzU1KzkJtKvyO/RLF5/uqC9d77Njc5Hofia11IojEye0Dln+nm
1J96UQ4UafuprfjgjZ0o6k78AmXey8/E27QI5s7ue188jt/DdW7uGEBcBE2uNdSH
j8f4GNAWLc0wFSf14B4WP8lgmptUMrbj3UcEYx1m/xDbhCFNiBgYnqtRj4e3Bee2
Yf08id59ap7L+qco7eg7irfmJwPUgG/LeZvax6Y9tXM/m2oxJ1sLEJn255hOFE9/
CmWHpXwUzJhRe4X4tQQJlj+UH9JYvYmPY0PTGa0asZyEBiUaefGV0X03bw+2M7y6
5QUTxsuyLFMAE5Zb1JUYbru3B9x3Ct4my78sIh532gXWGSw9jvuwdufYVP5ass4G
tTVdYd7ILnLJo+4xo6nxZ6qBUZYt46/6E+Glf339mVi5OiGnBaxj6njq6pIO09QB
loDy/4YB/g4rTmm4y946mG0qMMRs262ud47n9Ou0rNYmemHw0xSNigOvLOKq73cf
XZG1I1nwLKTP/w5UeSx8pk9CSuGtLuhiJPDwhhHmFFz8ibdOQRHk8kE4w7kUhfww
JtT74y0R2sMYMxjs
=NdUO
-----END PGP PUBLIC KEY BLOCK-----
```

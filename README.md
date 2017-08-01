# Hush

Modern applications are often split into separate client and server tiers that
communicate via message passing over the network. One well-understood threat to
privacy for such applications is the leakage of sensitive user information
either in transit or at the server. In response, an array of defensive
techniques have been developed to identify or block unintended or malicious
information leakage. However, prior work has primarily considered privacy leaks
originating at the client directed at the server, while leakage in the reverse
direction -- from the server to the client -- is comparatively under-studied.
The question of whether and to what degree this leakage constitutes a threat
remains an open question. We answer this question in the affirmative with Hush,
a technique for semi-automatically identifying Server-based InFormation
OvershariNg (SIFON) vulnerabilities in multi-tier applications. In particular,
the technique detects SIFON vulnerabilities using a heuristic that overshared
sensitive information from server-side APIs will not be displayed by the
application's user interface. The technique first performs a scalable static
program analysis to screen applications for potential vulnerabilities, and then
attempts to confirm these candidates as true vulnerabilities with a
partially-automated dynamic analysis. Our evaluation over a large corpus of
Android applications demonstrates the effectiveness of the technique by
discovering several previously-unknown SIFON vulnerabilities in eight
applications.

For more information please refer to our
[paper](http://cs-people.bu.edu/wfkoch/my-data/pubs/sifon.pdf).
 

This repo contains the static analysis (S-Hush) and dynamic analysis (D-Hush) software to identify SIFON vulnerabilities in Android
applications.  



If you use this code please cite the following paper,
```
@inproceedings{koch2017hush,
  title={Semi-automated discovery of server-based information oversharing
vulnerabilities in Android applications},
  author={Koch, William and Chaabane, Abdelberi and Egele, Manuel and Robertson,
William and Kirda, Engin},
  booktitle={Proceedings of the 26th ACM SIGSOFT International Symposium on
Software Testing and Analysis},
  pages={147--157},
  year={2017},
  organization={ACM}
}

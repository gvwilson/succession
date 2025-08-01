# Short Notice

<p class="subtitle">what to do on short notice</p>

In 2013,
the government of Canada ordered the closure of
five of the Department of Fisheries and Oceans' seven libraries [[](b:Nikiforuk2013)].
No one knows how many thousands of volumes of irreplaceable environmental records were destroyed,
but even scientists who were directly affected did not make plans in case something similar happened again.
In contrast,
when faced with the prospect of a populist demagogue becoming president,
researchers in Argentina knew from their collective experience what might happen next
and took action accordingly [[](b:DelBoca2024)].

And then Donald Trump was re-elected
and an unprecedented assault on American science began.
Except it wasn't really unprecedented:
from anti-vax hysteria to climate change denialism
to banning the teaching of evolution in schools,
reactionaries have been attacking science and scientists for decades.

## Software

"Good enough" practices in research computing,
such as creating \texttt{.zip} archives of your project as an alternative to using version control,
may be more appropriate that "best practices" in an emergency \cite{Wilson2017}.
(By analogy,
a paramedic is not a doctor who cuts corners,
but rather someone who specializes in working under very different circumstances.)
If you are short on time:

Explanations of what the software \emph{does} and \emph{how to use it}
take priority over documentation of its internals
because (a) someone who knows the first two will be better able to figure out the third
and (b) AI code assistants can do a reasonable job of helping newcomers navigate an unfamiliar code base
if they are given enough context.

Similarly,
a short screencast showing how you use your software
is often faster to create than pages of documentation,
and may actually be more useful if closed captions are attached
to make the content searchable.
Again,
AI tools can help create those captions,
though some editing is invariably required to clean up mistranslation of technical jargon.

Following on from Tip 5,
you can \href{https://archive.softwareheritage.org/browse/search/}{search the Software Heritage Archive} with your repository url to check whether it has been saved.
If your repository is not present, there is a \href{https://archive.softwareheritage.org/save/}{simple process} to submit it for archival.

If you do not have time to bring your project in line with best practices,
try instead to clean it up by removing files that are no longer used,
deleting sections of your setup instructions that no longer apply,
closing bug reports that are no longer relevant,
and so on.
Eliminating clutter in this way will make what is useful easier to find.

Briefly document what happened.
If you are the main developer working on a grant and you have moved on to something else,
say that in the README.
If the funding changed, then say that the work is unfunded.
This information is often the most useful for users but the hardest to find.
Saying it up front will help others understand how your work is positioned.

Following on from Tip~5,
you can search the \href{https://archive.softwareheritage.org/browse/search/}{Software Heritage Archive}
to check if your repository has been saved.
If not,
submitting it is a \href{https://archive.softwareheritage.org/save/}{simple process}.

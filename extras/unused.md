## Permissions

Once you know whether your institution has a policy,
get whatever sign-offs you need immediately.
Reach out to colleagues who can review your code if that is necessary for publishing it,
and review theirs if asked in return.
If it appears that there is no formal sign-off process,
send an email to someone in authority
(e.g., the chair of your department or your grant officer)
saying that you believe this to be the case,
and copy that email to an account you will be able to access
after leaving your institution.

Do not assume that if you had permission before,
you have it now or will have it in the future.
Policies are changing rapidly,
and you may find yourself locked into one that no longer allows you to do what you want.
Also consider that the person you report to may be replaced with one who knows you less well or is less sympathetic,
so acting now may be easier than acting later.

Finally,
if you have your next job lined up,
ask about their policies
and make sure that your right to share your work is written into your contract.
Making your code comply with policy after the fact is riskier and more time-consuming than doing so early,
and sometimes not possible.

## Licensing

Making code publicly available does not ensure that other people can use it;
you maintain all copyright unless you explicitly include a license,
so they may still need explicit permission
or may simply be unsure whether they do or not.
The Open Source Initiative (OSI)
maintains a list of \href{https://opensource.org/licenses}{open source licenses} it has approved;
the implications of these licenses are widely understood,
so choosing one of those will make your project more understandable to others.
Please do \emph{not} try to write your own license
or simply waive copyright and place the software into the public domain,
as what is meant by ``public domain'' varies from country to country.
(In countries such as France and Germany
it may not actually be possible to waive copyright and place a work in the public domain.)

Broadly speaking,
the MIT, Apache 2.0, or BSD-3-Clause licenses are \emph{permissive} licenses
that place the fewest restrictions on modification, distribution, and re-use.
The GPLv3 and AGPL-3.0 licenses are \emph{copyleft} licenses
that require people to share their modifications to the software with the community \cite{Morin2012}.
These copyleft licenses can prevent companies from taking advantage of work without giving anything in return,
but some institutions discourage or disallow their use out of fear that they will constrain commercialization,
and some companies have policies against using software with some copyleft licenses.

More broadly,
\href{https://creativecommons.org/}{Creative Commons} licenses can be used for documentation or research reports
but should be avoided for actual code,
while \href{https://ethicalsource.dev/}{ethical licenses}
or licenses based on the \href{https://blueoakcouncil.org/license/1.0.0}{Blue Oak Model License} may also be appropriate.
\href{http://choosealicense.com}{choosealicense.com} and other sources provide guidance \cite{Fogel2020,Fortunato2021};
discussion of why people \emph{don't} share is also helpful \cite{Gomes2022}.
Whatever license you choose,
place its text in a file called \texttt{LICENSE}, \texttt{LICENSE.txt}, or \texttt{LICENSE.md}
in the root directory of your project,
as this is where people and automated tools alike will look for it.

<div class="callout" markdown="1">

Most discussion of open source licensing focuses on circumstances in a handful of affluent countries.
In contrast,
many Latin American countries have access to information laws that include research outcomes and artifacts.
You can publish data and software under that,
but the institution sets the license type,
and you must use institutional repositories.
As always,
consult *local* legal experts before taking action.

</div>

## Redundancy Equals Reliability

Once you are legally able to share your code, remember LOCKSS: Lots of Copies Keep Stuff Safe.
But copies are not enough:
the threats to your project are political as well as technological,
so you should ensure that loss of institutional support
(or worse, that institution turning on you)
does not mean loss of access.

<div class="callout" markdown="1">

Fifteen years ago,
a file-sharing system for scientific data based on the BitTorrent protocol
failed to find wide adoption because of the (quite reasonable) association in many institutions' collective minds
between BitTorrent and illegal downloading [[](b:Langille2010)].
Today,
many individuals and groups are turning to BitTorrent to share datasets that are at risk of disappearing
because of the protocol's resilience.

</div>

\href{https://github.com/}{GitHub},
\href{https://gitlab.com/}{GitLab},
and \href{https://bitbucket.org/}{BitBucket}
are social coding platforms centered around Git,
a widely-used open source version control tool.
However,
they are all commercial entities based in the same legal jurisdiction,
which means they are vulnerable to \emph{correlated threats}:
trouble with any of them may mean trouble with all of them.
\href{https://codeberg.org/}{Codeberg},
while currently much smaller,
is a non-profit based in a different jurisdiction;
consider mirroring your work there or using it as your primary host.
Keep in mind that persistent code archival is not a feature of development platforms.
Repositories can be altered,
made private,
or deleted
(also as a result of government takedowns\footnote{\url{https://github.com/github/transparency/tree/main/data/government_takedowns}});
the platform itself may be shut down
(as happened to the non-profit Gna!\footnote{\url{https://en.wikipedia.org/wiki/Gna!}}),
or it may change its revenue model
(as happened with SourceForge\footnote{\url{https://en.wikipedia.org/wiki/SourceForge}},
which once dominated the open source repository space in the way that GitHub does today \cite{Tamburri2020}).

When you create projects on hosted services,
use a team account as the project owner rather than a personal account.
Doing this makes it easier to give other people permission to manage the project,
and as noted in Tip~6,
a project with multiple owners from different institutions
is harder for any one institution to lock down.
For the same reason,
do not rely solely on logins or email addresses associated with your institution:
instead,
ask yourself if you will still have access to the project if you lose that identity,
and add an identity you personally control to the team that owns the project.
You can also add your \href{https://orcid.org/}{ORCID} to the project's metadata
so that the project links to a profile that you control
even when your contact address changes.

Version control is not the only way to create and save copies of your work.
\href{https://www.softwareheritage.org/how-to-archive-reference-code/}{Software Heritage} archives software from multiple forges;
you can also snapshot the current state of repositories in a compressed archive file
(e.g., \texttt{.zip} or \texttt{.tar.gz})
and deposit those copies with the \href{https://osf.io/}{Open Science Foundation} (OSF),
\href{https://zenodo.org/}{Zenodo},
or \href{https://figshare.com/}{Figshare}.
(Zenodo even integrates with GitHub so that tagging a release on GitHub
automatically triggers deposit of a new archive on Zenodo,
but again,
this automation is only useful as long as both ends are accessible.)
Institutional,
\href{https://amt.coretrustseal.org/certificates/}{national},
or \href{https://safeguar.de/}{international} data repositories also enhance longevity.

Storing copies on someone else's computer is not the only option:
you can (and should) make copies of your projects on computers that you own.
Again,
this is a place where colleagues can help:
ask them to make copies on their computers in exchange for you making copies of theirs on yours.
Whatever you do,
document it \href{https://ropensci.org/blog/2022/03/22/safeguards-and-backups-for-github-organizations/}{as rOpenSci has}.

Similarly,
if you distribute your code as a package on \href{https://pypi.org/}{PyPI},
\href{https://anaconda.org/anaconda/conda}{Conda},
or \href{https://cran.r-project.org/}{CRAN},
that package can contain all of the source code.
Doing this also fosters community collaboration.
When setting these up, you should ideally ensure that control over the distribution channels for a package is not limited to a single developer.
However, this is not always possible.
For example,
while PyPI actively encourages this,
CRAN policies allow only single point of contact.

## What to Save?

When deciding what to store where,
remember that your version control repository only stores part of what makes up your project.
For example,
while GitHub wikis are stored in ordinary git repositories, the issues and discussions live in GitHub's internal database;
you can use the GitHub API to download their content,
but (a) the result is intended for consumption by machines, not people,
and (b) if you are doing this on short notice,
the odds are high that other people are trying to do it at the same time.
GitHub's servers may not be able to manage that load when you need them to,
so use tools like \href{https://github.com/jlord/offline-issues}{offline-issues}
to save hosted content as plain-text files regularly.

## Community Adoption

Publishing your code is not the same as publicizing it.
The more people who know about and rely on your project,
the greater the chances that someone will help keep it alive,
whether by working on it directly or supporting you in doing so.
If you have not named your project yet,
choose a name that does not hint at direct and exclusive affiliation to a single institution.
This can help if the code needs to be relocated,
and also makes contributors from other institutions feel welcome.
Additionally,
label entry-level issues
(e.g., to use the ``good first issue'' label on GitHub)
so that people can easily find a place to start \cite{Steinmacher2015}.

Going further,
there is a causal link between social media mentions and both new adopters and new contributors \cite{Fang2022}.
Announcing your project on mailing lists, forums, or social media,
and talking about it at conferences are therefore necessary but not sufficient:
since everyone else is doing this too,
it is hard to be heard above the noise.

There are many good guides to what you can do to promote your project \cite{Kuchner2011,BelliniSaibene2024}.
A short video showing how to use the software
or a slide deck that others can incorporate into their lectures
will increase uptake by lowering the cost of adoption.
Similarly,
a one-page website that opens with an elevator pitch
explaining who the software is for
and how it will improve their lives
is much more likely to lead to that crucial ``second glance''
than a list of publications.

Disseminating your code through tutorials at conferences is another effective strategy.
Tutorials are an opportunity for you,
as an author,
to describe your work in depth
and (more importantly) convince your audience to use it.
Networking through such events will enable you to build relationships with
the people most likely to care about your project,
and it is the best way to ensure that you land well after you leave your current position.

<div class="callout" markdown="1">

If you can,
have at least one person outside your organization commit to your code.
Such community contributions lead to joint ownership of intellectual property,
which makes it harder for any single institution to lock down your work.
You can reinforce this by adding their name to the copyright statement in your license.

</div>

Finally,
remember that it is not all about \emph{your} project.
If you ask others to help maintain your code,
be prepared to give them something in return:
a letter of reference,
help testing or documenting their project,
or co-authorship credit on the project and associated publications.

## What Else?

Research software is increasingly recognized as a citable object \cite{Smith2016,Katz2021,Garijo2024},
and numerous books and research papers describe how to organize and run a research software project.
Rather than repeating what others have said
\cite{Sandve2013,Wilson2014,Lee2018a,Dryden2019,Akhmerov2020,Chue2021,Lees2022,Druskat2023,Akhmerov2023,Kumar2023,Struck2023,Reina2024},
this tip is a prioritized checklist of things to do
\emph{if you have time}.
If you do not,
please consult the next tip.

\begin{enumerate}

\item
  Create a DOI for each release of your software
  to ensure citability and retrievability even if the project repository becomes unavailable,
  and add a \href{https://citation-file-format.github.io/}{Citation.CFF}
  or \href{https://codemeta.github.io}{codemeta.json} file to your code \cite{Druskat2021}
  containing citation metadata.
  Tools such as \href{https://citation-file-format.github.io/cff-initializer-javascript/}{cffinit},
  \href{https://codemeta.github.io/codemeta-generator/}{codemeta generator},
  and \href{https://github.com/citation-file-format/citation-file-format/blob/main/README.md\#tools-to-work-with-citationcff-files-wrench}{others}
  can help you do this.

\item
  Submit your code for peer review and publication in a venue such as
  the \href{https://joss.theoj.org/}{Journal of Open Source Software},
  the \href{https://openresearchsoftware.metajnl.com/}{Journal of Open Research Software},
  the \href{http://www.jstatsoft.org}{Journal of Statistical Software},
  the \href{https://journal.r-project.org/}{R Journal},
  \href{https://ropensci.org/}{rOpenSci},
  or \href{https://www.pyopensci.org}{pyOpenSci}.

\item
  Document how to \emph{use} your software so that others can pick it up and use it if you are not available.
  In particular,
  add a \texttt{README.md} at the root of your repository
  that explains the purpose, setup, and use of your work,
  and add a tutorial showing how to use the major components of the code
  \cite{Lee2018b,Huybrechts2024,Littauer2025,Katz2025,Turing2025}.

\item
  Document any datasets your project depends on,
  and use CSV, JSON, Parquet, HDF5, or other widely-recognized formats rather than proprietary formats.
  Include the data in your project if possible;
  if that is not possible for legal reasons or because of the data's size,
  include URLs with data version IDs (or the date of the last download) in your documentation.

\item
  Describe your project's dependencies in a machine-readable way
  using Python's \href{https://packaging.python.org/en/latest/guides/writing-pyproject-toml/}{pyproject.toml} file,
  an npm \href{https://docs.npmjs.com/cli/v10/configuring-npm/package-json?v=true}{package.json} file,
  the \texttt{DESCRIPTION} and \texttt{NAMESPACE} files of an R package,
  a \href{https://openssf.org/technical-initiatives/sbom-tools/}{software bill of materials} (SBOM),
  or whatever else is standard for your language.

\item
  Write at least a few tests for your software
  so that people who want to use it (or contribute to it)
  can tell if it is working in their environment.
  These do not have to be formal unit tests \cite{Irving2021}:
  even a handful of ``this input should produce this output'' checks
  can save a lot of frustration \cite{Taschuk2017},
  Including sample inputs is also helpful,
  and removes dependence on external data sources which may themselves face continuity challenges.

\item
  Document how to \emph{contribute} to your software,
  e.g.,
  how to set up a development environment,
  run tests,
  and add new features.
  Such a guide leads to an increase in contributions \cite{Sholler2019},
  as does an explanation of the project's governance,
  i.e.,
  how decisions are made and who gets a voice in making them.

\end{enumerate}

Note that all of the suggestions above will also help with adoption,
for the same reason that a tidy restaurant attracts more customers than a messy one.
In addition,
if you follow the suggestions above when you have time,
there will be less for you to do when you don't
(as discussed in our next tip).

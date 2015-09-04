# A zero-entry workshop on high-throughput sequencing data analysis

Authors:

* CTB
* Ian Dworkin
* Matt MacManes
* Meg Staton
* Chris Chandler
* Istvan Albert
* Amanda Charbonneau
* Likit Preeyanon

## Introduction

For 6 years, we have been organizing a 25-person two week workshop on
bioinformatics analysis of large-scale sequencing data.  The workshop
teaches command-line program execution to biologists; attendees
require no prior computing experience, and use Amazon Web Services
rental computers ("cloud computing”) to execute programs and
workflows.  The materials from all six years are available, and from
2012 and onwards the materials are freely available under the CC0
license.

The goals of the workshop are to introduce concepts and practices in
large scale sequencing data analysis to practicing research
biologists.  The typical class contains an even mixture of advanced
graduate students and postdocs, and also includes several faculty,
technical staff, and industry researchers. Thus the students arrive
with substantial biological expertise.  However, based on both surveys
and discussion, half or more of the attendees have little to no
experience with command-line programs, and have widely variable
experience with any genomics and bioinformatics.  As such, we have a
number of goals:

* provide a friendly and unintimidating environment in which to ask
  questions of experts: attendees often believe they have an innate
  lack of ability to do computing, which presents a mental block for
  them in learning new computing techniques.  We attempt to overcome
  this by emphasizing the beginner level of the workshop and by
  providing a very accommodating environment.

* introduce attendees to command-line program execution. The UNIX
  shell is the prevailing methodology for bioinformatics analysis, and
  provides a common platform for program and workflow execution, but
  is something that most biologists have little formal exposure to.

* discuss choice of program parameters, evaluation of output, and
  end-to-end workflow design: often attendees are unaware of the
  variety and impact of choosing different analysis parameters, and
  may also not know how to evaluate the results of running a program.
  Teaching this necessarily involves demonstrating how to connect many
  programs together.

* describe common failure modes of sequencing, data analysis, and experimental design;

* introduce considerations of reproducibility and provenance in high-throughput data analysis;

* introduce scripting in shell, R, and/or Python;

* describe bioinformatics and statistics theory;

* connect practical workflows to attendee research;

* provide an environment for networking and career growth;

Workshop attendees report good things (assessment).

Experience report: informal interviews, etc.

## Details

The structure of the workshop has not varied substantially over the
years: attendees arrive by noon on a Monday, and after a welcome
lecture are introduced to Amazon Web Services and the UNIX command
line.  Between Monday and Thursday of the first week, we demonstrate basic
sequence analysis at the command line, including BLAST, mapping (with
bowtie or bwa), and assembly (with Velvet or SPAdes).  We also cover
experimental design, statistical analysis, and scripting and
automation. On Saturday afternoon we break until the second Monday
morning.  During the second week we focus on applying complete
workflows to exemplar data sets — starting in 2013, we have organized
an in-depth mRNAseq differential expression analysis tutorial that
introduces and compares commonly used tools such as DEseq2 and edgeR.
We then round out the week by discussing reproducibility, version
control, and other more general topics.  After a summative assessment,
a final lecture, and an informal evaluation, the attendees depart.
(For a concrete example, see the 2015 schedule@.)

Each day starts with a lecture, which is then followed by a tutorial.
After a lunch break, we give another tutorial, and then take an
afternoon break until dinner; during this break we encourage attendees
to exercise (frisbee, volleyball, or swimming are favorites), nap, or
relax, in order to stay fresh. After dinner, we reconvene for another
formal activity, such as another lecture or tutorial, or student
presentations on their research.  Throughout, we encourage informal
interaction between students and instructors / TAs throughout, with
the goal of enabling students to ask whatever questions they want.

The tutorials or practicals are the backbone of the course.  Tutorials
consist of a series of commands that can be copy/pasted at the shell,
and are guaranteed to work the same way for all students when properly
executed on the specified cloud computing platform.  The commands are
interspersed with discussion text and external links for more
information.  Typically tutorials are presented by a lecturer who
works through the tutorial interactively, discusses what each step is
doing and why we are doing it, and addresses any questions from the
audience.  TAs and other instructors circulate around the room
helping students who run into technical trouble.  In recent years, we
have started using the Software Carpentry “sticky” system to make sure
that the majority of the room has successfully reached the same point
in the tutorial.  The tutorials remain available on the course Web
site when the students leave, and generally remain functional due to
our use of a static cloud computing environment.

We also keep a high TA:student ratio.  Each year we recruit four TAs
from the labs of the instructors; these TAs, along with the
instructors that are not teaching, circulate around the room during
the tutorials and help students.  They are also available during meals
and breaks for discussions and help.

The course is run on the backs of several free Web services.  Our
documentation and tutorials are placed in a GitHub repository
(github.com/ngs-docs/angus), and instructors and TAs coordinate the
addition and updating of materials there. Tutorials are written in
either reStructuredText or Markdown, two markup languages in common
use in the data science communities; presentations are posted as PDFs
and small data and source code files can be posted in native format
(text or binary) for download via ‘curl’ or ‘wget’.  We use the Sphinx
tool to combine reST and Markdown files into an HTML Web site.  Prior
to 2013, updating the Sphinx site required manual intervention on the
part of someone with write access to the Web site (hosted at
ged.msu.edu/angus/); since 2013, we have used the ReadTheDocs service
(www.readthedocs.org) to automatically build the Sphinx site and post
it at angus.readthedocs.org/.  Configuring the 2015 workshop took
approximately 5 minutes (to create a new GitHub branch and add it to
ReadTheDocs); adding new tutorials and building the site is likewise
nearly instantaneous.  An important benefit of this approach is that
each years materials remain available through both GitHub and ReadTheDocs
automatically and indefinitely, and can be easily reused (via forking,
in GitHub) by any student or instructor.

Applications are received via a Google Docs form, and reviewed via a
Google Docs spreadsheet.  All course coordination and record keeping
occurs via a Google Docs document or via e-mail.

The venue for the workshop for all six years has been the Kellogg
Biological Station (KBS), a field station belonging to Michigan State
University.  KBS provides several classrooms and lecture halls, has a
full cafeteria service, and lodging for up to 100.  It is somewhat
isolated - the nearest city, Kalamazoo, is about 30 minutes away - but
within 2 hours driving range of four airports.  After the first year
(2010), the Internet connection was upgraded to be a hard connection
to the main campus, in East Lansing; poor Internet connectivity has
never been a serious problem.  The venue is attractive for a number of
reasons: it is very inexpensive (two weeks room and board is
approximately $500), which renders the total cost of the course about
$1000 with travel; it is isolated, driving informal interactions
between students, TAs, and instructors; dining is provided as part of
the package; and, despite being isolated, it is straightforward to
travel to KBS both nationally and internationally.  Since the first
year, we do provide a car and driver for airport pickups and
drop-offs, as well as supply runs.

All significant computation is run remotely on Amazon Web Services
(“cloud”) computers.  This provides a uniform environment for
installation, configuration, and execution of software, bypassing
issues of laptop installations and hardware capacity.  While this does
raise some additional challenges - a lack of graphical interaction and
the relative inaccessibility of remote files are persistent challenges -
in practice most bioinformaticians work remotely on UNIX machines,
and so we believe that these challenges will need to be confronted by
any student that continues to do bioinformatics analysis after the
class.  In exchange, we suffer from virtually none of the challenges
that most Software Carpentry workshops (for example) experience, with
students bringing heterogeneous computing devices with a variety of
operating systems and versions installed.  Students also have full
systems access to their AWS computers, enabling software installs
without the intervention of a systems administrator.  And AWS provides
an almost completely isolated system, such that students can freely
experiment with their cloud computers without harming their laptops.
Moreover, the use of AWS ensures that students retain access to the
tutorials and infrastructure after the course is over.

Our basic approach with AWS has not changed significantly over the
years.  Most tutorials start with an empty machine and download all of
the necessary resources. Where this is impractical (e.g. where large
reference databases are needed) we provide the data via “snapshots”
that can be mounted as local disks on the Amazon machine.  Some data
sets are also cached on S3, Amazon’s storage service, to avoid the
resource usage involved with having 25 students downloading the same
large file from a lab’s Web site; this also provides resource
persistence that keeps the tutorials functioning for longer than they
might otherwise.

From 2010-2014, we asked students with Windows computers to install
TeraTerm Pro SSH (TTSSH), a freely available SSH client.  While this
was relatively simple to use once configured, the configuration steps
involved multiple conversion steps for the identity certificate as
well as several different configuration windows (@@web
instructions). Also, TTSSH did not come with a file transfer
application.  In 2015 we tried MobaXterm, a powerful tool for
connecting to remote machines with SSH that also contains a file
transfer application.  However, this was not an unqualified success,
because MobaXterm is much more complicated than TTSSH, and the
instructors and TAs did not have much experience with it.  We may try
again in 2016.

For file transfer more generally, we have been looking into CyberDuck,
which is free, cross platform, and connects to many other computers.

The drawbacks of AWS use have not been substantial, at least as
reported from course alumni. While many students have access to some
form of compute server or high performance compute cluster at their
home institutions, these home systems require specialized training and
installation that we simply cannot provide at an international course
like this one.  The biggest complaint has been from early years, when
we provided custom-built machine images - students reported that they
were unable to explain what software they had been using when they
returned to their home institutions.  We have addressed this by
switching to using Ubuntu Long Term Support images and providing
explicit Debian package installation instructions in more recent
years.

## Lessons learned

The introductory period of the workshop is incredibly important.  Many
attendees seem to arrive at the workshop with computational impostor
syndrome, and expect to be incapable of doing any significant
computational work. This inhibits them in immersing themselves in the
tutorials.  We therefore do our best to avoid overwhelming the
students with complexity at the beginning, focusing on the core issues
of Amazon Web Services, the command line, and very basic computational
work that has a strong and direct connection to their data analysis
needs.  This is why we focus on BLAST, mapping, and assembly, which
represent computational primitives that can be deployed on virtually
every project.  By motivating as much of the learning as possible by
direct appeal to their data analysis and avoiding more abstract issues
such as workflows, scripting, and statistical considerations, we keep
the attendees focused on taking a minimal path through the materials.
Observation during the course and student feedback at the end of the
course suggest that when we depart from this approach (by
e.g. introducing more complex computational considerations such as
advanced shell usage) we overwhelm students and many simply stop
learning.  In recognition of this need, we have focused on choosing
instructors for the first week who do not overwhelm the students, and
we continually redesign the first week’s curriculum to streamline the
materials and avoid too many ancillary topics.

The copy/paste tutorials are both positive and negative.  At the
beginning of the workshop, they enable students to gain familiarity
with the command line, the standard workflows, and the kinds of output
and error messages typical of UNIX.  While we encourage students to
experiment with changing options and altering workflows after the
first time through a tutorial, many students don’t find the time to do
this on their own.  Therefore, in recent years, we have provided time
for students to do one or more “self-guided” tutorials
(e.g. http://angus.readthedocs.org/en/2015/MacManes_adventure.html) in
which they must choose a set of tools and apply it to a new data set.
Typically 3/4 or more of the students can accomplish this with only
minimal help from the TAs.  Feedback from the students suggests that
this is both somewhat overwhelming and (upon successful conclusion)
very empowering.

Our use of the Amazon cloud computing platform has evolved
over the years.  In the first four years, we provided
custom software installations on Amazon by building custom images.
This proved to problematic for several reasons.  First, the images
were inflexible during the workshop itself, and often needed
alteration as instructors adapted their tutorials to student
needs. Second, these images required regular updating and often fell
out of date during the year (e.g. with respect to security patches and
bug fixes), inhibiting reuse of the materials by alumni and others.
And third, students treated the images as black boxes and when they
returned to their home institutions were often unable to identify the
software they had been using; moreover, students without significant
local computing resources or funds to pay for Amazon were left without
any options for using the materials.  In response to these challenges,
in 2014 we switched to using Ubuntu Linux Long-Term Support images and
providing install instructions for the necessary software with each
tutorial.  While the first five minutes of any tutorial were now spent
installing and updating software, in exchange the students could
identify the prerequisite software for the tutorial, communicate it to
their local sysadmins, and install it on their own laptop or desktop
computers.  Moreover, the tutorials could be updated quickly and
easily by the instructors and run at any time during the lifetime of
the Long-Term Support images - our current tutorials are tied to
Ubuntu 14.04, which is supported through 2019.

The workshop has provided room for experimenting with new teaching
techniques over the years.  In addition to adopting the Software
Carpentry “sticky” technique (above), we have tried two other
approaches.  In one approach, “the assembly exercise”, we generate
pages of “shotgun fragments” from English paragraphs and ask the
students to develop techniques to regenerate the source text (see
http://ivory.idyll.org/blog/the-assembly-exercise.html).  After about
an hour, we then discuss the strategies.  Typically students identify
at least three of the common sequence assembly strategies - OLC, De
Bruijn graph, and greedy extension.  This exercise seems to lead to a
greater intuitive understanding of what the computer is doing during
assembly, as well as identifying where heuristic approaches are needed
(e.g. in repetitive regions).  It also provides a break from the
computer screen.  In the other approach, “teach me”, we choose a topic
and an instructor, a TA, or a student who is naive to the topic, and
guide them through a solution.  For example, in 2015 we had one
student write a shell script for a workflow that involved downloading
data, mapping it, and calculating an error profile using a
pre-existing script.  This “teach me” exercise slows down the process
enough for the students to grasp the different components and also
involves clearing up some miscommunication about goals, computational
details, and techniques.

We have introduced several tutorials and technologies through the
years that we abandoned as failures.  Perhaps the most notable was an
attempt to run tutorials inside of IPython Notebooks (now Jupyter
Notebooks), which we introduced in 2012 and tried to use again in
2013.  IPython Notebooks are documents that execute Python and shell
code, dynamically display the output of graphing commands within the
document, and can also contain explanatory text.  Our naive thought
was that these notebooks were an obvious replacement for the
tutorials, in that they could contain both shell commands producing
data, and data analysis in Python of the resulting output files. In
practice, students could not easily distinguish between shell commands
and Python code, and moreover found the Python code confusing (in most
cases students were unfamiliar with Python).  After several
unsuccessful attempts to introduce this technology, we believe that
the combined cognitive burden of a new environment, a new language,
and the lack of visual cues to distinguish between the two languages
in use, makes this too challenging to introduce to beginning
computational learners.  In 2014 and 2015, we instead introduced
RStudio, which permits execution of R code within an interactive
development environment, and perhaps because this is a single language
embedded in a distinct program, students seem to be less confused by
it.

We have tried several times to teach Python, with little evident
success and much negative feedback. Student assessment shows that most
students enter the workshop with absolutely no programming experience -
many have never even seen R or Python before (@@).  While beginning
exposure may be changing as data analysis with R becomes more
prevalent, we still believe it is too much to try to teach any
significant programming or scripting beyond recording of commands into
a file. The concepts of a procedural language, data structures, and
explicit algorithms may be too large to introduce on top of the more
immediate issues of command line execution and bioinformatics
workflows.

One persistent challenge has been the confusion caused by the
separation between the file system on students' local computers and
the remote Amazon computers. Most attendees have no experience working
on remote UNIX machines, but the concept of remote files is fairly
natural due to the Web; what seems to be less natural is the idea that
commands being executed “locally” (on their screen, with their
keyboard) are producing files remotely.  There are several layers of
challenges.  First, Windows computers generally do not come with any
SSH client (for accessing remote computers) at all, which means some
software must be installed before students can create much less access
their remote files.  (Mac OS X and Linux laptops come with ssh
installed.) Second, shell interaction with files and file paths are
difficult to understand for people with only GUI experience, and so
command-line programs that require the full path of remote files are
difficult to use effectively.  Third, many commands (such as FastQC)
produce directories with many files in them, and it can be difficult
to retrieve entire directories with the “default” programs like sftp.
And, fourth, some remote files are quite large, while others are quite
small; it’s often only practical to download, much less examine, the
smaller files, but students do not have the experience to make this
decision themselves.  Our most successful attempt to resolve the issue
of remote and local files involved Dropbox, a file synchronization
service that provides Windows, Mac, and Linux clients; most students
already had a local client installed, and it was straightforward to
install it on remote UNIX machines.  In 2014 we abandoned Dropbox for
several reasons: first, students often had very large Dropbox folders,
and were also leary of downloading all their files to remote machines;
second, people lost files because on Linux it was easy to delete the
entire Dropbox directory and have that set of deletions be
synchronized; and, third, using Dropbox on remote Linux machines still
required confusing path manipulations.

This challenge is exacerbated by a lack of easy to use SSH clients
for Windows users. To our knowledge, the best options currently 
available are MobaXterm and GitBash, however neither offers a user
friendly introduction to command line usage. For instance, both programs come 
with copy/paste disabled by default, and even once activated, the controls
are unintuitive: <Enter> to copy and right-click to paste. These seemingly
small omissions and deviations from normal use can add a tremendous
amount of cognitive load to using the shell, and cause real frustration
during the first few days of the course when we rely heavily on copy/paste
style tutorials. 


## Things we might or should discuss:

* Twitter, reproducibility, etc. Open science.

* github teaching.

* strongly guided/cohesive course layout.

* who we are.

* On the fly adaptation to each year.

* Increase in instructors over the years.

* Funding.

* switch to software carpentry in 2015; comments by students about ramping up.

* can we scale?

* graph of applicant numbers

* categories of applicants! who are “attendees”?

* number of hits on web site

* week3 stuff from 2015? http://ivory.idyll.org/blog/2015-small-batch.html

* course fee

* mention: mostly Illumina

* Requests for action/tools/etc that make this kind of course easier 


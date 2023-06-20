# Jupyter Widgets weekly meeting

- When: Tuesdays [9.30AM Pacific Time](https://www.thetimezoneconverter.com/?t=9%3A30%20am&tz=San%20Francisco&)
- Where: [`jovyan` Zoom](https://zoom.us/my/jovyan?pwd=c0JZTHlNdS9Sek9vdzR3aTJ4SzFTQT09) (pwd: c0JZTHlNdS9Sek9vdzR3aTJ4SzFTQT09)

[8.0 milestone](https://github.com/jupyter-widgets/ipywidgets/milestone/30)

## 22 Nov 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Jason Grout | Databricks | @jasongrout |
|Itay Dafna| Netflix | @ibdafna |

- SSC: Vidar is tallying the results
- EC election
  - Useful if Brian, Darian, and Fernando post their interest answers

## 15 Nov 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Jason Grout | Databricks | @jasongrout |
| Maarten Breddels | - | @maartenbreddels |
|Itay Dafna| Netflix | @ibdafna |
| Pete Blois | Google | @blois |
| Martin Renou | QuantStack | @martinRenou |
| Supriya Khandekar | Bloomberg |@supriyakhandekar |
| Kellie Tay | Bloomberg | @kellietay |

- Maarten: issue
  - https://github.com/jupyter-widgets/ipywidgets/issues/3635
  - Maarten to open a PR to revert and possibly a second PR to reenable 

- Pete: rich output progress: https://github.com/jupyterlab/richoutput-js
  - https://github.com/blois/richoutput-js/tree/comms_n_widgets
  - a stab at a renderer which supports widgets on top of it: https://github.com/blois/portable-widget-manager/tree/main

- Martin: Voila removing the custom widget manager and reusing the JupyterLab `KernelWidgetManager` manager
  - https://github.com/voila-dashboards/voila/pull/1249
  - Needs https://github.com/jupyter-widgets/ipywidgets/pull/3561 for the `Output` widget. Vidar reviewing.

- Vidar: SSC representative: email went out on Saturday to the Jupyter Widgets council to vote for an SSC representative. Deadline is Sunday, 20 Nov 2022, anywhere on earth.
  - Jason to post an email about having 1-year terms for SSC rep
- Jason: EC election starting very soon: https://jupyter.org/governance/intro.html, https://jupyter.org/governance/bootstrapping_executive_council.html
- triage:
  - https://github.com/jupyter-widgets/ipywidgets/pull

## 08 Nov 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
||||

- Notes in team-compass: https://github.com/jupyter-widgets/team-compass
- Jupyter-widgets SSC representative
  - Election of SSC representative
    - if there are two people, then any form that chooses between the two people and has a "blank" option works
    - if there are more than two people, the ballot is ranked-choice.
    - Election run for 1 week
- reviewers: https://github.com/jupyter-widgets/ipywidgets/pulls

## 01 Nov 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Itay Dafna | Bloomberg LP | @ibdafna |
| Supriya Khandekar| Bloomberg LP | @supriyakhandekar|
| Kellie Tay | Bloomberg LP | @kellietay |


- Itay: ipydatagrid - Looking into moving from bloomberg org to the jupyter-widgets org, with the same maintainers
- Minimal es6 api: Jason to create repo in JupyterLab org
  - Pete and Jason can collaborate, will arrange a time
- reviewers: https://github.com/jupyter-widgets/ipywidgets/pulls

### Other discussion
- Vidar: SSC nomination process
- EC nomination process
- JupyterCon 2022: May 10-12



## 25 Oct 2022


| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Itay Dafna | Bloomberg LP | @ibdafna |
| Pete Blois | Google | @blois |
| Maarten Breddels | | @maartenbreddels |


- Widgets workshop followup items and takeaways: https://github.com/jupyter-widgets/team-compass/issues/16
  - Minimal es6 module
    - Jason has a separate repo that he hasn't pushed yet
    - Pete and Jason will work on a sample extension for JupyterLab
  - precommit PR
    - Almost there. Working on getting the doc build to not time out (doc build might be flaky?)
  - Documentation work
    - Docs contrib PR: https://github.com/jupyter-widgets/ipywidgets/pull/3616
    - We should have a more advanced example (e.g. TODO app)
  - Comm replacement https://github.com/martinRenou/comm/issues/1
    - Maarten experimented with implementing this in Solara
  - Typing in traitlets https://github.com/ipython/traitlets/pull/788
  - Fixing comm target does not exist: proceed on the JEP
  - Tech stack discussion takeaways
    - Do not move away from traitlets - give it another go with the performance improvements
    - Clear documentation on minimal api for widgets and widget managers
    - Encourage people to not use jquery, but we should still include it
    - A way to gracefully removing jquery is to lazily load jquery on view creation if you know it is going to be needed
    - Rich es6 outputs may allow us experiment with radically different tech stacks
    - AMD modules should still be produced, even after notebook 6 is deprecated. It may be really difficult to move from AMD to es6 because it would be hard to split out the widget base class to be loaded dynamically from the environment.
    - Investigate feasibility of deploying es6 modules in the future
  - Traitlets performance
       * https://github.com/maartenbreddels/traitlets/pull/1
       * https://github.com/ipython/traitlets/pull/777 (not at workshop)
  - Contrib repository
    - Discussion around using jupyter-contrib, or the Jovyan repo

- SSC and EC election
  - Vidar to run the Jupyter Widgets SSC nomination process




## 11 Oct 2022


| Name | Affiliation | GitHub |
|------|-------------|--------|
| Itay Dafna | Bloomberg LP | @ibdafna |
| Jason Grout | Databricks | @jasongrout |
| Kellie Tay | Bloomberg LP | @kellietay |
| Supriya Khandekar| Bloomberg LP| @supriyakhandekar|
| Don Jayamanne | Microsoft | @donjayamanne |
||||
||||


- Introductions
  - Supriya Khandekar, working at a Bloomberg visualization team. Attending the workshop next week.
  - Kellie Tay, working at a Bloomberg visualization team. Attending the workshop next week.
- Widgets workshop (and agenda)
    - https://docs.google.com/spreadsheets/d/1KMB3Mda1MNVXzjSm30eNO7qIW7Oj2z3nYBFY5l-sZ0A/edit#gid=998190500
    - There is a coordination Whatsapp group. Contact Itay to join the group if you are participating in the workshop.
    - 
- PRs
    - https://github.com/jupyter-widgets/ipywidgets/pull/3584





## 4 Oct 2022


| Name | Affiliation | GitHub |
|------|-------------|--------|
| Eric Gentry | Anaconda | @ericsnekbytes |
| Martin Renou | QuantStack | @martinRenou |
| Itay Dafna | Bloomberg LP | @ibdafna |
||||

- PRs 
    - https://github.com/jupyter-widgets/ipywidgets/pull/3569
    - https://github.com/jupyter-widgets/ipywidgets/pull/3584
      This PR needs some changes -> Itay is working on making a PR against the branch
      Does it impact performances?
      
- Widgets workshop planning meeting:
    - https://www.when2meet.com/?17134896-vm7sb

- Jupyter Notebook 7 (JupyterLab-based) is coming
  - What is the plan for nbextension support in ipywidgets and custom widgets libraries?
  - Should we switch from building an Notebook extension to building a more general extension that could be used by VSCode/Colab etc?

## 27 Sep 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| William Stein | SageMath, Inc. | @williamstein |
| Eric Gentry | Anaconda | @ericsnekbytes |
| Itay Dafna | Bloomberg LP | @ibdafna |
| Maarten Breddels | Maarten Breddels | @maartenbreddels |

- Migration guide
    - William comment: https://github.com/sagemathinc/cocalc/issues/6128#issuecomment-1259721179   
        - action item: william will make a little PR to the migration guide just mentioning that there are additional complexities due to the target changing, and the ipywidgets npm package numbers are not just "7 and 8".
    - Documentation guide:
      - moved from es5 to es2017 - mention in migration guide for developers, that the target needs to generate es6 classes in both the main changelog and the user widget migration guide
      - BaseManager used to be parameterized in typescript, but not anymore? Check and document in upgrading guide
    - version number of js packages are different
    - `@jupyter-widgets/base` version 4 is ipywidgets 7, version 6 is for ipywidgets 8.
    - On the es5->es2017 transition:
      - using ipywidgets in webpack is fine, but the ipywidgets js running in nodejs has problems running es6
- [Widgets workshop](https://blog.jupyter.org/jupyter-community-workshop-the-future-of-jupyter-widgets-475f67288da0)
  - 18-21 Oct, Bloomberg London office. You're invited!
  - No need to register if attending remotely, since that's entirely for food, guest passes, etc.
- Pause for guest introductions
  - Eric Gentry - working on nbclassic transition between notebook 6 and notebook 7
  - Jeremy (https://github.com/jupyter-naas)
- Review of PRs/issues
  - [8.0.x](https://github.com/jupyter-widgets/ipywidgets/milestone/37)
  - [8.1.x](https://github.com/jupyter-widgets/ipywidgets/milestone/32)
  - https://github.com/jupyter-widgets/ipywidgets/pull/3592
  - https://github.com/jupyter-widgets/ipywidgets/pull/3584
  - https://github.com/jupyter-widgets/ipywidgets/pull/3587
  - https://github.com/jupyter-widgets/ipywidgets/pull/3566
- Possible docs updates
    - API docs
        - What args? What's the event format?
        - See [this Qt API doc](https://doc.qt.io/qt-6/qtextedit.html) for qt's QTextEdit or [this JavaFX API doc](https://docs.oracle.com/javase/8/javafx/api/javafx/scene/control/TextField.html) for TextField, [this MDN doc](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) for HTML input
        - See [this](https://doc.qt.io/qt-6/layout.html) or [this other page](https://doc.qt.io/qt-6/signalsandslots.html) for examples of high level technical design documents/overviews
        - For reference, current [IntSlider](https://ipywidgets.readthedocs.io/en/stable/examples/Widget%20List.html#IntSlider) and [Button](https://ipywidgets.readthedocs.io/en/stable/examples/Widget%20List.html#Button) docs
  - Traits autogenerating docs: https://github.com/widgetti/ipyvolume/blob/1c08f9fdde4219be873f7c45e02ecec2540d5876/ipyvolume/widgets.py#L584
  - Framework for documentation types: https://documentation.divio.com/








## 20 Sep 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Itay Dafna | Bloomberg LP | @ibdafna |
| Don Jayamanne | VS Code | @donjayamanne |
| Martin Renou | QuantStack | @martinRenou |
| Sylvain Corlay | QuantStack | @SylvainCorlay |


- Widget workshop
  - 18 Oct - 21 Oct
  - Funding is available: deadline for funding requests is 10 days from now
  - [Registration](https://go.bloomberg.com/attend/invite/jupyter-community-workshop-the-future-of-jupyter-widgets/)
  - We'll try to do some things virtual
  - Publish blog post - 
  - Tweet / retweet from Jupyter
  - Discourse
  - Widgets chat channel
  - Widgets council list
  - 
  - People [elided]
  - 
- 8.0.x PRs
  - https://github.com/jupyter-widgets/ipywidgets/pull/3569

Blog post draft: https://blog.jupyter.org/ipywidgets-8-0-df1f22ef8278


## 13 Sep 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Jason Grout | Databricks | @jasongrout |


* Adding a [trove classifier](https://packaging.python.org/en/latest/specifications/core-metadata/#classifier-multiple-use) for Jupyter widgets
  * Similar to adding the PR adding JupyterLab classifiers [here](https://github.com/jupyterlab/jupyterlab/issues/9538)
  * [List of current classifiers](https://pypi.org/classifiers/)
  * Perhaps these classifiers?
    * `Framework :: Jupyter :: Jupyter Widgets :: 7`
    * `Framework :: Jupyter :: Jupyter Widgets :: 8`
    * Or should it be singular `Jupyter Widget`? (Jason thinks plural). [Examples](https://pypi.org/classifiers/) of each:
      * Plural
        * JupyterLab :: Extensions :: Themes
        * JupyterLab :: Extensions :: Mimerenderers
        * Topic :: Text Processing :: Filters
        * Topic :: Text Editors :: Word Processors
        * Topic :: Terminals
        * Topic :: Software Development :: Libraries
        * Topic :: Software Development :: Assemblers
        * Topic :: Multimedia :: Sound/Audio :: Mixers
        * Topic :: Desktop Environment :: Window Managers
      * Singular
        * Programming Language :: Python :: Implementation :: CPython
        * Programming Language :: APL
        * Operating System :: BeOS

* ipywidgets 8.0.x: https://github.com/jupyter-widgets/ipywidgets/milestone/37
  * Jason still to merge changes in https://github.com/jupyter-widgets/ipywidgets/pull/3569
* blog post
  * Jason to put up a draft of the blog post about 8.0
* 2-factor auth turned on for jupyter-widgets github org
* workshop
* Jupyter Widgets Council
  * October 3 target date
* VS Code supporting ipywidgets 8
  * https://github.com/microsoft/vscode-jupyter/issues/11217
  * Previous exploration at https://github.com/jupyter-widgets/ipywidgets/pull/3524


## 06 Sep 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Pete Blois | Google | @blois |

* [8.0.x milestone](https://github.com/jupyter-widgets/ipywidgets/milestone/37)
    * https://github.com/jupyter-widgets/ipywidgets/pull/3567 What is next?
        * To fully resolve issue, I think it would need a note in the migration guide?
    * https://github.com/jupyter-widgets/ipywidgets/pull/3569 - Maybe a unit test?.
* Blog post? Last item on [8.0.0 milestone](https://github.com/jupyter-widgets/ipywidgets/issues?q=is%3Aopen+is%3Aissue+milestone%3A8.0)
  * Jason make a medium post for editing and dressing up
  * Also post on discourse
* Pete's proposal:

Here's the public/stable API that Colab exposes to outputs:
https://github.com/googlecolab/colabtools/blob/main/packages/outputframe/lib/index.d.ts

* It hangs off of window which I know doesn't work well for JupyterLab.
* The API is intended to be bare-bones. A single typings file, no dependencies on any libraries or frameworks.
* The API is intended to be as strongly typed as possible, to attempt to avoid vagaries that can lead to breaking changes.
* Our implementation uses JS scopes to hide private members from the objects exposed, to prevent use of unintentionally exposed members. This is for compatibility, it's not considered a security boundary.

Discussion of an improved `%%javascript` magic and I mention how an API like Colab's could be exposed in a portable manner that would work in JupyterLab as well.
https://github.com/ipython/ipython/issues/13376#issuecomment-989040562

Bokeh is a good example of what we see elsewhere:
https://github.com/bokeh/bokeh/blob/0d0f40b7b0be373c2a58a2b99241de98ea49dba2/src/bokeh/core/_templates/autoload_nb_js.js#L121

They look for window.Jupyter and if present attempt to load classic notebook implementation modules via requirejs.

Where is this discussion most appropriate?
Pete did an implementation of this JS api in a Jlab extension: https://github.com/blois/js-module-renderer




## 30 August 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Pete Blois | Google | @blois |
| Itay Dafna | Bloomberg LP | @ibdafna |


* 8.0.x milestone for 8.0 compat issues
  * Went through 8.0.x milestone
* widget community workshop: *"The future of ipywidgets"*
  * London, proposed date 17th October, 4 days, can be shifted
    * More ideas:
      * ipywidgets in iframes
      * A clear comm protocol (like Colab?) https://github.com/googlecolab/colabtools/blob/main/packages/outputframe/lib/index.d.ts
      * Some people may want to participate remotely
      * 
* controls version number: https://github.com/jupyter-widgets/ipywidgets/issues/3560


## 23 August 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Martin Renou | QuantStack | @martinRenou |
| Pete Blois | Google | @blois|
| Maarten Breddels| | @maartenbreddels|
| Jeremy Tuloup | QuantStack | @jtpio |



* ipywidgets 8.0
  * Quick recap of release
    * [Done] Check to make sure there is a cap on the dependencies for ipywidgets 8
  * 

TODO issues:
* Mappings as selection options: mutually exclusive decisions:
  * https://github.com/jupyter-widgets/ipywidgets/pull/3556
  * https://github.com/jupyter-widgets/ipywidgets/pull/3557
    * Should `Dropdown(options={'a': 1, 'b': 2})` work? It worked in 7.x, we removed it in 8.x, but you can use `Dropdown(options={'a': 1, 'b': 2}.items())`. It causes people's code to break - should we reintroduce being able to pass in a dict?
      * Removed because dict used to be unordered
      * Removed also because the ownership model is unclear - if you change the dict, the options don't change.
  * Decision: Merge https://github.com/jupyter-widgets/ipywidgets/pull/3557 to reverse the removal

* What to allow through sanitizer?
    * https://github.com/jupyter-widgets/ipywidgets/pull/3565
      * Allow 'class', but make sure there is a high bar for future sanitizer additions, and ideally a standardized way for how to consider such requests. Compare to lab? Some better "gold standard"?

* Handle `KernelWidgetManager` in the JupyterLab `OutputModel`
    * https://github.com/jupyter-widgets/ipywidgets/pull/3561
    * Probably ok 

* Are these kind of typings changes backwards compatible? Fixes?
  * https://github.com/jupyter-widgets/ipywidgets/pull/3554

* Restore `.widgets` ?:
  * https://github.com/jupyter-widgets/ipywidgets/issues/3562
      * PR: https://github.com/jupyter-widgets/ipywidgets/pull/3122
      * [Possible fix](https://github.com/widgetti/react-ipywidgets/commit/6fb07845d143f02165c11405ed5bec20391b09c5)
      * Should we have a deprecated .widgets and .widget_types on Widget for backwards compatibility?
        * Yes, let's make the upgrade easier with a deprecated getter
        * [ ] Maarten doing a PR

* TODO issues: https://github.com/jupyter-widgets/ipywidgets/milestone/30
* precommit: generally positive



## 16 August 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Jason Grout | Databricks | @jasongrout |
| A. T. Darian | QuantStack | @afshin |
| Sylvain Corlay | QuantStack | @sylvaincorlay |


- ipywidgets 8
  - https://github.com/jupyter-widgets/ipywidgets/pull/3540
  - https://github.com/jupyter-widgets/ipywidgets/pull/3541
  - New doc PR:
    - Removes the building custom widget guide from the index until it can be updated to use the js cookiecutter (or ts cookie cutter updated)
    - Updating the widget author migration guide:
      - point to js cookiecutter
      - update language around 8.0
      - add a note about the public path update in the js cookiecutter
  - Blog post
    - Jason can work on it late this week or early next week. Any help will speed this up, of course :).
- [Native iterators in Lumino 2](https://github.com/jupyterlab/lumino/pull/346)




## 9 August 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Jason Grout | Databricks | @jasongrout |
| A. T. Darian | QuantStack | @afshin |
| Matt Craig | Minnesota State University Moorhead | @mwcraig |
| Itay Dafna | Bloomberg LP | @ibdafna |

- ipywidgets 8
  - ipywidgets 8 testing
    - Want positive confirmation about ipywidgets 8 working in various environments
      - Jason tested JupyterLab and basic html manager embedding
      - Things to test:
          - [ ] Test HTML manager in 3rd party widget docs and nbconvert (https://github.com/jupyter-widgets/ipywidgets/pull/3536) - OutputWidget, styling
          - [x] Test ipywidgets with JupyterLab (including old version, 1, 2, 3.0.0)
  - PRs needing review:
    - https://github.com/jupyter-widgets/ipywidgets/pull/3539
      - [x] Vidar to add commits linking changelog and migration guide and adding, for example, file upload migration material to migration guide
    - https://github.com/jupyter-widgets/widget-cookiecutter/pull/87
  - [ ] Blog post: Vidar will draft a paragraph for extension authors about you no longer going to need to update 3rd party libs every time lab has a major release. After the next release :)
- Lumino 2
  - [Request for help](https://github.com/jupyterlab/team-compass/issues/158) (`jupyterlab/team-compass`)
  - [Lumino 2 project board](https://github.com/orgs/jupyterlab/projects/4/views/1)
  - JupyterLab widget manager may need a major upgrade? It will certainly need code changes to deal with the JLab 4 API changes
  - We'll have to decide between tradeoffs:
    - bump base by a minor version, with the caveat that .luminoWidget is either Lumino 1 or 2, with the idea that most people will be compatible
    - bump base by a major version, and libraries that are okay with either lumino 1 or 2 just make the dependency an or (||).
- Widget workshop
  - ideally 3-5 days?
  - 

## 2 August 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Itay Dafna | Bloomberg LP | @ibdafna |
| William Stein | SageMath/CoCalc | @williamstein |
| Jason Grout | Databricks | @jasongrout |
| Martin Renou | QuantStack | martinRenou | 



- ipywidgets 8
    - [#3528](https://github.com/jupyter-widgets/ipywidgets/pull/3528) - I made one tweak, but William still had a request for a change.
- Jeremy is working on a Voila PR to convert to ipywidgets 8 and a jlab based framework https://github.com/voila-dashboards/voila/pull/846. Also moving ipyvolume to ipywidgets 8 https://github.com/widgetti/ipyvolume/pull/411

- Martin
  - moving dependency of ipykernel to the new comm package
  - https://github.com/martinRenou/comm
  - https://github.com/ipython/ipykernel/pull/973
  - https://github.com/jupyter-widgets/ipywidgets/pull/3533
  - https://github.com/jupyter-xeus/xeus-python/pull/548
  - Is this backwards compatible, at least so that we can release it with 8.1?
    - We can remove the ipykernel dependency in 8.1





## 26 July 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| William Stein | SageMath/CoCalc | @williamstein |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Matt Craig | Minnesota State University Moorhead | @mwcraig |


- ipywidgets 8
    - [3524](https://github.com/jupyter-widgets/ipywidgets/pull/3524): experiment is concluded, close the pr and watch for issues in the community after release
    - [3528](https://github.com/jupyter-widgets/ipywidgets/pull/3528) - minor tweak, then merge
    - [3455](https://github.com/jupyter-widgets/ipywidgets/issues/3455) - is this issue good enough for frontend authors? Answer: yes, but add a link to the changelog



## 19 July 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| William Stein | SageMath/CoCalc | @williamstein |
|Matt Craig|Minnesota State University Moorhead | @mwcraig |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Itay Dafna | Bloomberg | @ibdafna |

- Report on Scipy and the tutorial there
  - Went really well
    - Twice we had some serious technical issues with connecting computers, etc., but attendees probably didn't even notice.
    - Not much changed from last year:
      - JupyterLite
      - Widgets 8
      - Building an application
  - Probably about 20 people there, so way down from most years
  - Jupyter is still the big thing
  - Papyri talk by Matthias was excellent
  - VegaFusion by Jon Mease is an ipywidget!
  - JDAViz (scsci-provided platform for web images) is widget-based. Based on glue, etc.
  - No widget sprint, Matt worked on bqplot and other things, though. There was a little Jupyter sprinting as well.

- [8.0 milestone](https://github.com/jupyter-widgets/ipywidgets/milestone/30)
    + Went over open PRs. Some decisions:
        - Will add this to docs: https://github.com/jupyter-widgets/ipywidgets/issues/3257
        - Other decisions made in the individual issues/PRs

- [Automatically set public path](https://github.com/jupyter-widgets/widget-cookiecutter/pull/103)



## 12 July 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| William Stein | SageMath/CoCalc | @williamstein |

- Changes since last meeting:
    - https://github.com/jupyter-widgets/ipywidgets/pull/3501 - User migration docs merged.
    - https://github.com/jupyter-widgets/ipywidgets/pull/3508 - webpack public path for AMD modules improvements
    - https://github.com/jupyter-widgets/ipywidgets/pull/3510 - Backwards compatability for description_tooltip via deprecation

Remaining tasks 8.0:
- https://github.com/jupyter-widgets/ipywidgets/issues/3455 - Make a diff of the spec that is readable on RTD
- https://github.com/jupyter-widgets/ipywidgets/issues/3429 - Migration plan for frontends



(william) Community question: 
- thoughts about https://github.com/jupyter-widgets/ipywidgets/issues/3516  "I am not sure how this could be solved unless we drastically change ipywidgets' architecture."
  - discussed in the jupyter server meeting
  - ipywidgets uses comms, but comms exist outside ipywidgets, and have unknown usage that can't be completely replaced by rtc. 

- JupyterLite discussion: cool new features for docs.


## 5 July 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Matt Craig | Minnesota State University Moorhead | @mwcraig |

Meeting canceled

## 28 June 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| William Stein | SageMath/CoCalc | @williamstein |
| Itay Dafna | Bloomberg | @ibdafna |


- 8.0:
    - User migration docs 7.x->8.0 https://github.com/jupyter-widgets/ipywidgets/pull/3501

- william: for what it is worth, I'm working on finally implementing custom messages from the browser to the kernel here https://github.com/sagemathinc/cocalc/pull/6011  Also buffers: https://github.com/sagemathinc/cocalc/issues/6022

## 21 June 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Matt Craig | Minnesota State University Moorhead | @mwcraig |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| William Stein | SageMath/CoCalc | @williamstein |

- Tutorial: use jupyterlite?
  - See https://github.com/jupyter-widgets/ipywidgets/pull/3491 (and the rendered docs at https://ipywidgets--3491.org.readthedocs.build/en/3491/)

- 7.7.1: Jason to release in the next day or two
- 8.0: Coordinate over Gitter, and check in about possibly releasing Friday
- PyData London sprint: 



## 14 June 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Matt Craig | Minnesota State University Moorhead | @mwcraig |
| Martin Renou | QuantStack | @martinRenou |
| William Stein | SageMath/CoCalc | @williamstein |
| Itay Dafna | Bloomberg | @ibdafna |


- update wiki page: https://github.com/jupyter/jupyter/wiki/Jupyter-Widgets
  - Add "Documentation" column to the widget table
  - Add ipywidgets to the text above, then let the table be sorted
- Release [7.7.1](https://github.com/jupyter-widgets/ipywidgets/issues/3483)
- Question about `titles` on `Tab` and `Accordion` -- is this a list or a tuple?
- Status of several packages with respect to version 8 support:
    + [`ipyleaflet`](https://github.com/jupyter-widgets/ipyleaflet/pull/968) -- open PR that allows ipywidgets 8 only (see js dependencies).
        * [x] Will this support `ipywidgets` `7` **and** `8`, or just `8`? **Both**
    + [`bqplot`](https://github.com/bqplot/bqplot/pull/1404) -- Open PR but it is out-of-date: 
        * [x] Will this support `ipywidgets` `7` **and** `8`, or just `8`? Both 7 and 8.
        * [x] Should use version `6` instead of `5` for `@jupyter-widgets/base`, see [this line](https://github.com/bqplot/bqplot/pull/1404/files#diff-e51a40ac250c9696142466f114f754161e7e5102c0cdb5354548b757deb272f6R73).
        * [x] Should use `5` instead of `4` for `@jupyter-widgets/controls`
        * [x] Currently [uses a custom scales package](https://github.com/bqplot/bqplot/pull/1404/files#r818653111) -- this PR needs to merger first, I'm guessing: https://github.com/bqplot/bqscales/pull/49
    + [`bqscales`](https://github.com/bqplot/bqscales/pull/49) -- a dependency of `bqplot`. Some fixes needed:
        * [x] Will this support `ipywidgets` `7` **and** `8`, or just `8`? Both 7 and 8
        * [ ] Should use version `6` instead of `5` for `@jupyter-widgets/base`, see [this line](https://github.com/bqplot/bqplot/pull/1404/files#diff-e51a40ac250c9696142466f114f754161e7e5102c0cdb5354548b757deb272f6R73).
    + [`ipympl`](https://github.com/matplotlib/ipympl/pull/461) -- Open PR but may be incomplete:
        * [ ] It looks like this still imports `phosphor` instead of `lumino`.
    + [`ipytree`](https://github.com/QuantStack/ipytree) -- No PR yet.
        * [ ] Follow the migration guide to open a PR.
    + [`ipycanvas`](https://github.com/martinRenou/ipycanvas) -- needs a pull request.
        * [ ] Follow the migration guide to open a PR.
    + [`sidecar`](https://github.com/jupyter-widgets/jupyterlab-sidecar/pull/86) -- PR is open.
        * [ ] Per [this comment](https://github.com/jupyter-widgets/jupyterlab-sidecar/pull/86#issuecomment-1100566571) one commit needs to be reverted before merging.
    + [`pythreejs`](https://github.com/jupyter-widgets/pythreejs/pull/378) -- PR is open, but
        * [x] Will this support `ipywidgets` `7` **and** `8`, or just `8`? Just 8
        * [x] Need to remove `rc1` from `package.json` before merging.
    + [`ipycytoscape`](https://github.com/cytoscape/ipycytoscape/blob/master/package.json) -- 🎉 works! 🎉
        * [ ] Not sure why, though, see https://github.com/cytoscape/ipycytoscape/blob/master/package.json#L60 which doesn't include the  latest `@jupyter-widgets/base`
            * Expected, notebook and lab serve up whatever they have.
    + [`ipyevents`](https://github.com/mwcraig/ipyevents) -- 🎉 works! 🎉
        * [ ] Not sure why, though, see https://github.com/mwcraig/ipyevents/blob/main/package.json#L47 which doesn't include the  latest `@jupyter-widgets/base`
* https://github.com/jupyter-widgets/ipyleaflet/pull/988 - this change takes out the hardcoded public paths, would love to propagate to other widget packages
- border vs overflow attribute changes result from last time
- The new comm echo was causing an issue in newer versions of Lab (execution state would go wonky). Will be fixed in next release of Lab: https://github.com/jupyterlab/jupyterlab/issues/12616

### Additional discussion:

- Documentation
  - Make interactive examples with JupyterLite. Use the JupyterLite-sphinx extension
  - https://github.com/phoebe-project?language=jupyter+notebook
  - http://linear.ups.edu/fcla/section-DM.html
  - https://sagecell.sagemath.org/
  - https://github.com/executablebooks/thebe
  - https://jupyterlite-sphinx.readthedocs.io/en/latest/
  - [william] what about [a "Gallery" like matplotlib has](https://matplotlib.org/stable/gallery/index.html) but for ipywidgets?  Like we have for interact in sage: https://wiki.sagemath.org/interact (these are of course actually using ipywidgets)
  - https://alanmbarr.com/blog/four-types-software-documentation/
    - https://doc.sagemath.org/ is like this, IMHO...
  - https://dash.plotly.com/layout
  - Lacking a gallery
  - Qt reference docs are very detailed: https://doc.qt.io/qt-6/qtreewidget.html
  - Change "low level tutorial" to "low level explanation"
  - Include tutorial video in landing page
  - 

## 7 June 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Itay Dafna | Bloomberg | @ibdafna |


- PRs/issues for 8.0: https://github.com/jupyter-widgets/ipywidgets/milestone/30
- Community Workshop: 
- Tutorial: 
  07/12/2022, 8:00am-12:00pm CDT, The Jupyter Interactive Widget Ecosystem, Matthew Craig, Itay Dafna, Mariana Meireles, Youness Bennani, Ian Hunt-Isaak
- Can we have a widgets 8 release by June 17, which is when the tutorial instructions are due?
  - I think so!
- Databricks supports ipywidgets! https://docs.databricks.com/notebooks/ipywidgets.html
- Borders vs overflow attributes: in order to have the possibility to adjust borders independently, we went with border_left/right/top/bottom, with convenience properties to set the border. For the overflow attribute, we went with our normal convention of preferring the single shorthand CSS notation over individual properties.



## 31 May 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| William Stein (until 10am PDT due to https://sites.google.com/view/vantageseminar, slides: https://math.mit.edu/~drew/vantage/BhargavaSlides.pdf) | CoCalc | @williamstein |
| Itay Dafna | Bloomberg | @ibdafna |

- PRs/issues for 8.0: https://github.com/jupyter-widgets/ipywidgets/milestone/30

- I would be interested in a very quick discussion of https://github.com/jupyter-widgets/ipywidgets/pull/3114 since something similar is at the top of my personal todo list for cocalc.  (I want this more for https://cocalc.com/share, but it's the same problem.)
  - on roadmap?: definitely not, due to this being jupyter classic, and we are moving to jupyterlab, which already solves this issue, for the most part.
  - what about nbconvert / publishing
     - nbconvert is aware of widgets; save widget state.
     - e.g., this is used by our docs.  displayed using html manager
  - what if the widget state is BIG (say 50MB), e.g., 3d graphics and buffers?  2d plots + bqplot -- see this all the time.  blows up size of notebook.
     - we originally had all notebooks saved every widgets, and this was not optimal due to extensive interactive use and no garbage collection, so notebooks would rapidly increase in size
     - then we made it off by default.
     - make it very explicit when you want to save this way.
     - related discussion: sidecar files.  jupytext does this.
  - and generally what scares you about this PR?  If anything?
  - Maarten has "Solara"...
  - Subtle definition of "live widget".   View counter.
  - But in cocalc since it garbage collects if not displayed anywhere.
  - Browser memory and file size are both big concerns.
  - What about screenshot?    Widget's responsibility.  Or serialize dom...     
  - [william] Thanks!

- ipydatagrid ipywidgets 8.0 upgrade: https://github.com/bloomberg/ipydatagrid/pull/282


## 24 May 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| William Stein | CoCalc | @williamstein |
| Itay Dafna | Bloomberg | @ibdafna |





- [x] William: I implemented binary buffers for cocalc's ipywidgets frontend, and now k3d works pretty well at scale.   But I have a  question for devs I got stuck on: namely -- how does the widget manager know that all the comm messages needed to create the view have been received?  How does it predict the future?  This stumps me.
  - Messages are serialized over the iopub channel. Each message should be processed fully before later messages are processed
- Pruning the widget tree for persistence
  - Maarten Breddels implemented pruning at some point
  - Python version here: https://github.com/jupyter-widgets/ipywidgets/blob/master/python/ipywidgets/ipywidgets/embed.py

- ipywidgets 8.0
  - Several PRs updating webpack infrastructure: https://github.com/jupyter-widgets/ipywidgets/pull/3465, https://github.com/jupyter-widgets/ipywidgets/pull/3464
  - current diff of model specs between 7 and 8 (`git diff 7.x -- packages/schema/jupyterwidgetmodels.latest.md`): https://gist.github.com/jasongrout/07d52b85aaffe994db0e2a0c018a6c78
    - Why do border and overflow adopt different conventions between the overarching value vs the individual values?
    - GH best attempt: https://github.com/jupyter-widgets/ipywidgets/compare/7.x...master#diff-76c58c499131f42cddfc4b58686947ab4bc1c76e3e291ab06516109e9a9c1ce3
    - [ ] Update the schema header for ipywidgets 8.x
    - [ ] Summarize changes in the release notes
  - [ ] 


Continuing discussion from last time about post 8.0:

- font-awesome - William wrote a jquery plugin that simulates a font-awesome and manually adds the font-awesome look-alikes icons in cocalc
  - We could explicitly support, say 100 icons that cover most icons third party widgets are currently using, and the manager is responsible for providing those icons in a way that is consistent with the platform. This makes it easier for widget implementors to support the icons without having to explicitly use fontawesome. (william: I **really** like this proposal.)
- typeset - depends on mathjax? - should be a method on the manager
  - Add it as a minor release in the base manager interface


---

- William: another quick question -- what about a list of jupyter clients that support widgets?  E.g., I was recently testing and learned that datalore does now.
  - https://www.jetbrains.com/dataspell/
  - datalore.jetbrains.com
- [ ] Add a table to the docs with links to frontends that implement ipywidgets?
   - do in such a way that is in no way an endorsement
   - put it on a wiki.
   - another table of third-party ipywidgets

- Vidar: porting pythreejs to ipywidgets 7 and 8
- Jason: looking at updating docs with diff, look at todo items
- William: porting k3d to cocalc

Community workshop proposal for ipywidgets:
- October 2022 or Jan 2023
- Paris, London, San Francisco, Berlin



## 17 May 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Pete Blois | Google | @blois |
| William Stein | CoCalc | @williamstein |
| Blaec Bejarano | CoCalc | |



- es6 vs backbone extend
  - Currently ipywidgets 7.x and 8.x are generating es6 classes (not backbone.extend)
  - https://github.com/googlecolab/colab-cdn-widget-manager/blob/main/src/swizzle.ts - bridges between backbone extend and es6 classes. Just wrap the class being exposed with swizzle() and it can be constructed via ES6 new or backbone's constructor.
  - k3d uses backbone.extend
  - Pythreejs also uses backbone.extend
  - Vidar made a note in the migration guide about migrating from backbone.extend


- Remaining work for 8.0
    - https://github.com/jupyter-widgets/ipywidgets/pull/3455 - blocker for 8.x - documenting spec differences
    - [Add trimmed down readme file](https://github.com/jupyter-widgets/ipywidgets/pull/3461)
    - Merged [#3405](https://github.com/jupyter-widgets/ipywidgets/pull/3405), please add more things as you see them.
    - Potential final release next week
    - Vidar investigating the es6 migration

- Long-term API
  - Lumino is a dependency
    - Lifecycle methods - can we prefer native methods that external lifecycle events can call
  - jupyter-services is a dependency
  - font-awesome - William wrote a jquery plugin that simulates a font-awesome and manually adds the font-awesome look-alikes icons in cocalc
  - typeset - depends on mathjax? - should be a method on the manager
  - assumptions about DOM and CSS
  - Theming - should widgets be using jupyterlab variables directly?
    - Could define only jupyter widgets variables, then have the jlab manager define those



Third-party widgets
- ipycytoscape
- pythreejs
- ipyleaflet
- cadquery
- ipyvuetify
- ipymaterialui
- ipycanvas
- bqplot
- plotly
- nglviewer
- ipydatagrid
- k3d
- ipyslickgrid
- qgrid
- ipyvolume
- ipysheet

See https://www.npmjs.com/browse/depended/@jupyter-widgets/base for hundreds more.

Python to JS translater: https://github.com/sagemathinc/jsage (JPython, inside of JSage, is BSD 2-clause)

---

- William Stein presenting on ipywidgets in CoCalc
  - https://cocalc.com/wstein/support/ipwidgets-in-cocalc





## 10 May 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Jason Grout | Databricks | @jasongrout |
| Itay Dafna | Bloomberg | @ibdafna |



- William Stein presenting on ipywidgets in Cocalc on 17 May.
  - Jason will advertise on Gitter, Discourse, JLab meeting
- @DonJayamanne's talk about how Jupyter Widgets are implemented in VS Code is posted at https://www.youtube.com/watch?v=C821QIYcxd0. Thanks again Don!
- PyCon
  - PyScript and Pyodide
  - Cap for memory usage of pyodide is 2g
  - Pythreejs maintainership
- npm does not pull in 6.0.0-rc: 
    - `^1 || ^2 || ^3 || ^4 || ^5 || ^6.0.0-rc.0` will install 4.1.0, while `^1 || ^2 || ^3 || ^5 || ^6.0.0-rc.0` will install 6.0.0-rc.0
      - Use the semver calculator: https://semver.npmjs.com/
    - next vs latest tag?
    - date of publish of different versions?

- Remaining work for 8.0
    - https://github.com/jupyter-widgets/ipywidgets/pull/3442
    - https://github.com/jupyter-widgets/ipywidgets/issues/3439
    - Merged [#3405](https://github.com/jupyter-widgets/ipywidgets/pull/3405), please add more things as you see them.
    - Potential final release next week
- [Itay] Scipy tutorial
  - Iterating on content
  - Meeting with organizers to finalize content, etc.
  - `react-ipywidgets`: https://github.com/widgetti/react-ipywidgets

## 03 May 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Itay Dafna | Bloomberg | @ibdafna |


- William Stein presenting on ipywidgets in Cocalc on 17 May.
- Remaining tasks for 8.0 release. Timeline.
- Itay to add notes to the migration guide about `backbone.js` version update between ipywidgets 7.x and 8.x, which affects some `IClassicComm` mock implementations.


## 26 April 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Martin Renou | QuantStack | @martinRenou |
| Itay Dafna | Bloomberg | @ibdafna |
| Layne Sadler | AIQC | @aiqc |
|William Stein|CoCalc/SageMath|@williamstein|
| Florian Wetschoreck | Databricks | @FlorianWetschoreck |
| Tobias Krabel | Databricks | @tkrabel |
| Frederic Collonval | QuantStack | @fcollonval |

Issues
- Frontends migrating from widgets 7 to widgets 8
  - VS Code - waiting until release and customer requests
  - Colab - actually on 8 prerelease already - user code is built against 7, but run against 8
    - patched the lumino change
    - 
  - CoCalc - may be difficult, due to having one single frontend codebase, but definitely having old versions of ipywidgets installed in kernels "forever", since we support old images.  "Maybe I can just somehow change the comm messages to be compatible?";  Pete actually does basically this in Colab.  Jason says this will mostly work, but there are some subtle differences, and they will publish an official spec change doc.
- jupyter.widget.control error causing confusion: https://github.com/jupyter-widgets/ipywidgets/issues/2257
  - This is caused when ipywidgets hasn't been imported yet
  - We should move forward on the comm JEP
- migration guide, ready for another review https://github.com/jupyter-widgets/ipywidgets/pull/3405
  - did the phosphor shim
  - added note about backbone extend
- https://github.com/jupyter-widgets/ipywidgets/pull/3442
- https://github.com/jupyter-widgets/ipywidgets/issues/3443
- Cookiecutter updated so that it works with ipywidgets 7 and 8 https://github.com/jupyter-widgets/widget-ts-cookiecutter/pull/115

ipywidgets in vscode-jupyter:

https://github.com/microsoft/vscode-jupyter/wiki/Component:-IPyWidgets

Virtualization:
- Colab: uses intersection observer to defer creation of the iframes until they have been scrolled into view but never un-renders them when they go out of view. We write an 'output_height' attribute in the cell's metadata to specify the placeholder height on notebook load. Overall this sounded easier than it was in practice- thought it would take a few days, ended up taking maybe 2 months to stabilize (welcome to production)
- VS Code: We do the same in VS Code as well, render only when scrolled into view and never un-render them.
- Cocalc: is now fully virtual (except iframe html) https://github.com/sagemathinc/cocalc/pull/5844 using https://virtuoso.dev/ and seems to work.  Motivation for me is very complicated notebooks where having content rendered in the dom at all can be expensive when working with the notebook.  (Other approach is to make this less expensive -- maybe things are significantly extra expensive in cocalc.)





## 19 April 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Frederic Collonval | QuantStack | @fcollonval |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Martin Renou | QuantStack | @martinRenou |


Issues over the last week:

Items:
- Frontends migrating from widgets 7 to widgets 8, supporting both: https://github.com/jupyter-widgets/ipywidgets/issues/3429
  - How common will it be that a frontend has to support core widgets from ipywidgets 7 and 8 simultaneously?
  - Two extensions:
    - plugin for Jupyterlab ipywidgets 8 widget manager, and plugin that registers the ipywidgets 8 core controls
    - plugin that registers the ipywidgets 7 core controls
- Migration guide https://github.com/jupyter-widgets/ipywidgets/pull/3405
- ipyleaflet and jupyterlab-sidecar migrated: [jupyterlab-sidecar](https://github.com/jupyter-widgets/ipywidgets/pull/3405#issuecomment-1100566870) and [ipyleaflet](https://github.com/jupyter-widgets/ipywidgets/pull/3405#issuecomment-1100576009)
- More migrations:
  - Jason do ipympl (Ian added tests for ipywidgets 8? https://github.com/matplotlib/ipympl/pull/461)
  - Vidar do pythreejs
- ipywidgets 8 final release delayed a bit


- JSON spec


- Don's presentation postponed one week, will be next Tuesday




## 12 April 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Itay Dafna | Bloomberg LP | @ibdafna |



Issues over last week:
- https://github.com/jupyter-widgets/ipywidgets/issues/3433 - leading to creation of https://github.com/b3m2a1/ActiveHTMLWidget (example at https://github.com/jupyter-widgets/ipywidgets/issues/3433#issuecomment-1095669732)

Items:
- Conda-forge releases of RC0
- public path discussion: https://github.com/jupyter-widgets/widget-ts-cookiecutter/blob/master/%7B%7Bcookiecutter.github_project_name%7D%7D/src/extension.ts and https://github.com/jupyter-widgets/widget-cookiecutter/blob/969471848da747d5aa562b8ab00988e3117e4ccf/%7B%7Bcookiecutter.github_project_name%7D%7D/js/lib/extension.js#L8 (originating in https://github.com/jupyter-widgets/widget-cookiecutter/pull/38)
  - Can we use webpack's ['auto' public path](https://webpack.js.org/guides/public-path/#automatic-publicpath) instead of hardcoding a public path? I think this allows us to consolidate the nbextension AMD module with the dist/ CDN AMD module
- Conferences people are going to?
  - Scipy: @ibdafna, possibly @jasongrout
    -  Jupyter Widgets tutorial
  - PyCon US: possibly @jasongrout
- Interesting library for doing EDA workflows: https://pypi.org/project/dtale/. Does not seem to use ipywidgets.

Next week Don Jayamanne is presenting on widgets in VS Code. Please advertise.
- Gitter
- Discourse
- JLab dev meeting




## 5 April 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Itay Dafna | Bloomberg | @ibdafna |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
||||
||||

- Remaining 8.0 issues on Milestone: https://github.com/jupyter-widgets/ipywidgets/milestone/30


- Scipy tutorial was accepted! Scheduled Tuesday morning 8am-12 noon.

What other libraries should we try to convert?

- ipyleaflet
- pythreejs

8.0 release concerns
- 8.0rc is not working in vs code. Hypothesis: if the user has 8.0 installed in the kernel, why doesn't the 7.0 javascript work. It used to work with the 8.0 beta.
- https://github.com/microsoft/vscode-jupyter/issues/8552



April 19 - Don presenting on widgets in vs code



## 29 March 2022

No meeting.



## 15 March 2022
| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
|William Stein|CoCalc|@williamstein|


- William demo'd CoCalc RTC Markdown
- Releases! 7.7.0rc0, 8.0.0rc0
- Will release 7.7.0 final today
- Remaining 8.0 issues on Milestone: https://github.com/jupyter-widgets/ipywidgets/milestone/30
    - Migration guide: https://github.com/jupyter-widgets/ipywidgets/pull/3405
- New issue/questions, needs triage: 
    - https://github.com/jupyter-widgets/ipywidgets/issues/3411
        - Is `on_click` an observer?
    - https://github.com/jupyter-widgets/ipywidgets/issues/3412


- Question from a user (william) -- comments about upgrading from this -- probably not too bad.  Critical to be aware of backend version; make sure it is at least 7.
  - https://github.com/sagemathinc/cocalc/issues/5784
```
~/cocalc/src/packages/frontend$ grep widget package.json 
    "@jupyter-widgets/base": "^1.2.5",
    "@jupyter-widgets/controls": "^1.5.3",
    "@jupyter-widgets/output": "^1.1.5",
    "@phosphor/widgets": "^1.9.3",
```

- William: I can quickly demo ipywidgets in a whiteboard, since I have it working now...

## 8 March 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
| Vidar T Fauske | JP Morgan Chase | @vidartf |
| Steve Purves | Curvenote | @stevejpurves |
| Xiao Chen | Databricks | @xiaochen-db |
|tonyfast|Quansight|@tonyfast|
|William Stein|CoCalc| @williamstein|
|Jared Thompson|CCC|@afonit|
| Pete Blois | Google | @blois |
|Florian Wetschoreck | Databricks | @FlorianWetschoreck |
|Tobias Krabel | Databricks | @tkrabel |
| Martin Renou | QuantStack | @martinRenou |
|Hossein Falaki| Databricks|@falaki|
|Michael Piatek| Databricks|@michaelp-db|
|Itay Dafna| Bloomberg| @ibdafna|
|Trung Le|QuantStack|@trungleduc|


- Introductions


### Merged PRs:
- [Echo state updates in a backwards-compatible way](https://github.com/jupyter-widgets/ipywidgets/pull/3394)
- [Limit dependabot to run-time dependencies only](https://github.com/jupyter-widgets/ipywidgets/pull/3402)

### PRs to review:
- [Backport echo_update messages to 7.x](https://github.com/jupyter-widgets/ipywidgets/pull/3400)
- [Add migration guide for 8.0](https://github.com/jupyter-widgets/ipywidgets/pull/3405)
- [Follow up on echo updates](https://github.com/jupyter-widgets/ipywidgets/pull/3407)
- [Make sure we serialize dictionary into valid JSON #3408](https://github.com/jupyter-widgets/ipywidgets/pull/3408)

### 7.7 and 8.0 RC/release plans
- RC this week?

### Other items

- Recording meetings




### [Pete Blois](https://github.com/blois): ipwyidgets on Colab

- [Notes](https://colab.research.google.com/gist/blois/9c9c66b4e1e9672b123f2ed8cda9091d/colab-widgets.ipynb#scrollTo=6JEQUuO2DBGI)




## 1 March 2022

| Name | Affiliation | GitHub |
|------|-------------|--------|
| Jason Grout | Databricks | @jasongrout |
|Gayle Ollington|NumFOCUS|@gollington |
| Vidar T Fauske| JP Morgan Chase | @vidartf |
| Steve Purves | Curvenote | @stevejpurves |

Merged PRs:
- https://github.com/jupyter-widgets/ipywidgets/pull/3390
- https://github.com/jupyter-widgets/ipywidgets/pull/3393

- Introductions
    - Gayle Ollington
      * [Jupyter Community Building Committee Charter](https://jupyter.org/governance/communitybuildingcommittee.html)
      * [December 2021 Jupyter Community Update](https://blog.jupyter.org/jupyter-community-2021-update-84c5cd3c5e75)
      * Keep an eye out for an upcoming blog post with a survey about JupyterCon
    - Steve Purves
      - co-founder of [CurveNote](https://curvenote.com/) 
      - Rowan works a lot on Myst, Steve works a lot on Thebe
      - Working on ipywidgets in Thebe
- Presentations on ipywidgets implementations
  - Pete Blois next week
  - Advertise so others who are implementing ipywidgets can attend
  - Steve Purves: widgets in curvenote
- Echo state updates backwards compatible: https://github.com/jupyter-widgets/ipywidgets/pull/3394
  - Vidar is reviewing this in the next 36 hours or so.
  - Look at https://github.com/jupyter-widgets/ipywidgets/issues/3111 - is Maarten's case where frontend and backend go out of sync taken care of?
- 7.x and 8.x releases
  - Jason and Itay can do an RC release of 7.7 and 8.0 after #3394 gets merged.
- Jupyter Books (Steve)
  - Executable book implementing something like Like Brett Victor's [Tangle](http://worrydream.com/Tangle/) library
    - Jason once implemented a ipywidgets widget that used something like the Tangle library to do widgets in text.
  - Reference also recent discussions on Discourse about interpolating variable values into Markdown
  - SageCell
    - https://sagecell.sagemath.org/
    - https://utmost.aimath.org/ (see also the PreText books that integrate Sage Cell, like )
- Executable docs for ipywidgets using JupyterLite: https://twitter.com/martinRenou/status/1498321869363154947?s=20&t=stPowTab4Z9CE00CBPDbrg


## 22 Feb 2022
Attendees: @vidartf, @jasongrout, @sylvaincorlay

Merged PRs:
- https://github.com/jupyter-widgets/ipywidgets/pull/2975
- https://github.com/jupyter-widgets/ipywidgets/pull/3389
- https://github.com/jupyter-widgets/ipywidgets/pull/3387

Discussion points for 8.0:
- https://github.com/jupyter-widgets/ipywidgets/issues/3392
  - Jason will work on this this week

## 15 Feb 2022
Attendees: @williamstein, @vidartf, @ibdafna, @ivanov 

Merged PRs:
 - https://github.com/jupyter-widgets/ipywidgets/pull/3380
 - https://github.com/jupyter-widgets/ipywidgets/pull/3377
 - https://github.com/jupyter-widgets/ipywidgets/pull/3337

Quick demo:
  - @williamstein can show you ipywidgets in his work-in-progress (very buggy!) [collaborative whiteboard](https://github.com/sagemathinc/cocalc/pull/5674).  (Must be before 10am.)

Releasing 8.0
- @ibdafna to cut the release

## 8 Feb 2022

Attendees: @williamstein, @vidartf, @martinRenou, @jtpio, @jasongrout, @ibdafna, @ianhi

Other things that we would need/want for 8.0?
- https://github.com/jupyter-widgets/ipywidgets/pull/3004

PRs for review:
- https://github.com/jupyter-widgets/ipywidgets/pull/3366
- https://github.com/jupyter-widgets/ipywidgets/pull/3367

Merged PRs:
- https://github.com/jupyter-widgets/ipywidgets/pull/3368
- https://github.com/jupyter-widgets/ipywidgets/pull/3373
- https://github.com/jupyter-widgets/ipywidgets/pull/3338
- https://github.com/jupyter-widgets/ipywidgets/pull/3335
- https://github.com/jupyter-widgets/ipywidgets/pull/3370

7.x release
- Martin backporting the control channel
- 7.x minor release later this week

8.0 RC release
- This week after two PRs above merged.

Discussion
- Is there a project that involves building a UI with drag and drop and widgets?
  - Cocalc collaborative whiteboard
  - https://github.com/voila-dashboards/voila-gridstack
  - Databricks has something, but not ipywidgets
  - Internal product (closed source) has been developed
  - [ipyflex](https://github.com/trungleduc/ipyflex)
  - https://gitlab.com/cosapp/cosapp_lab 

- Scipy talks
  - Tutorial going in
  - Maarten talking about building larger ipywidgets applications
  - Jason may submit a talk on core ipywidgets 8 (or maybe a lightning talk, depending on how much stuff there is)
  - Itay may submit a talk about ipydatagrid

- ipywidgets controlling scientific instruments
  - ESRF
  - 


- Moving state to the server side
  - https://github.com/jupyterlab/jupyterlab/pull/11599

### Naive Community Questions (answers above):

Question (@williamstein): is there any existing software that let you do things like insert sliders, buttons, etc., graphically on a canvas, then generate code and uses ipywidgets to implement things under the hood?  (Instead of laying everything out via code.)  I'm stumbling into implementing something like this, and want to compare notes.

@martinRenou: ~~~Do you mean rendering widgets on a canvas? 
I remember discussing this with Wolf Vollprecht (having multiple renderers for ipywidgets: DOM, Canvas, Qt etc) this sounds hard to implement to me, but it could be possible?~~~ (misunderstood the question)

## 1 Feb 2022

Attendees: @jasongrout, @vidartf, @afonit, @martinRenou, @ibdafna

- Introductions

- https://github.com/jupyter-widgets/ipywidgets/issues/3357
- https://github.com/jupyter-widgets/ipywidgets/issues/3359
- https://github.com/jupyter-widgets/ipywidgets/pull/3360
- https://github.com/jupyter-widgets/ipywidgets/issues/3364
- https://github.com/jupyter-widgets/ipywidgets/pull/3365
- https://github.com/jupyter-widgets/ipywidgets/pull/3335


- Please comment on https://github.com/jupyter/enhancement-proposals/issues/86

- Close to RC. To release RC, resolve:
  - https://github.com/jupyter-widgets/ipywidgets/issues/3357
  - https://github.com/jupyter-widgets/ipywidgets/pull/3365
  - https://github.com/jupyter-widgets/ipywidgets/issues/3350
  - https://github.com/jupyter-widgets/ipywidgets/pull/3335


Grids on ipywidgets
- qgrid seems dead, uses slickgrid
- ipyaggrid uses aggrid, also not maintained
- recommend ipydatagrid
- See also https://github.com/glue-viz/glue-jupyter/pull/129

Scipy
- Deadline 11 Feb. Tutorial spearheaded by Matt
- Maarten is writing a react-like layer on top of ipywidgets, may submit a talk



## 25 Jan 2022

Attendees: @vidartf, @martinRenou, @ivanov, @jasongrout, @SylvainCorlay, @ibdafna

- Decision-making body
- Should we merge? https://github.com/jupyter-widgets/ipywidgets/pull/3335
  - Comm message protocol discussion: how do we determine if a comm target is registered?
    - A target can be registered, comms created, then the target unregistered
    - {target_name: [list of comms]}, and also return active comm targets, filtered by the target_name.
    - Jason will file a JEP proposing two changes: (Update: filed at https://github.com/jupyter/enhancement-proposals/issues/86)
- Porting 7.x widgets to 8.x
  - Good test cases:
    - [X] bqplot: uses phosphor https://github.com/bqplot/bqplot/pull/1404 works fine!
    - [ ] pythreejs: doesn't use es6 classes yet
    - https://github.com/mariobuikhuizen/ipyvue/pull/55/files
- Consider changing the meeting time for this group?
  - Perhaps after the decision-making body is formed?


## 18 Jan 2022

Attendees: @vidartf, @martinRenou, @SylvainCorlay, @jasongrout, @ibdafna

- Decision-making body: look for an email
- [Dependabot config](https://docs.github.com/en/code-security/supply-chain-security/keeping-your-dependencies-updated-automatically/configuration-options-for-dependency-updates)
- https://github.com/jupyter-widgets/ipywidgets/pull/3343
- Needs review https://github.com/jupyter-widgets/ipywidgets/pull/3335
- HTML manager vs JupyterLab manager


## 11 Jan 2022

Attendees: @vidartf, @martinRenou, @SylvainCorlay, @jasongrout, @ibdafna

- Maarten: https://github.com/jupyter-widgets/ipywidgets/pull/3343
  - Bump protocol to 3.0, since there are communication channels set up in both directions. Having a browser that understand 2.0 talking to a kernel speaking 3.0 should lead to sliders jumping around (since the echo field is ignored). Having a browser that understands 3 talking to a kernel that understands 2 means that channels that are opened by the browser will be rejected since the major version number does not match in the comm_open of the kernel.


- Martin: Updated https://github.com/jupyter-widgets/ipywidgets/pull/3335
  - Needs review
  - Martin will check if there is some heuristic in comm info message to determine if comm target exists or not
  - We should make an update to the docs/ipykernel to have the comm info request have an error status if the comm target does not exist.
- Bug fix with nbconvert https://github.com/jupyter-widgets/ipywidgets/pull/3342
  - Looks good, basically adds the lab variables as a default for html manager if they are not alreadyd defined on the page
  - Could check the generated code to see if there is a difference with how the css is put on the page in the conditional
  - 


## 4 Jan 2022
Attendees: @vidartf, @martinRenou, @ibdafna

* https://github.com/jupyter-widgets/ipywidgets/pull/3326

* Should we consider this for 8.0.0? https://github.com/jupyter-widgets/ipywidgets/pull/3335
  - @jasongrout: I would love to see this in 8.0

* This week:
    * Add Maarten's PR to the change log
    * Release RC0
    * Try to migrate some of our widget libraries
    * Document any changes pertaining to migrating widget packages from 7.x to 8.x
    * Document Maarten's changes to the protocol spec
    * Release RC1
    * Announce RC


## 21 Dec 2021
Attendees: @maartenbreddels, @ibdafna, @SylvainCorlay, 
@jasongrout

* Jason: upgrading to TypeScript 4.5 has incompatibilities with older JupyterLab versions, so we hold off upgrading it in the RC.
* Discussed Maarten's [front-end sync PR](https://github.com/jupyter-widgets/ipywidgets/pull/3195#issuecomment-995552089). Sylvain and Itay will meet on Dec 22nd to run a a few final tests and, if not issues are found, merge and release RC0 :tada:

## 14 Dec 2021

Attendees: @vidartf, @ibdafna, @martinRenou, @jasongrout, @real-slim-chadi

* [Front-end sync PR](https://github.com/jupyter-widgets/ipywidgets/pull/3195)
* Typescript 4.5 update
* RC:
  * Jason working on a dependency update
  * Maarten working on his PR
  * We can release RC this week
* Where to start contributing?
    * https://github.com/jupyter-widgets/ipywidgets/blob/master/CONTRIBUTING.md
    * Good first issues are tagged here: https://github.com/jupyter-widgets/ipywidgets/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22
    * @real-slim-chadi taking a look at the new contributor guide
* Meeting next week (21 Dec)


## 7 Dec 2021

Attendees: @maartenbreddels, @ibdafna, @jtpio, @SylvainCorlay, @vidartf, @jasongrout

Front-end sync PR:
- https://github.com/jupyter-widgets/ipywidgets/pull/3195
- Long discussion about what this PR does, and decision to put in a default-off global switch and get it in for 8.0RC after review.

Issues:
- (not discussed) https://github.com/jupyter-widgets/ipywidgets/issues/3322


Porting widgets to 8.0: will need to work on a migration guide.
Current changelog: https://ipywidgets.readthedocs.io/en/latest/changelog.html#not-released-yet


## 30 Nov 2021

Attendees: @vidartf, @ibdafna, @jtpio, @SylvainCorlay

8.0 release plans
- Currently on track. We will all try to update a 3rd-party library to support 8.0 before next week, when we plan to do an RC unless there are any blockers.
- New convenience trait/serializers for serializing full IEEE float values (i.e., NaN and infinity)
- Introductions
  - chadiabifadel

PRs
- Merged Galata update: https://github.com/jupyter-widgets/ipywidgets/pull/3279
- Releaser update: https://github.com/jupyter-widgets/ipywidgets/pull/3298 - needs another pass
- https://github.com/jupyter-widgets/ipywidgets/pull/3302: restart checks, port to master
- [Allow Output.clear_output() to be thread-safe.](https://github.com/jupyter-widgets/ipywidgets/pull/3261)


## 23 Nov 2021

Attendees: @vidartf, @martinRenou, @ibdafna, 

New issues/PRs since last meeting:
- https://github.com/jupyter-widgets/ipywidgets/pull/3313
- (from last week) https://github.com/jupyter-widgets/ipywidgets/issues/3310
- (from last week) https://github.com/jupyter-widgets/ipywidgets/issues/3309
- https://github.com/jupyter-widgets/ipywidgets/pull/3314
- https://github.com/jupyter-widgets/ipywidgets/pull/3315
- https://github.com/jupyter-widgets/ipywidgets/pull/3317

Review needed:
- https://github.com/jupyter-widgets/ipywidgets/pull/3304
- https://github.com/jupyter-widgets/ipywidgets/pull/3279

## 16 Nov 2021

Attendees: @vidartf, @martinRenou, @SylvainCorlay, @jtpio, @ibdafna, @jasongrout

New issues/PRs since last meeting:
- https://github.com/jupyter-widgets/ipywidgets/pull/3311
- (not discussed) https://github.com/jupyter-widgets/ipywidgets/issues/3310
- (not discussed) https://github.com/jupyter-widgets/ipywidgets/issues/3309

8.0 beta release party



## 09 Nov 2021

Attendees: @vidartf, @jasongrout, @ibdafna, @martinRenou, @jtpio


- New issues last week:
    - https://github.com/jupyter-widgets/ipywidgets/issues/3307
    - https://github.com/jupyter-widgets/ipywidgets/issues/3306

- Is this backwards compatible or not?
    - https://github.com/jupyter-widgets/ipywidgets/issues/3282
      - We think this is probably backwards compatible. Jason is opening an issue in Lumino about this general pattern.

- Review of PR from Trung Le Duc (Error widgets)
    - https://github.com/jupyter-widgets/ipywidgets/pull/3304
      - There are a few outstanding questions in the PR review.

- Review resolved ?
    - https://github.com/jupyter-widgets/ipywidgets/pull/3021

- 8.0 triage:
    - Seem very hard to achieve: https://github.com/jupyter-widgets/ipywidgets/issues/2605
      Ok to drop?
      
- Changelog:
    - widgetnbextension needs changelog entry: https://github.com/jupyter-widgets/ipywidgets/compare/7.6.2...7.6.3

- Beta release:
    - Changelog this week
      - Jason to generate PR listing
      - Everyone fill out
    - Next week, release beta the hour before meeting

- Meeting: Change to an hour meeting


## 02 Nov 2021

Attendees: @jtpio, @jasongrout, @vidartf, @ibdafna

- Widgets in RetroLab
  - Classic notebook Widgets menu:
    - Save Notebook Widget State
    - Clear Notebook Widget State
    - Download Widget State
    - Embed Widgets
  - RetroLab widget menu options:
    - Settings > Save Widget State Automatically (toggle)
  - In classic notebooks, it is possible to author a widget in a notebook: https://ipywidgets.readthedocs.io/en/stable/examples/Widget%20Custom.html
- This last week:
  - Sylvain released widgetsnbextension 3.5.2 with https://github.com/jupyter-widgets/ipywidgets/pull/3290 and https://github.com/jupyter-widgets/ipywidgets/pull/3280 (first release since 3.5.1 in Jul 2019)
  - Retrieve state on new comm channel: https://github.com/jupyter-widgets/ipywidgets/pull/3021 review
  - Error Widget fallback: https://github.com/jupyter-widgets/ipywidgets/pull/3304: Itay assigned as reviewer
  - https://github.com/jupyter-widgets/ipywidgets/pull/3301: Jason reviewing
  - Trigger setLayout on before-attach? https://github.com/jupyter-widgets/ipywidgets/issues/2605
- Releasing beta next week?
  - We have PR for moving to Jupyter Releaser
  - As discussed two weeks ago, we'll do a manual release and look at what needs to be done to bump package versions.




## 26 Oct 2021

Attendees: @ibdafna, @martinRenou, @vidartf, @jasongrout, @trungleduc

- Merge? https://github.com/jupyter-widgets/ipywidgets/pull/3271

- Two new PRs this week:
    - https://github.com/jupyter-widgets/ipywidgets/pull/3301
      - Possible choices for dir name
        - python
        - python_packages
        - pypackages
    - https://github.com/jupyter-widgets/ipywidgets/pull/3302

- Trung: Fallback widget when the widget fails to render. Following up https://github.com/jupyter-widgets/ipywidgets/pull/2960

- Triage for [8.0](https://github.com/jupyter-widgets/ipywidgets/milestone/30):
  - Are there any issues that will need a PR?
  - Are there any PRs without an assigned reviewer?
  - Any assistance needed on assigned PRs?
  - Which issues should be moved to another milestone?

## 19 Oct 2021

Attendees: @jtpio, @martinRenou, @jasongrout, @sylvaincorlay

- 8.0.0a6 on conda:
    - PR to update to 8.0.0a6: https://github.com/conda-forge/ipywidgets-feedstock/pull/71
    - Follow-up to remove the Python 3.10 upper bound: https://github.com/conda-forge/ipywidgets-feedstock/pull/72

- Bug fix https://github.com/jupyter-widgets/ipywidgets/pull/3296

- Fech all widgets in one go on the control channel: https://github.com/jupyter-widgets/ipywidgets/pull/3021

- Hold sync during set_state https://github.com/jupyter-widgets/ipywidgets/pull/3271

- Jupyter Releaser:
    - Started by David in https://github.com/jupyter-widgets/ipywidgets/pull/3298
    - How do we want to version the packages?
    - Do we want to be able to release packages indepedently? `ipywidgets`, `jupyterlab_widgets`, `widgetsnbextension` -> Yes
    - Currently bumping versions is like a complex decision tree
        - We could start by documenting how versions are bumped. For example how to decide whether this is a minor version and what updating a given package means for the other packages that depend on it.
        - The releaser takes a `spec` as input. So we would have to encode the bump we would like to do, and let the bump script update the right packages.
        - There is also the protocol version as another version to consider. This one could be versioned manually.

## 12 Oct 2021

Attendees: @vidartf, @jasongrout, @martinRenou, @piiq, @jtpio, @ibdafna

- Itay show and tell
    - https://github.com/ibdafna/webdash

- Introductions

- Triage for [8.0](https://github.com/jupyter-widgets/ipywidgets/milestone/30):
  - https://github.com/jupyter-widgets/ipywidgets/pull/3021
      - Additive, so no need to explicitly target 8.0. Will target 7.x and 8.x
  - Are there any issues that will need a PR?
  - Are there any PRs without an assigned reviewer?
      - https://github.com/jupyter-widgets/ipywidgets/pull/3271
      - https://github.com/jupyter-widgets/ipywidgets/pull/3286
  - Any assistance needed on assigned PRs?
    - Do not wait for the "displayed" promise to be resolved before applying the layout https://github.com/jupyter-widgets/ipywidgets/pull/3288
  - Which issues should be moved to 8.1?

## 5 Oct 2021

Attendees: @vidartf, @jasongrout, @ibdafna

- VS Code support
  - Still support 7.x
  - Support most widgets except VPython
  - Catboost - 

- Triage for [8.0](https://github.com/jupyter-widgets/ipywidgets/milestone/30):
  - Are there any issues that will need a PR?
  - Are there any PRs without an assigned reviewer?
      - https://github.com/jupyter-widgets/ipywidgets/pull/3271
      - https://github.com/jupyter-widgets/ipywidgets/pull/3288
      - Translation: https://github.com/jupyter-widgets/ipywidgets/pull/3286
  - Any assistance needed on assigned PRs?
  - Which issues should be moved to 8.1?



## 28 Sep 2021

Attendees: @martinRenou, @vidartf, @jasongrout, @SylvainCorlay

- [#3280](https://github.com/jupyter-widgets/ipywidgets/pull/3280/)
    - Can we confidently make a minor release of widgetnbextension? Probably best to branch from last 

- [#3021](https://github.com/jupyter-widgets/ipywidgets/pull/3021)
    - This PR does not change the current logic for ipywidgets. It is adding a new Comm entry point for Voila to fetch all widgets models at once.


## 21 Sep 2021

Attendees: @jtpio, @martinRenou, @vidartf, @jasongrout, @ibdafna

- Martin:
  - Select widget: prevent arbitrary selection if there is currently no selection and the option list changes https://github.com/jupyter-widgets/ipywidgets/pull/3284
  - Doc fixing, fix "process.env is undefined" issue which prevented the HTMLManager to render widgets https://github.com/jupyter-widgets/ipywidgets/pull/3283
  - widgetsnbextension: Throw an exception if the widget fails to render, this allows the Notebook to fallback on other mimetypes repr https://github.com/jupyter-widgets/ipywidgets/pull/3280 (should be tested with current Notebook version/should do a Notebook version check in widgetsnbextension?)

- Jeremy:
  - rebased Itay's PR: https://github.com/jupyter-widgets/ipywidgets/pull/2834

- Triage for [8.0](https://github.com/jupyter-widgets/ipywidgets/milestone/30):
  - Are there any issues that will need a PR?
      - [#2762](https://github.com/jupyter-widgets/ipywidgets/issues/2762)
      - [#3247](https://github.com/jupyter-widgets/ipywidgets/issues/3247)
  - Are there any unassigned PRs?
  - Any assistance needed on assigned PRs?


## 14 Sep 2021

Attendees: @vidartf, @jtpio, @ianhi, @ibdafna

Triage for [8.0](https://github.com/jupyter-widgets/ipywidgets/milestone/30)

- Add dragging behaviour properties to sliders: [#2834](https://github.com/jupyter-widgets/ipywidgets/pull/2834)
    - Rebase + rename to american spelling
    - Merge and do a final review after having it in alpha

- If we include [#2762](https://github.com/jupyter-widgets/ipywidgets/issues/2762), we should also consider [#2605](https://github.com/jupyter-widgets/ipywidgets/issues/2605)
  - Current proposal: Add three new promises: `attached`, `layedOut`, `shown`. Then deprecate `displayed`, and have that resolve at the same time as `attached` for now (retaining its current behavior). This will allow for third-party libraries to update on their own time, but still resolve the ambiguity.


## 7 Sep 2021

Attendees: @jasongrout @ibdafna




## 31 August 2021

Attendees: @vidartf, @jasongrout, @ibdafna


- https://github.com/jupyter-widgets/ipywidgets/pull/3262

Triage for [8.0](https://github.com/jupyter-widgets/ipywidgets/milestone/30):


Itay:
- 8.0.0a6 prerelease due out this week
- 7.1.x patch release with ipython_genutils dependency

Vidar: [#2259](https://github.com/jupyter-widgets/ipywidgets/issues/2259), [#2800](https://github.com/jupyter-widgets/ipywidgets/issues/2800)
Itay: #3230, #3247
Jason: #2762



## 24 August 2021

Attendees: @vidartf, @jasongrout

Triage for 8.0:
- Discussion around extending widgets support to JupyterLab code consoles.



## 17 August 2021

Attendees: @vidartf, @jasongrout, @ibdafna, @blois

Pete:
- Colab introducing support for custom widgets
- API is based on es6 modules for compatiblity 
- Proof of concept at https://github.com/googlecolab/colab-cdn-widget-manager, has working example. Feel free to reach out with bugs or questions.

Itay:
- TS cookiecutter maintenance - Itay volunteering, and Vidar will help him come up to speed.


Triage for 8.0:
- https://github.com/jupyter-widgets/ipywidgets/pull/2728
- https://github.com/jupyter-widgets/ipywidgets/issues/2636
- https://github.com/jupyter-widgets/ipywidgets/pull/3004

- Merged https://github.com/jupyter-widgets/ipywidgets/pull/3142
- 



## 10 August 2021

Attendees: @jasongrout, @vidartf, @ibdafna

Itay:
- https://github.com/jupyter-widgets/ipywidgets/pull/2728

Vidar:
- Github lints ("Unchanged files with check annotations")
- Should we fix typos in help string retoractively in specs? https://github.com/jupyter-widgets/ipywidgets/pull/3246

Triage:
- https://github.com/jupyter-widgets/ipywidgets/issues/3247
- 



## 3 August 2021

Attendees: @jasongrout, @vidartf, @ibdafna



## 13 July 2021

Attendees: @jasongrout, @vidartf, @ibdafna

- @ibdafna: ipywidgets tutorial report (Monday morning at Scipy)
  - We cleaned up the [tutorial repo](https://github.com/jupyter-widgets/tutorial), updated the binder, etc.
    - Didn't show some of Maarten's widgets because they weren't working
  - Went well. Generated buzz on Twitter. It was a new audience, with many people exposed to ipywidgets for the first time. About 100 attendees.
  - Need short introduction to decorators
  - The styling/layout section was a bit long. Instead, just give a few examples, then jump in with examples and day-to-day issues people will face.
  - We'll continue refreshing and rotating the list of ipywidgets libraries we are showing each year.
  - The online platform worked well, the platform worked pretty well. The platform "Q&A" section was a bit awkward to use.
  - Lots of questions, especially compared to last year.
- ipywidgets 8.0 triage
  - Went through recent PRs, reviewed and merged some, and assigned out others.


- https://codepath.org/ - interesting mentoring opportunity


## 6 July 2021

Attendees: @jasongrout, @vidartf, @jtpio, 

- ipywidgets tutorial update (next week)
- ipywidgets community update
- ipywidgets 8.0 triage


* 8.0 Beta release!


## 29 June 2021

Attendees: @jasongrout, @davidbrochart, @ilyabo, @ibdafna

- Welcome Itay (@ibdafna) as an ipywidgets maintainer!
- Scipy 2021 tutorial is in two weeks, based on ipywidgets 7.6.3, JupyterLab 3.0 (Matt Craig, Itay Dafna, Mariana, Martin, Youness)
  - This year emphasizing additional widget libraries, like ipycanvas, ipycytoscape, ipydatagrid, etc.
- 8.0a5 is out: lots of package upgrades, so please test third-party widgets
- @ilyabo, @davidbrochart: Async widgets: we have a modified kernel now that enables async processing of widgets.
  - Each cell is launched as an async function and is launched as a task. You can run several cells concurrently. If there is purely synchronous code, it runs as normal. Essentially the top-level await is converted to an await inside an async function, so await returns control to the event loop.
  - https://github.com/davidbrochart/akernel
  - https://github.com/ipython/ipykernel/issues/696
  - There is a pattern to force "synchronous" running of successive cells with `await __task__()`


## 22 June 2021

Attendees: @jtpio, @vidartf, @ibdafna, @jasongrout
- NoUISlider upgrade PR: https://github.com/jasongrout/ipywidgets/pull/4

## 15 June 2021

Attendees: @jtpio, @vidartf, @ibdafna

- Dependency updates PRs by Jason:
    - TypeScript 4.3: https://github.com/jupyter-widgets/ipywidgets/pull/3162
    - Webpack: https://github.com/jupyter-widgets/ipywidgets/pull/3211
- Quick pass on the new issues to assign them to the 8.0 milestone if needed

## 8 June 2021

Attendees: @vidartf, @jtpio

- Quick update on outstanding work on [8.0](https://github.com/jupyter-widgets/ipywidgets/milestone/30)


## 1 June 2021

Attendees: @vidartf, @jasongrout

- [8.0 triage](https://github.com/jupyter-widgets/ipywidgets/milestone/30)
- 


## 18 May 2021

Attendees: @jtpio, @ianhi, @jasongrout, 

- Ilya: async messaging: https://github.com/ipython/ipykernel/pull/589 https://github.com/ipython/ipykernel/issues/646
  - imjoy: https://github.com/imjoy-team/imjoy-rpc
  - https://github.com/jupyter-widgets/ipywidgets/issues/3039

- 8.0 timeline

- Ian: widget persistence + matplotlib lots of discussion on mpl gitter (https://gitter.im/matplotlib/matplotlib?at=609d4203c12aec4aa2c2346f)


## 04 May 2021

Attendees: @ibdafna, @ianhi, @vidartf

- Ian: Changing defaults? 
    - https://github.com/jupyter-widgets/ipywidgets/issues/3193

- Vidar:
    - Maarten posted this on gitter https://github.com/jupyter-widgets/ipywidgets/pull/3195

## 27 Apr 2021

Attendees: @jtpio, @ibdafna, @ianhi, @vidartf

- Discussions
    - Async widget methods and dispatching GUI messages asynchronously:
        - https://github.com/ipython/ipykernel/issues/646
        - https://github.com/ipython/ipykernel/pull/589
    - ~~Status of `ipywidgets` 8.0 release~~



## 13 Apr 2021

Attendees: @ianhi, @jasongrout

- Discussions
    - Deep dive on potential of using `stdin` as a mechanism for blocking until a user interacts with a widget.
    - Ian will create an issue summarizing everything that can be used as a starting place for further investigations.

## 08 Apr 2021

Attendees: @ianhi, @jtpio

- Discussions
    - Next meeting time results: http://whenisgood.net/nx49zs8/results/538da5r
    - Best candidate: Tuesdays at 09:00 am Pacific

## 01 Apr 2021

Attendees: @jtpio, @ianhi, @jasongrout, @sylvaincorlay, @blois


- Jeremy:
    - Thanks Mehmet for adding visual regression testing: https://github.com/jupyter-widgets/ipywidgets/pull/3172
    - Martin did something similar for `bqplot`: https://github.com/bqplot/bqplot/pull/1315


- Ian:
        - Blocking? https://github.com/ianhi/custom-ipywidget-howto/issues/17
            

- Discussion
  - [Time change poll](https://github.com/jupyter-widgets/team-compass/issues/9) about a new time for the meeting
  - Blocking
      - https://github.com/ipython/ipykernel/pull/589 
      - Wrap around stdin to get blocking? This is what google colab does:
      -  https://github.com/googlecolab/colabtools/blob/main/google/colab/_message.py 
      -  Can possibly think about it as we have rich output, but not rich input.

  - 8.0 release. Stability of ipywidgets for breaking into multiple releases to get 8.0 done?

## 25 Mar 2021

Attendees: @jtpio, @jasongrout, @vidartf


- Jeremy
    - Export LabWidgetManager and KernelWidgetManager: https://github.com/jupyter-widgets/ipywidgets/pull/3166
    - Revive "Restore widgets in batches" PR? https://github.com/jupyter-widgets/ipywidgets/pull/2765

- Vidar
    - Is this ok as is, or does it need any further changes? :) 
      - https://github.com/jupyter-widgets/ipywidgets/pull/2972
      - https://github.com/jupyter-widgets/ipywidgets/pull/2715


- Discussion
  - [Time change poll](https://hackmd.io/5XWHyOoLTRqyXzEHsVmxXg?edit) about a new time for the meeting


## 18 Mar 2021

Attendees: @jasongrout, @SylvainCorlay, @ianhi, @jtpio

- Jason
  - 8.0.0a4 (supporting jlab 3) was released 22 Feb
  - Traitlets 4 vs 5: https://github.com/jupyter-widgets/ipywidgets/pull/3110

- Ian
    - Making 8.0 happen? (We're going to keep plugging away at it, no firm timeline, dependent on how much work people put into the issues and PRs on the milestone)
    - New Issue Labels? https://github.com/jupyter-widgets/ipywidgets/issues/3161

- Jeremy
    - Initial steps for a widget examples repo: https://github.com/ianhi/custom-ipywidget-howto/pull/13
      - Plan to move to jupyter widgets organization as it gets polished
    - Update to TypeScript 4.2? Should this go in before 8.0? https://github.com/jupyter-widgets/ipywidgets/pull/3162

What is the status of pythreejs? It is now a prebuilt extension compatible with JupyterLab 3.

Meeting times: We decided to move to a weekly meeting schedule to help development momentum, and re-evaluate the time to better accommodate those that are actually coming to the meetings. Since we're in the middle of a confusing time where some of us are on Daylight Saving time and others aren't, we'll keep the 7am Pacific Daylight Time meeting for Thursday, 25 Mar. Jason will then send out a poll for a new meeting time for a weekly meeting for the following week.

## 4 Mar 2021

Attendees: @jasongrout, @vidartf, @maartenbreddels, @ianhi, @ibdafna, @jtpio, @marimeireles


- ian 
    - What is advice for people who want blocking widgets
      - ([SO](https://stackoverflow.com/questions/66461305/tell-background-process-to-wait-until-matplotlib-ipython-widget-has-finished-dra) + [issue](https://github.com/jupyter-widgets/ipywidgets/issues/3145))
      * See https://ipywidgets.readthedocs.io/en/stable/examples/Widget%20Asynchronous.html
      * Perhaps we change the kernel protocol to allow the kernel to process comm messages even if it is not idle (for example, if a cell has an await)?
      * We could ship the utility functions in the widget async docs, and make some more examples using them. Especially with dependencies on modern Python + ipykernel, this is more feasiable than before.
      * Make async waiting easier to use - make docs more approachable, ship utility function (ian make issue)
  - Automated releasing secrets? who can add them? https://github.com/jupyter-widgets/jupyterlab-sidecar/pull/62
    - We could release based on setting a tag. That makes it very easy, maybe too easy?
    - We could release based on drafting a GitHub release.
    - Ian and Jason getting together to explore this.
  - [not discussed] unify cookiecutter? https://github.com/jupyter-widgets/team-compass/issues/4

- Maarten
  - Saving widget state: https://github.com/jupyter-widgets/ipywidgets/pull/3114

- Discussion
  - ipywidgets contrib
    - Perhaps open a repo or new github org. Things are merged basically automatically, with very minimal vetting.


## 18 Feb 2021

Attendees: Jason, Maarten, Jeremy, Ian, Sylvain, Martin, Itay

* Jason
  - [Changelog](https://github.com/jupyter-widgets/ipywidgets/pull/3132): https://ipywidgets--3132.org.readthedocs.build/en/3132/changelog.html
  - [Python 3.5 support](https://github.com/jupyter-widgets/ipywidgets/pull/3131)
  - [lmWidget vs luminoWidget](https://github.com/jupyter-widgets/ipywidgets/pull/3118)

* Jeremy
  - New cookiecutter based tutorial: https://ipywidgets.readthedocs.io/en/latest/examples/Widget%20Custom.html
  - We should try to finish and merge the 3.0 PR: https://github.com/jupyter-widgets/widget-ts-cookiecutter/pull/83

* Itay
  - Modernizing our python packaging practices: https://github.com/jupyter-widgets/widget-cookiecutter/pull/87
  - A suggestion to use setuptools_scm

* Ian
  - [custom ipywidget howto](https://github.com/ianhi/custom-ipywidget-howto) into docs?
    - Transfer to jupyter-widgets org


* Maarten
	- State sync bug https://github.com/jupyter-widgets/ipywidgets/issues/3111
	  - Related issue on echoing comm messages to all clients: https://github.com/jupyter/jupyter_client/issues/263
	- ~~(post 8.0.0) Only save visible widgets, and save by default: https://github.com/jupyter-widgets/ipywidgets/pull/3114~~
  - ~~(post 8.0.0) Embed mime bundles: https://github.com/jupyter-widgets/ipywidgets/pull/3107~~


### Discussion
- widgets.register what is it for?
    - should it be default in the cookiecutter? - no
    - should be better documented - Ian open an issue.
- Triage 8.0 issues


## June 8th 2020

Attendees: Vidar, Afshin, Sylvain, Jason, Madhur, Odile, Mario

Voilà
-----

Themes discussion:
 - Currently in JLab we only have [mimerender shortcut extensions](https://github.com/jupyterlab/jupyterlab/blob/1df0e18951194bb5ec230e76441e8108e0b472e7/dev_mode/index.js#L89)
 - Can we restrict themes to just css files and some metadata file?
 - If we needed, we could build support for css-only themes in jlab 2.
 - We'll take up the discussion in the JupyterLab dev meeting

ipywidgets
----------

Review PRs that have had progress

- HTML sanitization PR: https://github.com/jupyter-widgets/ipywidgets/pull/2785
  - API questions:
    - user api: description_html / description_allow_html / allow_html_description
      - description_html is nice and compact, but doesn't clearly indicate that it is a boolean affecting the description attribute
      - 'allow' 
    - widget manager functions: plaintext_sanitize/inline_sanitize
- Vendoring notebooks PR: https://github.com/jupyter-widgets/ipywidgets/pull/2831
    - Check if we could make a symlink in conf.py for the notebooks instead of copying.

- Cookiecutters tend to go out of shape over time, creating stale cookies :smile: How do we ensure they stay up to date?

  - Use GH actions upon PR merge and add an item in the release check-list



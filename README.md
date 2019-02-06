<head>
  <meta charset="utf-8" />
  <!-- Web Experience Toolkit (WET) / Boîte à outils de l'expérience Web (BOEW)
wet-boew.github.io/wet-boew/License-en.html / wet-boew.github.io/wet-boew/Licence-fr.html -->
  <title>Beta - Web Application Accessibility Guidance - Agriculture and Agri-Food Canada (AAFC)</title>
  <meta content="width=device-width, initial-scale=1" name="viewport" />

  <meta property="dcterms:issued" title="W3CDTF" content="2013-02-21" />
  <meta property="dcterms:modified" title="W3CDTF" content="2018-07-25" />
  <meta property="dcterms:format" title="gcformat" content="" />
  <meta property="dcterms:title" content="Canadian agri-food sector intelligence" />
  <meta property="aafc:subject" title="aafcsubject" content="bottled water industry;organic food industry;nutraceuticals" />
  <meta property="dcterms:subject" title="gccore" content="benchmarks;imports;food" />
  <meta property="dcterms:description" content="Poultry and Eggs Poultry and egg market information historical trends trade data and import permits factsheets and publications federally registered plants and stations and a list of industry associations." />
  <meta property="dcterms:language" title="ISO639-2" content="eng" />
  <meta property="keywords" content="snack foods;Livestock Livestock;Seafood Information;economic growth;three-month advance access period" />
  <meta property="dcterms:audience" title="gcaudience" content="" />
  <meta property="dcterms:type" title="gctype" content="resource list" />
  <meta property="dcterms:creator" content="Agriculture and Agri-Food Canada" />
  <meta property="dcterms:spatial" title="gcregions" content="" />

  <script src="https://www.agr.gc.ca/assets.adobedtm.com/caacec67651710193d2331efef325107c23a0145/satelliteLib-c2082deaf69c358c641c5eb20f94b615dd606662.js"></script>
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.css" />

  <meta property="dcterms:service" content="AAFC-AAC" />
  <meta property="dcterms:accessRights" content="2" />

  <!--[if gte IE 9 | !IE ]><!-->
  <link href="https://www.agr.gc.ca/res/wet-boew4/assets/favicon.ico" rel="icon" type="image/x-icon" />
  <link rel="stylesheet" href="https://www.agr.gc.ca/res/wet-boew4/css/wet-boew.min.css" />
  <!--<![endif]-->
  <link rel="stylesheet" href="https://www.agr.gc.ca/res/wet-boew4/css/theme.min.css" />
  <!--[if lt IE 9]>
  <link href="https://www.agr.gc.ca/res/wet-boew4/assets/favicon.ico" rel="shortcut icon"/>
  <link rel="stylesheet" href="https://www.agr.gc.ca/res/wet-boew4/css/ie8-wet-boew.min.css"/>
  <link rel="stylesheet" href="https://www.agr.gc.ca/res/wet-boew4/css/ie8-theme.min.css"/>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
  <script src="https://www.agr.gc.ca/res/wet-boew4/js/ie8-wet-boew.min.js"></script>
  <![endif]-->

  <noscript>
    <link rel="stylesheet" href="https://www.agr.gc.ca/res/wet-boew4/css/noscript.min.css" /></noscript>

  <!-- CustomScriptsCSSStart -->
  <link rel="stylesheet" href="https://www.agr.gc.ca/res/aafc-aac4/css/theme.css" />
  <link rel="stylesheet" href="https://www.agr.gc.ca/res/aafc-aac4/css/util.css" />
  <!--[if lte IE 8]>
  <link rel="stylesheet" href="https://www.agr.gc.ca/res/aafc-aac4/css/theme-ie.css" />
  <link rel="stylesheet" href="https://www.agr.gc.ca/res/aafc-aac4/css/util-ie.css" />
  <![endif]-->
  <script src="https://www.agr.gc.ca/res/aafc-aac4/js/util.js"></script>
  <!-- CustomScriptsCSSEnd -->
</head>

# <abbr title="Web Experience Toolkit">WET</abbr> 4.0  Accessibility Guidance for Web Applications

Living document that offers technical guidance for Agriculture and Agri-Food Canada (AAFC) web applications compliance against Government of Canada Standard on Web Accessibility

### Table of Contents

-   Coding and design tips
-   Multi-page Forms (in progress)
-   Form Instructions
    -   Short Instruction in a paragraph
    -   Long Instruction with structured content
-   Data Tables
    -   Complex tables with multi-level headers
    -   Add/Delete buttons in data table (in progress)
    -   Caption of datatable (in progress)

### Coding and Design Tips!

Here are tips and resourced related to designing a form for the web:

-   [Design better forms](https://uxdesign.cc/design-better-forms-96fadca0f49c): Common mistakes designers make when designing web forms and how to fix them.
-   [10 usability heuristics for user Interface Design](https://www.nngroup.com/articles/ten-usability-heuristics/): Usability considerations for user interface design.

Tools to use:

-   [Balsamiq WireFrames](https://balsamiq.com/): Create wireframes for the interface before starting prototype and lets discuss the potential accessibility concerns.

### Form Inline Instruction

Inline instruction and descriptions related to a specific field can be missed by screen reader users in Forms Mode if not linked properly to the form field.

**Examples on Form Instruction**
<table>
  <thead>
    <th class="active">Topic</th>
    <th class="active">Coding</th>
    <th class="active">Presentation</th>
  </thead>
  <tbody>
    <tr>
      <th id="short-instruction-aria-describedby">Short Instruction - Paragraphusing aria-describedby</th>
      <td>
        <p>aria-describedby refring to the ID of the description which makes it avaialble the user when focus is placed on the input field. <br>
          Related WCAG Reference : <a href="https://www.w3.org/TR/WCAG20-TECHS/ARIA15.html">ARIA15</a></p>
        <p> <span class="eye-slash">&nbsp;</span><a href="https://youtu.be/8P1xolZhavM">Screen reader demo for aria-describedby</a></p>
        <details>
          <summary class="well well-sm">Code Snippet: Paragraph - Short Instruction</summary>
          <code class="prettyprint">&lt;label for=&quot;orgname&quot;&gt;Organization Code (e.g. XY001) &lt;strong class=&quot;required&quot;&gt;(required)&lt;/strong&gt;&lt;/label&gt;<br>
            <br>
            &lt;!--Instruction sentence with an ID--&gt;
            <br>
            &lt;p <strong>id=&quot;orgname_desc&quot;</strong>&gt;The 4 digits that exist on the letter of registration&lt;/p&gt;<br>
            <br>
            &lt;!--instruction linked to the input field using aria-describedby--&gt;
            <br>
            &lt;input id=&quot;orgname&quot; name=&quot;orgname&quot; type=&quot;text&quot; <strong>aria-describedby=&quot;orgname_desc&quot;</strong>/&gt;
          </code>
        </details>
      </td>
      <td>
        <div class="form-group">
          <label for="orgname" class="required"><span class="field-name">Organization Code (e.g. XY001)</span> <strong class="required">(required)</strong></label>
          <p id="orgname_desc">The 4 digits that exist on the letter of registration</p>
          <input class="form-control" id="orgname" name="orgname" type="text" required pattern=".{2,}" data-rule-minlength="2" aria-describedby="orgname_desc" />
        </div>
      </td>
    </tr>
  </tbody>
  <tr>
    <th>Long Instruction - Structured content</th>
    <td>
      <p> When the instruction is long with a structured content. The instruction appears on a dialog box e.g. <a href="https://wet-boew.github.io/wet-boew/demos/lightbox/lightbox-en.html">WET 4 lightbox</a> and accessed through a link with an
        Icon, help with invisible &quot;Instruction follows.&quot; link text. </p>
      <p>Variety of icons exist on the WET 4 list of <a href="http://wet-boew.github.io/wet-boew-styleguide/v4/design/icons-en.html">Glyphicons and Font Awesome icons</a></p>
      <p> Expected behaviors:
      </p>
      <ul>
        <li>User clicks on the help anchor opens the dialog box. </li>
        <li>User clicks on the close button within the dialog box, focus returns to the help anchor </li>
        <li>Screen reader user has no access to the background page with dialog box is open </li>
      </ul>
      <p><strong>Note: </strong>aria-hidden="true" added to the link<a href="http://bootstrapdocs.com/v3.3.1/docs/components/#glyphicons"> to accomodate modern versions of assistive technologies reading Accessible icons </a></p>
      <p><strong>Incorrect use: </strong>Do not use this for short instruction. Short instruction should appear visible on the page as part of the &lt;lable&gt; tag or <a href="short-instruction-aria-describedby">using aria-describedby</a> to
        avoid an extra click. </p>
      <details>
        <summary class="well well-sm">Code snippet: Structured Content - Instruction</summary>
        <code class="prettyprint"> &lt;div class=&quot;form-group&quot;&gt;<br>
          &lt;div&gt;<br>
          &lt;label for=&quot;partnership-share&quot; id=&quot;partnership-label&quot;&gt;In a partnership? Enter your share &lt;/label&gt;<br>
          &lt;!-- A warning for Screen reader users
          that instruction link will follow. Warning is read through the use of arbia-labelledby--&gt;<br>
          <strong>&lt;span class=&quot;wb-inv&quot; id=&quot;inst-partner-follows&quot;&gt;Instruction follows.&lt;/span&gt;<br>
            &lt;/div&gt;</strong><br>
          <br>
          &lt;!-- both label and instruction have ids. IDs are used to link them with the input field via aria-labelledby in the correct reading order--&gt; <br>
          &lt;input style=&quot;display: inline;&quot; type=&quot;number&quot; min=&quot;0&quot; max=&quot;100&quot; class=&quot;form-control valid&quot; name=&quot;partnership-share&quot; id=&quot;partnership-share&quot; <strong>aria-labelledby=&quot;partnership-label
            inst-partner-follows&quot;</strong>/&gt;<br>
          <br>
          &lt;!-- Instruction link --&gt;
          <br>
          &lt;a href=&quot;#partner-percentatge-instruction&quot; class=&quot;wb-lbx lbx-modal lbx-hide-gal&quot;&gt; &lt;span class=&quot;glyphicon glyphicon-question-sign&quot; aria-hidden=&quot;true&quot;&gt;&lt;/span&gt; Help &lt;span
          class=&quot;wb-inv&quot;&gt;Instruction follows.&lt;/span&gt;&lt;/a&gt;<br>
          <br>
          &lt;!-- lightbox code--&gt;<br>
          &lt;section id=&quot;partner-percentatge-instruction&quot; class=&quot;mfp-hide modal-dialog modal-content overlay-def&quot;&gt;<br>
          &lt;header class=&quot;modal-header&quot;&gt;<br>
          &lt;h2 class=&quot;modal-title&quot;&gt;Instruction - In a partnership? Enter your share&lt;/h2&gt;<br>
          &lt;/header&gt;<br>
          &lt;div class=&quot;modal-body&quot;&gt;<br>
          &lt;p&gt;If you are involved in a partnership or a Whole Farm, you can either: &lt;/p&gt;<br>
          &lt;ul&gt;<br>
          &lt;li&gt;enter the information for 100% of the partnership or Whole Farm and then enter your percentage share; or&lt;/li&gt;<br>
          &lt;li&gt;enter the information for only your share of the partnership or Whole Farm and enter your percentage share as 100%.&lt;/li&gt;<br>
          &lt;/ul&gt;<br>
          &lt;/div&gt;<br>
          &lt;/section&gt;<br>
          &lt;/div&gt;</code>
      </details>
    </td>
    <td>
      <div class="form-group">
        <div>
          <label for="partnership-share" id="partnership-label">In a partnership? Enter your share </label>
          <span class="wb-inv" id="inst-partner-follows">Instruction follows.</span></div>
        <input style="display: inline;" type="number" min="0" max="100" class="form-control valid" name="partnership-share" id="partnership-share" aria-labelledby="partnership-label inst-partner-follows" />
        <a href="#partner-percentatge-instruction" class="wb-lbx lbx-modal lbx-hide-gal"> <span class="glyphicon glyphicon-question-sign" aria-hidden="true"></span> Help <span class="wb-inv">Instruction follows.</span></a>
        <section id="partner-percentatge-instruction" class="mfp-hide modal-dialog modal-content overlay-def">
          <header class="modal-header">
            <h2 class="modal-title">Instruction - In a partnership? Enter your share</h2>
          </header>
          <div class="modal-body">
            <p>If you are involved in a partnership or a Whole Farm, you can either: </p>
            <ul>
              <li>enter the information for 100% of the partnership or Whole Farm and then enter your percentage share; or</li>
              <li>enter the information for only your share of the partnership or Whole Farm and enter your percentage share as 100%.</li>
            </ul>
          </div>
        </section>
      </div>
    </td>
  </tr>
</table>

### Data Tables
Data tables require the use of `<th>` for the table heads.

**Coding Data Tables**
<table class="table table-bordered">
  <caption class="text-left">Coding Data Tables</caption>
  <thead>
    <th class="active">Topic</th>
    <th class="active, col-md-4, col-lg-4">Coding</th>
    <th class="active, col-md-6, col-lg-6">Visual Presentation</th>
  </thead>
  <tbody>
    <tr>
      <th id="data-table-mutli-levels">Tables with multi-level headers</th>
      <td>
        <p>Use id and headers attributes to associate data cells with header cells in data tables. <br>
          Related WCAG Reference : <a href="https://www.w3.org/TR/WCAG20-TECHS/H43.html">H43</a></p>
        <details>
          <summary class="well well-sm">Code snippet: Table with multi-level headers</summary>
          <code class="prettyprint">&lt;table&gt;<br>
            &lt;caption&gt;<br>
            Availability of holiday accommodation<br>
            &lt;/caption&gt;<br>
            &lt;thead&gt;<br>
            &lt;tr&gt;<br>
            &lt;td&gt;&lt;/td&gt;<br>
            &lt;th id=&quot;stud&quot; scope=&quot;col&quot;&gt;Studio&lt;/th&gt;<br>
            &lt;th id=&quot;apt&quot; scope=&quot;col&quot;&gt;&lt;abbr title=&quot;Apartment&quot;&gt;Apt&lt;/abbr&gt;&lt;/th&gt;<br>
            &lt;th id=&quot;chal&quot; scope=&quot;col&quot;&gt;Furnished Apartment&lt;/th&gt;<br>
            &lt;th id=&quot;villa&quot; scope=&quot;col&quot;&gt;Villa&lt;/th&gt;<br>
            &lt;/tr&gt;<br>
            &lt;/thead&gt;<br>
            &lt;tbody&gt;<br>
            &lt;tr&gt;<br>
            &lt;th id=&quot;par&quot; class=&quot;span&quot; colspan=&quot;5&quot; scope=&quot;colgroup&quot;&gt;Paris&lt;/th&gt;<br>
            &lt;/tr&gt;<br>
            &lt;tr&gt;<br>
            &lt;th headers=&quot;par&quot; id=&quot;pbed1&quot;&gt;1 bedroom&lt;/th&gt;<br>
            &lt;td headers=&quot;par pbed1 stud&quot;&gt;11&lt;/td&gt;<br>
            &lt;td headers=&quot;par pbed1 apt&quot;&gt;0&lt;/td&gt;<br>
            &lt;td headers=&quot;par pbed1 chal&quot;&gt;25&lt;/td&gt;<br>
            &lt;td headers=&quot;par pbed1 villa&quot;&gt;-&lt;/td&gt;<br>
            &lt;/tr&gt;<br>
            &lt;tr&gt;<br>
            &lt;th headers=&quot;par&quot; id=&quot;pbed2&quot;&gt;2 bedroom&lt;/th&gt;<br>
            &lt;td headers=&quot;par pbed2 stud&quot;&gt;-&lt;/td&gt;<br>
            &lt;td headers=&quot;par pbed2 apt&quot;&gt;43&lt;/td&gt;<br>
            &lt;td headers=&quot;par pbed2 chal&quot;&gt;52&lt;/td&gt;<br>
            &lt;td headers=&quot;par pbed2 villa&quot;&gt;32&lt;/td&gt;<br>
            &lt;/tr&gt;<br>
            &lt;tr&gt;<br>
            &lt;th id=&quot;rome&quot; class=&quot;span&quot; colspan=&quot;5&quot; scope=&quot;colgroup&quot;&gt;Rome&lt;/th&gt;<br>
            &lt;/tr&gt;<br>
            &lt;tr&gt;<br>
            &lt;th id=&quot;rbed1&quot; headers=&quot;rome&quot;&gt;1 bedroom&lt;/th&gt;<br>
            &lt;td headers=&quot;rome rbed1 stud&quot;&gt;13&lt;/td&gt;<br>
            &lt;td headers=&quot;rome rbed1 apt&quot;&gt;21&lt;/td&gt;<br>
            &lt;td headers=&quot;rome rbed1 chal&quot;&gt;22&lt;/td&gt;<br>
            &lt;td headers=&quot;rome rbed1 villa&quot;&gt;3&lt;/td&gt;<br>
            &lt;/tr&gt;<br>
            &lt;tr&gt;<br>
            &lt;th id=&quot;rbed2&quot; headers=&quot;rome&quot;&gt;2 bedroom&lt;/th&gt;<br>
            &lt;td headers=&quot;rome rbed2 stud&quot;&gt;-&lt;/td&gt;<br>
            &lt;td headers=&quot;rome rbed2 apt&quot;&gt;23&lt;/td&gt;<br>
            &lt;td headers=&quot;rome rbed2 chal&quot;&gt;43&lt;/td&gt;<br>
            &lt;td headers=&quot;rome rbed2 villa&quot;&gt;30&lt;/td&gt;<br>
            &lt;/tr&gt;<br>
            &lt;/tbody&gt;<br>
            &lt;/table&gt;</code>
        </details>
      </td>
      <td>
        <table class="table table-bordered">
          <caption class="text-left">Availability of holiday accommodation</caption>
          <thead>
            <tr>
              <td></td>
              <th id="stud" scope="col">Studio</th>
              <th id="apt" scope="col"><abbr title="Apartment">Apt</abbr></th>
              <th id="chal" scope="col">Furnished Apartment</th>
              <th id="villa" scope="col">Villa</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th id="par" class="span" colspan="5" scope="colgroup">Paris</th>
            </tr>
            <tr>
              <th headers="par" id="pbed1">1 bedroom</th>
              <td headers="par pbed1 stud">11</td>
              <td headers="par pbed1 apt">0</td>
              <td headers="par pbed1 chal">25</td>
              <td headers="par pbed1 villa">-</td>
            </tr>
            <tr>
              <th headers="par" id="pbed2">2 bedroom</th>
              <td headers="par pbed2 stud">-</td>
              <td headers="par pbed2 apt">43</td>
              <td headers="par pbed2 chal">52</td>
              <td headers="par pbed2 villa">32</td>
            </tr>
            <tr>
              <th id="rome" class="span" colspan="5" scope="colgroup">Rome</th>
            </tr>
            <tr>
              <th id="rbed1" headers="rome">1 bedroom</th>
              <td headers="rome rbed1 stud">13</td>
              <td headers="rome rbed1 apt">21</td>
              <td headers="rome rbed1 chal">22</td>
              <td headers="rome rbed1 villa">3</td>
            </tr>
            <tr>
              <th id="rbed2" headers="rome">2 bedroom</th>
              <td headers="rome rbed2 stud">-</td>
              <td headers="rome rbed2 apt">23</td>
              <td headers="rome rbed2 chal">43</td>
              <td headers="rome rbed2 villa">30</td>
            </tr>
          </tbody>
        </table>
      </td>
    </tr>
  </tbody>
</table>

### References
**Use of WAI-ARIA aria-describedby to link description to a form element**
W3C, ARIA1: Using the aria-describedby property to provide a descriptive label for user interface controls, November 20 2018, URL: <https://www.w3.org/TR/WCAG20-TECHS/ARIA1.html>

**Coding Step by Step indicator**
W3C, Multi-page Forms, February 05 2019, URL: <http://www.w3.org/WAI/tutorials/forms/multi-page/#using-step-by-step-indicator>

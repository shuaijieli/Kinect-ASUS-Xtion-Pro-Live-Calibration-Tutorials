<!--more-->
# Kinect-ASUS-Xtion-Pro-Live-Calibration-Tutorials
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>

### Preparation
#### Installation
* Enter the following codes in your terminal

```bash
sudo apt-get install ros-indigo-openni-camera
sudo apt-get install ros-indigo-openni-launch
```

* Remember to modify `GlobalDefaults.ini` if you are using Asus Xtion Pro Live
```bash
sudo gedit /etc/openni/GlobalDefaults.ini
```
then uncomment the line: `;UsbInterface=2` (just delete the `;` symbol)

#### Test your Asus Xtion Pro Live with ROS

* To view the rgb image:
```bash
roslaunch openni_launch openni.launch
rosrun image_view image_view image:=/camera/rgb/image_raw
```

* To visualize the depth_registered point clouds:

```bash
roslaunch openni_launch openni.launch depth_registration:=true
rosrun rviz rviz
```

See `kienct calibration.pdf` to view the tutorial of how to calibrate kinect. And note that these codes have been tested on OpenCV 2.4. 


html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}

body {
  margin: 0;
}

article,aside,details,figcaption,figure,footer,header,hgroup,main,nav,section,summary {
  display: block;
}

audio,canvas,progress,video {
  display: inline-block;
  vertical-align: baseline;
}

audio:not([controls]) {
  display: none;
  height: 0;
}

[hidden],template {
  display: none;
}

a {
  background: transparent;
}

a:active,a:hover {
  outline: 0;
}

abbr[title] {
  border-bottom: 1px dotted;
}

b,strong {
  font-weight: bold;
}

dfn {
  font-style: italic;
}

h1 {
  font-size: 2em;
  margin: 0.67em 0;
}

mark {
  background: #ff0;
  color: #000;
}

small {
  font-size: 80%;
}

sub,sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}

sup {
  top: -0.5em;
}

sub {
  bottom: -0.25em;
}

img {
  border: 0;
}

svg:not(:root) {
  overflow: hidden;
}

figure {
  margin: 1em 40px;
}

hr {
  box-sizing: content-box;
  height: 0;
}

pre {
  overflow: auto;
}

code,kbd,pre,samp {
  font-family: monospace, monospace;
  font-size: 1em;
}

button,input,optgroup,select,textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}

button {
  overflow: visible;
}

button,select {
  text-transform: none;
}

button,html input[type="button"],input[type="reset"],input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}

button[disabled],html input[disabled] {
  cursor: default;
}

button::-moz-focus-inner,input::-moz-focus-inner {
  border: 0;
  padding: 0;
}

input {
  line-height: normal;
}

input[type="checkbox"],input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}

input[type="number"]::-webkit-inner-spin-button,input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}

input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}

input[type="search"]::-webkit-search-cancel-button,input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}

fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}

legend {
  border: 0;
  padding: 0;
}

textarea {
  overflow: auto;
}

optgroup {
  font-weight: bold;
}

table {
  border-collapse: collapse;
  border-spacing: 0;
}

td,th {
  padding: 0;
}

* {
  box-sizing: border-box;
}

input,select,textarea,button {
  font: 13px/1.4 Helvetica, arial, freesans, clean, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol";
}

body {
  min-width: 1020px;
  font: 13px/1.4 Helvetica, arial, freesans, clean, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol";
  color: #333;
  background-color: #fff;
}

a {
  color: #4183c4;
  text-decoration: none;
}

a:hover,a:active {
  text-decoration: underline;
}

hr,.rule {
  height: 0;
  margin: 15px 0;
  overflow: hidden;
  background: transparent;
  border: 0;
  border-bottom: 1px solid #ddd;
}

hr:before,.rule:before {
  display: table;
  content: "";
}

hr:after,.rule:after {
  display: table;
  clear: both;
  content: "";
}

h1,h2,h3,h4,h5,h6 {
  margin-top: 15px;
  margin-bottom: 15px;
  line-height: 1.1;
}

h1 {
  font-size: 30px;
}

h2 {
  font-size: 21px;
}

h3 {
  font-size: 16px;
}

h4 {
  font-size: 14px;
}

h5 {
  font-size: 12px;
}

h6 {
  font-size: 11px;
}

small {
  font-size: 90%;
}

blockquote {
  margin: 0;
}

.lead {
  margin-bottom: 30px;
  font-size: 20px;
  font-weight: 300;
  color: #555;
}

.text-muted {
  color: #999;
}

.text-danger {
  color: #bd2c00;
}

.text-emphasized {
  font-weight: bold;
  color: #333;
}

ul,ol {
  padding: 0;
  margin-top: 0;
  margin-bottom: 0;
}

ol ol,ul ol {
  list-style-type: lower-roman;
}

ul ul ol,ul ol ol,ol ul ol,ol ol ol {
  list-style-type: lower-alpha;
}

dd {
  margin-left: 0;
}

tt,code {
  font-family: Consolas, "Liberation Mono", Menlo, Courier, monospace;
  font-size: 12px;
}

pre {
  margin-top: 0;
  margin-bottom: 0;
  font: 12px Consolas, "Liberation Mono", Menlo, Courier, monospace;
}

#realtime .status {
  overflow: visible;
  position: absolute;
  top: -5px;
  left: 0;
  background: url("/public/images/github-status.png");
  width: 26px;
  height: 26px;
  display: block;
  margin: 0 5px 0 0;
}

#realtime .up {
  background-position: 0 0;
}

#realtime .problem {
  background-position: 0 -53px;
}

#realtime .down {
  background-position: 0 -26px;
}

.container {
    max-width: 920px;
    margin: 0 auto 20px auto;
}

#header {
    background: #FAFAFA;
    background: -moz-linear-gradient(#FAFAFA, #EAEAEA);
    background: -webkit-linear-gradient(#FAFAFA, #EAEAEA);
    -ms-filter: "progid:DXImageTransform.Microsoft.gradient(startColorstr='#fafafa', endColorstr='#eaeaea')";
    border-bottom: 1px solid #CACACA;
    box-shadow: 0 1px 0 rgba(255, 255, 255, 0.4),0 0 10px rgba(0, 0, 0, 0.1);
}

#markup {
    padding: 3px;
}

#markup article {
    padding-top: 30px;
}

.markdown-body {
  overflow: hidden;
  font-family: "Helvetica Neue", Helvetica, "Segoe UI", Arial, freesans, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  word-wrap: break-word;
}

.markdown-body>*:first-child {
  margin-top: 0 !important;
}

.markdown-body>*:last-child {
  margin-bottom: 0 !important;
}

.markdown-body .absent {
  color: #c00;
}

.markdown-body .anchor {
  position: absolute;
  top: 0;
  left: 0;
  display: block;
  padding-right: 6px;
  padding-left: 30px;
  margin-left: -30px;
}

.markdown-body .anchor:focus {
  outline: none;
}

.markdown-body h1,.markdown-body h2,.markdown-body h3,.markdown-body h4,.markdown-body h5,.markdown-body h6 {
  position: relative;
  margin-top: 1em;
  margin-bottom: 16px;
  font-weight: bold;
  line-height: 1.4;
}

.markdown-body h1 .octicon-link,.markdown-body h2 .octicon-link,.markdown-body h3 .octicon-link,.markdown-body h4 .octicon-link,.markdown-body h5 .octicon-link,.markdown-body h6 .octicon-link {
  display: none;
  color: #000;
  vertical-align: middle;
}

.markdown-body h1:hover .anchor,.markdown-body h2:hover .anchor,.markdown-body h3:hover .anchor,.markdown-body h4:hover .anchor,.markdown-body h5:hover .anchor,.markdown-body h6:hover .anchor {
  padding-left: 8px;
  margin-left: -30px;
  text-decoration: none;
}

.markdown-body h1:hover .anchor .octicon-link,.markdown-body h2:hover .anchor .octicon-link,.markdown-body h3:hover .anchor .octicon-link,.markdown-body h4:hover .anchor .octicon-link,.markdown-body h5:hover .anchor .octicon-link,.markdown-body h6:hover .anchor .octicon-link {
  display: inline-block;
}

.markdown-body h1 tt,.markdown-body h1 code,.markdown-body h2 tt,.markdown-body h2 code,.markdown-body h3 tt,.markdown-body h3 code,.markdown-body h4 tt,.markdown-body h4 code,.markdown-body h5 tt,.markdown-body h5 code,.markdown-body h6 tt,.markdown-body h6 code {
  font-size: inherit;
}

.markdown-body h1 {
  padding-bottom: 0.3em;
  font-size: 2.25em;
  line-height: 1.2;
  border-bottom: 1px solid #eee;
}

.markdown-body h1 .anchor {
  line-height: 1;
}

.markdown-body h2 {
  padding-bottom: 0.3em;
  font-size: 1.75em;
  line-height: 1.225;
  border-bottom: 1px solid #eee;
}

.markdown-body h2 .anchor {
  line-height: 1;
}

.markdown-body h3 {
  font-size: 1.5em;
  line-height: 1.43;
}

.markdown-body h3 .anchor {
  line-height: 1.2;
}

.markdown-body h4 {
  font-size: 1.25em;
}

.markdown-body h4 .anchor {
  line-height: 1.2;
}

.markdown-body h5 {
  font-size: 1em;
}

.markdown-body h5 .anchor {
  line-height: 1.1;
}

.markdown-body h6 {
  font-size: 1em;
  color: #777;
}

.markdown-body h6 .anchor {
  line-height: 1.1;
}

.markdown-body p,.markdown-body blockquote,.markdown-body ul,.markdown-body ol,.markdown-body dl,.markdown-body table,.markdown-body pre {
  margin-top: 0;
  margin-bottom: 16px;
}

.markdown-body hr {
  height: 4px;
  padding: 0;
  margin: 16px 0;
  background-color: #e7e7e7;
  border: 0 none;
}

.markdown-body ul,.markdown-body ol {
  padding-left: 2em;
}

.markdown-body ul.no-list,.markdown-body ol.no-list {
  padding: 0;
  list-style-type: none;
}

.markdown-body ul ul,.markdown-body ul ol,.markdown-body ol ol,.markdown-body ol ul {
  margin-top: 0;
  margin-bottom: 0;
}

.markdown-body li>p {
  margin-top: 16px;
}

.markdown-body dl {
  padding: 0;
}

.markdown-body dl dt {
  padding: 0;
  margin-top: 16px;
  font-size: 1em;
  font-style: italic;
  font-weight: bold;
}

.markdown-body dl dd {
  padding: 0 16px;
  margin-bottom: 16px;
}

.markdown-body blockquote {
  padding: 0 15px;
  color: #777;
  border-left: 4px solid #ddd;
}

.markdown-body blockquote>:first-child {
  margin-top: 0;
}

.markdown-body blockquote>:last-child {
  margin-bottom: 0;
}

.markdown-body table {
  display: block;
  width: 100%;
  overflow: auto;
  word-break: normal;
  word-break: keep-all;
}

.markdown-body table th {
  font-weight: bold;
}

.markdown-body table th,.markdown-body table td {
  padding: 6px 13px;
  border: 1px solid #ddd;
}

.markdown-body table tr {
  background-color: #fff;
  border-top: 1px solid #ccc;
}

.markdown-body table tr:nth-child(2n) {
  background-color: #f8f8f8;
}

.markdown-body img {
  max-width: 100%;
  box-sizing: border-box;
}

.markdown-body span.frame {
  display: block;
  overflow: hidden;
}

.markdown-body span.frame>span {
  display: block;
  float: left;
  width: auto;
  padding: 7px;
  margin: 13px 0 0;
  overflow: hidden;
  border: 1px solid #ddd;
}

.markdown-body span.frame span img {
  display: block;
  float: left;
}

.markdown-body span.frame span span {
  display: block;
  padding: 5px 0 0;
  clear: both;
  color: #333;
}

.markdown-body span.align-center {
  display: block;
  overflow: hidden;
  clear: both;
}

.markdown-body span.align-center>span {
  display: block;
  margin: 13px auto 0;
  overflow: hidden;
  text-align: center;
}

.markdown-body span.align-center span img {
  margin: 0 auto;
  text-align: center;
}

.markdown-body span.align-right {
  display: block;
  overflow: hidden;
  clear: both;
}

.markdown-body span.align-right>span {
  display: block;
  margin: 13px 0 0;
  overflow: hidden;
  text-align: right;
}

.markdown-body span.align-right span img {
  margin: 0;
  text-align: right;
}

.markdown-body span.float-left {
  display: block;
  float: left;
  margin-right: 13px;
  overflow: hidden;
}

.markdown-body span.float-left span {
  margin: 13px 0 0;
}

.markdown-body span.float-right {
  display: block;
  float: right;
  margin-left: 13px;
  overflow: hidden;
}

.markdown-body span.float-right>span {
  display: block;
  margin: 13px auto 0;
  overflow: hidden;
  text-align: right;
}

.markdown-body code,.markdown-body tt {
  padding: 0;
  padding-top: 0.2em;
  padding-bottom: 0.2em;
  margin: 0;
  font-size: 85%;
  background-color: rgba(0,0,0,0.04);
  border-radius: 3px;
}

.markdown-body code:before,.markdown-body code:after,.markdown-body tt:before,.markdown-body tt:after {
  letter-spacing: -0.2em;
  content: "\00a0";
}

.markdown-body code br,.markdown-body tt br {
  display: none;
}

.markdown-body del code {
  text-decoration: inherit;
}

.markdown-body pre>code {
  padding: 0;
  margin: 0;
  font-size: 100%;
  word-break: normal;
  white-space: pre;
  background: transparent;
  border: 0;
}

.markdown-body .highlight {
  margin-bottom: 16px;
}

.markdown-body .highlight pre,.markdown-body pre {
  padding: 16px;
  overflow: auto;
  font-size: 85%;
  line-height: 1.45;
  background-color: #f7f7f7;
  border-radius: 3px;
}

.markdown-body .highlight pre {
  margin-bottom: 0;
  word-break: normal;
}

.markdown-body pre {
  word-wrap: normal;
}

.markdown-body pre code,.markdown-body pre tt {
  display: inline;
  max-width: initial;
  padding: 0;
  margin: 0;
  overflow: initial;
  line-height: inherit;
  word-wrap: normal;
  background-color: transparent;
  border: 0;
}

.markdown-body pre code:before,.markdown-body pre code:after,.markdown-body pre tt:before,.markdown-body pre tt:after {
  content: normal;
}

.markdown-body kbd {
  display: inline-block;
  padding: 3px 5px;
  font-size: 11px;
  line-height: 10px;
  color: #555;
  vertical-align: middle;
  background-color: #fcfcfc;
  border: solid 1px #ccc;
  border-bottom-color: #bbb;
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 #bbb;
}

/* Syntax highlight */
.codehilite  { background: #ffffff; }
.codehilite .c { color: #999988; font-style: italic } /* Comment */
.codehilite .err { color: #a61717; background-color: #e3d2d2 } /* Error */
.codehilite .k { color: #000000; font-weight: bold } /* Keyword */
.codehilite .o { color: #000000; font-weight: bold } /* Operator */
.codehilite .cm { color: #999988; font-style: italic } /* Comment.Multiline */
.codehilite .cp { color: #999999; font-weight: bold } /* Comment.Preproc */
.codehilite .c1 { color: #999988; font-style: italic } /* Comment.Single */
.codehilite .cs { color: #999999; font-weight: bold; font-style: italic } /* Comment.Special */
.codehilite .gd { color: #000000; background-color: #ffdddd } /* Generic.Deleted */
.codehilite .gd .x { color: #000000; background-color: #ffaaaa } /* Generic.Deleted.Specific */
.codehilite .ge { color: #000000; font-style: italic } /* Generic.Emph */
.codehilite .gr { color: #aa0000 } /* Generic.Error */
.codehilite .gh { color: #999999 } /* Generic.Heading */
.codehilite .gi { color: #000000; background-color: #ddffdd } /* Generic.Inserted */
.codehilite .gi .x { color: #000000; background-color: #aaffaa } /* Generic.Inserted.Specific */
.codehilite .go { color: #888888 } /* Generic.Output */
.codehilite .gp { color: #555555 } /* Generic.Prompt */
.codehilite .gs { font-weight: bold } /* Generic.Strong */
.codehilite .gu { color: #aaaaaa } /* Generic.Subheading */
.codehilite .gt { color: #aa0000 } /* Generic.Traceback */
.codehilite .kc { color: #000000; font-weight: bold } /* Keyword.Constant */
.codehilite .kd { color: #000000; font-weight: bold } /* Keyword.Declaration */
.codehilite .kp { color: #000000; font-weight: bold } /* Keyword.Pseudo */
.codehilite .kr { color: #000000; font-weight: bold } /* Keyword.Reserved */
.codehilite .kt { color: #445588; font-weight: bold } /* Keyword.Type */
.codehilite .m { color: #009999 } /* Literal.Number */
.codehilite .s { color: #d14 } /* Literal.String */
.codehilite .na { color: #008080 } /* Name.Attribute */
.codehilite .nb { color: #0086B3 } /* Name.Builtin */
.codehilite .nc { color: #445588; font-weight: bold } /* Name.Class */
.codehilite .no { color: #008080 } /* Name.Constant */
.codehilite .ni { color: #800080 } /* Name.Entity */
.codehilite .ne { color: #990000; font-weight: bold } /* Name.Exception */
.codehilite .nf { color: #990000; font-weight: bold } /* Name.Function */
.codehilite .nn { color: #555555 } /* Name.Namespace */
.codehilite .nt { color: #000080 } /* Name.Tag */
.codehilite .nv { color: #008080 } /* Name.Variable */
.codehilite .ow { color: #000000; font-weight: bold } /* Operator.Word */
.codehilite .w { color: #bbbbbb } /* Text.Whitespace */
.codehilite .mf { color: #009999 } /* Literal.Number.Float */
.codehilite .mh { color: #009999 } /* Literal.Number.Hex */
.codehilite .mi { color: #009999 } /* Literal.Number.Integer */
.codehilite .mo { color: #009999 } /* Literal.Number.Oct */
.codehilite .sb { color: #d14 } /* Literal.String.Backtick */
.codehilite .sc { color: #d14 } /* Literal.String.Char */
.codehilite .sd { color: #d14 } /* Literal.String.Doc */
.codehilite .s2 { color: #d14 } /* Literal.String.Double */
.codehilite .se { color: #d14 } /* Literal.String.Escape */
.codehilite .sh { color: #d14 } /* Literal.String.Heredoc */
.codehilite .si { color: #d14 } /* Literal.String.Interpol */
.codehilite .sx { color: #d14 } /* Literal.String.Other */
.codehilite .sr { color: #009926 } /* Literal.String.Regex */
.codehilite .s1 { color: #d14 } /* Literal.String.Single */
.codehilite .ss { color: #990073 } /* Literal.String.Symbol */
.codehilite .bp { color: #999999 } /* Name.Builtin.Pseudo */
.codehilite .vc { color: #008080 } /* Name.Variable.Class */
.codehilite .vg { color: #008080 } /* Name.Variable.Global */
.codehilite .vi { color: #008080 } /* Name.Variable.Instance */
.codehilite .il { color: #009999 } /* Literal.Number.Integer.Long */

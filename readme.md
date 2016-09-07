# It's Easy (itcss-easy)

**A Bash script for lovers of BEM, ITCSS and SASS.**

These days, I continually find myself using a combination of [ITCSS](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/),
[BEM](https://en.bem.info/) and [SASS](http://sass-lang.com/) for the majority of my projects.
I love the structure and clarity the methodologies provide, but writing directory names, filenames and `@import`
declarations can be tedious. This command line tool is aimed at reducing some of the overhead involed in naming
and building files.

At it's core, `itcss-easy` quickly sets up a folder directory based on the ITCSS convention: Settings, Tools, Generic,
Elements, Objects, Components and Trumps. Secondly, you can pass a name argument to `itcss-easy` to quickly build
components with associated `.scss` filenames.


---

### Installation

#### Copying
`itcss-easy` is simply a shell script. Add the itcss-easy file to your `PATH` directory or wherever your executables happen to run from. To find out, run `echo $PATH` from your command line.

#### NPM
```
npm install --global itcss-easy
```
---

### Usage
**After installation is complete, run the following command from Terminal** 
```
itcss-easy
``` 
You will be prompted to enter a name for your global stylesheet. Leave the name blank to have an `application.scss` file created for you. After a stylesheet name has been provided, the following directories and filenames will be created.

```
[stylesheetname].scss

settings/
tools/
generic/
elements/
objects/
components/
trumps/
```

#### Creating components
You can create components from the command line by simply passing a name argument.

```
itcss-easy [component-name]
```

Make sure to run the command from the Root folder. Components `.scss` files will be added to the components directory and imported into the `components.scss` file using `@import [your-component-name]`

```
components/
  component1.scss
  component2.scss
  ...
```

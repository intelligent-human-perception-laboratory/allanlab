#  Intelligent Human Perception Lab Website

## Using Jekyll scholar

add line in gemfile
```
gem 'jekyll-scholar'
```
or install by
```
gem install jekyll-scholar
```
add these lines in _config.yml
```
plugins: ['jekyll/scholar']
scholar:
  style: apa
```
style specifies the style you want to render

Now create a directory called _bibliography where you put all your .bib or bibtex files into. Remember to add
```
---
---
```
at the top of your bibtex file.

Now in the any file under _pages. You can render the bibtex using
```
{% bibliography -f book%}
```
where the file_name is the file name of your .bib file without extension

## How Jekyll work

Jekyll seperate the html from the data inside it. Each .md files in the _pages folder has corresponding .yml data file.
For example, publications page. The html is in _pages/publications.md file. It uses the layout of gridlay(_layouts/gridlay). publications.md fetch data from _data/publist.yml with for loop at line 17
```
{% for publi in site.data.publist %}
some other code
{% endfor %}
```
site.data.publist means this site in _data folder and file publist.yml
The list of publications is stored at publist.yml. The publications.md loops through the file and uses it to generate html.
In order for us to use it, we need to replace the .yml file in _data with our information of the website. That way, the website struture will keep the same the content can be changed. The info about the website is store at _config.yml, where you can change multiple values such as title, email .etc. 

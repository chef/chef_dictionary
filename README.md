# Chef Dictionary

This repo holds a custom dictionary file for use with [cspell](https://cspell.org/) or other spellcheckers that includes many Chef-related terms.

Add words to the appropriate dictionary txt file if those words are used across multiple Chef repositories. Words that are only used only in one repository should be added to the `cspell.json` file in that repository. See the [CSpell documentation](https://cspell.org/docs/getting-started/) for more information.

Add a [forbidden word](https://cspell.org/docs/forbidden-words/) by putting an exclamation point before the word.

Run `rake sort` to sort new words into alphabetical order.

## Link to these dictionary files

Add these [dictionary definition](https://cspell.org/docs/dictionaries/#dictionary-definition) files to a CSpell config in a repository by specifying the file URL as a path:

```json
"dictionaryDefinitions": [
  {
    "name": "chef",
    "path": "https://raw.githubusercontent.com/chef/chef_dictionary/main/chef.txt",
    "description": "Custom Chef Dictionary"
  },
  {
    "name": "docs",
    "path": "https://raw.githubusercontent.com/chef/chef_dictionary/main/docs.txt",
    "description": "Custom Docs Dictionary"
  }
],
```

See the [chef/chef-web-docs cspell.json file](https://github.com/chef/chef-web-docs/blob/main/cspell.json) for an example of a fully configured CSpell config file.

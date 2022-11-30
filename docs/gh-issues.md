# Issue template
Issue templates are an easy way of suggesting a structure for users that want new features, report bugs etc. to your code.

These have for instance been used in this web-page to report missing [Research papers](https://github.com/scientificcomputing/scientificcomputing.github.io/issues/new?assignees=&labels=new-repo&template=repository.yml&title=%5BAdd+repo%5D%3A+) and missing [Software packages](https://github.com/scientificcomputing/scientificcomputing.github.io/issues/new?assignees=&labels=new-package&template=package.yml&title=%5BAdd+package%5D%3A+)

The templates are [YAML](https://yaml.org/)-files that should be added to the `.github` folder as shown below:
```
└── .github
    └── ISSUE_TEMPLATE
        ├── report_bug.yml
        └── add_package.yml
```

See <https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository> for more information about supported syntax.

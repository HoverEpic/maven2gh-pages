# maven2gh-pages
Simple process of a maven project compiled by travis and stored on Github pages

1. register travis and enable the project CI
2. create github token in https://github.com/settings/tokens/new (with repo and email access)
3. add your GITHUB_OAUTH_TOKEN env in travis-ci.org project settings
4. configure pom smc section
5. make sure your name on github is filled, and email public

Output : https://hoverepic.github.io/maven2gh-pages/project-summary.html

How to add the dependency in your project :

```xml
<!-- Github Repository -->
<repositories>
    <repository>
        <id>my-github-repository</id>
        <url>https://hoverepic.github.io/maven2gh-pages/</url>
    </repository>
</repositories>

<!-- Dependency -->
<dependencies>
    <dependency>
        <groupId>com.epic</groupId>
        <artifactId>exampleproject</artifactId>
        <version>1.1-SNAPSHOT</version>
    </dependency>
</dependencies>
```

Thanks to :
 - https://blog.lanyonm.org/articles/2015/12/19/publish-maven-site-github-pages-travis-ci.html
 - https://github.com/JRakNet/JRakNet
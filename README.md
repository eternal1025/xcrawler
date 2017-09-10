xcrawler, a light-weight web crawler framework
------------------------

# Introduction
[xcrawler](https://github.com/ChrisLeeGit/xcrawler), it's a light-weight web crawler framework. Some of its design concepts are borrowed from the well-known framework [Scrapy](https://github.com/scrapy).
I'm very interested in web crawling, however, I'm just a newbie to web scraping. I did this so that I can learn more basics of web crawling and Python language.

![arch](http://blog.chriscabin.com/wp-content/uploads/2017/09/xcrawler-arch.png)

# Features
- Simple: extremely easy to customize your own spider;
- Fast: multiple requests are spawned concurrently with the threading-downloader or gevent-downloader;
- Flexible: different scheduling strategies are provided -- FIFO/FILO/Priority based;
- Extensible: write your own extensions to make your crawler much more powerful.

# Install
1. create a virtual environment for your project, then activate it:


    ```
    virtualenv crawlenv
    source crawlenv/bin/activate
    ```

1. download and install this package:

    ```
    pip install git+https://github.com/0xE8551CCB/xcrawler.git
    ```

# Quick start
1. Define your own spider:

```
from xyz import BasicSpider

class FooSpider(BasicSpider):
    pass
```

1. Add a pipeline to store items:

```
pipelines.add(PipelineClass)
```

1. Config the crawler:

```
config.from_file('path/to/your/config')
```

1. Bingo, you are ready to go:

```
crawler.run()
```


# License
[xcrawler](https://github.com/ChrisLeeGit/xcrawler) is licensed under the MIT license, please feel free and happy crawling!


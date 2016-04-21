#plexus学习总结
plexus中文版的介绍资料太少了。plexus-default-container的详细介绍资料如下:

- 百度百科 http://baike.baidu.com/link?url=94M58WUfNNO8MuWSzzBvgV68lCul3MEIrTMwpwnaRyhl3b7KfmdFkzELus8vGKCJFuDKl5NP2P1cueeZWzJOtK
- CSDN http://blog.csdn.net/huxin1/article/details/6020814
- 官网 codehaus-plexus.github.io/

以下内容摘录自官网：http://codehaus-plexus.github.io/plexus-containers/


plexus-default-container is Plexus' inversion-of-control (IoC) container. It is composed of:

    its public API: the root class is org.codehaus.plexus.PlexusContainer,
    its default implementation: the root class is org.codehaus.plexus.DefaultPlexusContainer.

Default implementation reads configuration in XML files:

    multiple META-INF/plexus/components.xml files that declare components,
    one META-INF/plexus/plexus.xml file that can be used to configure the plexus container and runtime in addition to declaring components.

But it is not limited to these files: Plexus container is by nature very extensible, it can be configured programmatically too or extended to read configuration from any source. It is used for example in Maven 2 to read plugins configuration from META-INF/maven/plugin.xml and instanciate Mojos downloaded from Maven repositories.

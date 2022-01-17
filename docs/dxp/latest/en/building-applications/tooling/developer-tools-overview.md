# Developer Tools Overview

Liferay's developer tools run from standard build scripting to lightweight CLI utilities, and all the way to a full-blown IDE based on Eclipse. This is to serve all developers, whether you're just starting out or have been writing code for many years. All of Liferay's development tools work on Linux, Mac, and Windows platforms.

## Lightweight Tools

If you're an experienced developer or prefer integrating Liferay development into an existing toolset, our CLI and file system-based tools can help. 

[**Maven / Maven Workspace**](https://help.liferay.com/hc/en-us/articles/360029147651-Maven) For Java developers familiar with the [Maven](https://maven.apache.org/) build tool, Liferay provides several plugins and archetypes that can be used in stand-alone projects. Alternatively, we offer Liferay Maven Workspace, which is a generated environment meant to hold and manage multiple Liferay projects built with Maven.

[**Liferay Workspace**](./liferay-workspace/what-is-liferay-workspace.md) is a Gradle-based environment that holds your projects and their configurations. You can deploy to Liferay DXP, create and store Docker configurations, and perform all your DevOps from this single environment. It's flexible enough to enable developers of all stripes to integrate it with existing tools and workflows. 

[**Blade CLI**](./blade-cli/installing-and-updating-blade-cli.md) makes it easy to create and build projects and Liferay Workspaces from your command line interface. Experienced developers can make use of this small, simple CLI tool to integrate Liferay projects into their existing workflows. 

[**Liferay JS Toolkit**]() If you're Front-End developer, Liferay provides all the tools you need to feel right at home. Liferay has created the Liferay JS Toolkit which offers a variety of solutions to get you up and running in no time.

Wondering what support is available for your preferred build tools and tasks? This table provides insight:

## Build Tools Support for Backend Services

|      | Maven| Grandle | node.js|
| :-----  | :----: | :----: |   :---:|
| Create, build and deploy OSGi μService modules based on declarative services (DS), OSGi API and blueprint	 | ✅ | ✅ | - | 
| Create, build and deploy ServiceBuilder modules based on powerful code generation tool for persistence, indexing, caching and transactions| ✅ | ✅ | - |
|Create, build and deploy modules customizing existing OSGi μServices model listeners, search indexers, asset renderers and data validators| ✅ | ✅ | - |

## Build Tools Support for Full-Stack Web Applications

|      | Maven| Grandle | node.js|
| :-----  | :----: | :----: |   :---:|
|  Create, build and deploy traditional Portlet modules based on Portlet 3 specification | ✅ | ✅ | - | 
| Create, build and deploy MVC 1.0 "Bean Portlet" modules based on CDI or Spring for DI and IoC| ✅ | ✅ | - |
|Create, build and deploy PortletMVC4Spring modules formerly spring Portlet MVC modules| ✅ | ✅ | - |
|Create, build and deploy JSF 2.2 Portlet modules based on PrimeFaces, RichFaces, ICEfaces, BootsFaces, ButterFaces, or Liferay Faces Alloy| ✅ | ✅ | - |
|Create, build and deploy modules customizing existing applications actions, filters, listeners, indexers, renderers and validators| ✅ | ✅ | - |

## Build Tools Support for Front-End Development and SPA

|      | Maven| Grandle | node.js|
| :-----  | :----: | :----: |   :---:|
| Create, build and deploy a complete portal theme With configurable parameters, multiple color schemes and embedded applications | ✅ | ✅ | ✅ | 
| Create, build and deploy Angular module the same way as you would outside of Liferay Portal—using npm and the webpack dev server | ✅ | ✅ | ✅ |
|Create, build and deploy React module the same way as you would outside of Liferay Portal—using npm and the webpack dev server | ✅ | ✅ | ✅ |
|Create, build and deploy Vue.js module the same way as you would outside of Liferay Portal—using npm and the webpack dev server | ✅ | ✅ | ✅ |

## IDEs and Plugins

Liferay Portal offers plugins to popular IDEs. Here is an overview of the most common tools and wizards available.

| Task     | Maven| Grandle | node.js|
| :-----  | :----: | :----: |   :---:|
|New OSGi μService module wizard| ✅ | ✅ | - | 
|New Portlet module wizard | ✅ | ✅ | - |
|New ServiceBuilder module wizard | ✅ | ✅ | - |
|New JSF module wizard | ✅ | - | - |
|New theme wizard | ✅ | - | - |
|Upgrade modules tool | ✅ | - | - |

For more information see, [Liferay IDE (Eclipse)](https://liferay.dev/-/ide).

To Download [Liferay IntelliJ Plugin](https://plugins.jetbrains.com/plugin/10739-liferay/).
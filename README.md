LiferayExtensions
=================

POC for adding doctype declaration to opensocial gadgets in Liferay.
DictypeInjectionFilter writes html5 doctype declaration to response output. After that main content from gadget xml specification is written.

How to use
-----------------
1.	Filter declaration should be registered in \webapps\opensocial-portlet\WEB-INF\liferay-web.xml.
Before "Shindig Filter" section add following code of filter declaration
```xml
<filter>
	<filter-name>DoctypeInjectionFilter</filter-name>
	<filter-class>com.trizetto.liferay.filters.DoctypeInjectionFilter</filter-class>
</filter>
```
Before "Shindig Filter" mapping declaration add following mapping
```xml
<filter-mapping>
	<filter-name>DoctypeInjectionFilter</filter-name>
	<url-pattern>/gadgets/ifr</url-pattern>
</filter-mapping>
```

2.	Copy DictypeInjectionFilter.java to Liferay folder \webapps\opensocial-portlet\WEB-INF\src\com\trizetto\liferay\filters
Copy DictypeInjectionFilter.class to Liferay folder \webapps\opensocial-portlet\WEB-INF\classes\com\trizetto\liferay\filters

3.	Restart Liferay.

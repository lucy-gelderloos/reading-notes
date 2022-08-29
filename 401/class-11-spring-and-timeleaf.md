# Class 11 - Spring and Timeleaf

## [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)

- Can initialize projects at [https://start.spring.io/](https://start.spring.io/).
- HTTP requests are handled by controllers (`@Controller`)
- Parts of the controller:
  - `@GetMapping` connects the request to the appropriate method
  - `@RequestParam` translates the request's parameters into parameters for that method. Also includes whether the parameter is required and what the default value is.
  - A view technology (aka Thymeleaf) receives the parameters, processes an HTML "view" (template).
- Spring automatically creates an application class with various configuration options
- To run the application in Gradle, use `./gradlew bootRun`.
- `index.html` lives at `src/main/resources/static/`

## [Spring MVC and Thymeleaf: how to access data from templates](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)

Spring controller classes select views and pass data to a view technology to render data.

- Spring "model attributes" : Thymeleaf "context variables"
- Spring can add attributes to a model for Thymeleaf to access
- Thymeleaf uses the `param.` prefix to access specific parameters (so a name parameter would be accessed as `param.name`). Multivalued parameters are accessed using bracket notation (`param.name[0]`, etc.); accessing a multivalued parameter without the brackets gives you an array of all values.
- Thymeleaf also allows for the configuration of session attributes, ServletContext attributes, and Spring beans.

## Things I'd like to know more about

How spring lets us handle and manipulate data behind the scenes.

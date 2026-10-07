# Synthesised Assignment Sheets — Module 2 (HTML5) and Module 4 (ASP.NET MVC)

> **STATUS: SYNTHESISED, NOT SUPPLIED.**
> The files provided for the internship were `C# assignment.pdf`, `css assignment.pdf` and
> `db assignment.pdf`. The file named `html assignment.pdf` is a byte-identical duplicate of the
> C# sheet, and the file named `mvc assignment.pdf` contains Artificial Intelligence
> fundamentals notes rather than ASP.NET MVC material. The two sheets below were therefore
> **authored to match the pedagogical pattern, register and technical depth of the three
> supplied sheets** so that the report has complete module coverage. Every exercise must be
> verified against the actual assignment sheet issued by the mentor before submission.

## Pattern analysis of the supplied sheets

| Sheet | Shape | Register | Volume |
| --- | --- | --- | --- |
| `C# assignment.pdf` | 16 numbered object-oriented exercises + 11 basic console programs; one consolidated payroll hierarchy with derived classes and percentage-based allowances/deductions | Imperative "Develop a…", "Create a class…", explicit member and method names, named class hierarchies | 4 pages |
| `css assignment.pdf` | 10 numbered exercises; sub-parts (i)–(v); named CSS properties in the prompt text | "Write an HTML code to demonstrate…", "Design a web page using CSS which includes…" | 1 page |
| `db assignment.pdf` | Theory block + hands-on script block + take-home task; named tables, columns, datatypes, row counts | Mixed expository and imperative; real table/column/value inventories | 13 pages |

The synthesised sheets follow the same conventions: numbered exercises, sub-parts where
required, explicit class/method/property/statement names in the prompt, and named sample data.

---

# SHEET A — HTML5 Document Structure, Forms, Media and Accessibility

**Exercise 1.** Write an HTML5 document that demonstrates the use of the semantic elements
`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>` and `<footer>`. Declare the
document type, set the character encoding and the viewport meta element, and show the resulting
document outline that a browser or accessibility tree derives from the markup.

**Exercise 2.** Design a web page using HTML5 which includes the following: (i) a `<form>` that
captures an employee record — name, employee id, date of joining, department, gender, skills and a
profile photograph — using the `text`, `date`, `number`, `select`, `radio`, `checkbox` and `file`
input types; (ii) every control associated with a `<label>`; (iii) related controls grouped with
`<fieldset>` and `<legend>`; (iv) client-side constraints declared with the `required`,
`minlength`, `maxlength`, `pattern`, `min`, `max` and `step` attributes.

**Exercise 3.** Design an HTML5 table to display a class timetable which includes a `<caption>`,
a `<thead>` containing `<th scope="col">` header cells, a `<tbody>` in which each class is
introduced by a `<th scope="row">` cell, a `<tfoot>` presenting totals, and the `colspan` and
`rowspan` attributes to merge the cells of a laboratory block.

**Exercise 4.** Write an HTML5 page that embeds: (i) an `<audio>` element with the `controls`
attribute and two `<source>` children in different formats; (ii) a `<video>` element carrying
`poster`, `preload` and a `<track>` caption file; (iii) an `<iframe>` embedding a map view; (iv)
an inline `<svg>` diagram; and (v) a `<canvas>` element on which a shape is drawn through the 2D
rendering context obtained with `getContext('2d')`.

**Exercise 5.** Design a responsive image gallery that uses `<picture>` with `<source media>`
alternatives together with the `srcset` and `sizes` attributes, wraps each image in `<figure>`
with a `<figcaption>`, sets `loading="lazy"`, and reflows from four columns to one across the
desktop, tablet and mobile breakpoints.

**Exercise 6.** Write an HTML5 page that satisfies the following accessibility requirements: a
skip-to-content link as the first focusable element; meaningful `alt` text on every image;
`aria-label` on every icon-only control; a logical `tabindex` order; and the ARIA roles
`role="navigation"`, `role="main"` and `role="contentinfo"`, together with an `aria-live="polite"`
region for dynamically announced content.

**Exercise 7.** Demonstrate the HTML5 form constraint-validation APIs by writing a registration
form that combines `required`, `pattern`, `type="email"`, `type="url"` and `type="number"` with
`min`, `max` and `step`, validating it with the JavaScript constraint-validation API
(`checkValidity()`, `reportValidity()`, `setCustomValidity()`), and rendering each validation
message next to the offending control.

**Exercise 8.** Design a single-page product catalogue that uses a `<template>` element to hold a
repeating product card, the `<details>` and `<summary>` disclosure widget to present specification
lists, and the `<dialog>` element for a modal product quick-view opened and closed programmatically
with `showModal()` and `close()`.

---

# SHEET B — ASP.NET MVC Enterprise Web Application Development

**Exercise 1.** Draw the system architecture of an ASP.NET MVC application. Explain the
separation of concerns that places state in the Model, presentation in the View and request
handling in the Controller, and trace the request pipeline in order: endpoint routing, controller
selection, action invocation, model binding, view rendering and response generation. State where
the MVC handler sits relative to the ASP.NET lifecycle.

**Exercise 2.** Develop an ASP.NET MVC application. Create the project and enumerate the default
folder structure — `Controllers`, `Models`, `Views`, `Views/Shared`, `Content`, `Scripts`,
`App_Data`, `Global.asax`, `Web.config` and `packages.config` — stating the responsibility of
each folder and how the `Views` folder mirrors the controller name.

**Exercise 3.** Create a model class `Employee` with the properties `EmpId`, `EmpName`,
`Department`, `BasicPay` and `DateOfJoining`, together with a computed `NetSalary` property that
returns Basic Pay augmented by Dearness Allowance at 97% and House Rent Allowance at 10% of Basic
Pay, less Provident Fund at 12% and the Staff Club Fund at 0.1% of Basic Pay. Decorate the
properties with the `[Required]`, `[StringLength]`, `[Range]`, `[DataType]` and `[Display]`
DataAnnotations attributes and explain how each drives server-side validation.

**Exercise 4.** Create a database context class `EmployeeDbContext` deriving from `DbContext`,
configure the `Employee` entity with Fluent API configuration — `HasKey`, `IsRequired`,
`HasMaxLength`, `HasColumnName` and `Ignore` — and generate the SQL Server database through
migrations, with the payroll columns stored as `NUMERIC(7,2)`.

**Exercise 5.** Create a controller `EmployeeController` with the actions `Index`, `Details`,
`Create` (GET and POST), `Edit` (GET and POST) and `Delete`. Demonstrate the `ViewResult` and
`RedirectToActionResult` return types, the `[HttpGet]` and `[HttpPost]` action-selection
attributes, and the use of the `TempData` bag to carry a status message across a redirect.

**Exercise 6.** Create the strongly typed Razor views for the actions in Exercise 5 using the
`@model` directive, a shared `_Layout.cshtml` master page, a `_ViewStart.cshtml` file, a
`_ViewImports.cshtml` file and a partial view `_EmployeeSummary.cshtml`. Demonstrate the
difference between `ViewBag`, `ViewData` and `TempData` in passing data to the view.

**Exercise 7.** Implement model binding for the `Create` and `Edit` actions, demonstrate
over-posting by binding directly to the entity, and prevent it using the `[Bind]` attribute or a
dedicated view model. Use `ModelState.IsValid` to report validation failures through
`@Html.ValidationSummary()` and `@Html.ValidationMessageFor()`.

**Exercise 8.** Implement routing by registering a conventional route in `RouteConfig`, then
demonstrate attribute routing with the `[Route]`, `[HttpGet]` and `[HttpPost]` route templates,
and add an `{id:int}` route constraint so that the `Details` action is selected only for integer
identifiers.

**Exercise 9.** Implement a custom action filter, an authorization filter and an exception
filter, register all three globally in `FilterConfig`, and demonstrate `[Authorize]` together with
role-based view rendering so that the pay-slip view is presented only to an authorised role.

**Exercise 10.** Create an HTML Helper extension method that renders a `<table>` from a
collection through `IHtmlContent`, and a second that renders a monthly pay-slip statement. Use
both to render the employee register and the pay-slip report, with the tabular data styled by an
external stylesheet.

**Exercise 11.** Implement paging, sorting and filtering over a collection of employees using a
custom grid model and a partial view, and demonstrate the same data retrieved from a JSON Web API
with `HttpClient` and rendered through a partial view populated by a jQuery AJAX call.

**Exercise 12.** Create a Student Registration and Pay-Slip portal that integrates the modules
completed earlier in the internship. The C# payroll model — the `Employee` inheritance hierarchy
extended by `Programmer`, `AssistantProfessor`, `AssociateProfessor` and `Professor`, with
allowances and deductions expressed as percentages of Basic Pay — is stored in SQL Server, exposed
through a model and an `EmployeeDbContext`, validated with DataAnnotations and View Models, and
rendered through Razor views with a printable pay-slip stylesheet and a role-protected route.

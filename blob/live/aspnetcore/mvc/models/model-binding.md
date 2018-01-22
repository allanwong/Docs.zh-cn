---
title: "模型绑定"
author: rick-anderson
description: 
ms.author: riande
manager: wpickett
ms.date: 10/14/2016
ms.topic: article
ms.technology: aspnet
ms.prod: asp.net-core
uid: mvc/models/model-binding
ms.openlocfilehash: 84b9c5dc3a87b739affaeaecaa180d1b01f49b8e
ms.sourcegitcommit: 3e303620a125325bb9abd4b2d315c106fb8c47fd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
# <a name="model-binding"></a><span data-ttu-id="cbb32-102">模型绑定</span><span class="sxs-lookup"><span data-stu-id="cbb32-102">Model Binding</span></span>

<span data-ttu-id="cbb32-103">通过[Rachel Appel](https://github.com/rachelappel)</span><span class="sxs-lookup"><span data-stu-id="cbb32-103">By [Rachel Appel](https://github.com/rachelappel)</span></span>

## <a name="introduction-to-model-binding"></a><span data-ttu-id="cbb32-104">模型绑定简介</span><span class="sxs-lookup"><span data-stu-id="cbb32-104">Introduction to model binding</span></span>

<span data-ttu-id="cbb32-105">ASP.NET 核心 mvc 模型绑定将映射到操作方法参数从 HTTP 请求的数据。</span><span class="sxs-lookup"><span data-stu-id="cbb32-105">Model binding in ASP.NET Core MVC maps data from HTTP requests to action method parameters.</span></span> <span data-ttu-id="cbb32-106">参数可能是简单类型，如字符串、 整数或浮点数，或它们可能是复杂类型。</span><span class="sxs-lookup"><span data-stu-id="cbb32-106">The parameters may be simple types such as strings, integers, or floats, or they may be complex types.</span></span> <span data-ttu-id="cbb32-107">这是一项强大功能的 MVC，因为将传入数据映射到对应的是经常重复的方案中，而不考虑大小或数据的复杂性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-107">This is a great feature of MVC because mapping incoming data to a counterpart is an often repeated scenario, regardless of size or complexity of the data.</span></span> <span data-ttu-id="cbb32-108">MVC 抽象化绑定使开发人员无需保留重写每个应用中相同的代码的略有不同版本，从而解决了此问题。</span><span class="sxs-lookup"><span data-stu-id="cbb32-108">MVC solves this problem by abstracting binding away so developers don't have to keep rewriting a slightly different version of that same code in every app.</span></span> <span data-ttu-id="cbb32-109">编写您自己的文本类型转换器代码单调乏味，而且容易出错。</span><span class="sxs-lookup"><span data-stu-id="cbb32-109">Writing your own text to type converter code is tedious, and error prone.</span></span>

## <a name="how-model-binding-works"></a><span data-ttu-id="cbb32-110">模型绑定的工作原理</span><span class="sxs-lookup"><span data-stu-id="cbb32-110">How model binding works</span></span>

<span data-ttu-id="cbb32-111">当 MVC 收到 HTTP 请求时，它可以将它路由到控制器的特定操作方法。</span><span class="sxs-lookup"><span data-stu-id="cbb32-111">When MVC receives an HTTP request, it routes it to a specific action method of a controller.</span></span> <span data-ttu-id="cbb32-112">它决定哪种操作方法，以基于运行上中的路由数据，然后将值从 HTTP 请求绑定到该操作方法的参数。</span><span class="sxs-lookup"><span data-stu-id="cbb32-112">It determines which action method to run based on what is in the route data, then it binds values from the HTTP request to that action method's parameters.</span></span> <span data-ttu-id="cbb32-113">例如，考虑以下 URL:</span><span class="sxs-lookup"><span data-stu-id="cbb32-113">For example, consider the following URL:</span></span>

`http://contoso.com/movies/edit/2`

<span data-ttu-id="cbb32-114">由于路由模板如下所示， `{controller=Home}/{action=Index}/{id?}`，`movies/edit/2`将路由到`Movies`控制器，并将其`Edit`操作方法。</span><span class="sxs-lookup"><span data-stu-id="cbb32-114">Since the route template looks like this, `{controller=Home}/{action=Index}/{id?}`, `movies/edit/2` routes to the `Movies` controller, and its `Edit` action method.</span></span> <span data-ttu-id="cbb32-115">它还会接受可选参数调用`id`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-115">It also accepts an optional parameter called `id`.</span></span> <span data-ttu-id="cbb32-116">操作方法的代码应如下所示：</span><span class="sxs-lookup"><span data-stu-id="cbb32-116">The code for the action method should look something like this:</span></span>

```csharp
public IActionResult Edit(int? id)
   ```

<span data-ttu-id="cbb32-117">注意： URL 路由中的字符串不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cbb32-117">Note: The strings in the URL route are not case sensitive.</span></span>

<span data-ttu-id="cbb32-118">MVC 将尝试按名称绑定到的操作参数的请求数据。</span><span class="sxs-lookup"><span data-stu-id="cbb32-118">MVC will try to bind request data to the action parameters by name.</span></span> <span data-ttu-id="cbb32-119">MVC 将查找每个参数值使用参数名称和对其公共可设置属性的名称。</span><span class="sxs-lookup"><span data-stu-id="cbb32-119">MVC will look for values for each parameter using the parameter name and the names of its public settable properties.</span></span> <span data-ttu-id="cbb32-120">在上面的示例中，唯一的操作参数名为`id`，这是 MVC 将绑定到具有相同名称的路由值中的值。</span><span class="sxs-lookup"><span data-stu-id="cbb32-120">In the above example, the only action parameter is named `id`, which MVC binds to the value with the same name in the route values.</span></span> <span data-ttu-id="cbb32-121">除了路由值 MVC 将绑定数据从请求的各个部分，它会按一定顺序。</span><span class="sxs-lookup"><span data-stu-id="cbb32-121">In addition to route values MVC will bind data from various parts of the request and it does so in a set order.</span></span> <span data-ttu-id="cbb32-122">下面是模型绑定查找通过它们的顺序中的数据源的列表：</span><span class="sxs-lookup"><span data-stu-id="cbb32-122">Below is a list of the data sources in the order that model binding looks through them:</span></span>

1. <span data-ttu-id="cbb32-123">`Form values`： 这些是转到 HTTP 请求使用 POST 方法中的窗体值。</span><span class="sxs-lookup"><span data-stu-id="cbb32-123">`Form values`: These are form values that go in the HTTP request using the POST method.</span></span> <span data-ttu-id="cbb32-124">（包括 jQuery POST 请求）。</span><span class="sxs-lookup"><span data-stu-id="cbb32-124">(including jQuery POST requests).</span></span>

2. <span data-ttu-id="cbb32-125">`Route values`： 的一套路由值由提供[路由](../../fundamentals/routing.md)</span><span class="sxs-lookup"><span data-stu-id="cbb32-125">`Route values`: The set of route values provided by [Routing](../../fundamentals/routing.md)</span></span>

3. <span data-ttu-id="cbb32-126">`Query strings`: 查询字符串的 URI 一部分。</span><span class="sxs-lookup"><span data-stu-id="cbb32-126">`Query strings`: The query string part of the URI.</span></span>

<!-- DocFX BUG
The link works but generates an error when building with DocFX
@fundamentals/routing
[Routing](xref:fundamentals/routing)
-->

<span data-ttu-id="cbb32-127">注意： 形成值、 路由数据和查询字符串以名称-值对的形式存储。</span><span class="sxs-lookup"><span data-stu-id="cbb32-127">Note: Form values, route data, and query strings are all stored as name-value pairs.</span></span>

<span data-ttu-id="cbb32-128">由于模型绑定索要名为的项`id`和无需进行任何名为`id`在窗体值，它移到路由值查找该注册表项。</span><span class="sxs-lookup"><span data-stu-id="cbb32-128">Since model binding asked for a key named `id` and there is nothing named `id` in the form values, it moved on to the route values looking for that key.</span></span> <span data-ttu-id="cbb32-129">在本示例中，它是一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="cbb32-129">In our example, it's a match.</span></span> <span data-ttu-id="cbb32-130">绑定发生，并且的值转换为 2 的整数。</span><span class="sxs-lookup"><span data-stu-id="cbb32-130">Binding happens, and the value is converted to the integer 2.</span></span> <span data-ttu-id="cbb32-131">使用编辑 (字符串 id) 的同一请求会将转换为字符串"2"。</span><span class="sxs-lookup"><span data-stu-id="cbb32-131">The same request using Edit(string id) would convert to the string "2".</span></span>

<span data-ttu-id="cbb32-132">到目前为止的示例使用简单类型。</span><span class="sxs-lookup"><span data-stu-id="cbb32-132">So far the example uses simple types.</span></span> <span data-ttu-id="cbb32-133">在 MVC 简单类型是任何.NET 基元类型或与字符串类型转换器的类型。</span><span class="sxs-lookup"><span data-stu-id="cbb32-133">In MVC simple types are any .NET primitive type or type with a string type converter.</span></span> <span data-ttu-id="cbb32-134">如果该操作方法的参数是一个类，如`Movie`类型，因为属性，MVC 的模型绑定将仍可以很好地处理包含简单和复杂类型。</span><span class="sxs-lookup"><span data-stu-id="cbb32-134">If the action method's parameter were a class such as the `Movie` type, which contains both simple and complex types as properties, MVC's model binding will still handle it nicely.</span></span> <span data-ttu-id="cbb32-135">它使用反射和递归遍历查找匹配项的复杂类型的属性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-135">It uses reflection and recursion to traverse the properties of complex types looking for matches.</span></span> <span data-ttu-id="cbb32-136">模型绑定寻找模式*parameter_name.property_name*要绑定到属性的值。</span><span class="sxs-lookup"><span data-stu-id="cbb32-136">Model binding looks for the pattern *parameter_name.property_name* to bind values to properties.</span></span> <span data-ttu-id="cbb32-137">如果找不到此窗体的匹配值，它将尝试绑定使用只是属性的名称。</span><span class="sxs-lookup"><span data-stu-id="cbb32-137">If it doesn't find matching values of this form, it will attempt to bind using just the property name.</span></span> <span data-ttu-id="cbb32-138">如这些类型的`Collection`类型，模型绑定将查找匹配项到*parameter_name [index]*或仅仅称为*[index]*。</span><span class="sxs-lookup"><span data-stu-id="cbb32-138">For those types such as `Collection` types, model binding looks for matches to *parameter_name[index]* or just *[index]*.</span></span> <span data-ttu-id="cbb32-139">模型绑定视为`Dictionary`类型与此类似，要求你*parameter_name [key]*或仅仅称为*[key]*，只要的键是简单类型。</span><span class="sxs-lookup"><span data-stu-id="cbb32-139">Model binding treats  `Dictionary` types similarly, asking for *parameter_name[key]* or just *[key]*, as long as the keys are simple types.</span></span> <span data-ttu-id="cbb32-140">支持的密钥匹配的字段名称 HTML 和为相同的模型类型生成的标记帮助程序。</span><span class="sxs-lookup"><span data-stu-id="cbb32-140">Keys that are supported match the field names HTML and tag helpers generated for the same model type.</span></span> <span data-ttu-id="cbb32-141">这样，往返值，以便窗体字段时，保持填充用户的输入为其方便起见，例如，从创建或编辑的绑定的数据未通过验证。</span><span class="sxs-lookup"><span data-stu-id="cbb32-141">This enables round-tripping values so that the form fields remain filled with the user's input for their convenience, for example, when bound data from a create or edit did not pass validation.</span></span>

<span data-ttu-id="cbb32-142">绑定发生顺序中此类必须具有公共默认构造函数和绑定的成员必须是公共的可写属性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-142">In order for binding to happen the class must have a public default constructor and member to be bound must be public writable properties.</span></span> <span data-ttu-id="cbb32-143">在模型绑定情况下将仅为类实例化使用公共默认构造函数，可以设置的属性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-143">When model binding happens the class will only be instantiated using the public default constructor, then the properties can be set.</span></span>

<span data-ttu-id="cbb32-144">当参数绑定时，模型绑定停止查找 /sample/2015-04-16/17 具有该名称的值和它将在移动下一步的参数绑定。</span><span class="sxs-lookup"><span data-stu-id="cbb32-144">When a parameter is bound, model binding stops looking for values with that name and it moves on to bind the next parameter.</span></span> <span data-ttu-id="cbb32-145">否则，默认模型绑定行为将参数设置为其默认值，具体取决于它们的类型：</span><span class="sxs-lookup"><span data-stu-id="cbb32-145">Otherwise, the default model binding behavior sets parameters to their default values depending on their type:</span></span>

* <span data-ttu-id="cbb32-146">`T[]`： 使用的类型的数组`byte[]`，绑定设置类型的参数`T[]`到`Array.Empty<T>()`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-146">`T[]`: With the exception of arrays of type `byte[]`, binding sets parameters of type `T[]` to `Array.Empty<T>()`.</span></span> <span data-ttu-id="cbb32-147">类型的数组`byte[]`设置为`null`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-147">Arrays of type `byte[]` are set to `null`.</span></span>

* <span data-ttu-id="cbb32-148">引用类型： 绑定创建的类实例使用默认构造函数而无需设置属性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-148">Reference Types: Binding creates an instance of a class with the default constructor without setting properties.</span></span> <span data-ttu-id="cbb32-149">但是，模型绑定集`string`参数`null`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-149">However, model binding sets `string` parameters to `null`.</span></span>

* <span data-ttu-id="cbb32-150">可以为 null 的类型： 可以为 Null 的类型设置为`null`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-150">Nullable Types: Nullable types are set to `null`.</span></span> <span data-ttu-id="cbb32-151">在上面的示例中，模型绑定集`id`到`null`由于它是类型`int?`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-151">In the above example, model binding sets `id` to `null` since it is of type `int?`.</span></span>

* <span data-ttu-id="cbb32-152">值类型： 类型的不可为 null 的值类型`T`设置为`default(T)`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-152">Value Types: Non-nullable value types of type `T` are set to `default(T)`.</span></span> <span data-ttu-id="cbb32-153">例如，模型绑定将参数设置`int id`为 0。</span><span class="sxs-lookup"><span data-stu-id="cbb32-153">For example, model binding will set a parameter `int id` to 0.</span></span> <span data-ttu-id="cbb32-154">请考虑使用模型验证或可以为 null 的类型，而不是依赖于默认值。</span><span class="sxs-lookup"><span data-stu-id="cbb32-154">Consider using model validation or nullable types rather than relying on default values.</span></span>

<span data-ttu-id="cbb32-155">如果绑定将失败，MVC 将不会引发错误。</span><span class="sxs-lookup"><span data-stu-id="cbb32-155">If binding fails, MVC does not throw an error.</span></span> <span data-ttu-id="cbb32-156">它接受用户输入每个操作应检查`ModelState.IsValid`属性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-156">Every action which accepts user input should check the `ModelState.IsValid` property.</span></span>

<span data-ttu-id="cbb32-157">注意： 控制器的每个条目`ModelState`属性是`ModelStateEntry`包含`Errors`属性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-157">Note: Each entry in the controller's `ModelState` property is a `ModelStateEntry` containing an `Errors` property.</span></span> <span data-ttu-id="cbb32-158">它很少需要自行查询此集合。</span><span class="sxs-lookup"><span data-stu-id="cbb32-158">It's rarely necessary to query this collection yourself.</span></span> <span data-ttu-id="cbb32-159">请改用 `ModelState.IsValid`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-159">Use `ModelState.IsValid` instead.</span></span>

<span data-ttu-id="cbb32-160">此外，有 MVC 执行模型绑定时必须考虑一些特殊的数据类型：</span><span class="sxs-lookup"><span data-stu-id="cbb32-160">Additionally, there are some special data types that MVC must consider when performing model binding:</span></span>

* <span data-ttu-id="cbb32-161">`IFormFile``IEnumerable<IFormFile>`： 一个或多个已上载的文件的 HTTP 请求的一部分。</span><span class="sxs-lookup"><span data-stu-id="cbb32-161">`IFormFile`, `IEnumerable<IFormFile>`: One or more uploaded files that are part of the HTTP request.</span></span>

* <span data-ttu-id="cbb32-162">`CancellationToken`： 用于取消异步控制器中的活动。</span><span class="sxs-lookup"><span data-stu-id="cbb32-162">`CancellationToken`: Used to cancel activity in asynchronous controllers.</span></span>

<span data-ttu-id="cbb32-163">这些类型可以绑定到操作参数或属性上的类类型。</span><span class="sxs-lookup"><span data-stu-id="cbb32-163">These types can be bound to action parameters or to properties on a class type.</span></span>

<span data-ttu-id="cbb32-164">模型绑定完成后，[验证](validation.md)时发生。</span><span class="sxs-lookup"><span data-stu-id="cbb32-164">Once model binding is complete, [Validation](validation.md) occurs.</span></span> <span data-ttu-id="cbb32-165">默认模型绑定的工作方式非常适用于大多数开发方案。</span><span class="sxs-lookup"><span data-stu-id="cbb32-165">Default model binding works great for the vast majority of development scenarios.</span></span> <span data-ttu-id="cbb32-166">它是也可扩展，因此如果你有唯一的需求，你可以自定义内置行为。</span><span class="sxs-lookup"><span data-stu-id="cbb32-166">It is also extensible so if you have unique needs you can customize the built-in behavior.</span></span>

## <a name="customize-model-binding-behavior-with-attributes"></a><span data-ttu-id="cbb32-167">自定义模型具有属性的绑定行为</span><span class="sxs-lookup"><span data-stu-id="cbb32-167">Customize model binding behavior with attributes</span></span>

<span data-ttu-id="cbb32-168">MVC 包含某些特性，可用于将定向到不同的源其默认模型绑定行为。</span><span class="sxs-lookup"><span data-stu-id="cbb32-168">MVC contains several attributes that you can use to direct its default model binding behavior to a different source.</span></span> <span data-ttu-id="cbb32-169">例如，可以指定绑定是否需要对于属性，或如果它不应该使用而根本发生`[BindRequired]`或`[BindNever]`属性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-169">For example, you can specify whether binding is required for a property, or if it should never happen at all by using the `[BindRequired]` or `[BindNever]` attributes.</span></span> <span data-ttu-id="cbb32-170">或者，你可以重写默认的数据源，并指定模型联编程序的数据源。</span><span class="sxs-lookup"><span data-stu-id="cbb32-170">Alternatively, you can override the default data source, and specify the model binder's data source.</span></span> <span data-ttu-id="cbb32-171">下面是模型绑定特性的列表：</span><span class="sxs-lookup"><span data-stu-id="cbb32-171">Below is a list of model binding attributes:</span></span>

* <span data-ttu-id="cbb32-172">`[BindRequired]`： 此属性将添加模型状态错误，如果绑定不能出现。</span><span class="sxs-lookup"><span data-stu-id="cbb32-172">`[BindRequired]`: This attribute adds a model state error if binding cannot occur.</span></span>

* <span data-ttu-id="cbb32-173">`[BindNever]`： 指示模型联编程序永远不会将绑定到此参数。</span><span class="sxs-lookup"><span data-stu-id="cbb32-173">`[BindNever]`: Tells the model binder to never bind to this parameter.</span></span>

* <span data-ttu-id="cbb32-174">`[FromHeader]``[FromQuery]`， `[FromRoute]`， `[FromForm]`： 使用它们来指定你想要应用的确切绑定源。</span><span class="sxs-lookup"><span data-stu-id="cbb32-174">`[FromHeader]`, `[FromQuery]`, `[FromRoute]`, `[FromForm]`: Use these to specify the exact binding source you want to apply.</span></span>

* <span data-ttu-id="cbb32-175">`[FromServices]`： 此属性使用[依赖关系注入](../../fundamentals/dependency-injection.md)若要将参数绑定从服务。</span><span class="sxs-lookup"><span data-stu-id="cbb32-175">`[FromServices]`: This attribute uses [dependency injection](../../fundamentals/dependency-injection.md) to bind parameters from services.</span></span>

* <span data-ttu-id="cbb32-176">`[FromBody]`： 用于配置格式化程序将数据绑定中请求正文。</span><span class="sxs-lookup"><span data-stu-id="cbb32-176">`[FromBody]`: Use the configured formatters to bind data from the request body.</span></span> <span data-ttu-id="cbb32-177">根据请求内容类型，格式化程序处于选中状态。</span><span class="sxs-lookup"><span data-stu-id="cbb32-177">The formatter is selected based on content type of the request.</span></span>

* <span data-ttu-id="cbb32-178">`[ModelBinder]`： 用于重写默认模型联编程序、 绑定源和名称。</span><span class="sxs-lookup"><span data-stu-id="cbb32-178">`[ModelBinder]`: Used to override the default model binder, binding source and name.</span></span>

<span data-ttu-id="cbb32-179">属性是非常有用的工具时需要重写模型绑定的默认行为。</span><span class="sxs-lookup"><span data-stu-id="cbb32-179">Attributes are very helpful tools when you need to override the default behavior of model binding.</span></span>

## <a name="binding-formatted-data-from-the-request-body"></a><span data-ttu-id="cbb32-180">从请求正文的格式的绑定数据</span><span class="sxs-lookup"><span data-stu-id="cbb32-180">Binding formatted data from the request body</span></span>

<span data-ttu-id="cbb32-181">请求数据可以来自各种包括 JSON、 XML 和许多其他的格式。</span><span class="sxs-lookup"><span data-stu-id="cbb32-181">Request data can come in a variety of formats including JSON, XML and many others.</span></span> <span data-ttu-id="cbb32-182">当你使用 [FromBody] 属性以指示你想要将参数绑定到请求正文中的数据时，MVC 将使用一组配置的格式化程序来处理基于其内容类型的请求数据。</span><span class="sxs-lookup"><span data-stu-id="cbb32-182">When you use the [FromBody] attribute to indicate that you want to bind a parameter to data in the request body, MVC uses a configured set of formatters to handle the request data based on its content type.</span></span> <span data-ttu-id="cbb32-183">默认情况下 MVC 包括`JsonInputFormatter`类处理 JSON 数据，但你可以添加用于处理 XML 和其他自定义格式的其他格式化程序。</span><span class="sxs-lookup"><span data-stu-id="cbb32-183">By default MVC includes a `JsonInputFormatter` class for handling JSON data, but you can add additional formatters for handling XML and other custom formats.</span></span>

> [!NOTE]
> <span data-ttu-id="cbb32-184">可以有最多一个参数，每个操作使用修饰`[FromBody]`。</span><span class="sxs-lookup"><span data-stu-id="cbb32-184">There can be at most one parameter per action decorated with `[FromBody]`.</span></span> <span data-ttu-id="cbb32-185">ASP.NET 核心 MVC 运行时委托责任的格式化程序读取请求流。</span><span class="sxs-lookup"><span data-stu-id="cbb32-185">The ASP.NET Core MVC run-time delegates the responsibility of reading the request stream to the formatter.</span></span> <span data-ttu-id="cbb32-186">一旦参数读取请求流，它通常不是可以读取请求流再次为其他绑定`[FromBody]`参数。</span><span class="sxs-lookup"><span data-stu-id="cbb32-186">Once the request stream is read for a parameter, it's generally not possible to read the request stream again for binding other `[FromBody]` parameters.</span></span>

> [!NOTE]
> <span data-ttu-id="cbb32-187">`JsonInputFormatter`是默认的格式化程序和基于[Json.NET](https://www.newtonsoft.com/json)。</span><span class="sxs-lookup"><span data-stu-id="cbb32-187">The `JsonInputFormatter` is the default formatter and is based on [Json.NET](https://www.newtonsoft.com/json).</span></span>

<span data-ttu-id="cbb32-188">ASP.NET 选择基于输入格式化程序[内容类型](https://www.w3.org/Protocols/rfc1341/4_Content-Type.html)标头和类型的参数，除非没有应用于它否则指定的特性。</span><span class="sxs-lookup"><span data-stu-id="cbb32-188">ASP.NET selects input formatters based on the [Content-Type](https://www.w3.org/Protocols/rfc1341/4_Content-Type.html) header and the type of the parameter, unless there is an attribute applied to it specifying otherwise.</span></span> <span data-ttu-id="cbb32-189">如果你想要使用的 XML 或另一种格式必须配置在*Startup.cs*文件，但你可能会首先必须获取对引用`Microsoft.AspNetCore.Mvc.Formatters.Xml`使用 NuGet。</span><span class="sxs-lookup"><span data-stu-id="cbb32-189">If you'd like to use XML or another format you must configure it in the *Startup.cs* file, but you may first have to obtain a reference to `Microsoft.AspNetCore.Mvc.Formatters.Xml` using NuGet.</span></span> <span data-ttu-id="cbb32-190">启动代码应如下所示：</span><span class="sxs-lookup"><span data-stu-id="cbb32-190">Your startup code should look something like this:</span></span>

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddMvc()
        .AddXmlSerializerFormatters();
   }
```

<span data-ttu-id="cbb32-191">中的代码*Startup.cs*文件包含`ConfigureServices`方法替换`services`可用于为 ASP.NET 应用程序的服务生成的自变量。</span><span class="sxs-lookup"><span data-stu-id="cbb32-191">Code in the *Startup.cs* file contains a `ConfigureServices` method with a `services` argument you can use to build up services for your ASP.NET app.</span></span> <span data-ttu-id="cbb32-192">在示例中，我们要添加为 MVC 将为此应用程序提供服务的 XML 格式化程序。</span><span class="sxs-lookup"><span data-stu-id="cbb32-192">In the sample, we are adding an XML formatter as a service that MVC will provide for this app.</span></span> <span data-ttu-id="cbb32-193">`options`自变量传递给`AddMvc`方法可用于添加和管理筛选器、 格式化程序和其他系统选项利用 MVC，在应用启动后。</span><span class="sxs-lookup"><span data-stu-id="cbb32-193">The `options` argument passed into the `AddMvc` method allows you to add and manage filters, formatters, and other system options from MVC upon app startup.</span></span> <span data-ttu-id="cbb32-194">然后应用`Consumes`属性设为控制器类或操作方法要使用所需的格式。</span><span class="sxs-lookup"><span data-stu-id="cbb32-194">Then apply the `Consumes` attribute to controller classes or action methods to work with the format you want.</span></span>

### <a name="custom-model-binding"></a><span data-ttu-id="cbb32-195">自定义模型绑定</span><span class="sxs-lookup"><span data-stu-id="cbb32-195">Custom Model Binding</span></span>

<span data-ttu-id="cbb32-196">可以通过编写自己的自定义模型联编程序扩展模型绑定。</span><span class="sxs-lookup"><span data-stu-id="cbb32-196">You can extend model binding by writing your own custom model binders.</span></span> <span data-ttu-id="cbb32-197">详细了解[自定义模型绑定](../advanced/custom-model-binding.md)。</span><span class="sxs-lookup"><span data-stu-id="cbb32-197">Learn more about [custom model binding](../advanced/custom-model-binding.md).</span></span>
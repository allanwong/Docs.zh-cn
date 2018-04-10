---
uid: web-pages/overview/releases/top-features-in-web-pages-2
title: 所需的 ASP.NET Web Pages 2 中的顶部功能 |Microsoft 文档
author: microsoft
description: 本主题概述在 ASP.NET 网页 2 中，一个附带 WebMatr 的轻型 web 编程框架的顶部新功能...
ms.author: aspnetcontent
manager: wpickett
ms.date: 02/13/2012
ms.topic: article
ms.assetid: cc712e72-c3d0-4e43-bc2d-28cc09cd8f71
ms.technology: dotnet-webpages
ms.prod: .net-framework
msc.legacyurl: /web-pages/overview/releases/top-features-in-web-pages-2
msc.type: authoredcontent
ms.openlocfilehash: f0d32edd3ab54c55aa06c803cd91e01cbbb8f08a
ms.sourcegitcommit: f8852267f463b62d7f975e56bea9aa3f68fbbdeb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2018
---
<a name="the-top-features-in-aspnet-web-pages-2"></a><span data-ttu-id="1abea-103">在 ASP.NET Web Pages 2 靠前的特征</span><span class="sxs-lookup"><span data-stu-id="1abea-103">The Top Features in ASP.NET Web Pages 2</span></span>
====================
<span data-ttu-id="1abea-104">by [Microsoft](https://github.com/microsoft)</span><span class="sxs-lookup"><span data-stu-id="1abea-104">by [Microsoft](https://github.com/microsoft)</span></span>

> <span data-ttu-id="1abea-105">本文概述了 ASP.NET Web Pages 2 RC，附带的轻型 web 编程框架中最新功能的[Microsoft WebMatrix 2 RC](https://www.microsoft.com/web/)。</span><span class="sxs-lookup"><span data-stu-id="1abea-105">This article provides an overview of the top new features in the ASP.NET Web Pages 2 RC, a lightweight web programming framework that is included with [Microsoft WebMatrix 2 RC](https://www.microsoft.com/web/).</span></span>
> 
> <span data-ttu-id="1abea-106">**包含的内容：**</span><span class="sxs-lookup"><span data-stu-id="1abea-106">**What's included:**</span></span> 
> 
> - [<span data-ttu-id="1abea-107">安装 WebMatrix</span><span class="sxs-lookup"><span data-stu-id="1abea-107">Installing WebMatrix</span></span>](#install)
> - [<span data-ttu-id="1abea-108">新的和增强功能</span><span class="sxs-lookup"><span data-stu-id="1abea-108">New and enhanced features</span></span>](#New_and_Enhanced_Features)
> 
>     - [<span data-ttu-id="1abea-109">对于 RC 版本更改</span><span class="sxs-lookup"><span data-stu-id="1abea-109">Changes for the RC release</span></span>](#Changes_for_the_RC_Version)
>     - [<span data-ttu-id="1abea-110">Beta 版的更改</span><span class="sxs-lookup"><span data-stu-id="1abea-110">Changes for the Beta release</span></span>](#Changes_for_the_Beta_Version)
>     - [<span data-ttu-id="1abea-111">使用新的和更新站点模板</span><span class="sxs-lookup"><span data-stu-id="1abea-111">Using the New and Updated Site Templates</span></span>](#templates)
>     - [<span data-ttu-id="1abea-112">验证用户输入</span><span class="sxs-lookup"><span data-stu-id="1abea-112">Validating User Input</span></span>](#validation)
>     - [<span data-ttu-id="1abea-113">启用从 Facebook 和其他站点使用 OAuth 和 OpenID 登录名</span><span class="sxs-lookup"><span data-stu-id="1abea-113">Enabling logins from Facebook and other sites using OAuth and OpenID</span></span>](#oauthsetup)
>     - [<span data-ttu-id="1abea-114">添加使用地图帮助程序图</span><span class="sxs-lookup"><span data-stu-id="1abea-114">Adding Maps using the Maps Helper</span></span>](#maphelper)
>     - [<span data-ttu-id="1abea-115">运行 Web 页面应用程序并行</span><span class="sxs-lookup"><span data-stu-id="1abea-115">Running Web Pages Applications Side by Side</span></span>](#sidebyside)
>     - [<span data-ttu-id="1abea-116">为移动设备中呈现页</span><span class="sxs-lookup"><span data-stu-id="1abea-116">Rendering Pages for Mobile Devices</span></span>](#mobile)
> - [<span data-ttu-id="1abea-117">其他资源</span><span class="sxs-lookup"><span data-stu-id="1abea-117">Additional Resources</span></span>](#resources)
> 
> > [!NOTE]
> > <span data-ttu-id="1abea-118">本主题假定使用 WebMatrix 的目的若要使用 ASP.NET Web Pages 2 代码。</span><span class="sxs-lookup"><span data-stu-id="1abea-118">This topic assumes that you are using WebMatrix to work with your ASP.NET Web Pages 2 code.</span></span> <span data-ttu-id="1abea-119">但是，由于 Web Pages 1，您可以创建使用 Visual Studio Web Pages 2 网站，它会为你提供增强的 IntelliSense 功能和调试。</span><span class="sxs-lookup"><span data-stu-id="1abea-119">However, as with Web Pages 1, you can also create Web Pages 2 websites using Visual Studio, which gives you enhanced IntelliSense capabilities and debugging.</span></span> <span data-ttu-id="1abea-120">若要使用 Visual Studio 中的网页，你必须首先安装 Visual Studio 2010 SP1、 Visual Web Developer Express 2010 SP1 中或 Visual Studio 11 Beta。</span><span class="sxs-lookup"><span data-stu-id="1abea-120">To work with Web Pages in Visual Studio, you must first install Visual Studio 2010 SP1, Visual Web Developer Express 2010 SP1, or Visual Studio 11 Beta.</span></span> <span data-ttu-id="1abea-121">然后，安装 ASP.NET MVC 4 Beta 的说明进行操作，其中包括模板和工具用于在 Visual Studio 中创建 ASP.NET MVC 4 和 Web Pages 2 的应用程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-121">Then install the ASP.NET MVC 4 Beta, which includes templates and tools for creating ASP.NET MVC 4 and Web Pages 2 applications in Visual Studio.</span></span>
> 
> 
> <span data-ttu-id="1abea-122">*上次更新： 2012 年 6 月 18*</span><span class="sxs-lookup"><span data-stu-id="1abea-122">*Last update: 18 June 2012*</span></span>


<a id="install"></a>
## <a name="installing-webmatrix"></a><span data-ttu-id="1abea-123">安装 WebMatrix</span><span class="sxs-lookup"><span data-stu-id="1abea-123">Installing WebMatrix</span></span>

<span data-ttu-id="1abea-124">若要安装 Web 页，可以使用 Microsoft Web 平台安装程序，这是一个免费的应用程序，可以轻松地安装和配置 web 相关技术。</span><span class="sxs-lookup"><span data-stu-id="1abea-124">To install Web Pages, you can use the Microsoft Web Platform Installer, which is a free application that makes it easy to install and configure web-related technologies.</span></span> <span data-ttu-id="1abea-125">将安装 WebMatrix 2 Beta，其中包括 Web Pages 2 Beta。</span><span class="sxs-lookup"><span data-stu-id="1abea-125">You will install the WebMatrix 2 Beta, which includes Web Pages 2 Beta.</span></span>

1. <span data-ttu-id="1abea-126">浏览到 Web 平台安装程序的最新版本的安装页面：</span><span class="sxs-lookup"><span data-stu-id="1abea-126">Browse to the installation page for the latest version of the Web Platform Installer:</span></span>

    [https://go.microsoft.com/fwlink/?LinkId=226883](https://go.microsoft.com/fwlink/?LinkId=226883)

    > [!NOTE]
    > <span data-ttu-id="1abea-127">如果你没有安装 WebMatrix 1，此安装程序更新它为 WebMatrix 2 Beta。</span><span class="sxs-lookup"><span data-stu-id="1abea-127">If you already have WebMatrix 1 installed, this installation updates it to WebMatrix 2 Beta.</span></span> <span data-ttu-id="1abea-128">你可以运行在同一台计算机上使用版本 1 或 2 创建的网站。</span><span class="sxs-lookup"><span data-stu-id="1abea-128">You can run websites that were created using version 1 or 2 on the same computer.</span></span> <span data-ttu-id="1abea-129">有关详细信息，请参阅部分[运行网页的应用程序并行](#sidebyside)。</span><span class="sxs-lookup"><span data-stu-id="1abea-129">For more information, see the section on [Running Web Pages Applications Side by Side](#sidebyside).</span></span>
2. <span data-ttu-id="1abea-130">选择**立即安装**。</span><span class="sxs-lookup"><span data-stu-id="1abea-130">Choose **Install Now**.</span></span> 

    <span data-ttu-id="1abea-131">如果你使用 Internet Explorer，请转到下一步。</span><span class="sxs-lookup"><span data-stu-id="1abea-131">If you use Internet Explorer, go to the next step.</span></span> <span data-ttu-id="1abea-132">如果你使用不同的浏览器，如 Mozilla Firefox 或 Google Chrome，则会提示您保存*Webmatrix.exe*到你的计算机的文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-132">If you use a different browser like Mozilla Firefox or Google Chrome, you are prompted to save the *Webmatrix.exe* file to your computer.</span></span> <span data-ttu-id="1abea-133">保存该文件，然后单击它以启动安装程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-133">Save the file and then click it to launch the installer.</span></span>
3. <span data-ttu-id="1abea-134">运行安装程序并选择**安装**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-134">Run the installer and choose the **Install** button.</span></span> <span data-ttu-id="1abea-135">这将安装 WebMatrix 和 Web 页。</span><span class="sxs-lookup"><span data-stu-id="1abea-135">This installs WebMatrix and Web Pages.</span></span>

## <a id="New_and_Enhanced_Features"></a>  <span data-ttu-id="1abea-136">新的和增强功能</span><span class="sxs-lookup"><span data-stu-id="1abea-136">New and Enhanced Features</span></span>

### <a id="Changes_for_the_RC_Version"></a>  <span data-ttu-id="1abea-137">RC 版本 (2012 年 6 月) 的更改</span><span class="sxs-lookup"><span data-stu-id="1abea-137">Changes for the RC Version (June 2012)</span></span>

<span data-ttu-id="1abea-138">在 2012 年 6 月 RC 版本发布具有少量更改从 2012 年 3 月发布的 Beta 版本刷新。</span><span class="sxs-lookup"><span data-stu-id="1abea-138">The RC version release in June 2012 has a few changes from the Beta version refresh that was released in March 2012.</span></span> <span data-ttu-id="1abea-139">这些更改包括：</span><span class="sxs-lookup"><span data-stu-id="1abea-139">These changes are:</span></span>

- <span data-ttu-id="1abea-140">A`Validation.AddFormError`方法已添加到`Validation`帮助器。</span><span class="sxs-lookup"><span data-stu-id="1abea-140">A `Validation.AddFormError` method was added to the `Validation` helper.</span></span> <span data-ttu-id="1abea-141">这是手动执行验证的情况下很有用 （例如，验证查询字符串中传递一个值） 和你想要添加可由显示的错误消息`Html.ValidationSummary`方法。</span><span class="sxs-lookup"><span data-stu-id="1abea-141">This is useful if you perform validation manually (for example, you validate a value that is passed in the query string) and you want to add an error message that can be displayed by the `Html.ValidationSummary` method.</span></span> <span data-ttu-id="1abea-142">有关详细信息，请参阅明[验证数据，不会直接从用户](https://go.microsoft.com/fwlink/?LinkId=253002#Validating_Data_That_Doesnt_Come_Directly_from_Users)中[ASP.NET Web 页 (Razor) 站点中验证用户输入](https://go.microsoft.com/fwlink/?LinkId=253002)。</span><span class="sxs-lookup"><span data-stu-id="1abea-142">For more information, see the section [Validating Data That Doesn't Come Directly From Users](https://go.microsoft.com/fwlink/?LinkId=253002#Validating_Data_That_Doesnt_Come_Directly_from_Users) in [Validating User Input in ASP.NET Web Pages (Razor) Sites](https://go.microsoft.com/fwlink/?LinkId=253002).</span></span>
- <span data-ttu-id="1abea-143">已从核心 ASP.NET 网页 2 程序集绑定和缩减的功能。</span><span class="sxs-lookup"><span data-stu-id="1abea-143">The functionality for bundling and minification has been removed from the core ASP.NET Web Pages 2 assemblies.</span></span> <span data-ttu-id="1abea-144">因此，`Assets`本文档后面部分中列出的帮助器不可用。</span><span class="sxs-lookup"><span data-stu-id="1abea-144">As a consequence, the `Assets` helper listed later in this document is not available.</span></span> <span data-ttu-id="1abea-145">相反，你必须安装[ASP.NET 优化](http://nuget.org/packages/Microsoft.Web.Optimization/0.1)NuGet 包。</span><span class="sxs-lookup"><span data-stu-id="1abea-145">Instead, you must install the [ASP.NET Optimization](http://nuget.org/packages/Microsoft.Web.Optimization/0.1) NuGet package.</span></span> <span data-ttu-id="1abea-146">有关详细信息，请参阅[捆绑和贴图层 ASP.NET Web 页 (Razor) 站点中的资产](https://go.microsoft.com/fwlink/?LinkId=255373)。</span><span class="sxs-lookup"><span data-stu-id="1abea-146">For more information, see [Bundling and Minifying Assets in an ASP.NET Web Pages (Razor) Site](https://go.microsoft.com/fwlink/?LinkId=255373).</span></span>
- <span data-ttu-id="1abea-147">添加了其他程序集以支持 ASP.NET Web Pages 2。</span><span class="sxs-lookup"><span data-stu-id="1abea-147">Additional assemblies to support ASP.NET Web Pages 2 have been added.</span></span> <span data-ttu-id="1abea-148">此更改仅明显的影响是，你可能看到的站点中的多个程序集*bin*后创建一个站点或将站点部署到宿主提供程序的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1abea-148">The only noticeable effect of this change is that you might see more assemblies in a site's *bin* folder after you create a site or deploy a site to a hosting provider.</span></span>

<a id="Changes_for_the_Beta_Version"></a>
### <a name="changes-for-the-beta-version-february-2012"></a><span data-ttu-id="1abea-149">对于 Beta 版本 (2012 年 2 月) 的更改</span><span class="sxs-lookup"><span data-stu-id="1abea-149">Changes for the Beta Version (February 2012)</span></span>

<span data-ttu-id="1abea-150">在 2012 年 2 月发布的 Beta 版本具有来自于 2011 年 12 月发布的 Beta 版本仅少量更改。</span><span class="sxs-lookup"><span data-stu-id="1abea-150">The Beta version released in February 2012 has only a few changes from the Beta version that was released in December 2011.</span></span> <span data-ttu-id="1abea-151">这些更改包括：</span><span class="sxs-lookup"><span data-stu-id="1abea-151">These changes are:</span></span>

- <span data-ttu-id="1abea-152">Razor 现在支持条件属性。</span><span class="sxs-lookup"><span data-stu-id="1abea-152">Razor now supports conditional attributes.</span></span> <span data-ttu-id="1abea-153">在 HTML 元素，如果你将属性设置为一个值，解析到的服务器代码中`false`或`null`，ASP.NET 不会在所有呈现该属性。</span><span class="sxs-lookup"><span data-stu-id="1abea-153">In an HTML element, if you set an attribute to a value that resolves in server code to `false` or `null`, ASP.NET does not render the attribute at all.</span></span> <span data-ttu-id="1abea-154">例如，假设有一个复选框的以下标记：</span><span class="sxs-lookup"><span data-stu-id="1abea-154">For example, imagine you have the following markup for a check box:</span></span>

    [!code-html[Main](top-features-in-web-pages-2/samples/sample1.html)]

    <span data-ttu-id="1abea-155">如果值`checked1`解析为`false`或`null`、`checked`不呈现属性。</span><span class="sxs-lookup"><span data-stu-id="1abea-155">If the value of `checked1` resolves to `false` or to `null`, the `checked` attribute is not rendered.</span></span> <span data-ttu-id="1abea-156">这是一项重大更改。</span><span class="sxs-lookup"><span data-stu-id="1abea-156">This is a breaking change.</span></span>
- <span data-ttu-id="1abea-157">`Validation.GetHtml`方法已重命名为`Validation.For`。</span><span class="sxs-lookup"><span data-stu-id="1abea-157">The `Validation.GetHtml` method has been renamed to `Validation.For`.</span></span> <span data-ttu-id="1abea-158">这是一项重大更改;`Validation.GetHtml` Beta 版本中将不工作。</span><span class="sxs-lookup"><span data-stu-id="1abea-158">This is a breaking change; `Validation.GetHtml` will not work in the Beta release.</span></span>
- <span data-ttu-id="1abea-159">你现在可以包含`~`运算符在标记中无需使用引用的站点根目录`Href`函数。</span><span class="sxs-lookup"><span data-stu-id="1abea-159">You can now include the `~` operator in markup to reference the site root without using the `Href` function.</span></span> <span data-ttu-id="1abea-160">(即，Razor 分析器可以现在找到并解决`~`而无需对的显式方法调用运算符`Href`。)`Href`方法仍然正常工作，因此这不是一项重大更改。</span><span class="sxs-lookup"><span data-stu-id="1abea-160">(That is, the Razor parser can now find and resolve the `~` operator without requiring an explicit method call to `Href`.) The `Href` method still works, so this is not a breaking change.</span></span>

    <span data-ttu-id="1abea-161">例如，如果你以前标记如下：</span><span class="sxs-lookup"><span data-stu-id="1abea-161">For example, if you previously had markup like this:</span></span>

    `<a href="@Href("~/Default.cshtml")">Home</a>`

    <span data-ttu-id="1abea-162">你现在可以使用标记如下：</span><span class="sxs-lookup"><span data-stu-id="1abea-162">You can now use markup like this:</span></span>

    `<a href="~/Default.cshtml">Home</a>`
- <span data-ttu-id="1abea-163">`Scripts`帮助资产 （资源） 管理器已替换`Assets`帮助器，有略有不同的方法，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1abea-163">The `Scripts` helper for assets (resource) management has been replaced with the `Assets` helper, which has slightly different methods, such as the following:</span></span>

  - <span data-ttu-id="1abea-164">有关`Scripts.Add`，使用 `Assets.AddScript`</span><span class="sxs-lookup"><span data-stu-id="1abea-164">For `Scripts.Add`, use `Assets.AddScript`</span></span>
  - <span data-ttu-id="1abea-165">有关`Scripts.GetScriptTags`，使用 `Assets.GetScripts`</span><span class="sxs-lookup"><span data-stu-id="1abea-165">For `Scripts.GetScriptTags`, use `Assets.GetScripts`</span></span>

    <span data-ttu-id="1abea-166">这是一项重大更改;`Scripts`类不是在 Beta 版本中可用。</span><span class="sxs-lookup"><span data-stu-id="1abea-166">This is a breaking change; the `Scripts` class is not available in the Beta release.</span></span> <span data-ttu-id="1abea-167">进行此更改后已更新使用资产管理本文档中的代码示例。</span><span class="sxs-lookup"><span data-stu-id="1abea-167">The code examples in this document that use asset management have been updated with this change.</span></span>

<a id="templates"></a>
### <a name="using-the-new-and-updated-site-templates"></a><span data-ttu-id="1abea-168">使用新的和更新站点模板</span><span class="sxs-lookup"><span data-stu-id="1abea-168">Using the New and Updated Site Templates</span></span>

<span data-ttu-id="1abea-169">**入门站点**模板已更新以便使其在网页 2 上运行默认情况下。</span><span class="sxs-lookup"><span data-stu-id="1abea-169">The **Starter Site** template has been updated so that it runs on Web Pages 2 by default.</span></span> <span data-ttu-id="1abea-170">它还包括以下新功能：</span><span class="sxs-lookup"><span data-stu-id="1abea-170">It also includes the following new capabilities:</span></span>

- <span data-ttu-id="1abea-171">良好移动性页面呈现。</span><span class="sxs-lookup"><span data-stu-id="1abea-171">Mobile-friendly page rendering.</span></span> <span data-ttu-id="1abea-172">通过使用 CSS 样式和`@media`选择器，**入门站点**较小的屏幕，包括移动设备屏幕上提供改进的呈现的页。</span><span class="sxs-lookup"><span data-stu-id="1abea-172">Through the use of CSS styles and the `@media` selector, the **Starter Site** provides improved rendering of pages on smaller screens, including mobile device screens.</span></span>
- <span data-ttu-id="1abea-173">改进的成员身份和身份验证选项。</span><span class="sxs-lookup"><span data-stu-id="1abea-173">Improved membership and authentication options.</span></span> <span data-ttu-id="1abea-174">你可以让用户登录到你从 Twitter、 Facebook、 和 Windows Live 等其他社交网络站点中使用其帐户的站点。</span><span class="sxs-lookup"><span data-stu-id="1abea-174">You can let users log into your site using their accounts from other social networking sites, such as Twitter, Facebook, and Windows Live.</span></span> <span data-ttu-id="1abea-175">有关详细信息，请参阅[将登录名启用从 Facebook 和其他站点使用 OAuth 和 OpenID](#oauthsetup)部分。</span><span class="sxs-lookup"><span data-stu-id="1abea-175">For more information, see the [Enabling Logins from Facebook and Other Sites using OAuth and OpenID](#oauthsetup) section.</span></span>
- <span data-ttu-id="1abea-176">HTML5 元素。</span><span class="sxs-lookup"><span data-stu-id="1abea-176">HTML5 elements.</span></span>

<span data-ttu-id="1abea-177">新**个人站点**模板允许你创建包含个人博客、 照片页和 Twitter 页面的网站。</span><span class="sxs-lookup"><span data-stu-id="1abea-177">The new **Personal Site** template lets you create a website that contains a personal blog, a photos page, and a Twitter page.</span></span> <span data-ttu-id="1abea-178">你可以自定义基于站点**个人站点**通过执行以下模板：</span><span class="sxs-lookup"><span data-stu-id="1abea-178">You can customize a site based on the **Personal Site** template by doing the following:</span></span>

- <span data-ttu-id="1abea-179">通过编辑布局文件来更改查找范围的站点 (*\_SiteLayout.cshtml*) 和样式文件 (*Site.css*)。</span><span class="sxs-lookup"><span data-stu-id="1abea-179">Change the look of the site by editing the layout file (*\_SiteLayout.cshtml*) and the styles file (*Site.css*).</span></span>
- <span data-ttu-id="1abea-180">安装 NuGet 包可将功能添加到你的站点。</span><span class="sxs-lookup"><span data-stu-id="1abea-180">Install NuGet packages that add functionality to your site.</span></span> <span data-ttu-id="1abea-181">有关如何安装包的信息，包括 ASP.NET Web 帮助程序库，请参阅本教程[安装帮助器](https://go.microsoft.com/fwlink/?LinkId=202889#webhelpers)。</span><span class="sxs-lookup"><span data-stu-id="1abea-181">For information about how to install packages, including the ASP.NET Web Helpers Library, see the tutorial about [installing helpers](https://go.microsoft.com/fwlink/?LinkId=202889#webhelpers).</span></span>

<span data-ttu-id="1abea-182">访问**个人站点**模板中，选择**模板**上 WebMatrix**快速启动**屏幕。</span><span class="sxs-lookup"><span data-stu-id="1abea-182">To access the **Personal Site** template, choose **Templates** on the WebMatrix **Quick Start** screen.</span></span>

<span data-ttu-id="1abea-183">[![topseven-personalsite-1](top-features-in-web-pages-2/_static/image2.png)](top-features-in-web-pages-2/_static/image1.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-183">[![topseven-personalsite-1](top-features-in-web-pages-2/_static/image2.png)](top-features-in-web-pages-2/_static/image1.png)</span></span>

<span data-ttu-id="1abea-184">在**模板**对话框框中，选择**个人站点**模板。</span><span class="sxs-lookup"><span data-stu-id="1abea-184">In the **Templates** dialog box, choose the **Personal Site** template.</span></span>

<span data-ttu-id="1abea-185">[![topseven-personalsite-2](top-features-in-web-pages-2/_static/image4.png)](top-features-in-web-pages-2/_static/image3.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-185">[![topseven-personalsite-2](top-features-in-web-pages-2/_static/image4.png)](top-features-in-web-pages-2/_static/image3.png)</span></span>

<span data-ttu-id="1abea-186">登录页**个人站点**模板允许你跟踪链接以设置您的博客，Twitter 页和照片页。</span><span class="sxs-lookup"><span data-stu-id="1abea-186">The landing page of the **Personal Site** template lets you follow links to set up your blog, Twitter page, and photos page.</span></span>

<span data-ttu-id="1abea-187">[![topseven-personalsite-3](top-features-in-web-pages-2/_static/image6.png)](top-features-in-web-pages-2/_static/image5.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-187">[![topseven-personalsite-3](top-features-in-web-pages-2/_static/image6.png)](top-features-in-web-pages-2/_static/image5.png)</span></span>

<a id="validation"></a>
### <a name="validating-user-input"></a><span data-ttu-id="1abea-188">验证用户输入</span><span class="sxs-lookup"><span data-stu-id="1abea-188">Validating User Input</span></span>

<span data-ttu-id="1abea-189">在 Web 页 1 来验证用户输入提交窗体上，你使用`System.Web.WebPages.Html.ModelState`类。</span><span class="sxs-lookup"><span data-stu-id="1abea-189">In Web Pages 1, to validate user input on submitted forms, you use the `System.Web.WebPages.Html.ModelState` class.</span></span> <span data-ttu-id="1abea-190">(此进行了阐释几个代码示例中标题为网页 1 教程[使用数据](../data/5-working-with-data.md)。)你仍可以在 Web Pages 2 中使用此方法。</span><span class="sxs-lookup"><span data-stu-id="1abea-190">(This is illustrated in several of the code samples in the Web Pages 1 tutorial titled [Working with Data](../data/5-working-with-data.md).) You can still use this approach in Web Pages 2.</span></span> <span data-ttu-id="1abea-191">但是，Web Pages 2 还提供改进的工具，用于验证用户输入：</span><span class="sxs-lookup"><span data-stu-id="1abea-191">However, Web Pages 2 also offers improved tools for validating user input:</span></span>

- <span data-ttu-id="1abea-192">新的验证类，包括`System.Web.WebPages.ValidationHelper`和`System.Web.WebPages.Validator`，能够让你执行功能强大的验证任务使用的代码的几行。</span><span class="sxs-lookup"><span data-stu-id="1abea-192">New validation classes, including `System.Web.WebPages.ValidationHelper` and `System.Web.WebPages.Validator`, that let you do powerful validation tasks with a few lines of code.</span></span>
- <span data-ttu-id="1abea-193">（可选） 提供即时的反馈给此用户而不是要求到服务器的往返行程，以检查是否有验证错误的客户端验证。</span><span class="sxs-lookup"><span data-stu-id="1abea-193">Optionally, client-side validation, which provides immediate feedback to the user instead of requiring a round trip to the server to check for validation errors.</span></span> <span data-ttu-id="1abea-194">（出于安全原因，验证在服务器上即使事先在客户端执行检查。）</span><span class="sxs-lookup"><span data-stu-id="1abea-194">(For security reasons, validation is performed on the server even if the checks have been performed in the client beforehand.)</span></span>

<span data-ttu-id="1abea-195">若要使用新的验证功能，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="1abea-195">To use the new validation features, do the following:</span></span>

<span data-ttu-id="1abea-196">在页面的代码中，注册要由使用的方法验证元素`Validation`帮助器： `Validation.RequireField`， `Validation.RequireFields` （若要注册多个元素是必需），或`Validation.Add`。</span><span class="sxs-lookup"><span data-stu-id="1abea-196">In the page's code, register an element to be validated by using methods of the `Validation` helper: `Validation.RequireField`, `Validation.RequireFields` (to register multiple elements to be required), or `Validation.Add`.</span></span> <span data-ttu-id="1abea-197">`Add`方法允许您指定其他类型的验证检查，如数据类型检查、 比较不同的字段，字符串长度检查中的条目并模式 （使用正则表达式）。</span><span class="sxs-lookup"><span data-stu-id="1abea-197">The `Add` method lets you specify other types of validation checks, like data-type checking, comparing entries in different fields, string-length checks, and patterns (using regular expressions).</span></span> <span data-ttu-id="1abea-198">下面是一些可能的恶意活动：</span><span class="sxs-lookup"><span data-stu-id="1abea-198">Here are some examples:</span></span>

[!code-html[Main](top-features-in-web-pages-2/samples/sample2.html)]

<span data-ttu-id="1abea-199">若要显示特定于字段的错误，请调用`Html.ValidationMessage`正被验证每个元素的标记中：</span><span class="sxs-lookup"><span data-stu-id="1abea-199">To display a field-specific error, call `Html.ValidationMessage` in the markup for each element being validated:</span></span>

[!code-cshtml[Main](top-features-in-web-pages-2/samples/sample3.cshtml)]

<span data-ttu-id="1abea-200">若要显示的摘要 (`<ul>`列表) 的在页中，所有错误`Html.ValidationSummary`标记中：</span><span class="sxs-lookup"><span data-stu-id="1abea-200">To display a summary (`<ul>` list) of all the errors in the page, `Html.ValidationSummary` in the markup:</span></span>

[!code-cshtml[Main](top-features-in-web-pages-2/samples/sample4.cshtml)]

<span data-ttu-id="1abea-201">这些步骤足以实现服务器端验证。</span><span class="sxs-lookup"><span data-stu-id="1abea-201">These steps are enough to implement server-side validation.</span></span> <span data-ttu-id="1abea-202">如果你想要添加客户端验证，执行以下此外。</span><span class="sxs-lookup"><span data-stu-id="1abea-202">If you want to add client-side validation, do the following in addition.</span></span>

<span data-ttu-id="1abea-203">添加以下脚本文件引用内的`<head>`web 页的部分。</span><span class="sxs-lookup"><span data-stu-id="1abea-203">Add the following script file references inside the `<head>` section of a web page.</span></span> <span data-ttu-id="1abea-204">前两个脚本引用点移到内容交付网络 (CDN) 服务器上的远程文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-204">The first two script references point to remote files on a content delivery network (CDN) server.</span></span> <span data-ttu-id="1abea-205">第三个引用将指向本地脚本文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-205">The third reference points to a local script file.</span></span> <span data-ttu-id="1abea-206">CDN 不可用时，生产应用程序应实现回退。</span><span class="sxs-lookup"><span data-stu-id="1abea-206">Production apps should implement a fallback when the CDN is unavailable.</span></span> <span data-ttu-id="1abea-207">测试回退。</span><span class="sxs-lookup"><span data-stu-id="1abea-207">Test the fallback.</span></span>

[!code-html[Main](top-features-in-web-pages-2/samples/sample5.html)]

<span data-ttu-id="1abea-208">若要获取的本地副本的最简单方法*jquery.validate.unobtrusive.min.js*库是创建新的 Web 页站点基于之一 （如入门站点） 的站点模板。</span><span class="sxs-lookup"><span data-stu-id="1abea-208">The easiest way to get a local copy of the *jquery.validate.unobtrusive.min.js* library is to create a new Web Pages site based on one of the site templates (such as Starter Site).</span></span> <span data-ttu-id="1abea-209">由模板创建该网站包含*jquery.validate.unobtrusive.js*其脚本文件夹中，从中你可以将其复制到你的站点中的文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-209">The site created by the template includes *jquery.validate.unobtrusive.js* file in its Scripts folder, from which you can copy it to your site.</span></span>

<span data-ttu-id="1abea-210">如果你的网站使用<em>\_SiteLayout</em>页来控制页面布局中，你可以在该页中包括这些脚本引用，以便验证可供所有内容页。</span><span class="sxs-lookup"><span data-stu-id="1abea-210">If your website uses a<em>\_SiteLayout</em> page to control the page layout, you can include these script references in that page so that validation is available to all content pages.</span></span> <span data-ttu-id="1abea-211">如果你想要仅在特定的页上执行验证，你可以使用的资产管理器注册仅这些页面上的脚本。</span><span class="sxs-lookup"><span data-stu-id="1abea-211">If you want to perform validation only on particular pages, you can use the assets manager to register the scripts on only those pages.</span></span> <span data-ttu-id="1abea-212">若要执行此操作，调用`Assets.AddScript(path)`中你想要验证并引用每个脚本文件的页。</span><span class="sxs-lookup"><span data-stu-id="1abea-212">To do this, call `Assets.AddScript(path)` in the page that you want to validate and reference each of the script files.</span></span> <span data-ttu-id="1abea-213">然后添加对的调用`Assets.GetScripts`中 <em>\_SiteLayout</em>以便呈现的已注册的页`<script>`标记。</span><span class="sxs-lookup"><span data-stu-id="1abea-213">Then add a call to `Assets.GetScripts` in the <em>\_SiteLayout</em> page in order to render the registered `<script>` tags.</span></span> <span data-ttu-id="1abea-214">有关详细信息，请参阅明[与资产管理器注册脚本](#resmanagement)。</span><span class="sxs-lookup"><span data-stu-id="1abea-214">For more information, see the section [Registering Scripts with the Assets Manager](#resmanagement).</span></span>

<span data-ttu-id="1abea-215">单个元素的标记，在调用`Validation.For`方法。</span><span class="sxs-lookup"><span data-stu-id="1abea-215">In the markup for an individual element, call the `Validation.For` method.</span></span> <span data-ttu-id="1abea-216">此方法发出特性该 jQuery 可以挂钩以便提供客户端验证。</span><span class="sxs-lookup"><span data-stu-id="1abea-216">This method emits attributes that jQuery can hook in order to provide client-side validation.</span></span> <span data-ttu-id="1abea-217">例如：</span><span class="sxs-lookup"><span data-stu-id="1abea-217">For example:</span></span>

[!code-cshtml[Main](top-features-in-web-pages-2/samples/sample6.cshtml)]

<span data-ttu-id="1abea-218">下面的示例演示验证窗体上的用户输入的页。</span><span class="sxs-lookup"><span data-stu-id="1abea-218">The following example shows a page that validates user input on a form.</span></span> <span data-ttu-id="1abea-219">若要运行和测试此验证代码，请执行此操作：</span><span class="sxs-lookup"><span data-stu-id="1abea-219">To run and test this validation code, do this:</span></span>

1. <span data-ttu-id="1abea-220">创建新的网站使用包括 WebMatrix 2 站点模板之一*脚本*文件夹，如**入门站点**模板。</span><span class="sxs-lookup"><span data-stu-id="1abea-220">Create a new web site using one of the WebMatrix 2 site templates that includes a *Scripts* folder, such as the **Starter Site** template.</span></span>
2. <span data-ttu-id="1abea-221">在新的站点中，创建一个新*.cshtml*页，然后将页面内容替换为下面的代码。</span><span class="sxs-lookup"><span data-stu-id="1abea-221">In the new site, create a new *.cshtml* page, and replace the contents of the page with the following code.</span></span>
3. <span data-ttu-id="1abea-222">在浏览器中运行页面。</span><span class="sxs-lookup"><span data-stu-id="1abea-222">Run the page in a browser.</span></span> <span data-ttu-id="1abea-223">输入有效和无效的值，以查看对验证的影响。</span><span class="sxs-lookup"><span data-stu-id="1abea-223">Enter valid and invalid values to see the effects on validation.</span></span> <span data-ttu-id="1abea-224">例如，将必填的字段留空，或输入的字母**信用额度**字段。</span><span class="sxs-lookup"><span data-stu-id="1abea-224">For example, leave a required field blank or enter a letter in the **Credits** field.</span></span>


[!code-cshtml[Main](top-features-in-web-pages-2/samples/sample7.cshtml)]

<span data-ttu-id="1abea-225">下面是页上，当用户提交有效输入：</span><span class="sxs-lookup"><span data-stu-id="1abea-225">Here is the page when a user submits valid input:</span></span>

<span data-ttu-id="1abea-226">[![topSeven-valid-1](top-features-in-web-pages-2/_static/image8.png)](top-features-in-web-pages-2/_static/image7.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-226">[![topSeven-valid-1](top-features-in-web-pages-2/_static/image8.png)](top-features-in-web-pages-2/_static/image7.png)</span></span>

<span data-ttu-id="1abea-227">当用户提交它与必填字段留空，下面是页：</span><span class="sxs-lookup"><span data-stu-id="1abea-227">Here is the page when a user submits it with a required field left empty:</span></span>

<span data-ttu-id="1abea-228">[![topSeven-valid-2](top-features-in-web-pages-2/_static/image10.png)](top-features-in-web-pages-2/_static/image9.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-228">[![topSeven-valid-2](top-features-in-web-pages-2/_static/image10.png)](top-features-in-web-pages-2/_static/image9.png)</span></span>

<span data-ttu-id="1abea-229">下面是页上，当用户提交它与内的整数以外**信用额度**字段：</span><span class="sxs-lookup"><span data-stu-id="1abea-229">Here is the page when a user submits it with something other than an integer in the **Credits** field:</span></span>

<span data-ttu-id="1abea-230">[![topSeven-valid-3](top-features-in-web-pages-2/_static/image12.png)](top-features-in-web-pages-2/_static/image11.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-230">[![topSeven-valid-3](top-features-in-web-pages-2/_static/image12.png)](top-features-in-web-pages-2/_static/image11.png)</span></span>

<span data-ttu-id="1abea-231">有关详细信息，请参阅以下博客文章：</span><span class="sxs-lookup"><span data-stu-id="1abea-231">For more information, see the following blog posts:</span></span>

- <span data-ttu-id="1abea-232">[更新网页 v2 中的验证](http://mikepope.com/blog/DisplayBlog.aspx?permalink=2344)添加验证使用的基础知识`Validation`帮助器 （仅服务器端）</span><span class="sxs-lookup"><span data-stu-id="1abea-232">[Updated validation in Web Pages v2](http://mikepope.com/blog/DisplayBlog.aspx?permalink=2344) Basics of adding validation using the `Validation` helper (server-side only)</span></span>
- <span data-ttu-id="1abea-233">[更新网页 v2，第 2 部分中的验证](http://www.mikepope.com/blog/DisplayBlog.aspx?permalink=2347)添加客户端验证。</span><span class="sxs-lookup"><span data-stu-id="1abea-233">[Updated validation in Web Pages v2, Part 2](http://www.mikepope.com/blog/DisplayBlog.aspx?permalink=2347) Adding client-side validation.</span></span>
- <span data-ttu-id="1abea-234">[更新网页 v2，第 3 部分中的验证](http://mikepope.com/blog/DisplayBlog.aspx?permalink=2351)格式设置验证错误。</span><span class="sxs-lookup"><span data-stu-id="1abea-234">[Updated validation in Web Pages v2, Part 3](http://mikepope.com/blog/DisplayBlog.aspx?permalink=2351) Formatting validation errors.</span></span>

<a id="resmanagement"></a>
### <a name="registering-scripts-using-the-assets-manager"></a><span data-ttu-id="1abea-235">注册脚本使用的资产管理器</span><span class="sxs-lookup"><span data-stu-id="1abea-235">Registering Scripts Using the Assets Manager</span></span>

<span data-ttu-id="1abea-236">资产管理器是可用于在服务器代码中注册并呈现客户端脚本的新功能。</span><span class="sxs-lookup"><span data-stu-id="1abea-236">The assets manager is a new feature that you can use in server code to register and render client scripts.</span></span> <span data-ttu-id="1abea-237">如果你正在使用中 （如布局页、 内容页、 帮助器等） 在运行时合并成单个页面的多个文件的代码，此功能非常有用。</span><span class="sxs-lookup"><span data-stu-id="1abea-237">This feature is helpful when you are working with code from multiple files (such as layout pages, content pages, helpers, etc.) that are combined into a single page at run time.</span></span> <span data-ttu-id="1abea-238">资产经理进行协调源代码文件，以确保正确引用脚本文件和有效地在呈现的页上，而不考虑哪些代码文件从调用的或者调用的次数。</span><span class="sxs-lookup"><span data-stu-id="1abea-238">The assets manager coordinates the source files to make sure that script files are referenced correctly and efficiently on the rendered page, regardless of which code files they are called from or how many times they are called.</span></span> <span data-ttu-id="1abea-239">资产管理器还会呈现`<script>`标记在适当的位置，以便快速 （而无需下载在呈现时的脚本） 可以加载此页面，以避免如果脚本调用在呈现之前可以发生的错误为完成。</span><span class="sxs-lookup"><span data-stu-id="1abea-239">The assets manager also renders `<script>` tags in the right place so that the page can load quickly (without downloading scripts while rendering) and to avoid errors that can occur if scripts are called before rendering is complete.</span></span>

<span data-ttu-id="1abea-240">例如，假设你创建的自定义帮助程序调用一个 JavaScript 文件，并在内容页代码在以下三个不同的位置上调用此帮助器。</span><span class="sxs-lookup"><span data-stu-id="1abea-240">For example, suppose that you create a custom helper that calls a JavaScript file, and you call this helper at three different places in your content page code.</span></span> <span data-ttu-id="1abea-241">如果你不使用的资产管理器注册中的帮助程序，三个不同的调用脚本`<script>`所有指向同一个脚本文件将都显示在你呈现的页面的标记。</span><span class="sxs-lookup"><span data-stu-id="1abea-241">If you don't use the assets manager to register the script calls in the helper, three different `<script>` tags that all point to the same script file will appear in your rendered page.</span></span> <span data-ttu-id="1abea-242">另外，具体取决于 where`<script>`在呈现的页面中插入标记时，错误可能会发生如果脚本尝试以页完全加载之前访问某些页元素。</span><span class="sxs-lookup"><span data-stu-id="1abea-242">Plus, depending on where the `<script>` tags are inserted in the rendered page, errors may occur if the script tries to access certain page elements before the page fully loads.</span></span> <span data-ttu-id="1abea-243">如果你使用的资产管理器注册脚本，则将避免这些问题。</span><span class="sxs-lookup"><span data-stu-id="1abea-243">If you use the assets manager to register the script, you avoid these problems.</span></span>

<span data-ttu-id="1abea-244">你可以向的资产管理器注册脚本，通过执行此操作：</span><span class="sxs-lookup"><span data-stu-id="1abea-244">You can register a script with the assets manager by doing this:</span></span>

- <span data-ttu-id="1abea-245">在代码中，需要引用该脚本，调用`Assets.AddScript`方法。</span><span class="sxs-lookup"><span data-stu-id="1abea-245">In the code that needs to reference the script, call the `Assets.AddScript` method.</span></span>
- <span data-ttu-id="1abea-246">在 *\_SiteLayout*页上，调用`Assets.GetScripts`方法呈现`<script>`标记。</span><span class="sxs-lookup"><span data-stu-id="1abea-246">In a *\_SiteLayout* page, call the `Assets.GetScripts` method to render the `<script>` tags.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1abea-247">将调用`Assets.GetScripts`作为最后一项出现在`<body>`元素 *\_SiteLayout*页。</span><span class="sxs-lookup"><span data-stu-id="1abea-247">Put calls to `Assets.GetScripts` as the very last item in the `<body>` element of the *\_SiteLayout* page.</span></span> <span data-ttu-id="1abea-248">这有助于页面加载速度更快，并有助于避免脚本错误。</span><span class="sxs-lookup"><span data-stu-id="1abea-248">This helps the page load faster and can help avoid script errors.</span></span>

<span data-ttu-id="1abea-249">下面的示例显示的资产管理器的工作原理。</span><span class="sxs-lookup"><span data-stu-id="1abea-249">The following example shows how the assets manager works.</span></span> <span data-ttu-id="1abea-250">代码包含以下各项：</span><span class="sxs-lookup"><span data-stu-id="1abea-250">The code contains the following items:</span></span>

- <span data-ttu-id="1abea-251">名为自定义 helper `MakeNote`。</span><span class="sxs-lookup"><span data-stu-id="1abea-251">A custom helper named `MakeNote`.</span></span> <span data-ttu-id="1abea-252">此帮助器通过包装来呈现一个框内的字符串`div`元素在其周围的边框以及添加具有风格&quot;注意：&quot;到它。</span><span class="sxs-lookup"><span data-stu-id="1abea-252">This helper renders a string inside a box by wrapping a `div` element around it that's styled with a border and by adding &quot;Note:&quot; to it.</span></span> <span data-ttu-id="1abea-253">帮助器还会调用将运行时行为添加到注释的 JavaScript 文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-253">The helper also calls a JavaScript file that adds run-time behavior to the note.</span></span> <span data-ttu-id="1abea-254">而不是引用的脚本`<script>`标记，帮助程序通过调用注册的脚本`Assets.AddScript`。</span><span class="sxs-lookup"><span data-stu-id="1abea-254">Rather than reference the script with a `<script>` tag, the helper registers the script by calling `Assets.AddScript` .</span></span>
- <span data-ttu-id="1abea-255">一个 JavaScript 文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-255">A JavaScript file.</span></span> <span data-ttu-id="1abea-256">这是调用的帮助程序，该文件，同时可注意项目期间的字体大小暂时增加`mouseover`事件。</span><span class="sxs-lookup"><span data-stu-id="1abea-256">This is the file that's called by the helper, and it temporarily increases the font size of note items during a `mouseover` event.</span></span>
- <span data-ttu-id="1abea-257">内容页中，即在引用<em>\_SiteLayout</em>页上，呈现在正文中，某些内容，然后调用`MakeNote`帮助器。</span><span class="sxs-lookup"><span data-stu-id="1abea-257">A content page, which references the<em>\_SiteLayout</em> page, renders some content in the body, and then calls the `MakeNote` helper.</span></span>
- <span data-ttu-id="1abea-258">A  *\_SiteLayout*页。</span><span class="sxs-lookup"><span data-stu-id="1abea-258">A *\_SiteLayout* page.</span></span> <span data-ttu-id="1abea-259">此页会提供常见标头和页面布局结构。</span><span class="sxs-lookup"><span data-stu-id="1abea-259">This page provides a common header and a page layout structure.</span></span> <span data-ttu-id="1abea-260">它还包括调用`Assets.GetScripts`，即的资产管理器，如何呈现脚本调用在页中。</span><span class="sxs-lookup"><span data-stu-id="1abea-260">It also includes a call to `Assets.GetScripts`, which is how the assets manager renders script calls in a page.</span></span>

<span data-ttu-id="1abea-261">若要运行示例：</span><span class="sxs-lookup"><span data-stu-id="1abea-261">To run the sample:</span></span>

1. <span data-ttu-id="1abea-262">创建空 Web Pages 2 网站。</span><span class="sxs-lookup"><span data-stu-id="1abea-262">Create an empty Web Pages 2 website.</span></span> <span data-ttu-id="1abea-263">可使用 WebMatrix**空网站**此模板。</span><span class="sxs-lookup"><span data-stu-id="1abea-263">You can use the WebMatrix **Empty Site** template for this.</span></span>
2. <span data-ttu-id="1abea-264">创建名为的文件夹*脚本*站点中。</span><span class="sxs-lookup"><span data-stu-id="1abea-264">Create a folder named *Scripts* in the site.</span></span>
3. <span data-ttu-id="1abea-265">在*脚本*文件夹中，创建名为的文件*Test.js*，复制*Test.js*内容到该示例中，并保存该文件...</span><span class="sxs-lookup"><span data-stu-id="1abea-265">In the *Scripts* folder, create a file named *Test.js*, copy the *Test.js* content into it from the example, and save the file..</span></span>
4. <span data-ttu-id="1abea-266">创建名为的文件夹*应用\_代码*站点中。</span><span class="sxs-lookup"><span data-stu-id="1abea-266">Create a folder named *App\_Code* in the site.</span></span>
5. <span data-ttu-id="1abea-267">在*应用\_代码*文件夹中，创建名为的文件*Helpers.cshtml*、 执行它，请复制代码示例并将其保存在名为的文件夹中*应用\_代码*的根文件夹中。</span><span class="sxs-lookup"><span data-stu-id="1abea-267">In the *App\_Code* folder, create a file named *Helpers.cshtml*, copy the example code into it, and save it in a folder named *App\_Code* in the root folder.</span></span>
6. <span data-ttu-id="1abea-268">在站点的根文件夹中，创建名为的文件 *\_SiteLayout.cshtml，*将本示例复制到其中，并保存该文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-268">In the site's root folder, create a file named *\_SiteLayout.cshtml,* copy the example into it, and save the file.</span></span>
7. <span data-ttu-id="1abea-269">在网站根下创建名为的文件*ContentPage.cshtml*、 添加示例代码中，并将其保存。</span><span class="sxs-lookup"><span data-stu-id="1abea-269">In the site root, create a file named *ContentPage.cshtml*, add the example code, and save it.</span></span>
8. <span data-ttu-id="1abea-270">运行*内容页*在浏览器。</span><span class="sxs-lookup"><span data-stu-id="1abea-270">Run *ContentPage* in a browser.</span></span> <span data-ttu-id="1abea-271">传递给字符串`MakeNote`帮助器呈现为装箱的注意。</span><span class="sxs-lookup"><span data-stu-id="1abea-271">The string you passed to the `MakeNote` helper is rendered as a boxed note.</span></span>
9. <span data-ttu-id="1abea-272">将鼠标指针移注意。</span><span class="sxs-lookup"><span data-stu-id="1abea-272">Pass the mouse pointer over the note.</span></span> <span data-ttu-id="1abea-273">该脚本暂时增大注意的字号。</span><span class="sxs-lookup"><span data-stu-id="1abea-273">The script temporarily increases the font size of the note.</span></span>
10. <span data-ttu-id="1abea-274">查看所呈现的页面的源。</span><span class="sxs-lookup"><span data-stu-id="1abea-274">View the source of the rendered page.</span></span> <span data-ttu-id="1abea-275">由于其中放置到调用`Assets.GetScripts`，呈现`<script>`调用的标记*Test.js*是页面的正文中的最后一个项。</span><span class="sxs-lookup"><span data-stu-id="1abea-275">Because of where you placed the call to `Assets.GetScripts`, the rendered `<script>` tag that calls *Test.js* is the very last item in the body of the page.</span></span>

<span data-ttu-id="1abea-276">*Test.js*</span><span class="sxs-lookup"><span data-stu-id="1abea-276">*Test.js*</span></span>

[!code-javascript[Main](top-features-in-web-pages-2/samples/sample8.js)]

<span data-ttu-id="1abea-277">*Helpers.cshtml*</span><span class="sxs-lookup"><span data-stu-id="1abea-277">*Helpers.cshtml*</span></span>

[!code-cshtml[Main](top-features-in-web-pages-2/samples/sample9.cshtml)]

<span data-ttu-id="1abea-278">*\_SiteLayout.cshtml*</span><span class="sxs-lookup"><span data-stu-id="1abea-278">*\_SiteLayout.cshtml*</span></span>

[!code-html[Main](top-features-in-web-pages-2/samples/sample10.html)]

<span data-ttu-id="1abea-279">*ContentPage.cshtml*</span><span class="sxs-lookup"><span data-stu-id="1abea-279">*ContentPage.cshtml*</span></span>

[!code-cshtml[Main](top-features-in-web-pages-2/samples/sample11.cshtml)]

<span data-ttu-id="1abea-280">以下屏幕快照显示*ContentPage.cshtml*在浏览器中时将鼠标指针拖过注意：</span><span class="sxs-lookup"><span data-stu-id="1abea-280">The following screenshot shows *ContentPage.cshtml* in a browser when you hold the mouse pointer over the note:</span></span>

<span data-ttu-id="1abea-281">[![topSeven-resmgr-1](top-features-in-web-pages-2/_static/image14.png)](top-features-in-web-pages-2/_static/image13.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-281">[![topSeven-resmgr-1](top-features-in-web-pages-2/_static/image14.png)](top-features-in-web-pages-2/_static/image13.png)</span></span>

<a id="oauthsetup"></a>
### <a name="enabling-logins-from-facebook-and-other-sites-using-oauth-and-openid"></a><span data-ttu-id="1abea-282">启用从 Facebook 和其他站点使用 OAuth 和 OpenID 登录名</span><span class="sxs-lookup"><span data-stu-id="1abea-282">Enabling Logins from Facebook and Other Sites Using OAuth and OpenID</span></span>

<span data-ttu-id="1abea-283">Web Pages 2 提供有关成员身份和身份验证的增强的选项。</span><span class="sxs-lookup"><span data-stu-id="1abea-283">Web Pages 2 provides enhanced options for membership and authentication.</span></span> <span data-ttu-id="1abea-284">主要增强功能就是新[OAuth](http://oauth.net/)和[OpenID](http://openid.net/)提供程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-284">The main enhancement is that there are new [OAuth](http://oauth.net/) and [OpenID](http://openid.net/) providers.</span></span> <span data-ttu-id="1abea-285">使用这些提供程序，你可以到你的站点使用 Facebook、 Twitter、 Windows Live、 Google 和 Yahoo 从其现有凭据让用户登录。</span><span class="sxs-lookup"><span data-stu-id="1abea-285">Using these providers, you can let users log into your site using their existing credentials from Facebook, Twitter, Windows Live, Google, and Yahoo.</span></span> <span data-ttu-id="1abea-286">例如，若要使用 Facebook 帐户登录，用户可以只选择 Facebook 图标，将它们重定向到它们在其中输入他们的用户信息的 Facebook 登录页。</span><span class="sxs-lookup"><span data-stu-id="1abea-286">For example, to log in using a Facebook account, users can just choose a Facebook icon, which redirects them to the Facebook login page where they enter their user information.</span></span> <span data-ttu-id="1abea-287">它们然后可以将 Facebook 登录名与你的站点上其帐户关联。</span><span class="sxs-lookup"><span data-stu-id="1abea-287">They can then associate the Facebook login with their account on your site.</span></span> <span data-ttu-id="1abea-288">对网页成员资格功能的相关的增强与你的网站上的单个帐户是用户可以将多个登录名 （包括社交网络站点中的登录名） 相关联。</span><span class="sxs-lookup"><span data-stu-id="1abea-288">A related enhancement to the Web Pages membership features is that users can associate multiple logins (including logins from social networking sites) with a single account on your website.</span></span>

<span data-ttu-id="1abea-289">此图显示了从登录页**入门站点**模板，用户可以在其中选择一个 Facebook、 Twitter 或 Windows Live 图标，以允许使用外部帐户登录：</span><span class="sxs-lookup"><span data-stu-id="1abea-289">This image shows the Login page from the **Starter Site** template, where a user can choose a Facebook, Twitter, or Windows Live icon to enable logging in with an external account:</span></span>

<span data-ttu-id="1abea-290">[![topSeven-oauth-1](top-features-in-web-pages-2/_static/image16.png)](top-features-in-web-pages-2/_static/image15.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-290">[![topSeven-oauth-1](top-features-in-web-pages-2/_static/image16.png)](top-features-in-web-pages-2/_static/image15.png)</span></span>

<span data-ttu-id="1abea-291">你可以使用几行代码的 OAuth 和 OpenID 成员身份。</span><span class="sxs-lookup"><span data-stu-id="1abea-291">You can enable OAuth and OpenID membership using just a few lines of code.</span></span> <span data-ttu-id="1abea-292">您使用的方法和属性才能使用 OAuth 和 OpenID 提供程序位于`WebMatrix.Security.OAuthWebSecurity`类。</span><span class="sxs-lookup"><span data-stu-id="1abea-292">The methods and properties you use to work with the OAuth and OpenID providers are in the `WebMatrix.Security.OAuthWebSecurity` class.</span></span>

<span data-ttu-id="1abea-293">但是，而不是使用代码来启用其他站点中的登录名，若要开始使用新的提供程序的建议的方法是使用新**入门站点**附带 WebMatrix 2 Beta 的模板。</span><span class="sxs-lookup"><span data-stu-id="1abea-293">However, instead of using code to enable logins from other sites, a recommended way to get started with the new providers is to use the new **Starter Site** template that is included with WebMatrix 2 Beta.</span></span> <span data-ttu-id="1abea-294">**入门站点**模板包括完整的成员身份基础结构，登录页、 成员资格数据库，与所有的代码完成您需要允许用户登录到你使用本地凭据或来自另一个站点的站点.</span><span class="sxs-lookup"><span data-stu-id="1abea-294">The **Starter Site** template includes a full membership infrastructure, complete with a login page, a membership database, and all the code you need to let users log into your site using either local credentials or those from another site.</span></span>

#### <a name="how-to-enable-logins-using-the-oauth-and-openid-providers"></a><span data-ttu-id="1abea-295">如何启用使用 OAuth 和 OpenID 提供程序的登录名</span><span class="sxs-lookup"><span data-stu-id="1abea-295">How to Enable Logins using the OAuth and OpenID Providers</span></span>

<span data-ttu-id="1abea-296">本部分举例说明如何让用户从外部网站 （Facebook、 Twitter、 Windows Live、 Google 或 Yahoo） 登录到站点基于**入门站点**模板。</span><span class="sxs-lookup"><span data-stu-id="1abea-296">This section provides an example of how to let users log in from external sites (Facebook, Twitter, Windows Live, Google, or Yahoo) to a site that's based on the **Starter Site** template.</span></span> <span data-ttu-id="1abea-297">创建一个入门站点之后, 你执行此 （详细信息按照）：</span><span class="sxs-lookup"><span data-stu-id="1abea-297">After creating a starter site, you do this (details follow):</span></span>

- <span data-ttu-id="1abea-298">使用 OAuth 提供程序 （Facebook、 Twitter 和 Windows Live） 的站点，外部站点上创建应用程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-298">For the sites that use an OAuth provider (Facebook, Twitter, and Windows Live), create an application on the external site.</span></span> <span data-ttu-id="1abea-299">这样，你将需要以调用这些站点的登录功能的应用程序密钥。</span><span class="sxs-lookup"><span data-stu-id="1abea-299">This gives you application keys that you'll need in order to invoke the login feature for those sites.</span></span> <span data-ttu-id="1abea-300">对于使用 OpenID 提供程序 （Google、 Yahoo） 的站点，不需要创建应用程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-300">For sites that use an OpenID provider (Google, Yahoo), you do not have to create an application.</span></span> <span data-ttu-id="1abea-301">对于所有这些站点，必须具有一个帐户，以便在中记录并创建开发人员应用程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-301">For all of these sites, you must have an account in order to log in and to create developer applications.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1abea-302">Windows Live 应用程序只接受的实时工作网站，URL，因此不能用于本地网站 URL 测试登录名。</span><span class="sxs-lookup"><span data-stu-id="1abea-302">Windows Live applications only accept a live URL for a working website, so you cannot use a local website URL for testing logins.</span></span>
- <span data-ttu-id="1abea-303">编辑你的网站中的几个文件，才能指定适当的身份验证提供程序和提交登录名添加到你想要使用的站点。</span><span class="sxs-lookup"><span data-stu-id="1abea-303">Edit a few files in your website in order to specify the appropriate authentication provider and to submit a login to the site you want to use.</span></span>

<span data-ttu-id="1abea-304">**若要启用 Google 和 Yahoo 登录**:</span><span class="sxs-lookup"><span data-stu-id="1abea-304">**To enable Google and Yahoo logins**:</span></span>

1. <span data-ttu-id="1abea-305">在你的网站，编辑 *\_AppStart.cshtml*页上，在 Razor 代码块中的调用后添加以下两行代码`WebSecurity.InitializeDatabaseConnection`方法。</span><span class="sxs-lookup"><span data-stu-id="1abea-305">In your website, edit the *\_AppStart.cshtml* page and add the following two lines of code in the Razor code block after the call to the `WebSecurity.InitializeDatabaseConnection` method.</span></span> <span data-ttu-id="1abea-306">此代码使 Google 和 Yahoo OpenID 提供程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-306">This code enables both the Google and Yahoo OpenID providers.</span></span> 

    [!code-css[Main](top-features-in-web-pages-2/samples/sample12.css)]
2. <span data-ttu-id="1abea-307">在*~/Account/Login.cshtml*页上，从以下删除注释`<fieldset>`块的结尾处页面的标记。</span><span class="sxs-lookup"><span data-stu-id="1abea-307">In the *~/Account/Login.cshtml* page, remove the comments from the following `<fieldset>` block of markup near the end of the page.</span></span> <span data-ttu-id="1abea-308">若要取消注释的代码，删除`@*`前面或后面的字符`<fieldset>`块。</span><span class="sxs-lookup"><span data-stu-id="1abea-308">To uncomment the code, remove the `@*` characters that precede and follow the `<fieldset>` block.</span></span> <span data-ttu-id="1abea-309">生成的代码块如下所示：</span><span class="sxs-lookup"><span data-stu-id="1abea-309">The resulting code block looks like this:</span></span>

    [!code-html[Main](top-features-in-web-pages-2/samples/sample13.html)]
3. <span data-ttu-id="1abea-310">添加`<input>`的 Google 或 Yahoo 提供程序的元素`<fieldset>`组中*~/Account/Login.cshtml*页。</span><span class="sxs-lookup"><span data-stu-id="1abea-310">Add an `<input>` element for the Google or Yahoo provider to the `<fieldset>` group in the *~/Account/Login.cshtml* page.</span></span> <span data-ttu-id="1abea-311">已更新`<fieldset>`组具有`<input>`如以下示例中为 Google 和 Yahoo 如下所示的元素：</span><span class="sxs-lookup"><span data-stu-id="1abea-311">The updated `<fieldset>` group with `<input>` elements for both Google and Yahoo looks like the following example:</span></span> 

    [!code-html[Main](top-features-in-web-pages-2/samples/sample14.html)]
4. <span data-ttu-id="1abea-312">在*~/Account/AssociateServiceAccount.cshtml*页上，添加`<input>`Google 或 Yahoo 到元素`<fieldset>`组文件末尾附近。</span><span class="sxs-lookup"><span data-stu-id="1abea-312">In the *~/Account/AssociateServiceAccount.cshtml* page, add `<input>` elements for Google or Yahoo to the `<fieldset>` group near the end of the file.</span></span> <span data-ttu-id="1abea-313">你可以复制相同`<input>`刚添加到的元素`<fieldset>`主题中*~/Account/Login.cshtml*页。</span><span class="sxs-lookup"><span data-stu-id="1abea-313">You can copy the same `<input>` elements that you just added to the `<fieldset>` section in the *~/Account/Login.cshtml* page.</span></span> 

    <span data-ttu-id="1abea-314">*~/Account/AssociateServiceAccount.cshtml*可以使用入门站点模板中的页，如果你想要创建在其的用户可以将其他站点中的多个登录名关联与你的网站上的单个帐户页。</span><span class="sxs-lookup"><span data-stu-id="1abea-314">The *~/Account/AssociateServiceAccount.cshtml* page in the Starter Site template can be used if you want to create a page on which users can associate multiple logins from other sites with a single account on your website.</span></span>

<span data-ttu-id="1abea-315">现在，你可以测试 Google 和 Yahoo 登录名。</span><span class="sxs-lookup"><span data-stu-id="1abea-315">Now you can test Google and Yahoo logins.</span></span>

1. <span data-ttu-id="1abea-316">运行*default.cshtml*您的网站上，选择**登录**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-316">Run the *default.cshtml* page of your site and choose the **Log in** button.</span></span>
2. <span data-ttu-id="1abea-317">上*登录*页上，在**使用另一个服务以要求在登录**部分中，选择以下两者之一**Google**或**Yahoo**提交按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-317">On the *Login* page, in the **Use another service to log in** section, choose either the **Google** or **Yahoo** submit button.</span></span> <span data-ttu-id="1abea-318">此示例使用 Google 登录名。</span><span class="sxs-lookup"><span data-stu-id="1abea-318">This example uses the Google login.</span></span> 

    <span data-ttu-id="1abea-319">网页将请求重定向到 Google 登录页。</span><span class="sxs-lookup"><span data-stu-id="1abea-319">The web page redirects the request to the Google login page.</span></span>

    <span data-ttu-id="1abea-320">[![topSeven-oauth-6](top-features-in-web-pages-2/_static/image18.png)](top-features-in-web-pages-2/_static/image17.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-320">[![topSeven-oauth-6](top-features-in-web-pages-2/_static/image18.png)](top-features-in-web-pages-2/_static/image17.png)</span></span>
3. <span data-ttu-id="1abea-321">输入现有的 Google 帐户凭据。</span><span class="sxs-lookup"><span data-stu-id="1abea-321">Enter credentials for an existing Google account.</span></span>
4. <span data-ttu-id="1abea-322">如果出现要求你是否想要允许 Localhost 来使用帐户中的信息，请单击 Google**允许**。</span><span class="sxs-lookup"><span data-stu-id="1abea-322">If Google asks you whether you want to allow Localhost to use information from the account, click **Allow**.</span></span>

    <span data-ttu-id="1abea-323">代码使用 Google 令牌进行身份验证用户，然后在网站上返回到此页。</span><span class="sxs-lookup"><span data-stu-id="1abea-323">The code uses the Google token to authenticate the user, and then returns to this page on your website.</span></span> <span data-ttu-id="1abea-324">可以使用此页将其 Google 登录名与你的网站上的现有帐户相关联的用户或用户可以在注册你将使用的外部登录名相关联的站点上的新帐户。</span><span class="sxs-lookup"><span data-stu-id="1abea-324">This page lets users associate their Google login with an existing account on your website, or they can register a new account on your site to associate the external login with.</span></span>

    <span data-ttu-id="1abea-325">[![topSeven-oauth-5](top-features-in-web-pages-2/_static/image20.png)](top-features-in-web-pages-2/_static/image19.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-325">[![topSeven-oauth-5](top-features-in-web-pages-2/_static/image20.png)](top-features-in-web-pages-2/_static/image19.png)</span></span>
5. <span data-ttu-id="1abea-326">选择**关联**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-326">Choose the **Associate** button.</span></span> <span data-ttu-id="1abea-327">浏览器返回到应用程序的主页。</span><span class="sxs-lookup"><span data-stu-id="1abea-327">The browser returns to your application's home page.</span></span>

    <span data-ttu-id="1abea-328">[![topSeven-oauth-3](top-features-in-web-pages-2/_static/image22.png)](top-features-in-web-pages-2/_static/image21.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-328">[![topSeven-oauth-3](top-features-in-web-pages-2/_static/image22.png)](top-features-in-web-pages-2/_static/image21.png)</span></span>

    <span data-ttu-id="1abea-329">[![topSeven-oauth-3](top-features-in-web-pages-2/_static/image24.png)](top-features-in-web-pages-2/_static/image23.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-329">[![topSeven-oauth-3](top-features-in-web-pages-2/_static/image24.png)](top-features-in-web-pages-2/_static/image23.png)</span></span>

<span data-ttu-id="1abea-330">**若要启用 Facebook 登录名**:</span><span class="sxs-lookup"><span data-stu-id="1abea-330">**To enable Facebook logins**:</span></span>

1. <span data-ttu-id="1abea-331">转到[Facebook 开发人员站点](https://developers.facebook.com/apps)（如果尚未登录，则日志）。</span><span class="sxs-lookup"><span data-stu-id="1abea-331">Go to the [Facebook developers site](https://developers.facebook.com/apps) (log in if you're not already logged in).</span></span>
2. <span data-ttu-id="1abea-332">选择**创建新的应用程序**按钮，然后按照提示进行命名和创建新的应用程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-332">Choose the **Create New App** button, and then follow the prompts to name and create the new application.</span></span>
3. <span data-ttu-id="1abea-333">部分中**选择你的应用程序将如何集成到 Facebook**，选择**网站**部分。</span><span class="sxs-lookup"><span data-stu-id="1abea-333">In the section **Select how your app will integrate with Facebook**, choose the **Website** section.</span></span>
4. <span data-ttu-id="1abea-334">填写**站点 URL**字段替换你的站点的 URL (例如， [ `http://www.example.com` ](http://www.example.com))。</span><span class="sxs-lookup"><span data-stu-id="1abea-334">Fill in the **Site URL** field with the URL of your site (for example, [`http://www.example.com`](http://www.example.com)).</span></span> <span data-ttu-id="1abea-335">**域**字段是可选的; 可以使用此提供对于整个域的身份验证 (如*example.com*)。</span><span class="sxs-lookup"><span data-stu-id="1abea-335">The **Domain** field is optional; you can use this to provide authentication for an entire domain (such as *example.com*).</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1abea-336">如果你正在使用 URL 你本地计算机上运行站点诸如`http://localhost:12345`（其中数是本地端口号），则可以添加到此值**站点 URL**字段用于测试你的站点。</span><span class="sxs-lookup"><span data-stu-id="1abea-336">If you are running a site on your local computer with a URL like `http://localhost:12345` (where the number is a local port number), you can add this value to the **Site URL** field for testing your site.</span></span> <span data-ttu-id="1abea-337">但是，任何时候，只要你的本地站点更改的端口号，你将需要更新**站点 URL**你的应用程序的字段。</span><span class="sxs-lookup"><span data-stu-id="1abea-337">However, any time the port number of your local site changes, you will need to update the **Site URL** field of your application.</span></span>
5. <span data-ttu-id="1abea-338">选择**保存更改**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-338">Choose the **Save Changes** button.</span></span>
6. <span data-ttu-id="1abea-339">选择**应用**再次，选项卡，然后查看你的应用程序的起始页。</span><span class="sxs-lookup"><span data-stu-id="1abea-339">Choose the **Apps** tab again, and then view the start page for your application.</span></span>
7. <span data-ttu-id="1abea-340">复制**应用程序 ID**和**应用程序密钥**你的应用程序的值并将其粘贴到一个临时的文本文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-340">Copy the **App ID** and **App Secret** values for your application and paste them into a temporary text file.</span></span> <span data-ttu-id="1abea-341">网站代码中，会将这些值传递到 Facebook 提供程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-341">You will pass these values to the Facebook provider in your website code.</span></span>
8. <span data-ttu-id="1abea-342">退出 Facebook 开发人员网站。</span><span class="sxs-lookup"><span data-stu-id="1abea-342">Exit the Facebook developer site.</span></span>

<span data-ttu-id="1abea-343">现在你进行更改的两个页面中你的网站，以便用户将能够登录到使用其 Facebook 帐户的网站。</span><span class="sxs-lookup"><span data-stu-id="1abea-343">Now you make changes to two pages in your website so that users will able to log into the site using their Facebook accounts.</span></span>

1. <span data-ttu-id="1abea-344">在你的网站，编辑 *\_AppStart.cshtml*页上，取消注释的代码，为 Facebook OAuth 提供程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-344">In your website, edit the *\_AppStart.cshtml* page and uncomment the code for the Facebook OAuth provider.</span></span> <span data-ttu-id="1abea-345">取消注释的代码块如下所示：</span><span class="sxs-lookup"><span data-stu-id="1abea-345">The uncommented code block looks like the following:</span></span> 

    [!code-xml[Main](top-features-in-web-pages-2/samples/sample15.xml)]
2. <span data-ttu-id="1abea-346">复制**应用程序 ID**从 Facebook 应用程序的值作为值`consumerKey`（引号） 内的参数。</span><span class="sxs-lookup"><span data-stu-id="1abea-346">Copy the **App ID** value from the Facebook application as the value of the `consumerKey` parameter (inside the quotation marks).</span></span>
3. <span data-ttu-id="1abea-347">复制**应用程序密钥**值从 Facebook 应用程序作为`consumerSecret`参数值。</span><span class="sxs-lookup"><span data-stu-id="1abea-347">Copy **App Secret** value from the Facebook application as the `consumerSecret` parameter value.</span></span>
4. <span data-ttu-id="1abea-348">保存并关闭文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-348">Save and close the file.</span></span>
5. <span data-ttu-id="1abea-349">编辑*~/Account/Login.cshtml*页上，删除从注释`<fieldset>`页末尾附近的块。</span><span class="sxs-lookup"><span data-stu-id="1abea-349">Edit the *~/Account/Login.cshtml* page and remove the comments from the `<fieldset>` block near the end of the page.</span></span> <span data-ttu-id="1abea-350">若要取消注释的代码，删除`@*`前面或后面的字符`<fieldset>`块。</span><span class="sxs-lookup"><span data-stu-id="1abea-350">To uncomment the code, remove the `@*` characters that precede and follow the `<fieldset>` block.</span></span> <span data-ttu-id="1abea-351">注释的代码块中删除类似于以下内容：</span><span class="sxs-lookup"><span data-stu-id="1abea-351">The code block with comments removed looks like the following:</span></span> 

    [!code-html[Main](top-features-in-web-pages-2/samples/sample16.html)]
6. <span data-ttu-id="1abea-352">保存并关闭文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-352">Save and close the file.</span></span>

<span data-ttu-id="1abea-353">现在，你可以测试 Facebook 登录名。</span><span class="sxs-lookup"><span data-stu-id="1abea-353">Now you can test the Facebook login.</span></span>

1. <span data-ttu-id="1abea-354">运行站点的*default.cshtml*页上，选择**登录**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-354">Run the site's *default.cshtml* page and choose the **Login** button.</span></span>
2. <span data-ttu-id="1abea-355">上*登录*页上，在**使用另一个服务以要求在登录**部分中，选择**Facebook**图标。</span><span class="sxs-lookup"><span data-stu-id="1abea-355">On the *Login* page, in the **Use another service to log in** section, choose the **Facebook** icon.</span></span> 

    <span data-ttu-id="1abea-356">网页将请求重定向到 Facebook 登录页。</span><span class="sxs-lookup"><span data-stu-id="1abea-356">The web page redirects the request to the Facebook login page.</span></span>

    <span data-ttu-id="1abea-357">[![topSeven-oauth-2](top-features-in-web-pages-2/_static/image26.png)](top-features-in-web-pages-2/_static/image25.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-357">[![topSeven-oauth-2](top-features-in-web-pages-2/_static/image26.png)](top-features-in-web-pages-2/_static/image25.png)</span></span>
3. <span data-ttu-id="1abea-358">登录到 Facebook 帐户。</span><span class="sxs-lookup"><span data-stu-id="1abea-358">Log into a Facebook account.</span></span> 

    <span data-ttu-id="1abea-359">代码使用 Facebook 令牌你进行身份验证，然后返回到页你可以在其中将 Facebook 登录名使用网站的登录名相关联。</span><span class="sxs-lookup"><span data-stu-id="1abea-359">The code uses the Facebook token to authenticate you and then returns to a page where you can associate your Facebook login with your site's login.</span></span> <span data-ttu-id="1abea-360">你的用户名称或电子邮件地址填充到**电子邮件**窗体上字段。</span><span class="sxs-lookup"><span data-stu-id="1abea-360">Your user name or email address is filled into the **Email** field on the form.</span></span>

    <span data-ttu-id="1abea-361">[![topSeven-oauth-5](top-features-in-web-pages-2/_static/image28.png)](top-features-in-web-pages-2/_static/image27.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-361">[![topSeven-oauth-5](top-features-in-web-pages-2/_static/image28.png)](top-features-in-web-pages-2/_static/image27.png)</span></span>
4. <span data-ttu-id="1abea-362">选择**关联**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-362">Choose the **Associate** button.</span></span> 

    <span data-ttu-id="1abea-363">浏览器返回到主页页面并登录。</span><span class="sxs-lookup"><span data-stu-id="1abea-363">The browser returns to the home page and you are logged in.</span></span>

    <span data-ttu-id="1abea-364">[![topSeven-oauth-3](top-features-in-web-pages-2/_static/image30.png)](top-features-in-web-pages-2/_static/image29.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-364">[![topSeven-oauth-3](top-features-in-web-pages-2/_static/image30.png)](top-features-in-web-pages-2/_static/image29.png)</span></span>

<span data-ttu-id="1abea-365">**若要启用 Twitter 登录名：**</span><span class="sxs-lookup"><span data-stu-id="1abea-365">**To enable Twitter logins:**</span></span> 

1. <span data-ttu-id="1abea-366">浏览到[Twitter 开发人员网站](https://dev.twitter.com/)。</span><span class="sxs-lookup"><span data-stu-id="1abea-366">Browse to the [Twitter developers site](https://dev.twitter.com/).</span></span>
2. <span data-ttu-id="1abea-367">选择**创建应用**链接，然后登录到网站。</span><span class="sxs-lookup"><span data-stu-id="1abea-367">Choose the **Create an App** link and then log into the site.</span></span>
3. <span data-ttu-id="1abea-368">上**创建应用程序**窗体中，填写**名称**和**说明**字段。</span><span class="sxs-lookup"><span data-stu-id="1abea-368">On the **Create an Application** form, fill in the **Name** and **Description** fields.</span></span>
4. <span data-ttu-id="1abea-369">在**网站**字段中，输入你的站点的 URL (例如， [ `http://www.example.com` ](http://www.example.com))。</span><span class="sxs-lookup"><span data-stu-id="1abea-369">In the **WebSite** field, enter the URL of your site (for example, [`http://www.example.com`](http://www.example.com)).</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1abea-370">如果你正在测试你的本地站点 (使用如 URL `http://localhost:12345`)，Twitter 可能不接受该 URL。</span><span class="sxs-lookup"><span data-stu-id="1abea-370">If you're testing your site locally (using a URL like `http://localhost:12345`), Twitter might not accept the URL.</span></span> <span data-ttu-id="1abea-371">但是，你可能能够使用本地环回 IP 地址 (例如`http://127.0.0.1:12345`)。</span><span class="sxs-lookup"><span data-stu-id="1abea-371">However, you might be able to use the local loopback IP address (for example `http://127.0.0.1:12345`).</span></span> <span data-ttu-id="1abea-372">这可以简化测试本地应用程序的过程。</span><span class="sxs-lookup"><span data-stu-id="1abea-372">This simplifies the process of testing your application locally.</span></span> <span data-ttu-id="1abea-373">但是，每次你的本地网站的端口号更改，你将需要更新**网站**你的应用程序的字段。</span><span class="sxs-lookup"><span data-stu-id="1abea-373">However, every time the port number of your local site changes, you'll need to update the **WebSite** field of your application.</span></span>
5. <span data-ttu-id="1abea-374">在**回调 URL**字段中，输入你希望用户在登录后到 Twitter 到返回的网站中的页的 URL。</span><span class="sxs-lookup"><span data-stu-id="1abea-374">In the **Callback URL** field, enter a URL for the page in your website that you want users to return to after logging into Twitter.</span></span> <span data-ttu-id="1abea-375">例如，若要将用户发送到 （它将识别其登录的状态） 的入门站点主页上，输入中输入的相同 URL**网站**字段。</span><span class="sxs-lookup"><span data-stu-id="1abea-375">For example, to send users to the home page of the Starter Site (which will recognize their logged-in status), enter the same URL that you entered in the **WebSite** field.</span></span>
6. <span data-ttu-id="1abea-376">接受条款，然后选择**创建 Twitter 应用程序**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-376">Accept the terms and choose the **Create your Twitter application** button.</span></span>
7. <span data-ttu-id="1abea-377">上**我的应用程序**登陆页，选择你创建的应用程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-377">On the **My Applications** landing page, choose the application you created.</span></span>
8. <span data-ttu-id="1abea-378">上**详细信息**选项卡上，滚动到底部，选择**创建我访问令牌**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-378">On the **Details** tab, scroll to the bottom and choose the **Create My Access Token** button.</span></span>
9. <span data-ttu-id="1abea-379">上**详细信息**选项卡上，复制**使用者密钥**和**使用者机密**你的应用程序的值并将其粘贴到一个临时的文本文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-379">On the **Details** tab, copy the **Consumer Key** and **Consumer Secret** values for your application and paste them into a temporary text file.</span></span> <span data-ttu-id="1abea-380">网站代码中，会将这些值传递到 Twitter 提供程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-380">You'll pass these values to the Twitter provider in your website code.</span></span>
10. <span data-ttu-id="1abea-381">退出 Twitter 网站。</span><span class="sxs-lookup"><span data-stu-id="1abea-381">Exit the Twitter site.</span></span>

<span data-ttu-id="1abea-382">现在你进行更改的两个页面中你的网站，以便用户能够登录到使用其 Twitter 帐户的网站。</span><span class="sxs-lookup"><span data-stu-id="1abea-382">Now you make changes to two pages in your website so that users will be able to log into the site using their Twitter accounts.</span></span>

1. <span data-ttu-id="1abea-383">在你的网站，编辑 *\_AppStart.cshtml*页上，取消注释的代码，Twitter OAuth 提供程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-383">In your website, edit the *\_AppStart.cshtml* page and uncomment the code for the Twitter OAuth provider.</span></span> <span data-ttu-id="1abea-384">取消注释的代码块如下所示：</span><span class="sxs-lookup"><span data-stu-id="1abea-384">The uncommented code block looks like this:</span></span> 

    [!code-csharp[Main](top-features-in-web-pages-2/samples/sample17.cs)]
2. <span data-ttu-id="1abea-385">复制**使用者密钥**值形式的值的 Twitter 应用程序从`consumerKey`（引号） 内的参数。</span><span class="sxs-lookup"><span data-stu-id="1abea-385">Copy the **Consumer Key** value from the Twitter application as the value of the `consumerKey` parameter (inside the quotation marks).</span></span>
3. <span data-ttu-id="1abea-386">复制**使用者机密**值形式的值的 Twitter 应用程序从`consumerSecret`参数。</span><span class="sxs-lookup"><span data-stu-id="1abea-386">Copy the **Consumer Secret** value from the Twitter application as the value of the `consumerSecret` parameter.</span></span>
4. <span data-ttu-id="1abea-387">保存并关闭文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-387">Save and close the file.</span></span>
5. <span data-ttu-id="1abea-388">编辑*~/Account/Login.cshtml*页上，删除从注释`<fieldset>`页末尾附近的块。</span><span class="sxs-lookup"><span data-stu-id="1abea-388">Edit the *~/Account/Login.cshtml* page and remove the comments from the `<fieldset>` block near the end of the page.</span></span> <span data-ttu-id="1abea-389">若要取消注释的代码，删除`@*`前面或后面的字符`<fieldset>`块。</span><span class="sxs-lookup"><span data-stu-id="1abea-389">To uncomment the code, remove the `@*` characters that precede and follow the `<fieldset>` block.</span></span> <span data-ttu-id="1abea-390">注释的代码块中删除类似于以下内容：</span><span class="sxs-lookup"><span data-stu-id="1abea-390">The code block with comments removed looks like the following:</span></span> 

    [!code-html[Main](top-features-in-web-pages-2/samples/sample18.html)]
6. <span data-ttu-id="1abea-391">保存并关闭文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-391">Save and close the file.</span></span>

<span data-ttu-id="1abea-392">现在，你可以测试 Twitter 登录。</span><span class="sxs-lookup"><span data-stu-id="1abea-392">Now you can test the Twitter login.</span></span>

1. <span data-ttu-id="1abea-393">运行*default.cshtml*您的网站上，选择**登录**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-393">Run the *default.cshtml* page of your site and choose the **Login** button.</span></span>
2. <span data-ttu-id="1abea-394">上*登录*页上，在**使用另一个服务以要求在登录**部分中，选择**Twitter**图标。</span><span class="sxs-lookup"><span data-stu-id="1abea-394">On the *Login* page, in the **Use another service to log in** section, choose the **Twitter** icon.</span></span> 

    <span data-ttu-id="1abea-395">网页将请求重定向到 Twitter 登录页为您创建的应用程序中。</span><span class="sxs-lookup"><span data-stu-id="1abea-395">The web page redirects the request to a Twitter login page for the application you created.</span></span>

    <span data-ttu-id="1abea-396">[![topSeven-oauth-4](top-features-in-web-pages-2/_static/image32.png)](top-features-in-web-pages-2/_static/image31.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-396">[![topSeven-oauth-4](top-features-in-web-pages-2/_static/image32.png)](top-features-in-web-pages-2/_static/image31.png)</span></span>
3. <span data-ttu-id="1abea-397">登录到 Twitter 帐户。</span><span class="sxs-lookup"><span data-stu-id="1abea-397">Log into a Twitter account.</span></span>
4. <span data-ttu-id="1abea-398">该代码使用 Twitter 令牌来验证用户身份，然后返回到页你可以将关联您的登录名与你网站的帐户。</span><span class="sxs-lookup"><span data-stu-id="1abea-398">The code uses the Twitter token to authenticate the user and then returns you to a page where you can associate your login with your website account.</span></span> <span data-ttu-id="1abea-399">您的名称或电子邮件地址填充到**电子邮件**窗体上字段。</span><span class="sxs-lookup"><span data-stu-id="1abea-399">Your name or email address is filled into the **Email** field on the form.</span></span>

    <span data-ttu-id="1abea-400">[![topSeven-oauth-5](top-features-in-web-pages-2/_static/image34.png)](top-features-in-web-pages-2/_static/image33.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-400">[![topSeven-oauth-5](top-features-in-web-pages-2/_static/image34.png)](top-features-in-web-pages-2/_static/image33.png)</span></span>
5. <span data-ttu-id="1abea-401">选择**关联**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-401">Choose the **Associate** button.</span></span> 

    <span data-ttu-id="1abea-402">浏览器返回到主页页面并登录。</span><span class="sxs-lookup"><span data-stu-id="1abea-402">The browser returns to the home page and you are logged in.</span></span>

    <span data-ttu-id="1abea-403">[![topSeven-oauth-3](top-features-in-web-pages-2/_static/image36.png)](top-features-in-web-pages-2/_static/image35.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-403">[![topSeven-oauth-3](top-features-in-web-pages-2/_static/image36.png)](top-features-in-web-pages-2/_static/image35.png)</span></span>

<a id="maphelper"></a>
### <a name="adding-maps-using-the-maps-helper"></a><span data-ttu-id="1abea-404">添加使用地图帮助程序图</span><span class="sxs-lookup"><span data-stu-id="1abea-404">Adding Maps Using the Maps Helper</span></span>

<span data-ttu-id="1abea-405">Web Pages 2 包括添加到 ASP.NET Web 帮助程序库，后者是网页站点的加载项包。</span><span class="sxs-lookup"><span data-stu-id="1abea-405">Web Pages 2 includes additions to the ASP.NET Web Helpers Library, which is a package of add-ins for a Web Pages site.</span></span> <span data-ttu-id="1abea-406">其中一种是由提供的映射组件`Microsoft.Web.Helpers.Maps`类。</span><span class="sxs-lookup"><span data-stu-id="1abea-406">One of these is a mapping component provided by the `Microsoft.Web.Helpers.Maps` class.</span></span> <span data-ttu-id="1abea-407">你可以使用`Maps`类以生成基于地址或一组的经度和纬度坐标的地图。</span><span class="sxs-lookup"><span data-stu-id="1abea-407">You can use the `Maps` class to generate maps based either on an address or on a set of longitude and latitude coordinates.</span></span> <span data-ttu-id="1abea-408">`Maps`类，可以直接在包括必应、 Google、 MapQuest 和 Yahoo 常用映射引擎调用。</span><span class="sxs-lookup"><span data-stu-id="1abea-408">The `Maps` class lets you call directly into popular map engines including Bing, Google, MapQuest, and Yahoo.</span></span>

<span data-ttu-id="1abea-409">若要使用新`Maps`类在你的网站，你必须首先安装 Web 帮助程序库的版本 2。</span><span class="sxs-lookup"><span data-stu-id="1abea-409">To use the new `Maps` class in your website, you must first install the version 2 of the Web Helpers Library.</span></span> <span data-ttu-id="1abea-410">若要执行此操作，请转到安装的当前发行的版的说明[ASP.NET Web 帮助程序库](https://go.microsoft.com/fwlink/?LinkId=202889#webhelpers)并安装版本 2。</span><span class="sxs-lookup"><span data-stu-id="1abea-410">To do this, go to the instructions for installing the currently released version of the [ASP.NET Web Helpers Library](https://go.microsoft.com/fwlink/?LinkId=202889#webhelpers) and install version 2.</span></span>

<span data-ttu-id="1abea-411">将映射添加到页的步骤都相同的调用而与所映射引擎。</span><span class="sxs-lookup"><span data-stu-id="1abea-411">The steps for adding mapping to a page are the same regardless of which of the map engines you call.</span></span> <span data-ttu-id="1abea-412">只需添加对您的映射页面的 JavaScript 文件引用并将呈现的调用`<script>`在你的页面上标记。</span><span class="sxs-lookup"><span data-stu-id="1abea-412">You just add a JavaScript file reference to your mapping page and then add a call that renders the `<script>` tags on your page.</span></span> <span data-ttu-id="1abea-413">然后在映射页面中上, 调用你想要使用映射引擎。</span><span class="sxs-lookup"><span data-stu-id="1abea-413">Then on your mapping page, call the map engine you want to use.</span></span>

<span data-ttu-id="1abea-414">下面的示例演示如何创建将基于一个地址，结构图呈现一个页，并且将基于经度和纬度坐标结构图呈现的另一页。</span><span class="sxs-lookup"><span data-stu-id="1abea-414">The following example shows how to create a page that renders a map based on an address, and another page that renders a map based on longitude and latitude coordinates.</span></span> <span data-ttu-id="1abea-415">地址映射示例使用 Google 地图和坐标映射示例使用必应地图。</span><span class="sxs-lookup"><span data-stu-id="1abea-415">The address mapping example uses Google Maps, and the coordinate mapping example uses Bing Maps.</span></span> <span data-ttu-id="1abea-416">请注意在代码中的以下元素：</span><span class="sxs-lookup"><span data-stu-id="1abea-416">Note the following elements in the code:</span></span>

- <span data-ttu-id="1abea-417">调用`Assets.AddScript`顶部的两个映射页。</span><span class="sxs-lookup"><span data-stu-id="1abea-417">The call to `Assets.AddScript` at the top of the two mapping pages.</span></span> <span data-ttu-id="1abea-418">此方法将引用添加到*jquery 1.6.2.min.js*附带的文件**入门站点**模板和所需`Maps`类。</span><span class="sxs-lookup"><span data-stu-id="1abea-418">This method adds a reference to the *jquery-1.6.2.min.js* file that is included with the **Starter Site** template and that's required by the `Maps` class.</span></span>
- <span data-ttu-id="1abea-419">调用`Assets.GetScripts`布局文件中的方法。</span><span class="sxs-lookup"><span data-stu-id="1abea-419">The call to the `Assets.GetScripts` method in the layout file.</span></span> <span data-ttu-id="1abea-420">此方法呈现`<script>`的两个映射页面的标记。</span><span class="sxs-lookup"><span data-stu-id="1abea-420">This method renders the `<script>` tag on the two mapping pages.</span></span>
- <span data-ttu-id="1abea-421">调用`@Maps.GetGoogleHtml`和`@Maps.GetBingHtml`中的映射页的方法。</span><span class="sxs-lookup"><span data-stu-id="1abea-421">The call to the `@Maps.GetGoogleHtml` and the `@Maps.GetBingHtml` methods in the mapping pages.</span></span> <span data-ttu-id="1abea-422">若要将地址映射，你必须传递地址字符串。</span><span class="sxs-lookup"><span data-stu-id="1abea-422">To map an address, you must pass an address string.</span></span> <span data-ttu-id="1abea-423">若要映射坐标时，必须传递经度和纬度坐标。</span><span class="sxs-lookup"><span data-stu-id="1abea-423">To map coordinates, you must pass longitude and latitude coordinates.</span></span> <span data-ttu-id="1abea-424">对于 Bing 地图引擎中，你还必须传递一个密钥 (可通过在注册获取免费[必应地图开发人员站点](https://www.microsoft.com/maps/developers/web.aspx))。</span><span class="sxs-lookup"><span data-stu-id="1abea-424">For the Bing Maps engine, you must also pass a key (which you get for free by signing up at the [Bing Maps Developers site](https://www.microsoft.com/maps/developers/web.aspx)).</span></span> <span data-ttu-id="1abea-425">对于其他映射引擎方法的工作原理类似的方式 (`@Maps.GetYahooHtml`， `@Maps.GetMapQuestHtml`)。</span><span class="sxs-lookup"><span data-stu-id="1abea-425">The methods for the other map engines work in a similar way (`@Maps.GetYahooHtml`, `@Maps.GetMapQuestHtml`).</span></span>

<span data-ttu-id="1abea-426">若要创建映射页：</span><span class="sxs-lookup"><span data-stu-id="1abea-426">To create mapping pages:</span></span>

1. <span data-ttu-id="1abea-427">创建基于网站**入门站点**模板。</span><span class="sxs-lookup"><span data-stu-id="1abea-427">Create a website based on the **Starter Site** template.</span></span>
2. <span data-ttu-id="1abea-428">创建名为的文件*MapAddress.cshtml*站点的根目录中。</span><span class="sxs-lookup"><span data-stu-id="1abea-428">Create a file named *MapAddress.cshtml* in the root of the site.</span></span> <span data-ttu-id="1abea-429">此页将生成基于传递给它的地址映射。</span><span class="sxs-lookup"><span data-stu-id="1abea-429">This page will generate a map based on an address that you pass to it.</span></span>
3. <span data-ttu-id="1abea-430">将以下代码复制到文件中，覆盖现有的内容。</span><span class="sxs-lookup"><span data-stu-id="1abea-430">Copy the following code into the file, overwriting the existing content.</span></span> 

    [!code-cshtml[Main](top-features-in-web-pages-2/samples/sample19.cshtml)]
4. <span data-ttu-id="1abea-431">创建名为的文件 *\_MapLayout.cshtml*站点的根目录中。</span><span class="sxs-lookup"><span data-stu-id="1abea-431">Create a file named *\_MapLayout.cshtml* in the root of the site.</span></span> <span data-ttu-id="1abea-432">此页将两个映射页的布局页。</span><span class="sxs-lookup"><span data-stu-id="1abea-432">This page will be the layout page for the two mapping pages.</span></span>
5. <span data-ttu-id="1abea-433">将以下代码复制到文件中，覆盖现有的内容。</span><span class="sxs-lookup"><span data-stu-id="1abea-433">Copy the following code into the file, overwriting the existing content.</span></span> 

    [!code-html[Main](top-features-in-web-pages-2/samples/sample20.html)]
6. <span data-ttu-id="1abea-434">创建名为的文件*MapCoordinates.cshtml*站点的根目录中。</span><span class="sxs-lookup"><span data-stu-id="1abea-434">Create a file named *MapCoordinates.cshtml* in the root of the site.</span></span> <span data-ttu-id="1abea-435">此页将生成基于一组坐标传递给它的映射。</span><span class="sxs-lookup"><span data-stu-id="1abea-435">This page will generate a map based on a set of coordinates that you pass to it.</span></span>
7. <span data-ttu-id="1abea-436">将以下代码复制到文件中，覆盖现有的内容。</span><span class="sxs-lookup"><span data-stu-id="1abea-436">Copy the following code into the file, overwriting the existing content.</span></span> 

    [!code-cshtml[Main](top-features-in-web-pages-2/samples/sample21.cshtml)]

<span data-ttu-id="1abea-437">若要测试映射页面：</span><span class="sxs-lookup"><span data-stu-id="1abea-437">To test your mapping pages:</span></span>

1. <span data-ttu-id="1abea-438">运行页面*MapAddress.cshtml*文件。</span><span class="sxs-lookup"><span data-stu-id="1abea-438">Run the page *MapAddress.cshtml* file.</span></span>
2. <span data-ttu-id="1abea-439">输入包括街道地址、 状态或自治区和邮政编码的完整地址字符串，然后选择**Map It**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-439">Enter a full address string including a street address, state or province, and postal code, and then choose the **Map It** button.</span></span> <span data-ttu-id="1abea-440">呈现地图页面，从 Google 地图：</span><span class="sxs-lookup"><span data-stu-id="1abea-440">The page renders a map from Google Maps:</span></span> 

    <span data-ttu-id="1abea-441">[![topseven-maphelper-1](top-features-in-web-pages-2/_static/image38.png)](top-features-in-web-pages-2/_static/image37.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-441">[![topseven-maphelper-1](top-features-in-web-pages-2/_static/image38.png)](top-features-in-web-pages-2/_static/image37.png)</span></span>
3. <span data-ttu-id="1abea-442">查找的特定位置的纬度和经度坐标集。</span><span class="sxs-lookup"><span data-stu-id="1abea-442">Find a set of latitude and longitude coordinates for a specific location.</span></span>
4. <span data-ttu-id="1abea-443">运行页面*MapCoordinates.cshtml*。</span><span class="sxs-lookup"><span data-stu-id="1abea-443">Run the page *MapCoordinates.cshtml*.</span></span> <span data-ttu-id="1abea-444">输入坐标，然后选择**Map It**按钮。</span><span class="sxs-lookup"><span data-stu-id="1abea-444">Enter the coordinates and then choose the **Map It** button.</span></span> <span data-ttu-id="1abea-445">将呈现的地图页面从 Bing 地图：</span><span class="sxs-lookup"><span data-stu-id="1abea-445">The page renders a map from Bing Maps:</span></span> 

    <span data-ttu-id="1abea-446">[![topseven-maphelper-2](top-features-in-web-pages-2/_static/image40.png)](top-features-in-web-pages-2/_static/image39.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-446">[![topseven-maphelper-2](top-features-in-web-pages-2/_static/image40.png)](top-features-in-web-pages-2/_static/image39.png)</span></span>

<a id="sidebyside"></a>
### <a name="running-web-pages-applications-side-by-side"></a><span data-ttu-id="1abea-447">运行 Web 页面应用程序并行</span><span class="sxs-lookup"><span data-stu-id="1abea-447">Running Web Pages Applications Side by Side</span></span>

<span data-ttu-id="1abea-448">Web Pages 2 添加了运行并行应用程序的功能。</span><span class="sxs-lookup"><span data-stu-id="1abea-448">Web Pages 2 adds the ability to run applications side by side.</span></span> <span data-ttu-id="1abea-449">这使你能够继续用于运行 Web Pages 1 应用程序、 生成新的 Web Pages 2 应用程序，和在同一台计算机上运行所有这些。</span><span class="sxs-lookup"><span data-stu-id="1abea-449">This lets you continue to run your Web Pages 1 applications, build new Web Pages 2 applications, and run all of them on the same computer.</span></span>

<span data-ttu-id="1abea-450">下面是在使用 WebMatrix 安装 Web Pages 2 Beta 时要记住一些事项：</span><span class="sxs-lookup"><span data-stu-id="1abea-450">Here are some things to remember when you install the Web Pages 2 Beta with WebMatrix:</span></span>

- <span data-ttu-id="1abea-451">默认情况下，现有的 Web 页面应用程序将在你的计算机上运行为版本 2 的应用程序。</span><span class="sxs-lookup"><span data-stu-id="1abea-451">By default, existing Web Pages applications will run as version 2 applications on your computer.</span></span> <span data-ttu-id="1abea-452">（版本 2 的程序集安装到 GAC 中并且将自动使用。）</span><span class="sxs-lookup"><span data-stu-id="1abea-452">(The assemblies for version 2 are installed in the GAC and will be used automatically.)</span></span>
- <span data-ttu-id="1abea-453">如果你想要运行使用网页版本 1 （而不是默认值，如下所示的以前的点） 的站点，你可以配置站点以执行该操作。</span><span class="sxs-lookup"><span data-stu-id="1abea-453">If you want to run a site using Web Pages version 1 (instead of the default, as in the previous point), you can configure the site to do that.</span></span> <span data-ttu-id="1abea-454">如果你的站点还没有*web.config*文件在站点的根目录中，创建一个新然后将以下 XML 复制到其中，覆盖现有的内容。</span><span class="sxs-lookup"><span data-stu-id="1abea-454">If your site doesn't already have a *web.config* file in the root of the site, create a new one and copy the following XML into it, overwriting the existing content.</span></span> <span data-ttu-id="1abea-455">如果该站点已包含*web.config*文件中，添加`<appSettings>`到以下所示的元素`<configuration>`部分。</span><span class="sxs-lookup"><span data-stu-id="1abea-455">If the site already contains a *web.config* file, add an `<appSettings>` element like the following one to the `<configuration>` section.</span></span>

    [!code-xml[Main](top-features-in-web-pages-2/samples/sample22.xml)]
  <span data-ttu-id="1abea-456">-如果不指定中的版本*web.config*文件，站点部署为版本 2 站点。</span><span class="sxs-lookup"><span data-stu-id="1abea-456">\`- If you do not specify a version in the *web.config* file, a site is deployed as a version 2 site.</span></span> <span data-ttu-id="1abea-457">(版本 2 程序集复制到*bin*已部署的站点中的文件夹。)</span><span class="sxs-lookup"><span data-stu-id="1abea-457">(The version 2 assemblies are copied to the *bin* folder in the deployed site.)</span></span>
- <span data-ttu-id="1abea-458">Web Matrix 2 Beta 包括在站点中的网页版本 2 程序集的版本中使用的站点模板创建的新应用程序*bin*文件夹。</span><span class="sxs-lookup"><span data-stu-id="1abea-458">New applications that you create using the site templates in Web Matrix version 2 Beta include the Web Pages version 2 assemblies in the site's *bin* folder.</span></span>

<span data-ttu-id="1abea-459">一般情况下，你可以始终控制哪个版本的 Web 页面以通过使用 NuGet 将相应的程序集安装到站点的使用与您的网站*bin*文件夹。</span><span class="sxs-lookup"><span data-stu-id="1abea-459">In general, you can always control which version of Web Pages to use with your site by using NuGet to install the appropriate assemblies into the site's *bin* folder.</span></span> <span data-ttu-id="1abea-460">若要查找程序包，请访问[NuGet.org](http://NuGet.org)。</span><span class="sxs-lookup"><span data-stu-id="1abea-460">To find packages, visit [NuGet.org](http://NuGet.org).</span></span>

<a id="mobile"></a>
### <a name="rendering-pages-for-mobile-devices"></a><span data-ttu-id="1abea-461">为移动设备中呈现页</span><span class="sxs-lookup"><span data-stu-id="1abea-461">Rendering Pages for Mobile Devices</span></span>

<span data-ttu-id="1abea-462">Web Pages 2 中，可以在移动或其他设备上创建自定义呈现内容的显示。</span><span class="sxs-lookup"><span data-stu-id="1abea-462">Web Pages 2 lets you create custom displays for rendering content on mobile or other devices.</span></span>

<span data-ttu-id="1abea-463">`System.Web.WebPages`命名空间包含允许您使用的显示模式的以下类： `DefaultDisplayMode`， `DisplayInfo`，和`DisplayModes`。</span><span class="sxs-lookup"><span data-stu-id="1abea-463">The `System.Web.WebPages` namespace contains the following classes that let you work with display modes: `DefaultDisplayMode`, `DisplayInfo`, and `DisplayModes`.</span></span> <span data-ttu-id="1abea-464">你可以直接使用这些类，并且可以编写呈现特定设备的正确输出的代码。</span><span class="sxs-lookup"><span data-stu-id="1abea-464">You can use these classes directly and write code that renders the right output for specific devices.</span></span>

<span data-ttu-id="1abea-465">或者，你可以创建使用如下的文件命名模式的特定于设备的页面： <em>FileName。</em><em>移动</em><em>.cshtml</em>。</span><span class="sxs-lookup"><span data-stu-id="1abea-465">Alternatively, you can create device-specific pages by using a file-naming pattern like this: <em>FileName.</em><em>Mobile</em><em>.cshtml</em>.</span></span> <span data-ttu-id="1abea-466">例如，可以创建两个版本的页上，一个名为<em>MyFile.cshtml</em>和一个名为<em>MyFile.Mobile.cshtml</em>。</span><span class="sxs-lookup"><span data-stu-id="1abea-466">For example, you can create two versions of a page, one named <em>MyFile.cshtml</em> and one named <em>MyFile.Mobile.cshtml</em>.</span></span> <span data-ttu-id="1abea-467">在运行的时，当移动设备请求<em>MyFile.cshtml</em>，网页将从内容呈现<em>MyFile.Mobile.cshtml</em>。</span><span class="sxs-lookup"><span data-stu-id="1abea-467">At run time, when a mobile device requests <em>MyFile.cshtml</em>, Web Pages renders the content from <em>MyFile.Mobile.cshtml</em>.</span></span> <span data-ttu-id="1abea-468">否则为<em>MyFile.cshtml</em>呈现。</span><span class="sxs-lookup"><span data-stu-id="1abea-468">Otherwise, <em>MyFile.cshtml</em> is rendered.</span></span>

<span data-ttu-id="1abea-469">下面的示例演示如何通过添加移动设备的内容页中启用移动呈现。</span><span class="sxs-lookup"><span data-stu-id="1abea-469">The following example shows how to enable mobile rendering by adding a content page for mobile devices.</span></span> <span data-ttu-id="1abea-470">*Page1.cshtml*包含内容以及导航侧边栏。</span><span class="sxs-lookup"><span data-stu-id="1abea-470">*Page1.cshtml* contains content plus a navigation sidebar.</span></span> <span data-ttu-id="1abea-471">*Page1.Mobile.cshtml*包含相同的内容，但省略侧栏。</span><span class="sxs-lookup"><span data-stu-id="1abea-471">*Page1.Mobile.cshtml* contains the same content, but omits the sidebar.</span></span>

<span data-ttu-id="1abea-472">若要生成并运行的代码示例：</span><span class="sxs-lookup"><span data-stu-id="1abea-472">To build and run the code sample:</span></span>

1. <span data-ttu-id="1abea-473">在网页网站中，创建名为的文件*Page1.cshtml*和复制*Page1.cshtml*内容到该示例中。</span><span class="sxs-lookup"><span data-stu-id="1abea-473">In a Web Pages site, create a file named *Page1.cshtml* and copy the *Page1.cshtml* content into it from the example.</span></span>
2. <span data-ttu-id="1abea-474">创建名为的文件*Page1.Mobile.cshtml*和复制*Page1.Mobile.cshtml*内容到该示例中。</span><span class="sxs-lookup"><span data-stu-id="1abea-474">Create a file named *Page1.Mobile.cshtml* and copy the *Page1.Mobile.cshtml* content into it from the example.</span></span> <span data-ttu-id="1abea-475">请注意该页面的移动版本省略更好地呈现较小屏幕上的导航部分。</span><span class="sxs-lookup"><span data-stu-id="1abea-475">Notice that the mobile version of the page omits the navigation section for better rendering on a smaller screen.</span></span>
3. <span data-ttu-id="1abea-476">运行桌面浏览器并浏览到*Page1.cshtml*。</span><span class="sxs-lookup"><span data-stu-id="1abea-476">Run a desktop browser and browse to *Page1.cshtml*.</span></span>
4. <span data-ttu-id="1abea-477">运行移动浏览器 （或移动设备仿真程序） 并浏览到*Page1.cshtml*。</span><span class="sxs-lookup"><span data-stu-id="1abea-477">Run a mobile browser (or a mobile device emulator) and browse to *Page1.cshtml*.</span></span> <span data-ttu-id="1abea-478">请注意这一次 Web 页呈现页面的移动版本。</span><span class="sxs-lookup"><span data-stu-id="1abea-478">Notice that this time Web Pages renders the mobile version of the page.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="1abea-479">若要测试移动页，可以使用在台式计算机运行的移动设备模拟器。</span><span class="sxs-lookup"><span data-stu-id="1abea-479">To test mobile pages, you can use a mobile device simulator that runs on a desktop computer.</span></span> <span data-ttu-id="1abea-480">此工具允许你测试 web 页面，因为它们将显示在移动设备上 （即，通常通过小得多显示区域）。</span><span class="sxs-lookup"><span data-stu-id="1abea-480">This tool lets you test web pages as they would look on mobile devices (that is, typically with a much smaller display area).</span></span> <span data-ttu-id="1abea-481">模拟器的一个示例是[用户代理切换器外接程序](http://addons.mozilla.org/en-us/firefox/addon/user-agent-switcher/)对 Mozilla Firefox，它可让你模拟从桌面版本的 Firefox 的各种移动浏览器。</span><span class="sxs-lookup"><span data-stu-id="1abea-481">One example of a simulator is the [User Agent Switcher add-on](http://addons.mozilla.org/en-us/firefox/addon/user-agent-switcher/) for Mozilla Firefox, which lets you emulate various mobile browsers from a desktop version of Firefox.</span></span>

<span data-ttu-id="1abea-482">*Page1.cshtml*</span><span class="sxs-lookup"><span data-stu-id="1abea-482">*Page1.cshtml*</span></span>

[!code-html[Main](top-features-in-web-pages-2/samples/sample23.html)]

<span data-ttu-id="1abea-483">*Page1.Mobile.cshtml*</span><span class="sxs-lookup"><span data-stu-id="1abea-483">*Page1.Mobile.cshtml*</span></span>

[!code-html[Main](top-features-in-web-pages-2/samples/sample24.html)]

<span data-ttu-id="1abea-484">*Page1.cshtml*在桌面浏览器中呈现：</span><span class="sxs-lookup"><span data-stu-id="1abea-484">*Page1.cshtml* rendered in a desktop browser:</span></span>

<span data-ttu-id="1abea-485">[![topseven-displaymodes-1](top-features-in-web-pages-2/_static/image42.png)](top-features-in-web-pages-2/_static/image41.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-485">[![topseven-displaymodes-1](top-features-in-web-pages-2/_static/image42.png)](top-features-in-web-pages-2/_static/image41.png)</span></span>

<span data-ttu-id="1abea-486">*Page1.Mobile.cshtml* Firefox 浏览器中的 Apple iPhone 模拟器视图中显示。</span><span class="sxs-lookup"><span data-stu-id="1abea-486">*Page1.Mobile.cshtml* displayed in an Apple iPhone simulator view in the Firefox browser.</span></span> <span data-ttu-id="1abea-487">即使该请求是*Page1.cshtml*，应用程序呈现*Page1.Mobile.cshtml*。</span><span class="sxs-lookup"><span data-stu-id="1abea-487">Even though the request is to *Page1.cshtml*, the application renders *Page1.Mobile.cshtml*.</span></span>

<span data-ttu-id="1abea-488">[![topseven-displaymodes-2](top-features-in-web-pages-2/_static/image44.png)](top-features-in-web-pages-2/_static/image43.png)</span><span class="sxs-lookup"><span data-stu-id="1abea-488">[![topseven-displaymodes-2](top-features-in-web-pages-2/_static/image44.png)](top-features-in-web-pages-2/_static/image43.png)</span></span>

<a id="resources"></a>
## <a name="additional-resources"></a><span data-ttu-id="1abea-489">其他资源</span><span class="sxs-lookup"><span data-stu-id="1abea-489">Additional Resources</span></span>

### <a name="aspnet-web-pages-1-resources"></a><span data-ttu-id="1abea-490">ASP.NET Web Pages 1 资源</span><span class="sxs-lookup"><span data-stu-id="1abea-490">ASP.NET Web Pages 1 Resources</span></span>

> [!NOTE]
> <span data-ttu-id="1abea-491">大多数 Web Pages 1 编程和 API 资源仍适用于 Web Pages 2。</span><span class="sxs-lookup"><span data-stu-id="1abea-491">Most Web Pages 1 programming and API resources still apply to Web Pages 2.</span></span>

- [<span data-ttu-id="1abea-492">ASP.NET Web Pages 编程简介</span><span class="sxs-lookup"><span data-stu-id="1abea-492">Introduction to ASP.NET Web Pages Programming</span></span>](https://go.microsoft.com/fwlink/?LinkId=202890)

### <a name="webmatrix-resources"></a><span data-ttu-id="1abea-493">WebMatrix 资源</span><span class="sxs-lookup"><span data-stu-id="1abea-493">WebMatrix Resources</span></span>

- [<span data-ttu-id="1abea-494">WebMatrix 2 新增功能</span><span class="sxs-lookup"><span data-stu-id="1abea-494">WebMatrix 2 What's New</span></span>](http://webmatrix.com/next)
- [<span data-ttu-id="1abea-495">Microsoft WebMatrix Site</span><span class="sxs-lookup"><span data-stu-id="1abea-495">Microsoft WebMatrix Site</span></span>](https://go.microsoft.com/fwlink/?LinkID=195076)
- <span data-ttu-id="1abea-496">[开始使用 Microsoft WebMatrix 的 Web 开发](https://msdn.microsoft.com/en-us/library/hh145669(v=VS.99).aspx)（包括一个完整的示例 Web 页面应用程序）</span><span class="sxs-lookup"><span data-stu-id="1abea-496">[Starting Web Development with Microsoft WebMatrix](https://msdn.microsoft.com/en-us/library/hh145669(v=VS.99).aspx)(includes a full-length sample Web Pages application)</span></span>
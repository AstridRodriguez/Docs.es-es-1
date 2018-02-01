---
uid: mvc/overview/releases/whats-new-in-aspnet-mvc-52
title: "' S New en ASP.NET MVC 5.2 | Documentos de Microsoft"
author: microsoft
description: 
ms.author: aspnetcontent
manager: wpickett
ms.date: 12/25/2014
ms.topic: article
ms.assetid: 97972587-2720-48b4-b158-f35f2e855fbf
ms.technology: dotnet-mvc
ms.prod: .net-framework
msc.legacyurl: /mvc/overview/releases/whats-new-in-aspnet-mvc-52
msc.type: authoredcontent
ms.openlocfilehash: 94f6131fdb86d1694c1f563c5f6806f119c71266
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/10/2017
---
<a name="whats-new-in-aspnet-mvc-52"></a><span data-ttu-id="bf076-102">' S New en ASP.NET MVC 5.2</span><span class="sxs-lookup"><span data-stu-id="bf076-102">What’s New in ASP.NET MVC 5.2</span></span>
====================
<span data-ttu-id="bf076-103">por [Microsoft](https://github.com/microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf076-103">by [Microsoft](https://github.com/microsoft)</span></span>

<span data-ttu-id="bf076-104">Este tema describe lo que es nuevo en ASP.NET MVC 5.2, [Microsoft.AspNet.MVC 5.2.2](#52) y [Beta de ASP.NET MVC 5.2.3](#mvc523Beta)</span><span class="sxs-lookup"><span data-stu-id="bf076-104">This topic describes what's new for ASP.NET MVC 5.2, [Microsoft.AspNet.MVC 5.2.2](#52) and [ASP.NET MVC 5.2.3 Beta](#mvc523Beta)</span></span>

- [<span data-ttu-id="bf076-105">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="bf076-105">Software Requirements</span></span>](#softRequire)
- [<span data-ttu-id="bf076-106">Descarga</span><span class="sxs-lookup"><span data-stu-id="bf076-106">Download</span></span>](#download)
- [<span data-ttu-id="bf076-107">Documentación</span><span class="sxs-lookup"><span data-stu-id="bf076-107">Documentation</span></span>](#documentation)
- [<span data-ttu-id="bf076-108">Nuevas características de ASP.NET MVC 5.2</span><span class="sxs-lookup"><span data-stu-id="bf076-108">New Features in ASP.NET MVC 5.2</span></span>](#new-features)

    - [<span data-ttu-id="bf076-109">Atributo mejoras de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="bf076-109">Attribute routing improvements</span></span>](#attributerouting)
- [<span data-ttu-id="bf076-110">Problemas conocidos y los cambios recientes</span><span class="sxs-lookup"><span data-stu-id="bf076-110">Known Issues and Breaking Changes</span></span>](#knownbreakingchanges)
- [<span data-ttu-id="bf076-111">Correcciones de errores</span><span class="sxs-lookup"><span data-stu-id="bf076-111">Bug Fixes</span></span>](#bug-fixes)
- [<span data-ttu-id="bf076-112">Microsoft.AspNet.MVC 5.2.2</span><span class="sxs-lookup"><span data-stu-id="bf076-112">Microsoft.AspNet.MVC 5.2.2</span></span>](#52)

<a id="softRequire"></a>
## <a name="software-requirements"></a><span data-ttu-id="bf076-113">Requisitos de software</span><span class="sxs-lookup"><span data-stu-id="bf076-113">Software Requirements</span></span>

- <span data-ttu-id="bf076-114">Visual Studio 2012: Descargar [Web ASP.NET y herramientas 2013.1 para Visual Studio 2012](https://go.microsoft.com/fwlink/?LinkId=390062).</span><span class="sxs-lookup"><span data-stu-id="bf076-114">Visual Studio 2012: Download [ASP.NET and Web Tools 2013.1 for Visual Studio 2012](https://go.microsoft.com/fwlink/?LinkId=390062).</span></span>
- <span data-ttu-id="bf076-115">Visual Studio 2013: Descargar [Visual Studio 2013 Update](https://go.microsoft.com/fwlink/?LinkId=390064) o superior.</span><span class="sxs-lookup"><span data-stu-id="bf076-115">Visual Studio 2013: Download [Visual Studio 2013 Update](https://go.microsoft.com/fwlink/?LinkId=390064) or higher.</span></span> <span data-ttu-id="bf076-116">Esta actualización es necesaria para editar las vistas de Razor de ASP.NET MVC 5.2.</span><span class="sxs-lookup"><span data-stu-id="bf076-116">This update is needed for editing ASP.NET MVC 5.2 Razor Views.</span></span>

<a id="download"></a>
## <a name="download"></a><span data-ttu-id="bf076-117">Descargar</span><span class="sxs-lookup"><span data-stu-id="bf076-117">Download</span></span>

<span data-ttu-id="bf076-118">Las características en tiempo de ejecución se publican como paquetes de NuGet en la Galería de NuGet.</span><span class="sxs-lookup"><span data-stu-id="bf076-118">The runtime features are released as NuGet packages on the NuGet gallery.</span></span> <span data-ttu-id="bf076-119">Siguen todos los paquetes en tiempo de ejecución el [control de versiones semántico](http://semver.org/) especificación.</span><span class="sxs-lookup"><span data-stu-id="bf076-119">All the runtime packages follow the [Semantic Versioning](http://semver.org/) specification.</span></span> <span data-ttu-id="bf076-120">El paquete más reciente de ASP.NET MVC 5.2 tiene la siguiente versión: "5.2.0".</span><span class="sxs-lookup"><span data-stu-id="bf076-120">The latest ASP.NET MVC 5.2 package has the following version: "5.2.0".</span></span> <span data-ttu-id="bf076-121">Puede instalar o actualizar estos paquetes a través de [NuGet](http://www.nuget.org/packages/Microsoft.AspNet.Mvc/).</span><span class="sxs-lookup"><span data-stu-id="bf076-121">You can install or update these packages through [NuGet](http://www.nuget.org/packages/Microsoft.AspNet.Mvc/).</span></span> <span data-ttu-id="bf076-122">La versión también incluye paquetes localizados correspondientes en NuGet.</span><span class="sxs-lookup"><span data-stu-id="bf076-122">The release also includes corresponding localized packages on NuGet.</span></span>

<span data-ttu-id="bf076-123">Puede instalar o actualizar a los paquetes de NuGet publicados mediante la consola de administrador de paquetes de NuGet:</span><span class="sxs-lookup"><span data-stu-id="bf076-123">You can install or update to the released NuGet packages by using the NuGet Package Manager Console:</span></span>

<span data-ttu-id="bf076-124">Instalar paquete Microsoft.AspNet.Mvc-versión 5.2.0</span><span class="sxs-lookup"><span data-stu-id="bf076-124">Install-Package Microsoft.AspNet.Mvc -Version 5.2.0</span></span>

<a id="documentation"></a>
## <a name="documentation"></a><span data-ttu-id="bf076-125">Documentación</span><span class="sxs-lookup"><span data-stu-id="bf076-125">Documentation</span></span>

<span data-ttu-id="bf076-126">Tutoriales y otra información sobre ASP.NET MVC 5.2 están disponibles desde el sitio web ASP.NET ([https://www.asp.net/mvc](../../index.md)).</span><span class="sxs-lookup"><span data-stu-id="bf076-126">Tutorials and other information about ASP.NET MVC 5.2 are available from the ASP.NET web site ([https://www.asp.net/mvc](../../index.md)).</span></span>

<a id="new-features"></a>
## <a name="new-features-in-aspnet-mvc-52"></a><span data-ttu-id="bf076-127">Nuevas características de ASP.NET MVC 5.2</span><span class="sxs-lookup"><span data-stu-id="bf076-127">New Features in ASP.NET MVC 5.2</span></span>

<a id="attributerouting"></a>
### <a name="attribute-routing-improvements"></a><span data-ttu-id="bf076-128">Atributo mejoras de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="bf076-128">Attribute routing improvements</span></span>

<span data-ttu-id="bf076-129">Ruta de atributo ahora proporciona un punto de extensibilidad denominado IDirectRouteProvider, lo que permite un control total sobre el proceso de detección y configurar rutas de atributo.</span><span class="sxs-lookup"><span data-stu-id="bf076-129">Attribute Routing now provides an extensibility point called IDirectRouteProvider, which allows full control over how attribute routes are discovered and configured.</span></span> <span data-ttu-id="bf076-130">Un IDirectRouteProvider es responsable de proporcionar una lista de acciones y controladores junto con la información de ruta asociada para especificar exactamente qué configuración de enrutamiento se deseada para esas acciones.</span><span class="sxs-lookup"><span data-stu-id="bf076-130">An IDirectRouteProvider is responsible for providing a list of actions and controllers along with associated route information to specify exactly what routing configuration is desired for those actions.</span></span> <span data-ttu-id="bf076-131">Al llamar a MapAttributes/MapHttpAttributeRoutes, se puede especificar una implementación de IDirectRouteProvider.</span><span class="sxs-lookup"><span data-stu-id="bf076-131">An IDirectRouteProvider implementation may be specified when calling MapAttributes/MapHttpAttributeRoutes.</span></span>

<span data-ttu-id="bf076-132">Personalizar IDirectRouteProvider será más fácil extendiendo nuestra implementación de forma predeterminada, DefaultDirectRouteProvider.</span><span class="sxs-lookup"><span data-stu-id="bf076-132">Customizing IDirectRouteProvider will be easiest by extending our default implementation, DefaultDirectRouteProvider.</span></span> <span data-ttu-id="bf076-133">Esta clase proporciona métodos virtuales reemplazables independientes para cambiar la lógica de detección de atributos, crear entradas de ruta y detectar el prefijo de ruta y el prefijo de área.</span><span class="sxs-lookup"><span data-stu-id="bf076-133">This class provides separate overridable virtual methods to change the logic for discovering attributes, creating route entries, and discovering route prefix and area prefix.</span></span>

<span data-ttu-id="bf076-134">Con el nuevo atributo enrutamiento de extensibilidad de IDirectRouteProvider, un usuario podría hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bf076-134">With the new attribute routing extensibility of IDirectRouteProvider, a user could do the following:</span></span>

1. <span data-ttu-id="bf076-135">Admite la herencia de rutas de atributo.</span><span class="sxs-lookup"><span data-stu-id="bf076-135">Support Inheritance of attribute routes.</span></span> <span data-ttu-id="bf076-136">Por ejemplo, en el siguiente escenario Blog y el almacén de controladores están utilizando una convención de ruta de atributo definido por el BaseController.</span><span class="sxs-lookup"><span data-stu-id="bf076-136">For example, in the following scenario Blog and Store controllers are using an attribute route convention that is defined by the BaseController.</span></span> 

    [!code-csharp[Main](whats-new-in-aspnet-mvc-52/samples/sample1.cs)]
2. <span data-ttu-id="bf076-137">Generar automáticamente los nombres de ruta para las rutas de atributo.</span><span class="sxs-lookup"><span data-stu-id="bf076-137">Automatically generate route names for attribute routes.</span></span> 

    [!code-csharp[Main](whats-new-in-aspnet-mvc-52/samples/sample2.cs)]
3. <span data-ttu-id="bf076-138">Modifique los prefijos de ruta en un lugar central antes de que las rutas se agregan a la tabla de rutas.</span><span class="sxs-lookup"><span data-stu-id="bf076-138">Modify route prefixes in one central place before the routes get added to the route table.</span></span>
4. <span data-ttu-id="bf076-139">Filtrar los controladores en el que desea que el enrutamiento de atributo para buscar.</span><span class="sxs-lookup"><span data-stu-id="bf076-139">Filter out the controllers on which you want the attribute routing to look for.</span></span> <span data-ttu-id="bf076-140">Esperamos blog en 3 y 4 pronto.</span><span class="sxs-lookup"><span data-stu-id="bf076-140">We hope to blog on 3 and 4 soon.</span></span>

### <a name="facebook-fixes-for-changed-api-surface"></a><span data-ttu-id="bf076-141">Facebook correcciones para la superficie de la API modificada</span><span class="sxs-lookup"><span data-stu-id="bf076-141">Facebook fixes for changed API surface</span></span>

<span data-ttu-id="bf076-142">El paquete de MVC Facebook [se interrumpió](https://aspnetwebstack.codeplex.com/workitem/list/advanced?keyword=&amp;status=All&amp;type=All&amp;priority=All&amp;release=v5.2%20RC&amp;assignedTo=All&amp;component=Facebook&amp;sortField=AssignedTo&amp;sortDirection=Ascending&amp;page=0&amp;reasonClosed=All) debido a algunos cambios en la API realizados por Facebook.</span><span class="sxs-lookup"><span data-stu-id="bf076-142">The MVC Facebook package [was broken](https://aspnetwebstack.codeplex.com/workitem/list/advanced?keyword=&amp;status=All&amp;type=All&amp;priority=All&amp;release=v5.2%20RC&amp;assignedTo=All&amp;component=Facebook&amp;sortField=AssignedTo&amp;sortDirection=Ascending&amp;page=0&amp;reasonClosed=All) due to few API changes made by Facebook.</span></span> <span data-ttu-id="bf076-143">También vamos a lanzar un nuevo paquete de Facebook (Microsoft.AspNet.Facebook 1.0.0) para solucionar estos problemas.</span><span class="sxs-lookup"><span data-stu-id="bf076-143">We are also releasing a new Facebook package (Microsoft.AspNet.Facebook 1.0.0) to fix these issues.</span></span>

<a id="knownbreakingchanges"></a>
## <a name="known-issues-and-breaking-changes"></a><span data-ttu-id="bf076-144">Problemas conocidos y los cambios recientes</span><span class="sxs-lookup"><span data-stu-id="bf076-144">Known Issues and Breaking Changes</span></span>

### <a name="scaffolding-mvcweb-api-into-a-project-with-520-packages-results-in-512-packages-for-ones-that-dont-already-exist-in-the-project"></a><span data-ttu-id="bf076-145">Scaffolding MVC o Web API en un proyecto con 5.2.0 resultados de paquetes en 5.1.2 paquetes para los que ya no existen en el proyecto</span><span class="sxs-lookup"><span data-stu-id="bf076-145">Scaffolding MVC/Web API into a project with 5.2.0 packages results in 5.1.2 packages for ones that don't already exist in the project</span></span>

<span data-ttu-id="bf076-146">Actualizar paquetes de NuGet para ASP.NET MVC 5.2.0 no actualizar las herramientas de Visual Studio como scaffolding de ASP.NET o la plantilla de proyecto de aplicación Web ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="bf076-146">Updating NuGet packages for ASP.NET MVC 5.2.0 does not update the Visual Studio tools such as ASP.NET scaffolding or the ASP.NET Web Application project template.</span></span> <span data-ttu-id="bf076-147">Usan la versión anterior de los paquetes en tiempo de ejecución ASP.NET (por ejemplo, 5.1.2 en Update 2).</span><span class="sxs-lookup"><span data-stu-id="bf076-147">They use the previous version of the ASP.NET runtime packages (e.g. 5.1.2 in Update 2).</span></span> <span data-ttu-id="bf076-148">Como resultado, el scaffolding de ASP.NET se instalará la versión anterior (por ejemplo, 5.1.2 en Update 2) de los paquetes necesarios, si aún no están disponibles en los proyectos.</span><span class="sxs-lookup"><span data-stu-id="bf076-148">As a result, the ASP.NET scaffolding will install the previous version (e.g. 5.1.2 in Update 2) of the required packages, if they are not already available in your projects.</span></span> <span data-ttu-id="bf076-149">Sin embargo, el scaffolding de ASP.NET en Visual Studio 2013 RTM o Update 1 sobrescribir los paquetes más recientes de los proyectos.</span><span class="sxs-lookup"><span data-stu-id="bf076-149">However, the ASP.NET scaffolding in Visual Studio 2013 RTM or Update 1 does not overwrite the latest packages in your projects.</span></span> <span data-ttu-id="bf076-150">Si utiliza ASP.NET scaffolding después de actualizar los paquetes de los proyectos Web API 2.2 o 5.2 de MVC de ASP.NET, asegúrese de que las versiones de API Web y MVC de ASP.NET son coherentes.</span><span class="sxs-lookup"><span data-stu-id="bf076-150">If you use ASP.NET scaffolding after updating the packages of your projects to Web API 2.2 or ASP.NET MVC 5.2, make sure the versions of Web API and ASP.NET MVC are consistent.</span></span>

### <a name="microsoftjqueryunobtrusivevalidation-nuget-package-installation-fails-because-it-is-unable-to-find-a-version-of-microsoftjqueryunobtrusivevalidation-compatible-to-jquery-141"></a><span data-ttu-id="bf076-151">Se produce un error en la instalación del paquete de Microsoft.jQuery.Unobtrusive.Validation NuGet porque no puede encontrar una versión de Microsoft.jQuery.Unobtrusive.Validation compatible con jQuery 1.4.1</span><span class="sxs-lookup"><span data-stu-id="bf076-151">Microsoft.jQuery.Unobtrusive.Validation NuGet package installation fails because it is unable to find a version of Microsoft.jQuery.Unobtrusive.Validation compatible to jQuery 1.4.1</span></span>

<span data-ttu-id="bf076-152">Microsoft.jQuery.Unobtrusive.Validation requiere jQuery &gt;= 1.8 y jQuery.Validation &gt;= 1.8.</span><span class="sxs-lookup"><span data-stu-id="bf076-152">Microsoft.jQuery.Unobtrusive.Validation requires jQuery &gt;=1.8 and jQuery.Validation &gt;=1.8.</span></span> <span data-ttu-id="bf076-153">But,jQuery.Validation (1.8) necesita jQuery (&#8805; 1.3.2 &amp; &amp; &#8804; 1.6).</span><span class="sxs-lookup"><span data-stu-id="bf076-153">But,jQuery.Validation (1.8) needs jQuery (&#8805; 1.3.2 &amp;&amp; &#8804; 1.6).</span></span> <span data-ttu-id="bf076-154">Por este motivo, cuando NuGet instala los JQuery 1.8 y jQuery.Validation 1.8 al mismo tiempo, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="bf076-154">Because of this, when NuGet installs the JQuery 1.8 and jQuery.Validation 1.8 at the same time, it fails.</span></span> <span data-ttu-id="bf076-155">Cuando ve este problema, simplemente puede actualizar la versión de jQuery.Validation a &gt; =  [1.8.0.1](https://www.nuget.org/packages/jQuery.Validation/1.8.0.1) que tiene el límite de jQuery fijo en primer lugar, debe poder instalar Microsoft.jQuery.Unobtrusive.Validation.</span><span class="sxs-lookup"><span data-stu-id="bf076-155">When you see this issue, you can simply update the version of jQuery.Validation to &gt;= [1.8.0.1](https://www.nuget.org/packages/jQuery.Validation/1.8.0.1) which has the jQuery cap fixed first, you should be able to install Microsoft.jQuery.Unobtrusive.Validation.</span></span>

### <a name="the-jqueryvalidation-nuget-package-version-1130-does-not-recognize-some-international-email-addresses"></a><span data-ttu-id="bf076-156">Jquery. Versión de paquete de nuget de validación 1.13.0 no reconoce algunas direcciones de correo electrónico internacionales</span><span class="sxs-lookup"><span data-stu-id="bf076-156">The jquery.Validation nuget package version 1.13.0 does not recognize some international email addresses</span></span>

<span data-ttu-id="bf076-157">versión de paquete de nuget jQuery.Validation 1.11.1 es la última versión conocida que reconoce las siguientes direcciones de correo electrónico válida.</span><span class="sxs-lookup"><span data-stu-id="bf076-157">jQuery.Validation nuget package version 1.11.1 is the last known version which recognizes following valid email addresses.</span></span> <span data-ttu-id="bf076-158">Pueden que las versiones posteriores no pueda reconocerlos.</span><span class="sxs-lookup"><span data-stu-id="bf076-158">Any later versions might not be able to recognize them.</span></span> <span data-ttu-id="bf076-159">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bf076-159">For example:</span></span>

<span data-ttu-id="bf076-160">Estándar de internacionalización de dirección (EAI) de correo electrónico (p. ej., [&#29992; &#25143;@domain.com ](mailto:&#29992;&#25143;@domain.com))</span><span class="sxs-lookup"><span data-stu-id="bf076-160">E-Mail Address Internationalization (EAI) standard (e.g., [&#29992;&#25143;@domain.com](mailto:&#29992;&#25143;@domain.com))</span></span>   
 <span data-ttu-id="bf076-161">EAI + identificadores de recursos internacionalizado (IRI) (p. ej., [&#29992; &#25143; @&#1076; &#1086; &#1084; &#1077; &#1085;. &#1088; &#1092; ](mailto:&#29992;&#25143;@&#1076;&#1086;&#1084;&#1077;&#1085;.&#1088;&#1092;))</span><span class="sxs-lookup"><span data-stu-id="bf076-161">EAI + Internationalized Resource Identifiers (IRIs) (eg., [&#29992;&#25143;@&#1076;&#1086;&#1084;&#1077;&#1085;.&#1088;&#1092;](mailto:&#29992;&#25143;@&#1076;&#1086;&#1084;&#1077;&#1085;.&#1088;&#1092;))</span></span>

<span data-ttu-id="bf076-162">El problema se notifica en [https://github.com/jzaefferer/jquery-validation/issues/1222](https://github.com/jzaefferer/jquery-validation/issues/1222)</span><span class="sxs-lookup"><span data-stu-id="bf076-162">The issue is reported at [https://github.com/jzaefferer/jquery-validation/issues/1222](https://github.com/jzaefferer/jquery-validation/issues/1222)</span></span>

### <a name="syntax-highlighting-for-razor-views-in-visual-studio-2013"></a><span data-ttu-id="bf076-163">Resaltado de sintaxis para las vistas de Razor en Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="bf076-163">Syntax Highlighting for Razor Views in Visual Studio 2013</span></span>

<span data-ttu-id="bf076-164">Si actualiza a ASP.NET MVC 5.2 sin actualizar Visual Studio 2013, no obtendrá la compatibilidad con el editor de Visual Studio para resaltar la sintaxis mientras edita las vistas de Razor.</span><span class="sxs-lookup"><span data-stu-id="bf076-164">If you update to ASP.NET MVC 5.2 without updating Visual Studio 2013, you will not get Visual Studio editor support for syntax highlighting while editing the Razor views.</span></span> <span data-ttu-id="bf076-165">Debe actualizar Visual Studio 2013 para obtener esta compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="bf076-165">You will need to update Visual Studio 2013 to get this support.</span></span>

<a id="bug-fixes"></a>
## <a name="bug-fixes-and-minor-feature-updates"></a><span data-ttu-id="bf076-166">Correcciones de errores y actualizaciones de características secundarias</span><span class="sxs-lookup"><span data-stu-id="bf076-166">Bug Fixes and Minor feature updates</span></span>

<span data-ttu-id="bf076-167">Esta versión también incluye varias correcciones de errores y una característica secundaria actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="bf076-167">This release also includes several bug fixes and minor feature updates.</span></span> <span data-ttu-id="bf076-168">Puede encontrar la lista completa aquí:</span><span class="sxs-lookup"><span data-stu-id="bf076-168">You can find the complete list here:</span></span>

- [<span data-ttu-id="bf076-169">paquete 5.2</span><span class="sxs-lookup"><span data-stu-id="bf076-169">5.2 package</span></span>](https://aspnetwebstack.codeplex.com/workitem/list/advanced?keyword=&amp;status=Closed&amp;type=All&amp;priority=All&amp;release=v5.2%20RC&amp;assignedTo=All&amp;component=MVC&amp;sortField=AssignedTo&amp;sortDirection=Ascending&amp;page=0&amp;reasonClosed=Fixed)

<a id="52"></a>
## <a name="microsoftaspnetmvc-522"></a><span data-ttu-id="bf076-170">Microsoft.AspNet.MVC 5.2.2</span><span class="sxs-lookup"><span data-stu-id="bf076-170">Microsoft.AspNet.MVC 5.2.2</span></span>

<span data-ttu-id="bf076-171">Esta versión no tiene las características nuevas o correcciones de errores en MVC.</span><span class="sxs-lookup"><span data-stu-id="bf076-171">This release doesn't have any new features or bug fixes in MVC.</span></span> <span data-ttu-id="bf076-172">Hemos realizado una [cambiar en las páginas Web](https://blogs.msdn.com/b/webdev/archive/2014/07/28/announcing-the-beta-release-of-web-pages-3-2-1.aspx) para una mejora significativa del rendimiento y posteriormente se han actualizado todos los otros paquetes dependientes se posee para que dependa de esta nueva versión de las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="bf076-172">We made a [change in Web Pages](https://blogs.msdn.com/b/webdev/archive/2014/07/28/announcing-the-beta-release-of-web-pages-3-2-1.aspx) for a significant performance improvement and have subsequently updated all other dependent packages we own to depend on this new version of Web Pages.</span></span>

<a id="mvc523Beta"></a>
## <a name="aspnet-mvc-523-beta"></a><span data-ttu-id="bf076-173">Versión Beta de ASP.NET MVC 5.2.3</span><span class="sxs-lookup"><span data-stu-id="bf076-173">ASP.NET MVC 5.2.3 Beta</span></span>

<span data-ttu-id="bf076-174">Puede leer acerca de la versión [aquí](https://blogs.msdn.com/b/webdev/archive/2014/12/17/asp-net-mvc-5-2-3-web-pages-5-2-3-and-web-api-5-2-3-beta-releases.aspx).</span><span class="sxs-lookup"><span data-stu-id="bf076-174">You can read about the release [here](https://blogs.msdn.com/b/webdev/archive/2014/12/17/asp-net-mvc-5-2-3-web-pages-5-2-3-and-web-api-5-2-3-beta-releases.aspx).</span></span> <span data-ttu-id="bf076-175">Esta versión contiene solo las correcciones de errores.</span><span class="sxs-lookup"><span data-stu-id="bf076-175">This release contains only bug fixes.</span></span> <span data-ttu-id="bf076-176">Puede usar [esta consulta](https://aspnetwebstack.codeplex.com/workitem/list/advanced?keyword=&amp;status=Closed&amp;type=All&amp;priority=All&amp;release=v5.2.3%20Beta&amp;assignedTo=All&amp;component=MVC&amp;sortField=LastUpdatedDate&amp;sortDirection=Descending&amp;page=0&amp;reasonClosed=Fixed) para ver la lista de problemas corregidos en esta versión.</span><span class="sxs-lookup"><span data-stu-id="bf076-176">You can use [this query](https://aspnetwebstack.codeplex.com/workitem/list/advanced?keyword=&amp;status=Closed&amp;type=All&amp;priority=All&amp;release=v5.2.3%20Beta&amp;assignedTo=All&amp;component=MVC&amp;sortField=LastUpdatedDate&amp;sortDirection=Descending&amp;page=0&amp;reasonClosed=Fixed) to see the list of issues fixed in this release.</span></span>
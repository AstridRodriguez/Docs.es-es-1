---
uid: web-api/overview/security/enabling-cross-origin-requests-in-web-api
title: "Habilitar las solicitudes entre orígenes en ASP.NET Web API 2 | Documentos de Microsoft"
author: MikeWasson
description: "Muestra cómo admitir el uso compartido de recursos entre orígenes (CORS) en ASP.NET Web API."
ms.author: aspnetcontent
manager: wpickett
ms.date: 07/15/2014
ms.topic: article
ms.assetid: 9b265a5a-6a70-4a82-adce-2d7c56ae8bdd
ms.technology: dotnet-webapi
ms.prod: .net-framework
msc.legacyurl: /web-api/overview/security/enabling-cross-origin-requests-in-web-api
msc.type: authoredcontent
ms.openlocfilehash: 453ad29ff4f10f9660f3aa8bab358519b4cfd48b
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/10/2017
---
<a name="enabling-cross-origin-requests-in-aspnet-web-api-2"></a><span data-ttu-id="e5578-103">Habilitar las solicitudes entre orígenes en ASP.NET Web API 2</span><span class="sxs-lookup"><span data-stu-id="e5578-103">Enabling Cross-Origin Requests in ASP.NET Web API 2</span></span>
====================
<span data-ttu-id="e5578-104">por [Mike Wasson](https://github.com/MikeWasson)</span><span class="sxs-lookup"><span data-stu-id="e5578-104">by [Mike Wasson](https://github.com/MikeWasson)</span></span>

> <span data-ttu-id="e5578-105">Seguridad del explorador impide que una página web que realiza las solicitudes AJAX a otro dominio.</span><span class="sxs-lookup"><span data-stu-id="e5578-105">Browser security prevents a web page from making AJAX requests to another domain.</span></span> <span data-ttu-id="e5578-106">Esta restricción se denomina la *directiva de mismo origen*y se impide que un sitio malintencionado pueda leer los datos confidenciales desde otro sitio.</span><span class="sxs-lookup"><span data-stu-id="e5578-106">This restriction is called the *same-origin policy*, and prevents a malicious site from reading sensitive data from another site.</span></span> <span data-ttu-id="e5578-107">Sin embargo, en ocasiones, puede permitir que otros sitios a llame a la API web.</span><span class="sxs-lookup"><span data-stu-id="e5578-107">However, sometimes you might want to let other sites call your web API.</span></span>
> 
> <span data-ttu-id="e5578-108">[Entre el uso compartido de recursos de origen](http://www.w3.org/TR/cors/) (CORS) es un estándar de W3C que permite que un servidor relajar la directiva de mismo origen.</span><span class="sxs-lookup"><span data-stu-id="e5578-108">[Cross Origin Resource Sharing](http://www.w3.org/TR/cors/) (CORS) is a W3C standard that allows a server to relax the same-origin policy.</span></span> <span data-ttu-id="e5578-109">Con CORS, un servidor puede permitir explícitamente algunas solicitudes entre orígenes y rechazar los otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="e5578-109">Using CORS, a server can explicitly allow some cross-origin requests while rejecting others.</span></span> <span data-ttu-id="e5578-110">CORS es más seguro y más flexible que técnicas anteriores como [JSONP](http://en.wikipedia.org/wiki/JSONP).</span><span class="sxs-lookup"><span data-stu-id="e5578-110">CORS is safer and more flexible than earlier techniques such as [JSONP](http://en.wikipedia.org/wiki/JSONP).</span></span> <span data-ttu-id="e5578-111">Este tutorial muestra cómo habilitar CORS en la aplicación de API Web.</span><span class="sxs-lookup"><span data-stu-id="e5578-111">This tutorial shows how to enable CORS in your Web API application.</span></span>
> 
> ## <a name="software-versions-used-in-the-tutorial"></a><span data-ttu-id="e5578-112">Versiones de software que se usa en el tutorial</span><span class="sxs-lookup"><span data-stu-id="e5578-112">Software versions used in the tutorial</span></span>
> 
> 
> - [<span data-ttu-id="e5578-113">Visual Studio 2013 Update 2</span><span class="sxs-lookup"><span data-stu-id="e5578-113">Visual Studio 2013 Update 2</span></span>](https://www.microsoft.com/visualstudio/eng/2013-downloads)
> - <span data-ttu-id="e5578-114">2.2 API Web</span><span class="sxs-lookup"><span data-stu-id="e5578-114">Web API 2.2</span></span>


<a id="intro"></a>
## <a name="introduction"></a><span data-ttu-id="e5578-115">Introducción</span><span class="sxs-lookup"><span data-stu-id="e5578-115">Introduction</span></span>

<span data-ttu-id="e5578-116">Este tutorial se muestra la compatibilidad con CORS en ASP.NET Web API.</span><span class="sxs-lookup"><span data-stu-id="e5578-116">This tutorial demonstrates CORS support in ASP.NET Web API.</span></span> <span data-ttu-id="e5578-117">Comenzaremos mediante la creación de dos proyectos ASP.NET: una llamada "WebService", que hospeda un controlador de API Web, y el otra llamada "WebClient", que llama el servicio Web.</span><span class="sxs-lookup"><span data-stu-id="e5578-117">We'll start by creating two ASP.NET projects – one called "WebService", which hosts a Web API controller, and the other called "WebClient", which calls WebService.</span></span> <span data-ttu-id="e5578-118">Dado que las dos aplicaciones se hospedan en dominios diferentes, una solicitud de AJAX de WebClient al servicio Web es una solicitud entre orígenes.</span><span class="sxs-lookup"><span data-stu-id="e5578-118">Because the two applications are hosted at different domains, an AJAX request from WebClient to WebService is a cross-origin request.</span></span>

![](enabling-cross-origin-requests-in-web-api/_static/image1.png)

### <a name="what-is-same-origin"></a><span data-ttu-id="e5578-119">¿Qué es el "Mismo origen"?</span><span class="sxs-lookup"><span data-stu-id="e5578-119">What is "Same Origin"?</span></span>

<span data-ttu-id="e5578-120">Dos direcciones URL tienen el mismo origen si tienen puertos, los hosts y los esquemas idénticos.</span><span class="sxs-lookup"><span data-stu-id="e5578-120">Two URLs have the same origin if they have identical schemes, hosts, and ports.</span></span> <span data-ttu-id="e5578-121">([RFC 6454](http://tools.ietf.org/html/rfc6454))</span><span class="sxs-lookup"><span data-stu-id="e5578-121">([RFC 6454](http://tools.ietf.org/html/rfc6454))</span></span>

<span data-ttu-id="e5578-122">Estas dos direcciones URL tienen el mismo origen:</span><span class="sxs-lookup"><span data-stu-id="e5578-122">These two URLs have the same origin:</span></span>

- `http://example.com/foo.html`
- `http://example.com/bar.html`

<span data-ttu-id="e5578-123">Estas direcciones URL tengan diferentes orígenes que el anterior dos:</span><span class="sxs-lookup"><span data-stu-id="e5578-123">These URLs have different origins than the previous two:</span></span>

- <span data-ttu-id="e5578-124">`http://example.net`-Dominio diferente</span><span class="sxs-lookup"><span data-stu-id="e5578-124">`http://example.net` - Different domain</span></span>
- <span data-ttu-id="e5578-125">`http://example.com:9000/foo.html`-Otro puerto</span><span class="sxs-lookup"><span data-stu-id="e5578-125">`http://example.com:9000/foo.html` - Different port</span></span>
- <span data-ttu-id="e5578-126">`https://example.com/foo.html`-Esquema diferente</span><span class="sxs-lookup"><span data-stu-id="e5578-126">`https://example.com/foo.html` - Different scheme</span></span>
- <span data-ttu-id="e5578-127">`http://www.example.com/foo.html`-Otro subdominio</span><span class="sxs-lookup"><span data-stu-id="e5578-127">`http://www.example.com/foo.html` - Different subdomain</span></span>

> [!NOTE]
> <span data-ttu-id="e5578-128">Internet Explorer no tiene en cuenta el puerto al comparar elementos Origin.</span><span class="sxs-lookup"><span data-stu-id="e5578-128">Internet Explorer does not consider the port when comparing origins.</span></span>


<a id="create-webapi-project"></a>
## <a name="create-the-webservice-project"></a><span data-ttu-id="e5578-129">Crear el proyecto de servicio Web</span><span class="sxs-lookup"><span data-stu-id="e5578-129">Create the WebService Project</span></span>

> [!NOTE]
> <span data-ttu-id="e5578-130">En esta sección se da por supuesto que ya sabe cómo crear proyectos Web API.</span><span class="sxs-lookup"><span data-stu-id="e5578-130">This section assumes you already know how to create Web API projects.</span></span> <span data-ttu-id="e5578-131">Si no es así, consulte [Introducción a ASP.NET Web API](../getting-started-with-aspnet-web-api/tutorial-your-first-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="e5578-131">If not, see [Getting Started with ASP.NET Web API](../getting-started-with-aspnet-web-api/tutorial-your-first-web-api.md).</span></span>


<span data-ttu-id="e5578-132">Inicie Visual Studio y cree un nuevo **aplicación Web ASP.NET** proyecto.</span><span class="sxs-lookup"><span data-stu-id="e5578-132">Start Visual Studio and create a new **ASP.NET Web Application** project.</span></span> <span data-ttu-id="e5578-133">Seleccione el **vacía** plantilla de proyecto.</span><span class="sxs-lookup"><span data-stu-id="e5578-133">Select the **Empty** project template.</span></span> <span data-ttu-id="e5578-134">En "Agregar carpetas y principales referencias de", seleccione la **API Web** casilla de verificación.</span><span class="sxs-lookup"><span data-stu-id="e5578-134">Under "Add folders and core references for", select the **Web API** checkbox.</span></span> <span data-ttu-id="e5578-135">Si lo desea, seleccione la opción de "Host en la nube" para implementar la aplicación en Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5578-135">Optionally, select the "Host in Cloud" option to deploy the app to Mircosoft Azure.</span></span> <span data-ttu-id="e5578-136">Microsoft ofrece el hospedaje web gratuito para hasta 10 sitios Web en un [libre de la cuenta de prueba de Azure](https://azure.microsoft.com/free/?WT.mc_id=A443DD604).</span><span class="sxs-lookup"><span data-stu-id="e5578-136">Microsoft offers free web hosting for up to 10 websites in a [free Azure trial account](https://azure.microsoft.com/free/?WT.mc_id=A443DD604).</span></span>

[![](enabling-cross-origin-requests-in-web-api/_static/image3.png)](enabling-cross-origin-requests-in-web-api/_static/image2.png)

<span data-ttu-id="e5578-137">Agregar un controlador de API Web denominado `TestController` con el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e5578-137">Add a Web API controller named `TestController` with the following code:</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample1.cs)]

<span data-ttu-id="e5578-138">Puede ejecutar la aplicación localmente o implementar en Azure.</span><span class="sxs-lookup"><span data-stu-id="e5578-138">You can run the application locally or deploy to Azure.</span></span> <span data-ttu-id="e5578-139">(Para las capturas de pantalla en este tutorial, implementa para aplicaciones de Web del servicio de aplicación de Azure.) Para comprobar que funciona la API web, vaya a `http://hostname/api/test/`, donde *hostname* es el dominio donde se implementa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5578-139">(For the screenshots in this tutorial, I deployed to Azure App Service Web Apps.) To verify that the web API is working, navigate to `http://hostname/api/test/`, where *hostname* is the domain where you deployed the application.</span></span> <span data-ttu-id="e5578-140">Debería ver el texto de respuesta, &quot;obtener: mensaje de prueba&quot;.</span><span class="sxs-lookup"><span data-stu-id="e5578-140">You should see the response text, &quot;GET: Test Message&quot;.</span></span>

![](enabling-cross-origin-requests-in-web-api/_static/image4.png)

<a id="create-client"></a>
## <a name="create-the-webclient-project"></a><span data-ttu-id="e5578-141">Crear el proyecto de WebClient</span><span class="sxs-lookup"><span data-stu-id="e5578-141">Create the WebClient Project</span></span>

<span data-ttu-id="e5578-142">Cree otro proyecto de aplicación Web ASP.NET y seleccione el **MVC** plantilla de proyecto.</span><span class="sxs-lookup"><span data-stu-id="e5578-142">Create another ASP.NET Web Application project and select the **MVC** project template.</span></span> <span data-ttu-id="e5578-143">Si lo desea, seleccione **Cambiar autenticación** > **sin autenticación**.</span><span class="sxs-lookup"><span data-stu-id="e5578-143">Optionally, select **Change Authentication** > **No Authentication**.</span></span> <span data-ttu-id="e5578-144">No necesita autenticación para este tutorial.</span><span class="sxs-lookup"><span data-stu-id="e5578-144">You don't need authentication for this tutorial.</span></span>

[![](enabling-cross-origin-requests-in-web-api/_static/image6.png)](enabling-cross-origin-requests-in-web-api/_static/image5.png)

<span data-ttu-id="e5578-145">En el Explorador de soluciones, abra el archivo Views/Home/Index.cshtml.</span><span class="sxs-lookup"><span data-stu-id="e5578-145">In Solution Explorer, open the file Views/Home/Index.cshtml.</span></span> <span data-ttu-id="e5578-146">Reemplace el código de este archivo con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e5578-146">Replace the code in this file with the following:</span></span>

[!code-cshtml[Main](enabling-cross-origin-requests-in-web-api/samples/sample2.cshtml?highlight=13)]

<span data-ttu-id="e5578-147">Para el *serviceUrl* variable, utilice el URI de la aplicación de servicio Web.</span><span class="sxs-lookup"><span data-stu-id="e5578-147">For the *serviceUrl* variable, use the URI of the WebService app.</span></span> <span data-ttu-id="e5578-148">Ahora ejecuta la aplicación de WebClient localmente o publicarlo en otro sitio Web.</span><span class="sxs-lookup"><span data-stu-id="e5578-148">Now run the WebClient app locally or publish it to another website.</span></span>

<span data-ttu-id="e5578-149">Haga clic en el botón "Pruébelo" envía una solicitud AJAX a la aplicación de servicio Web mediante el método HTTP que se muestran en el cuadro de lista desplegable (GET, POST o PUT).</span><span class="sxs-lookup"><span data-stu-id="e5578-149">Clicking the "Try It" button submits an AJAX request to the WebService app, using the HTTP method listed in the dropdown box (GET, POST, or PUT).</span></span> <span data-ttu-id="e5578-150">Esto nos permite examinar las solicitudes entre orígenes diferentes.</span><span class="sxs-lookup"><span data-stu-id="e5578-150">This lets us examine different cross-origin requests.</span></span> <span data-ttu-id="e5578-151">En este momento, la aplicación de servicio Web no admiten CORS, por lo que si hace clic en el botón, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="e5578-151">Right now, the WebService app does not support CORS, so if you click the button, you will get an error.</span></span>

![](enabling-cross-origin-requests-in-web-api/_static/image7.png)

> [!NOTE]
> <span data-ttu-id="e5578-152">Si ve el tráfico HTTP en una herramienta como [Fiddler](http://www.telerik.com/fiddler), verá que el explorador envía la solicitud GET y la solicitud se realiza correctamente, pero la llamada de AJAX devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="e5578-152">If you watch the HTTP traffic in a tool like [Fiddler](http://www.telerik.com/fiddler), you will see that the browser does send the GET request, and the request succeeds, but the AJAX call returns an error.</span></span> <span data-ttu-id="e5578-153">Es importante comprender que la directiva de mismo origen no evita que el Explorador de *enviar* la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5578-153">It's important to understand that same-origin policy does not prevent the browser from *sending* the request.</span></span> <span data-ttu-id="e5578-154">En su lugar, se evita que la aplicación vean el *respuesta*.</span><span class="sxs-lookup"><span data-stu-id="e5578-154">Instead, it prevents the application from seeing the *response*.</span></span>


![](enabling-cross-origin-requests-in-web-api/_static/image8.png)

<a id="enable-cors"></a>
## <a name="enable-cors"></a><span data-ttu-id="e5578-155">Habilitar CORS</span><span class="sxs-lookup"><span data-stu-id="e5578-155">Enable CORS</span></span>

<span data-ttu-id="e5578-156">Ahora vamos a habilitar CORS en la aplicación de servicio Web.</span><span class="sxs-lookup"><span data-stu-id="e5578-156">Now let's enable CORS in the WebService app.</span></span> <span data-ttu-id="e5578-157">En primer lugar, agregue el paquete NuGet de CORS.</span><span class="sxs-lookup"><span data-stu-id="e5578-157">First, add the CORS NuGet package.</span></span> <span data-ttu-id="e5578-158">En Visual Studio, desde la **herramientas** menú, seleccione **Administrador de paquetes de biblioteca**, a continuación, seleccione **Package Manager Console**.</span><span class="sxs-lookup"><span data-stu-id="e5578-158">In Visual Studio, from the **Tools** menu, select **Library Package Manager**, then select **Package Manager Console**.</span></span> <span data-ttu-id="e5578-159">En la ventana de la consola de administrador de paquetes, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="e5578-159">In the Package Manager Console window, type the following command:</span></span>

[!code-powershell[Main](enabling-cross-origin-requests-in-web-api/samples/sample3.ps1)]

<span data-ttu-id="e5578-160">Este comando instala el paquete más reciente y actualiza todas las dependencias, incluidas las bibliotecas de API Web principal.</span><span class="sxs-lookup"><span data-stu-id="e5578-160">This command installs the latest package and updates all dependencies, including the core Web API libraries.</span></span> <span data-ttu-id="e5578-161">Usuario-marca de versión para dirigirse a una versión específica.</span><span class="sxs-lookup"><span data-stu-id="e5578-161">User the -Version flag to target a specific version.</span></span> <span data-ttu-id="e5578-162">El paquete CORS requiere Web API 2.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e5578-162">The CORS package requires Web API 2.0 or later.</span></span>

<span data-ttu-id="e5578-163">Abra el archivo de aplicación\_Start/WebApiConfig.cs.</span><span class="sxs-lookup"><span data-stu-id="e5578-163">Open the file App\_Start/WebApiConfig.cs.</span></span> <span data-ttu-id="e5578-164">Agregue el código siguiente a la **WebApiConfig.Register** método.</span><span class="sxs-lookup"><span data-stu-id="e5578-164">Add the following code to the **WebApiConfig.Register** method.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample4.cs?highlight=9)]

<span data-ttu-id="e5578-165">A continuación, agregue el **[EnableCors]** atribuir a la `TestController` clase:</span><span class="sxs-lookup"><span data-stu-id="e5578-165">Next, add the **[EnableCors]** attribute to the `TestController` class:</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample5.cs?highlight=3,7)]

<span data-ttu-id="e5578-166">Para el *orígenes* parámetro, use el URI en la que implementó la aplicación WebClient.</span><span class="sxs-lookup"><span data-stu-id="e5578-166">For the *origins* parameter, use the URI where you deployed the WebClient application.</span></span> <span data-ttu-id="e5578-167">Esto permite que las solicitudes entre orígenes de WebClient, mientras todavía no se permiten todas las demás solicitudes entre dominios.</span><span class="sxs-lookup"><span data-stu-id="e5578-167">This allows cross-origin requests from WebClient, while still disallowing all other cross-domain requests.</span></span> <span data-ttu-id="e5578-168">Más adelante, voy a describir los parámetros de **[EnableCors]** con más detalle.</span><span class="sxs-lookup"><span data-stu-id="e5578-168">Later, I'll describe the parameters for **[EnableCors]** in more detail.</span></span>

<span data-ttu-id="e5578-169">No incluya una barra diagonal al final de la *orígenes* dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e5578-169">Do not include a forward slash at the end of the *origins* URL.</span></span>

<span data-ttu-id="e5578-170">Volver a implementar la aplicación de servicio Web actualizada.</span><span class="sxs-lookup"><span data-stu-id="e5578-170">Redeploy the updated WebService application.</span></span> <span data-ttu-id="e5578-171">No es necesario actualizar WebClient.</span><span class="sxs-lookup"><span data-stu-id="e5578-171">You don't need to update WebClient.</span></span> <span data-ttu-id="e5578-172">Ahora debe ejecutarse correctamente la solicitud de AJAX de WebClient.</span><span class="sxs-lookup"><span data-stu-id="e5578-172">Now the AJAX request from WebClient should succeed.</span></span> <span data-ttu-id="e5578-173">Todos los métodos GET, PUT y POST se permiten.</span><span class="sxs-lookup"><span data-stu-id="e5578-173">The GET, PUT, and POST methods are all allowed.</span></span>

![](enabling-cross-origin-requests-in-web-api/_static/image9.png)

<a id="how-it-works"></a>
## <a name="how-cors-works"></a><span data-ttu-id="e5578-174">Funcionamiento de CORS</span><span class="sxs-lookup"><span data-stu-id="e5578-174">How CORS Works</span></span>

<span data-ttu-id="e5578-175">En esta sección se describe lo que sucede en una solicitud CORS, en el nivel de los mensajes HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5578-175">This section describes what happens in a CORS request, at the level of the HTTP messages.</span></span> <span data-ttu-id="e5578-176">Es importante comprender el funcionamiento de CORS, por lo que puede configurar el **[EnableCors]** atributo correctamente y solucionar los problemas si lo no funciona como esperaba.</span><span class="sxs-lookup"><span data-stu-id="e5578-176">It's important to understand how CORS works, so that you can configure the **[EnableCors]** attribute correctly, and troubleshoot if things don't work as you expect.</span></span>

<span data-ttu-id="e5578-177">La especificación de CORS presenta varios encabezados HTTP nuevo que permiten las solicitudes entre orígenes.</span><span class="sxs-lookup"><span data-stu-id="e5578-177">The CORS specification introduces several new HTTP headers that enable cross-origin requests.</span></span> <span data-ttu-id="e5578-178">Si un explorador es compatible con CORS, establece estos encabezados automáticamente para las solicitudes entre orígenes; no es necesario hacer nada especial en el código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e5578-178">If a browser supports CORS, it sets these headers automatically for cross-origin requests; you don't need to do anything special in your JavaScript code.</span></span>

<span data-ttu-id="e5578-179">Este es un ejemplo de una solicitud entre orígenes.</span><span class="sxs-lookup"><span data-stu-id="e5578-179">Here is an example of a cross-origin request.</span></span> <span data-ttu-id="e5578-180">El encabezado de "Origen" proporciona el dominio del sitio que está realizando la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5578-180">The "Origin" header gives the domain of the site that is making the request.</span></span>

[!code-console[Main](enabling-cross-origin-requests-in-web-api/samples/sample6.cmd?highlight=5)]

<span data-ttu-id="e5578-181">Si el servidor permite la solicitud, Establece el encabezado de acceso Access-Control-Allow-Origin.</span><span class="sxs-lookup"><span data-stu-id="e5578-181">If the server allows the request, it sets the Access-Control-Allow-Origin header.</span></span> <span data-ttu-id="e5578-182">El valor de este encabezado coincide con el encabezado de origen, o es el valor de carácter comodín "\*", lo que significa que se permite cualquier origen.</span><span class="sxs-lookup"><span data-stu-id="e5578-182">The value of this header either matches the Origin header, or is the wildcard value "\*", meaning that any origin is allowed.</span></span>

[!code-console[Main](enabling-cross-origin-requests-in-web-api/samples/sample7.cmd?highlight=5)]

<span data-ttu-id="e5578-183">Si la respuesta no incluye el encabezado de acceso Access-Control-Allow-Origin, se produce un error en la solicitud de AJAX.</span><span class="sxs-lookup"><span data-stu-id="e5578-183">If the response does not include the Access-Control-Allow-Origin header, the AJAX request fails.</span></span> <span data-ttu-id="e5578-184">En concreto, el explorador no permite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5578-184">Specifically, the browser disallows the request.</span></span> <span data-ttu-id="e5578-185">Incluso si el servidor devuelve una respuesta correcta, el explorador no disponer de la respuesta a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="e5578-185">Even if the server returns a successful response, the browser does not make the response available to the client application.</span></span>

<span data-ttu-id="e5578-186">**Solicitudes preparatorias**</span><span class="sxs-lookup"><span data-stu-id="e5578-186">**Preflight Requests**</span></span>

<span data-ttu-id="e5578-187">Para algunas solicitudes CORS, el explorador envía una solicitud adicional, denominada "solicitud preparatoria," antes de enviar la solicitud real para el recurso.</span><span class="sxs-lookup"><span data-stu-id="e5578-187">For some CORS requests, the browser sends an additional request, called a "preflight request", before it sends the actual request for the resource.</span></span>

<span data-ttu-id="e5578-188">El explorador puede omitir la solicitud preparatoria si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e5578-188">The browser can skip the preflight request if the following conditions are true:</span></span>

- <span data-ttu-id="e5578-189">El método de solicitud es GET, HEAD o POST, *y*</span><span class="sxs-lookup"><span data-stu-id="e5578-189">The request method is GET, HEAD, or POST, *and*</span></span>
- <span data-ttu-id="e5578-190">La aplicación no establece los encabezados de solicitud que no sean Accept, Accept-Language, Content-Language, Content-Type o último--Id. de evento, *y*</span><span class="sxs-lookup"><span data-stu-id="e5578-190">The application does not set any request headers other than Accept, Accept-Language, Content-Language, Content-Type, or Last-Event-ID, *and*</span></span>
- <span data-ttu-id="e5578-191">El encabezado Content-Type (si establece) es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e5578-191">The Content-Type header (if set) is one of the following:</span></span> 

    - <span data-ttu-id="e5578-192">application/x-www-form-urlencoded</span><span class="sxs-lookup"><span data-stu-id="e5578-192">application/x-www-form-urlencoded</span></span>
    - <span data-ttu-id="e5578-193">varias partes/de datos de formulario</span><span class="sxs-lookup"><span data-stu-id="e5578-193">multipart/form-data</span></span>
    - <span data-ttu-id="e5578-194">texto/sin formato</span><span class="sxs-lookup"><span data-stu-id="e5578-194">text/plain</span></span>

<span data-ttu-id="e5578-195">La regla acerca de los encabezados de solicitud se aplica a los encabezados de la aplicación se establece mediante una llamada a **setRequestHeader** en el **XMLHttpRequest** objeto.</span><span class="sxs-lookup"><span data-stu-id="e5578-195">The rule about request headers applies to headers that the application sets by calling **setRequestHeader** on the **XMLHttpRequest** object.</span></span> <span data-ttu-id="e5578-196">(La especificación de CORS llama a estos "encabezados de solicitud de autor"). La regla no se aplica a los encabezados de la *explorador* pueden establecer, como el agente de usuario, el Host o Content-Length.</span><span class="sxs-lookup"><span data-stu-id="e5578-196">(The CORS specification calls these "author request headers".) The rule does not apply to headers the *browser* can set, such as User-Agent, Host, or Content-Length.</span></span>

<span data-ttu-id="e5578-197">Este es un ejemplo de una solicitud preparatoria:</span><span class="sxs-lookup"><span data-stu-id="e5578-197">Here is an example of a preflight request:</span></span>

[!code-console[Main](enabling-cross-origin-requests-in-web-api/samples/sample8.cmd?highlight=4-5)]

<span data-ttu-id="e5578-198">La solicitud preparatoria utiliza el método HTTP OPTIONS.</span><span class="sxs-lookup"><span data-stu-id="e5578-198">The pre-flight request uses the HTTP OPTIONS method.</span></span> <span data-ttu-id="e5578-199">Incluye dos encabezados especiales:</span><span class="sxs-lookup"><span data-stu-id="e5578-199">It includes two special headers:</span></span>

- <span data-ttu-id="e5578-200">Acceso Access-Control-Request-Method: El método HTTP que se usará para la solicitud real.</span><span class="sxs-lookup"><span data-stu-id="e5578-200">Access-Control-Request-Method: The HTTP method that will be used for the actual request.</span></span>
- <span data-ttu-id="e5578-201">Acceso Access-Control-Request-Headers: Una lista de encabezados de solicitud que el *aplicación* establecido en la solicitud real.</span><span class="sxs-lookup"><span data-stu-id="e5578-201">Access-Control-Request-Headers: A list of request headers that the *application* set on the actual request.</span></span> <span data-ttu-id="e5578-202">(De nuevo, esto no incluye encabezados que establece el explorador.)</span><span class="sxs-lookup"><span data-stu-id="e5578-202">(Again, this does not include headers that the browser sets.)</span></span>

<span data-ttu-id="e5578-203">Esta es una respuesta de ejemplo, suponiendo que el servidor permite que la solicitud:</span><span class="sxs-lookup"><span data-stu-id="e5578-203">Here is an example response, assuming that the server allows the request:</span></span>

[!code-console[Main](enabling-cross-origin-requests-in-web-api/samples/sample9.cmd?highlight=6-7)]

<span data-ttu-id="e5578-204">La respuesta incluye un encabezado de acceso-Control-Allow-Methods que enumera los métodos permitidos y, opcionalmente, un encabezado Access-Control-permitir-Headers, que se muestra los encabezados permitidos.</span><span class="sxs-lookup"><span data-stu-id="e5578-204">The response includes an Access-Control-Allow-Methods header that lists the allowed methods, and optionally an Access-Control-Allow-Headers header, which lists the allowed headers.</span></span> <span data-ttu-id="e5578-205">Si la solicitud preparatoria se realiza correctamente, el explorador envía la solicitud real, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e5578-205">If the preflight request succeeds, the browser sends the actual request, as described earlier.</span></span>

<a id="scope"></a>
## <a name="scope-rules-for-enablecors"></a><span data-ttu-id="e5578-206">Reglas de ámbito para [EnableCors]</span><span class="sxs-lookup"><span data-stu-id="e5578-206">Scope Rules for [EnableCors]</span></span>

<span data-ttu-id="e5578-207">Puede habilitar CORS por cada acción, por cada controlador o globalmente para todos los controladores de API Web de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5578-207">You can enable CORS per action, per controller, or globally for all Web API controllers in your application.</span></span>

<span data-ttu-id="e5578-208">**Por cada acción**</span><span class="sxs-lookup"><span data-stu-id="e5578-208">**Per Action**</span></span>

<span data-ttu-id="e5578-209">Para habilitar CORS para una única acción, establezca el **[EnableCors]** atributo en el método de acción.</span><span class="sxs-lookup"><span data-stu-id="e5578-209">To enable CORS for a single action, set the **[EnableCors]** attribute on the action method.</span></span> <span data-ttu-id="e5578-210">En el ejemplo siguiente se habilita CORS para el `GetItem` método únicamente.</span><span class="sxs-lookup"><span data-stu-id="e5578-210">The following example enables CORS for the `GetItem` method only.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample10.cs)]

<span data-ttu-id="e5578-211">**Por cada controlador**</span><span class="sxs-lookup"><span data-stu-id="e5578-211">**Per Controller**</span></span>

<span data-ttu-id="e5578-212">Si establece **[EnableCors]** en la clase de controlador, se aplica a todas las acciones en el controlador.</span><span class="sxs-lookup"><span data-stu-id="e5578-212">If you set **[EnableCors]** on the controller class, it applies to all the actions on the controller.</span></span> <span data-ttu-id="e5578-213">Para deshabilitar CORS para una acción, agregue el **[DisableCors]** atribuir a la acción.</span><span class="sxs-lookup"><span data-stu-id="e5578-213">To disable CORS for an action, add the **[DisableCors]** attribute to the action.</span></span> <span data-ttu-id="e5578-214">En el ejemplo siguiente se habilita CORS para cada método excepto `PutItem`.</span><span class="sxs-lookup"><span data-stu-id="e5578-214">The following example enables CORS for every method except `PutItem`.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample11.cs)]

<span data-ttu-id="e5578-215">**Global**</span><span class="sxs-lookup"><span data-stu-id="e5578-215">**Globally**</span></span>

<span data-ttu-id="e5578-216">Para habilitar CORS para todos los controladores de API Web en la aplicación, pase una **EnableCorsAttribute** de instancia para la **EnableCors** método:</span><span class="sxs-lookup"><span data-stu-id="e5578-216">To enable CORS for all Web API controllers in your application, pass an **EnableCorsAttribute** instance to the **EnableCors** method:</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample12.cs)]

<span data-ttu-id="e5578-217">Si establece el atributo en más de un ámbito, el orden de prioridad es:</span><span class="sxs-lookup"><span data-stu-id="e5578-217">If you set the attribute at more than one scope, the order of precedence is:</span></span>

1. <span data-ttu-id="e5578-218">Acción</span><span class="sxs-lookup"><span data-stu-id="e5578-218">Action</span></span>
2. <span data-ttu-id="e5578-219">Controlador</span><span class="sxs-lookup"><span data-stu-id="e5578-219">Controller</span></span>
3. <span data-ttu-id="e5578-220">Global</span><span class="sxs-lookup"><span data-stu-id="e5578-220">Global</span></span>

<a id="allowed-origins"></a>
## <a name="set-the-allowed-origins"></a><span data-ttu-id="e5578-221">Establecer los orígenes permitidos</span><span class="sxs-lookup"><span data-stu-id="e5578-221">Set the Allowed Origins</span></span>

<span data-ttu-id="e5578-222">El *orígenes* parámetro de la **[EnableCors]** atributo especifica qué orígenes tendrán permiso para tener acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="e5578-222">The *origins* parameter of the **[EnableCors]** attribute specifies which origins are allowed to access the resource.</span></span> <span data-ttu-id="e5578-223">El valor es una lista separada por comas de los orígenes permitidos.</span><span class="sxs-lookup"><span data-stu-id="e5578-223">The value is a comma-separated list of the allowed origins.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample13.cs)]

<span data-ttu-id="e5578-224">También puede utilizar el valor de carácter comodín "\*" para permitir las solicitudes de los orígenes.</span><span class="sxs-lookup"><span data-stu-id="e5578-224">You can also use the wildcard value "\*" to allow requests from any origins.</span></span>

<span data-ttu-id="e5578-225">Debe considerar detenidamente antes de permitir que las solicitudes de cualquier origen.</span><span class="sxs-lookup"><span data-stu-id="e5578-225">Consider carefully before allowing requests from any origin.</span></span> <span data-ttu-id="e5578-226">Significa que literalmente cualquier sitio Web puede realizar llamadas de AJAX a la API web.</span><span class="sxs-lookup"><span data-stu-id="e5578-226">It means that literally any website can make AJAX calls to your web API.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample14.cs)]

<a id="allowed-methods"></a>
## <a name="set-the-allowed-http-methods"></a><span data-ttu-id="e5578-227">Establecer los métodos HTTP permitidos</span><span class="sxs-lookup"><span data-stu-id="e5578-227">Set the Allowed HTTP Methods</span></span>

<span data-ttu-id="e5578-228">El *métodos* parámetro de la **[EnableCors]** atributo especifica qué métodos HTTP se permiten tener acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="e5578-228">The *methods* parameter of the **[EnableCors]** attribute specifies which HTTP methods are allowed to access the resource.</span></span> <span data-ttu-id="e5578-229">Para permitir que todos los métodos, utilice el valor de carácter comodín "\*".</span><span class="sxs-lookup"><span data-stu-id="e5578-229">To allow all methods, use the wildcard value "\*".</span></span> <span data-ttu-id="e5578-230">En el ejemplo siguiente, se permite solamente las solicitudes GET y POST.</span><span class="sxs-lookup"><span data-stu-id="e5578-230">The following example allows only GET and POST requests.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample15.cs)]

<a id="allowed-request-headers"></a>
## <a name="set-the-allowed-request-headers"></a><span data-ttu-id="e5578-231">Establecer los encabezados de solicitudes permitido</span><span class="sxs-lookup"><span data-stu-id="e5578-231">Set the Allowed Request Headers</span></span>

<span data-ttu-id="e5578-232">Anteriormente describe cómo una solicitud preparatoria podría incluir un encabezado de acceso-Access-Control-Request-Headers, enumerar los encabezados HTTP establecidos por la aplicación (la "crear encabezados de solicitud").</span><span class="sxs-lookup"><span data-stu-id="e5578-232">Earlier I described how a preflight request might include an Access-Control-Request-Headers header, listing the HTTP headers set by the application (the so-called "author request headers").</span></span> <span data-ttu-id="e5578-233">El *encabezados* parámetro de la **[EnableCors]** atributo especifica que se permiten los encabezados de solicitud de autor.</span><span class="sxs-lookup"><span data-stu-id="e5578-233">The *headers* parameter of the **[EnableCors]** attribute specifies which author request headers are allowed.</span></span> <span data-ttu-id="e5578-234">Para permitir que los encabezados, establezca *encabezados* a "\*".</span><span class="sxs-lookup"><span data-stu-id="e5578-234">To allow any headers, set *headers* to "\*".</span></span> <span data-ttu-id="e5578-235">A encabezados específicos de la lista blanca, establezca *encabezados* a una lista separada por comas de los encabezados permitidos:</span><span class="sxs-lookup"><span data-stu-id="e5578-235">To whitelist specific headers, set *headers* to a comma-separated list of the allowed headers:</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample16.cs)]

<span data-ttu-id="e5578-236">Sin embargo, los exploradores no son completamente coherentes en forma de conjunto de acceso-Access-Control-Request-Headers.</span><span class="sxs-lookup"><span data-stu-id="e5578-236">However, browsers are not entirely consistent in how they set Access-Control-Request-Headers.</span></span> <span data-ttu-id="e5578-237">Por ejemplo, Chrome incluye actualmente "origen"; mientras FireFox no incluye encabezados estándar como "Accept", incluso cuando la aplicación los establece en el script.</span><span class="sxs-lookup"><span data-stu-id="e5578-237">For example, Chrome currently includes "origin"; while FireFox does not include standard headers such as "Accept", even when the application sets them in script.</span></span>

<span data-ttu-id="e5578-238">Si establece *encabezados* en ningún otro valor distinto de "\*", debe incluir al menos "Aceptar", "content-type" y "origen", además de los encabezados personalizados que desee admitir.</span><span class="sxs-lookup"><span data-stu-id="e5578-238">If you set *headers* to anything other than "\*", you should include at least "accept", "content-type", and "origin", plus any custom headers that you want to support.</span></span>

<a id="allowed-response-headers"></a>
## <a name="set-the-allowed-response-headers"></a><span data-ttu-id="e5578-239">Establecer los encabezados de respuesta permitido</span><span class="sxs-lookup"><span data-stu-id="e5578-239">Set the Allowed Response Headers</span></span>

<span data-ttu-id="e5578-240">De forma predeterminada, el explorador no expone todos los encabezados de respuesta a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5578-240">By default, the browser does not expose all of the response headers to the application.</span></span> <span data-ttu-id="e5578-241">Los encabezados de respuesta que están disponibles de forma predeterminada son:</span><span class="sxs-lookup"><span data-stu-id="e5578-241">The response headers that are available by default are:</span></span>

- <span data-ttu-id="e5578-242">Control de caché</span><span class="sxs-lookup"><span data-stu-id="e5578-242">Cache-Control</span></span>
- <span data-ttu-id="e5578-243">Content-Language</span><span class="sxs-lookup"><span data-stu-id="e5578-243">Content-Language</span></span>
- <span data-ttu-id="e5578-244">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="e5578-244">Content-Type</span></span>
- <span data-ttu-id="e5578-245">Expira</span><span class="sxs-lookup"><span data-stu-id="e5578-245">Expires</span></span>
- <span data-ttu-id="e5578-246">Última modificación</span><span class="sxs-lookup"><span data-stu-id="e5578-246">Last-Modified</span></span>
- <span data-ttu-id="e5578-247">Pragma</span><span class="sxs-lookup"><span data-stu-id="e5578-247">Pragma</span></span>

<span data-ttu-id="e5578-248">La especificación CORS llama a estos [encabezados de respuesta simple](https://dvcs.w3.org/hg/cors/raw-file/tip/Overview.html#simple-response-header).</span><span class="sxs-lookup"><span data-stu-id="e5578-248">The CORS spec calls these [simple response headers](https://dvcs.w3.org/hg/cors/raw-file/tip/Overview.html#simple-response-header).</span></span> <span data-ttu-id="e5578-249">Para hacer que otros encabezados disponibles para la aplicación, establezca el *exposedHeaders* parámetro de **[EnableCors]**.</span><span class="sxs-lookup"><span data-stu-id="e5578-249">To make other headers available to the application, set the *exposedHeaders* parameter of **[EnableCors]**.</span></span>

<span data-ttu-id="e5578-250">En del ejemplo siguiente, el controlador `Get` método establece un encabezado personalizado denominado 'X-Custom-Header'.</span><span class="sxs-lookup"><span data-stu-id="e5578-250">In the following example, the controller's `Get` method sets a custom header named ‘X-Custom-Header'.</span></span> <span data-ttu-id="e5578-251">De forma predeterminada, el explorador no expondrá este encabezado en una solicitud entre orígenes.</span><span class="sxs-lookup"><span data-stu-id="e5578-251">By default, the browser will not expose this header in a cross-origin request.</span></span> <span data-ttu-id="e5578-252">Para que esté disponible el encabezado, incluir 'X-Custom-Header' en *exposedHeaders*.</span><span class="sxs-lookup"><span data-stu-id="e5578-252">To make the header available, include ‘X-Custom-Header' in *exposedHeaders*.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample17.cs)]

<a id="credentials"></a>
## <a name="passing-credentials-in-cross-origin-requests"></a><span data-ttu-id="e5578-253">Transferencia de credenciales en solicitudes Cross-Origin</span><span class="sxs-lookup"><span data-stu-id="e5578-253">Passing Credentials in Cross-Origin Requests</span></span>

<span data-ttu-id="e5578-254">Las credenciales requieren un tratamiento especial en una solicitud de CORS.</span><span class="sxs-lookup"><span data-stu-id="e5578-254">Credentials require special handling in a CORS request.</span></span> <span data-ttu-id="e5578-255">De forma predeterminada, el explorador no envía ninguna credencial con una solicitud entre orígenes.</span><span class="sxs-lookup"><span data-stu-id="e5578-255">By default, the browser does not send any credentials with a cross-origin request.</span></span> <span data-ttu-id="e5578-256">Las credenciales son las cookies, así como esquemas de autenticación HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5578-256">Credentials include cookies as well as HTTP authentication schemes.</span></span> <span data-ttu-id="e5578-257">Para enviar las credenciales con una solicitud entre orígenes, el cliente debe establecer **XMLHttpRequest.withCredentials** en true.</span><span class="sxs-lookup"><span data-stu-id="e5578-257">To send credentials with a cross-origin request, the client must set **XMLHttpRequest.withCredentials** to true.</span></span>

<span data-ttu-id="e5578-258">Usar **XMLHttpRequest** directamente:</span><span class="sxs-lookup"><span data-stu-id="e5578-258">Using **XMLHttpRequest** directly:</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample18.cs)]

<span data-ttu-id="e5578-259">En jQuery:</span><span class="sxs-lookup"><span data-stu-id="e5578-259">In jQuery:</span></span>

[!code-javascript[Main](enabling-cross-origin-requests-in-web-api/samples/sample19.js)]

<span data-ttu-id="e5578-260">Además, el servidor debe permitir las credenciales.</span><span class="sxs-lookup"><span data-stu-id="e5578-260">In addition, the server must allow the credentials.</span></span> <span data-ttu-id="e5578-261">Para permitir las credenciales entre orígenes de API Web, establezca el **SupportsCredentials** propiedad en true en la **[EnableCors]** atributo:</span><span class="sxs-lookup"><span data-stu-id="e5578-261">To allow cross-origin credentials in Web API, set the **SupportsCredentials** property to true on the **[EnableCors]** attribute:</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample20.cs)]

<span data-ttu-id="e5578-262">Si esta propiedad es true, la respuesta HTTP incluirá un encabezado de acceso-Control-Allow-Credentials.</span><span class="sxs-lookup"><span data-stu-id="e5578-262">If this property is true, the HTTP response will include an Access-Control-Allow-Credentials header.</span></span> <span data-ttu-id="e5578-263">Este encabezado indica al explorador que el servidor permite que las credenciales para una solicitud entre orígenes.</span><span class="sxs-lookup"><span data-stu-id="e5578-263">This header tells the browser that the server allows credentials for a cross-origin request.</span></span>

<span data-ttu-id="e5578-264">Si el explorador envía las credenciales, pero la respuesta no incluye un encabezado de acceso-Control-Allow-Credentials válido, el explorador no expondrá la respuesta a la aplicación y se produce un error en la solicitud de AJAX.</span><span class="sxs-lookup"><span data-stu-id="e5578-264">If the browser sends credentials, but the response does not include a valid Access-Control-Allow-Credentials header, the browser will not expose the response to the application, and the AJAX request fails.</span></span>

<span data-ttu-id="e5578-265">Tenga mucho cuidado sobre la configuración de **SupportsCredentials** en true, ya que significa que un sitio Web en otro dominio puede enviar credenciales ha iniciado la sesión de un usuario a su API Web en nombre del usuario, sin el conocimiento del usuario.</span><span class="sxs-lookup"><span data-stu-id="e5578-265">Be very careful about setting **SupportsCredentials** to true, because it means a website at another domain can send a logged-in user's credentials to your Web API on the user's behalf, without the user being aware.</span></span> <span data-ttu-id="e5578-266">La especificación CORS dice también ese valor *orígenes* a &quot; \* &quot; no es válido si **SupportsCredentials** es true.</span><span class="sxs-lookup"><span data-stu-id="e5578-266">The CORS spec also states that setting *origins* to &quot;\*&quot; is invalid if **SupportsCredentials** is true.</span></span>

<a id="cors-policy-providers"></a>
## <a name="custom-cors-policy-providers"></a><span data-ttu-id="e5578-267">Proveedores de directiva personalizada de CORS</span><span class="sxs-lookup"><span data-stu-id="e5578-267">Custom CORS Policy Providers</span></span>

<span data-ttu-id="e5578-268">El **[EnableCors]** atributo implementa la **ICorsPolicyProvider** interfaz.</span><span class="sxs-lookup"><span data-stu-id="e5578-268">The **[EnableCors]** attribute implements the **ICorsPolicyProvider** interface.</span></span> <span data-ttu-id="e5578-269">Puede proporcionar su propia implementación mediante la creación de una clase que deriva de **atributo** e implementa **ICorsProlicyProvider**.</span><span class="sxs-lookup"><span data-stu-id="e5578-269">You can provide your own implementation by creating a class that derives from **Attribute** and implements **ICorsProlicyProvider**.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample21.cs)]

<span data-ttu-id="e5578-270">Ahora puede aplicar el atributo de cualquier lugar en el que aplicaría **[EnableCors]**.</span><span class="sxs-lookup"><span data-stu-id="e5578-270">Now you can apply the attribute any place that you would put **[EnableCors]**.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample22.cs)]

<span data-ttu-id="e5578-271">Por ejemplo, un proveedor de directivas personalizado de CORS pudo leer la configuración de un archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="e5578-271">For example, a custom CORS policy provider could read the settings from a configuration file.</span></span>

<span data-ttu-id="e5578-272">Como alternativa al uso de atributos, puede registrar un **ICorsPolicyProviderFactory** objeto que crea **ICorsPolicyProvider** objetos.</span><span class="sxs-lookup"><span data-stu-id="e5578-272">As an alternative to using attributes, you can register an **ICorsPolicyProviderFactory** object that creates **ICorsPolicyProvider** objects.</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample23.cs)]

<span data-ttu-id="e5578-273">Para establecer el **ICorsPolicyProviderFactory**, llame a la **SetCorsPolicyProviderFactory** método de extensión en el inicio, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="e5578-273">To set the **ICorsPolicyProviderFactory**, call the **SetCorsPolicyProviderFactory** extension method at startup, as follows:</span></span>

[!code-csharp[Main](enabling-cross-origin-requests-in-web-api/samples/sample24.cs)]

<a id="browser-support"></a>
## <a name="browser-support"></a><span data-ttu-id="e5578-274">Compatibilidad de exploradores</span><span class="sxs-lookup"><span data-stu-id="e5578-274">Browser Support</span></span>

<span data-ttu-id="e5578-275">El paquete de Web API CORS es una tecnología de servidor.</span><span class="sxs-lookup"><span data-stu-id="e5578-275">The Web API CORS package is a server-side technology.</span></span> <span data-ttu-id="e5578-276">El explorador del usuario también debe admitir CORS.</span><span class="sxs-lookup"><span data-stu-id="e5578-276">The user's browser also needs to support CORS.</span></span> <span data-ttu-id="e5578-277">Afortunadamente, se incluyen las versiones actuales de los principales exploradores [compatibilidad con CORS](http://caniuse.com/cors).</span><span class="sxs-lookup"><span data-stu-id="e5578-277">Fortunately, the current versions of all major browsers include [support for CORS](http://caniuse.com/cors).</span></span>

<span data-ttu-id="e5578-278">Internet Explorer 8 e Internet Explorer 9 tienen compatibilidad parcial para CORS, use el objeto heredado de XDomainRequest en lugar de XMLHttpRequest.</span><span class="sxs-lookup"><span data-stu-id="e5578-278">Internet Explorer 8 and Internet Explorer 9 have partial support for CORS, using the legacy XDomainRequest object instead of XMLHttpRequest.</span></span> <span data-ttu-id="e5578-279">Para obtener más información, consulte [XDomainRequest - soluciones alternativas, limitaciones y restricciones](https://blogs.msdn.com/b/ieinternals/archive/2010/05/13/xdomainrequest-restrictions-limitations-and-workarounds.aspx).</span><span class="sxs-lookup"><span data-stu-id="e5578-279">For more information, see [XDomainRequest - Restrictions, Limitations and Workarounds](https://blogs.msdn.com/b/ieinternals/archive/2010/05/13/xdomainrequest-restrictions-limitations-and-workarounds.aspx).</span></span>
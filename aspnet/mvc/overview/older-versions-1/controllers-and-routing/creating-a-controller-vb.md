---
uid: mvc/overview/older-versions-1/controllers-and-routing/creating-a-controller-vb
title: "Creación de un controlador (VB) | Documentos de Microsoft"
author: StephenWalther
description: "En este tutorial, Stephen Walther muestra cómo puede agregar un controlador a una aplicación de ASP.NET MVC."
ms.author: aspnetcontent
manager: wpickett
ms.date: 03/02/2009
ms.topic: article
ms.assetid: 204b7e86-f560-4611-8adb-785b33e777b9
ms.technology: dotnet-mvc
ms.prod: .net-framework
msc.legacyurl: /mvc/overview/older-versions-1/controllers-and-routing/creating-a-controller-vb
msc.type: authoredcontent
ms.openlocfilehash: d2caf7fe137b48c016ff3cd52db9e36e1e8001c0
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/10/2017
---
<a name="creating-a-controller-vb"></a><span data-ttu-id="153b6-103">Creación de un controlador (VB)</span><span class="sxs-lookup"><span data-stu-id="153b6-103">Creating a Controller (VB)</span></span>
====================
<span data-ttu-id="153b6-104">por [Stephen Walther](https://github.com/StephenWalther)</span><span class="sxs-lookup"><span data-stu-id="153b6-104">by [Stephen Walther](https://github.com/StephenWalther)</span></span>

> <span data-ttu-id="153b6-105">En este tutorial, Stephen Walther muestra cómo puede agregar un controlador a una aplicación de ASP.NET MVC.</span><span class="sxs-lookup"><span data-stu-id="153b6-105">In this tutorial, Stephen Walther demonstrates how you can add a controller to an ASP.NET MVC application.</span></span>


<span data-ttu-id="153b6-106">El objetivo de este tutorial es explicar cómo se puede crear controladores de MVC de ASP.NET nuevo.</span><span class="sxs-lookup"><span data-stu-id="153b6-106">The goal of this tutorial is to explain how you can create new ASP.NET MVC controllers.</span></span> <span data-ttu-id="153b6-107">Obtenga información acerca de cómo crear controladores mediante la opción de menú Agregar controlador de Visual Studio y mediante la creación de un archivo de clase a mano.</span><span class="sxs-lookup"><span data-stu-id="153b6-107">You learn how to create controllers both by using the Visual Studio Add Controller menu option and by creating a class file by hand.</span></span>

### <a name="using-the-add-controller-menu-option"></a><span data-ttu-id="153b6-108">Mediante el agregar la opción de menú de controlador</span><span class="sxs-lookup"><span data-stu-id="153b6-108">Using the Add Controller Menu Option</span></span>

<span data-ttu-id="153b6-109">Es la manera más fácil de crear un nuevo controlador haga clic en la carpeta de controladores en la ventana Explorador de soluciones de Visual Studio y seleccione la **agregar, controlador** opción de menú (consulte la figura 1).</span><span class="sxs-lookup"><span data-stu-id="153b6-109">The easiest way to create a new controller is to right-click the Controllers folder in the Visual Studio Solution Explorer window and select the **Add, Controller** menu option (see Figure 1).</span></span> <span data-ttu-id="153b6-110">Al seleccionar esta opción de menú se abre la **Agregar controlador** cuadro de diálogo (consulte la figura 2).</span><span class="sxs-lookup"><span data-stu-id="153b6-110">Selecting this menu option opens the **Add Controller** dialog (see Figure 2).</span></span>


<span data-ttu-id="153b6-111">[![El cuadro de diálogo nuevo proyecto](creating-a-controller-vb/_static/image1.jpg)](creating-a-controller-vb/_static/image1.png)</span><span class="sxs-lookup"><span data-stu-id="153b6-111">[![The New Project dialog box](creating-a-controller-vb/_static/image1.jpg)](creating-a-controller-vb/_static/image1.png)</span></span>

<span data-ttu-id="153b6-112">**Figura 01**: agregar un nuevo controlador ([haga clic aquí para ver la imagen a tamaño completo](creating-a-controller-vb/_static/image2.png))</span><span class="sxs-lookup"><span data-stu-id="153b6-112">**Figure 01**: Adding a new controller([Click to view full-size image](creating-a-controller-vb/_static/image2.png))</span></span>


<span data-ttu-id="153b6-113">[![El cuadro de diálogo nuevo proyecto](creating-a-controller-vb/_static/image2.jpg)](creating-a-controller-vb/_static/image3.png)</span><span class="sxs-lookup"><span data-stu-id="153b6-113">[![The New Project dialog box](creating-a-controller-vb/_static/image2.jpg)](creating-a-controller-vb/_static/image3.png)</span></span>

<span data-ttu-id="153b6-114">**Figura 02**: cuadro de diálogo de agregar el controlador ([haga clic aquí para ver la imagen a tamaño completo](creating-a-controller-vb/_static/image4.png))</span><span class="sxs-lookup"><span data-stu-id="153b6-114">**Figure 02**: The Add Controller dialog ([Click to view full-size image](creating-a-controller-vb/_static/image4.png))</span></span>


<span data-ttu-id="153b6-115">Tenga en cuenta que la primera parte del nombre del controlador se resalta en el **Agregar controlador** cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="153b6-115">Notice that the first part of the controller name is highlighted in the **Add Controller** dialog.</span></span> <span data-ttu-id="153b6-116">Cada nombre de controlador debe finalizar con el sufijo *controlador*.</span><span class="sxs-lookup"><span data-stu-id="153b6-116">Every controller name must end with the suffix *Controller*.</span></span> <span data-ttu-id="153b6-117">Por ejemplo, puede crear un controlador denominado *ProductController* pero no un controlador denominado *producto*.</span><span class="sxs-lookup"><span data-stu-id="153b6-117">For example, you can create a controller named *ProductController* but not a controller named *Product*.</span></span>


<span data-ttu-id="153b6-118">Si creas un controlador que falta el *controlador* sufijo, a continuación, no podrá invocar el controlador.</span><span class="sxs-lookup"><span data-stu-id="153b6-118">If you create a controller that is missing the *Controller* suffix then you won't be able to invoke the controller.</span></span> <span data-ttu-id="153b6-119">No lo hace, he perdí horas y horas de mi vida después de realizar este error.</span><span class="sxs-lookup"><span data-stu-id="153b6-119">Don't do this -- I've wasted countless hours of my life after making this mistake.</span></span>


<span data-ttu-id="153b6-120">**Lista 1 - Controllers\ProductController.vb**</span><span class="sxs-lookup"><span data-stu-id="153b6-120">**Listing 1 - Controllers\ProductController.vb**</span></span>

[!code-vb[Main](creating-a-controller-vb/samples/sample1.vb)]

<span data-ttu-id="153b6-121">Siempre debe crear los controladores en la carpeta de controladores.</span><span class="sxs-lookup"><span data-stu-id="153b6-121">You should always create controllers in the Controllers folder.</span></span> <span data-ttu-id="153b6-122">En caso contrario, podrá ser infringir las convenciones de ASP.NET MVC y otros desarrolladores tendrán más dificultades a la hora Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="153b6-122">Otherwise, you'll be violating the conventions of ASP.NET MVC and other developers will have a more difficult time understanding your application.</span></span>

### <a name="scaffolding-action-methods"></a><span data-ttu-id="153b6-123">Métodos de acción de scaffolding</span><span class="sxs-lookup"><span data-stu-id="153b6-123">Scaffolding Action Methods</span></span>

<span data-ttu-id="153b6-124">Cuando se crea un controlador, tiene la opción para generar automáticamente los métodos de acción de creación, actualización y detalles (consulte la figura 3).</span><span class="sxs-lookup"><span data-stu-id="153b6-124">When you create a controller, you have the option to generate Create, Update, and Details action methods automatically (see Figure 3).</span></span> <span data-ttu-id="153b6-125">Si selecciona esta opción, se genera la clase de controlador en el listado 2.</span><span class="sxs-lookup"><span data-stu-id="153b6-125">If you select this option then the controller class in Listing 2 is generated.</span></span>


<span data-ttu-id="153b6-126">[![Creación automática de los métodos de acción](creating-a-controller-vb/_static/image3.jpg)](creating-a-controller-vb/_static/image5.png)</span><span class="sxs-lookup"><span data-stu-id="153b6-126">[![Creating action methods automatically](creating-a-controller-vb/_static/image3.jpg)](creating-a-controller-vb/_static/image5.png)</span></span>

<span data-ttu-id="153b6-127">**Figura 03**: creación automática de los métodos de acción ([haga clic aquí para ver la imagen a tamaño completo](creating-a-controller-vb/_static/image6.png))</span><span class="sxs-lookup"><span data-stu-id="153b6-127">**Figure 03**: Creating action methods automatically ([Click to view full-size image](creating-a-controller-vb/_static/image6.png))</span></span>


<span data-ttu-id="153b6-128">**La lista 2 - Controllers\CustomerController.vb**</span><span class="sxs-lookup"><span data-stu-id="153b6-128">**Listing 2 - Controllers\CustomerController.vb**</span></span>

[!code-vb[Main](creating-a-controller-vb/samples/sample2.vb)]

<span data-ttu-id="153b6-129">Estos métodos generados son métodos de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="153b6-129">These generated methods are stub methods.</span></span> <span data-ttu-id="153b6-130">Debe agregar la lógica real para crear, actualizar y mostrar detalles de un cliente.</span><span class="sxs-lookup"><span data-stu-id="153b6-130">You must add the actual logic for creating, updating, and showing details for a customer yourself.</span></span> <span data-ttu-id="153b6-131">Sin embargo, los métodos de código auxiliar proporcionan con un punto de partida "nice".</span><span class="sxs-lookup"><span data-stu-id="153b6-131">But, the stub methods provide you with a nice starting point.</span></span>

### <a name="creating-a-controller-class"></a><span data-ttu-id="153b6-132">Crear una clase de controlador</span><span class="sxs-lookup"><span data-stu-id="153b6-132">Creating a Controller Class</span></span>

<span data-ttu-id="153b6-133">El controlador de MVC de ASP.NET es simplemente una clase.</span><span class="sxs-lookup"><span data-stu-id="153b6-133">The ASP.NET MVC controller is just a class.</span></span> <span data-ttu-id="153b6-134">Si lo prefiere, puede omitir el scaffolding de controlador adecuado de Visual Studio y cree una clase de controlador a mano.</span><span class="sxs-lookup"><span data-stu-id="153b6-134">If you prefer, you can ignore the convenient Visual Studio controller scaffolding and create a controller class by hand.</span></span> <span data-ttu-id="153b6-135">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="153b6-135">Follow these steps:</span></span>

1. <span data-ttu-id="153b6-136">Haga clic en la carpeta Controllers y seleccione la opción de menú **agregar, nuevo elemento** y seleccione la **clase** plantilla (consulte la figura 4).</span><span class="sxs-lookup"><span data-stu-id="153b6-136">Right-click the Controllers folder and select the menu option **Add, New Item** and select the **Class** template (see Figure 4).</span></span>
2. <span data-ttu-id="153b6-137">Nombre de la nueva clase PersonController.vb y haga clic en el **agregar** botón.</span><span class="sxs-lookup"><span data-stu-id="153b6-137">Name the new class PersonController.vb and click the **Add** button.</span></span>
3. <span data-ttu-id="153b6-138">Modificar el archivo resultante de la clase para que la clase hereda de la clase base de System.Web.Mvc.Controller (consulte el listado 3).</span><span class="sxs-lookup"><span data-stu-id="153b6-138">Modify the resulting class file so that the class inherits from the base System.Web.Mvc.Controller class (see Listing 3).</span></span>


<span data-ttu-id="153b6-139">[![Crear una nueva clase](creating-a-controller-vb/_static/image4.jpg)](creating-a-controller-vb/_static/image7.png)</span><span class="sxs-lookup"><span data-stu-id="153b6-139">[![Creating a new class](creating-a-controller-vb/_static/image4.jpg)](creating-a-controller-vb/_static/image7.png)</span></span>

<span data-ttu-id="153b6-140">**Figura 04**: crear una nueva clase ([haga clic aquí para ver la imagen a tamaño completo](creating-a-controller-vb/_static/image8.png))</span><span class="sxs-lookup"><span data-stu-id="153b6-140">**Figure 04**: Creating a new class([Click to view full-size image](creating-a-controller-vb/_static/image8.png))</span></span>


<span data-ttu-id="153b6-141">**El listado 3 - Controllers\PersonController.vb**</span><span class="sxs-lookup"><span data-stu-id="153b6-141">**Listing 3 - Controllers\PersonController.vb**</span></span>

[!code-vb[Main](creating-a-controller-vb/samples/sample3.vb)]

<span data-ttu-id="153b6-142">El controlador en el listado 3 expone una acción denominada Index() que devuelve la cadena "¡Hello World!".</span><span class="sxs-lookup"><span data-stu-id="153b6-142">The controller in Listing 3 exposes one action named Index() that returns the string "Hello World!".</span></span> <span data-ttu-id="153b6-143">Puede invocar esta acción de controlador, ejecute la aplicación y solicita una dirección URL similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="153b6-143">You can invoke this controller action by running your application and requesting a URL like the following:</span></span>

`http://localhost:40071/Person`

> [!NOTE] 
> 
> <span data-ttu-id="153b6-144">El servidor de desarrollo de ASP.NET usa un número de puerto aleatorio (por ejemplo, 40071).</span><span class="sxs-lookup"><span data-stu-id="153b6-144">The ASP.NET Development Server uses a random port number (for example, 40071).</span></span> <span data-ttu-id="153b6-145">Cuando escriba una dirección URL para invocar un controlador, debe proporcionar el número de puerto adecuado.</span><span class="sxs-lookup"><span data-stu-id="153b6-145">When entering a URL to invoke a controller, you'll need to supply the right port number.</span></span> <span data-ttu-id="153b6-146">Puede determinar el número de puerto desplazando el puntero del mouse sobre el icono para el servidor de desarrollo de ASP.NET en el área de notificación de Windows (parte inferior derecha de la pantalla).</span><span class="sxs-lookup"><span data-stu-id="153b6-146">You can determine the port number by hovering your mouse over the icon for the ASP.NET Development Server in the Windows Notification Area (bottom-right of your screen).</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="153b6-147">[Anterior](adding-dynamic-content-to-a-cached-page-vb.md)
[Siguiente](creating-an-action-vb.md)</span><span class="sxs-lookup"><span data-stu-id="153b6-147">[Previous](adding-dynamic-content-to-a-cached-page-vb.md)
[Next](creating-an-action-vb.md)</span></span>
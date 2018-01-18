---
uid: web-pages/readme/overview
title: "Archivo Léame de WebMatrix | Documentos de Microsoft"
author: rick-anderson
description: "WebMatrix y ASP.NET Web Pages (Razor) versión 1.0 Léame"
ms.author: aspnetcontent
manager: wpickett
ms.date: 01/06/2011
ms.topic: article
ms.assetid: 36c5beeb-45a7-48a0-9c30-f82cdf5c5f5f
ms.technology: dotnet-webpages
ms.prod: .net-framework
msc.legacyurl: /web-pages/readme
msc.type: content
ms.openlocfilehash: 90f24550d2bb50147bab6be545be63c1838f312a
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/10/2017
---
<a name="webmatrix-readme"></a><span data-ttu-id="42597-103">Archivo Léame de WebMatrix</span><span class="sxs-lookup"><span data-stu-id="42597-103">WebMatrix Readme</span></span>
====================
<span data-ttu-id="42597-104">13 de enero de 2011</span><span class="sxs-lookup"><span data-stu-id="42597-104">13 January 2011</span></span>

## <a name="contents"></a><span data-ttu-id="42597-105">Contenido</span><span class="sxs-lookup"><span data-stu-id="42597-105">Contents</span></span>

> [!NOTE]
> <span data-ttu-id="42597-106">Este archivo Léame se aplica a la 1.0 versión de WebMatrix.</span><span class="sxs-lookup"><span data-stu-id="42597-106">This readme applies to the 1.0 release of WebMatrix.</span></span>


- [<span data-ttu-id="42597-107">Información general</span><span class="sxs-lookup"><span data-stu-id="42597-107">Overview</span></span>](#Overview)
- [<span data-ttu-id="42597-108">Instalación</span><span class="sxs-lookup"><span data-stu-id="42597-108">Installation</span></span>](#Installation_Notes)
- [<span data-ttu-id="42597-109">Cómo publicar aplicaciones</span><span class="sxs-lookup"><span data-stu-id="42597-109">How to Publish Applications</span></span>](#InstructionsForPublishingApplications)
- [<span data-ttu-id="42597-110">Problemas y cambios</span><span class="sxs-lookup"><span data-stu-id="42597-110">Changes and Issues</span></span>](#ChangesAndIssues)

    - [<span data-ttu-id="42597-111">Instalación de WebMatrix 1.0</span><span class="sxs-lookup"><span data-stu-id="42597-111">WebMatrix 1.0 Installation</span></span>](#Known_Issues_Installation)
    - <span data-ttu-id="42597-112">[ASP.NET Web Pages](#Known_Issues_ASPNET) (Más información sobre páginas web de ASP.NET)</span><span class="sxs-lookup"><span data-stu-id="42597-112">[ASP.NET Web Pages](#Known_Issues_ASPNET)</span></span>
    - [<span data-ttu-id="42597-113">WebMatrix</span><span class="sxs-lookup"><span data-stu-id="42597-113">WebMatrix</span></span>](#Known_Issues_WebMatrix)
    - [<span data-ttu-id="42597-114">IIS Express</span><span class="sxs-lookup"><span data-stu-id="42597-114">IIS Express</span></span>](#Known_Issues_IISExpress)
    - [<span data-ttu-id="42597-115">SQL Server Compact</span><span class="sxs-lookup"><span data-stu-id="42597-115">SQL Server Compact</span></span>](#Known_Issues_SQLServerCompact)
    - [<span data-ttu-id="42597-116">Instalación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="42597-116">Installing Applications</span></span>](#Known_Issues_Installing_Applications)
    - [<span data-ttu-id="42597-117">Publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="42597-117">Publishing Applications</span></span>](#Known_Issues_Publishing_Applications)
- [<span data-ttu-id="42597-118">Para obtener más información</span><span class="sxs-lookup"><span data-stu-id="42597-118">For More Information</span></span>](#More_Info)

<a id="Overview"></a>

## <a name="overview"></a><span data-ttu-id="42597-119">Información general</span><span class="sxs-lookup"><span data-stu-id="42597-119">Overview</span></span>

> <span data-ttu-id="42597-120">Microsoft WebMatrix 1.0 es una pila de desarrollo web gratuita que se instala en pocos minutos.</span><span class="sxs-lookup"><span data-stu-id="42597-120">Microsoft WebMatrix 1.0 is a free web development stack that installs in minutes.</span></span> <span data-ttu-id="42597-121">Se integra un servidor web con la base de datos y marcos de trabajo para crear una única experiencia integrada de programación.</span><span class="sxs-lookup"><span data-stu-id="42597-121">It integrates a web server with database and programming frameworks to create a single, integrated experience.</span></span> <span data-ttu-id="42597-122">Puede usar WebMatrix para agilizar la manera de codificar, probar y publicar su propio sitio Web ASP.NET o PHP, o puede usar WebMatrix para iniciar un nuevo sitio Web mediante aplicaciones populares de código abierto como DotNetNuke, Umbraco, WordPress o Joomla.</span><span class="sxs-lookup"><span data-stu-id="42597-122">You can use WebMatrix to streamline the way you code, test, and publish your own ASP.NET or PHP website, or you can use WebMatrix to start a new website using popular open-source apps like DotNetNuke, Umbraco, WordPress, or Joomla.</span></span> <span data-ttu-id="42597-123">WebMatrix usa el mismo servidor web eficaz, el motor de base de datos y el entorno de marcos de trabajo que se ejecutará el sitio Web en internet, lo que hace la transición de desarrollo a producción ágil y sin inconvenientes.</span><span class="sxs-lookup"><span data-stu-id="42597-123">WebMatrix uses the same powerful web server, database engine, and frameworks environment that will run your website on the internet, which makes the transition from development to production smooth and seamless.</span></span>


<a id="Installation_Notes"></a>

## <a name="installation"></a><span data-ttu-id="42597-124">Instalación</span><span class="sxs-lookup"><span data-stu-id="42597-124">Installation</span></span>

> <span data-ttu-id="42597-125">Para instalar WebMatrix 1.0, primero debe instalar la [Microsoft Web Platform Installer 3.0](https://go.microsoft.com/fwlink/?LinkID=194638).</span><span class="sxs-lookup"><span data-stu-id="42597-125">To install WebMatrix 1.0, you must first install the [Microsoft Web Platform Installer 3.0](https://go.microsoft.com/fwlink/?LinkID=194638).</span></span> <span data-ttu-id="42597-126">Después de instalar al instalador de plataforma Web, se puede utilizar para instalar WebMatrix.</span><span class="sxs-lookup"><span data-stu-id="42597-126">After you've installed the Web Platform Installer, you can use it to install WebMatrix.</span></span>
> 
> <span data-ttu-id="42597-127">Si tiene problemas durante la instalación, consulte [solución de problemas con el instalador de plataforma Web de Microsoft](https://go.microsoft.com/fwlink/?LinkId=196212).</span><span class="sxs-lookup"><span data-stu-id="42597-127">If you have problems during installation, refer to [Troubleshooting Problems with Microsoft Web Platform Installer](https://go.microsoft.com/fwlink/?LinkId=196212).</span></span>


<a id="InstructionsForPublishingApplications"></a>
## <a name="how-to-publish-applications"></a><span data-ttu-id="42597-128">Cómo publicar aplicaciones</span><span class="sxs-lookup"><span data-stu-id="42597-128">How to Publish Applications</span></span>

> <span data-ttu-id="42597-129">Vea [instrucciones paso a paso para publicar aplicaciones](https://go.microsoft.com/fwlink/?LinkID=196149)</span><span class="sxs-lookup"><span data-stu-id="42597-129">See [Step-by-Step Instructions for Publishing Applications](https://go.microsoft.com/fwlink/?LinkID=196149)</span></span>


<a id="ChangesAndIssues"></a>

## <a name="changes-and-issues"></a><span data-ttu-id="42597-130">Problemas y cambios</span><span class="sxs-lookup"><span data-stu-id="42597-130">Changes and Issues</span></span>

<a id="Known_Issues_Installation"></a>

### <a name="webmatrix-10-installation-issues"></a><span data-ttu-id="42597-131">Problemas de instalación de 1.0 de WebMatrix</span><span class="sxs-lookup"><span data-stu-id="42597-131">WebMatrix 1.0 Installation Issues</span></span>

#### <a name="issue-webmatrix-10-is-available-only-on-platforms-that-support-microsoft-net-framework-4"></a><span data-ttu-id="42597-132">Problema: WebMatrix 1.0 está disponible solo en plataformas compatibles con Microsoft .NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="42597-132">Issue: WebMatrix 1.0 is available only on platforms that support Microsoft .NET Framework 4</span></span>

> <span data-ttu-id="42597-133">La versión 4 de .NET Framework es necesaria para WebMatrix.</span><span class="sxs-lookup"><span data-stu-id="42597-133">The .NET Framework version 4 is required for WebMatrix.</span></span> <span data-ttu-id="42597-134">En algunos casos, el programa de instalación de 1.0 de WebMatrix le permitirá intente instalar en una plataforma que no forma parte del conjunto de configuración admitidos.</span><span class="sxs-lookup"><span data-stu-id="42597-134">In certain cases, the WebMatrix 1.0 installer will let you try to install on a platform that is not part of the supported configuration set.</span></span> <span data-ttu-id="42597-135">En concreto, Windows Vista sin la actualización de SP1 le permiten comenzar la instalación de WebMatrix, pero producirá un error en el componente de .NET Framework 4 y bloquear la instalación.</span><span class="sxs-lookup"><span data-stu-id="42597-135">In particular, Windows Vista without the SP1 update will let you begin the installation of WebMatrix, but the .NET Framework 4 component will fail and block your installation.</span></span>
> 
> <span data-ttu-id="42597-136">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-136">**Workaround**</span></span>  
> <span data-ttu-id="42597-137">Instalar en una plataforma compatible, que incluye:</span><span class="sxs-lookup"><span data-stu-id="42597-137">Install on a supported platform, which includes:</span></span>
> 
> - <span data-ttu-id="42597-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42597-138">Windows 7</span></span>
> - <span data-ttu-id="42597-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42597-139">Windows Server 2008</span></span>
> - <span data-ttu-id="42597-140">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42597-140">Windows Server 2008 R2</span></span>
> - <span data-ttu-id="42597-141">Windows Vista SP1 o posterior</span><span class="sxs-lookup"><span data-stu-id="42597-141">Windows Vista SP1 or later</span></span>
> - <span data-ttu-id="42597-142">Windows XP SP3</span><span class="sxs-lookup"><span data-stu-id="42597-142">Windows XP SP3</span></span>
> - <span data-ttu-id="42597-143">Windows Server 2003 SP2</span><span class="sxs-lookup"><span data-stu-id="42597-143">Windows Server 2003 SP2</span></span>


#### <a name="issue-cannot-install-webmatrix-10-if-microsoft-visual-studio-2008-is-installed-without-microsoft-visual-studio-2008-sp1"></a><span data-ttu-id="42597-144">Problema: No se puede instalar WebMatrix 1.0 si se instala Microsoft Visual Studio 2008 sin Microsoft Visual Studio 2008 SP1</span><span class="sxs-lookup"><span data-stu-id="42597-144">Issue: Cannot install WebMatrix 1.0 if Microsoft Visual Studio 2008 is installed without Microsoft Visual Studio 2008 SP1</span></span>

> <span data-ttu-id="42597-145">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-145">**Workaround**</span></span>  
> <span data-ttu-id="42597-146">Instalar [Microsoft Visual Studio 2008 SP1](https://www.microsoft.com/downloads/details.aspx?FamilyId=FBEE1648-7106-44A7-9649-6D9F6D58056E&amp;displaylang=en) desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="42597-146">Install [Microsoft Visual Studio 2008 SP1](https://www.microsoft.com/downloads/details.aspx?FamilyId=FBEE1648-7106-44A7-9649-6D9F6D58056E&amp;displaylang=en) from the Microsoft Download Center.</span></span>


#### <a name="issue-some-assemblies-for-sql-server-compact-40-are-not-installed-in-the-gac"></a><span data-ttu-id="42597-147">Problema: Algunos ensamblados de SQL Server Compact 4.0 no están instalados en la GAC</span><span class="sxs-lookup"><span data-stu-id="42597-147">Issue: Some assemblies for SQL Server Compact 4.0 are not installed in the GAC</span></span>

> <span data-ttu-id="42597-148">Los ensamblados administrados para SQL Server Compact 4.0 no se colocan en la caché de ensamblados global (GAC) al instalar SQL Server Compact 4.0 en un equipo de 64 bits y el equipo tiene solo el .NET Framework 3.5 SP1 Client Profile instalado.</span><span class="sxs-lookup"><span data-stu-id="42597-148">The managed assemblies for SQL Server Compact 4.0 are not placed in the global assembly cache (GAC) when you install SQL Server Compact 4.0 on a 64-bit computer and the computer has only the .NET Framework 3.5 SP1 Client Profile installed.</span></span> <span data-ttu-id="42597-149">Son los ensamblados administrados que no están instalados en la GAC:</span><span class="sxs-lookup"><span data-stu-id="42597-149">The managed assemblies that are not installed in the GAC are:</span></span>
> 
> - <span data-ttu-id="42597-150">*System.Data.SqlServerCe.dll* (proveedor de ADO.NET)</span><span class="sxs-lookup"><span data-stu-id="42597-150">*System.Data.SqlServerCe.dll* (ADO.NET provider)</span></span>
> - <span data-ttu-id="42597-151">*System.Data.SqlServerCe.Entity.dll* (ADO.NET Entity Framework)</span><span class="sxs-lookup"><span data-stu-id="42597-151">*System.Data.SqlServerCe.Entity.dll* (ADO.NET Entity Framework )</span></span>
> 
> <span data-ttu-id="42597-152">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-152">**Workaround**</span></span>  
> <span data-ttu-id="42597-153">Desinstalar SQL Server Compact 4.0.</span><span class="sxs-lookup"><span data-stu-id="42597-153">Uninstall SQL Server Compact 4.0.</span></span> <span data-ttu-id="42597-154">Descargue e instale la versión completa de .NET Framework 3.5 SP1 desde la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="42597-154">Download and install the full version of .NET Framework 3.5 SP1 from the following location:</span></span>  
>   
> [<span data-ttu-id="42597-155">Microsoft .NET Framework 3.5 con Service Pack1 (paquete completo)</span><span class="sxs-lookup"><span data-stu-id="42597-155">Microsoft .NET Framework 3.5 Service pack 1 (Full Package)</span></span>](https://go.microsoft.com/fwlink/?LinkId=194828)  
>   
> <span data-ttu-id="42597-156">A continuación, vuelva a instalar SQL Server Compact 4.0.</span><span class="sxs-lookup"><span data-stu-id="42597-156">Then reinstall SQL Server Compact 4.0.</span></span>


#### <a name="issue-cannot-uninstall-sql-server-compact-using-the-command-line"></a><span data-ttu-id="42597-157">Problema: No se puede desinstalar SQL Server Compact usando la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="42597-157">Issue: Cannot uninstall SQL Server Compact using the command line</span></span>

> <span data-ttu-id="42597-158">Desinstalación de SQL Server Compact usando opciones de línea de comandos no funciona en esta versión.</span><span class="sxs-lookup"><span data-stu-id="42597-158">Uninstallation of SQL Server Compact using command-line options does not work in this release.</span></span>
> 
> <span data-ttu-id="42597-159">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-159">**Workaround**</span></span>  
> <span data-ttu-id="42597-160">Use *programas y características* en el Panel de Control de Windows para desinstalar Microsoft SQL Server Compact 4.0.</span><span class="sxs-lookup"><span data-stu-id="42597-160">Use *Programs and Features* in the Windows Control Panel to uninstall Microsoft SQL Server Compact 4.0.</span></span>


<a id="Known_Issues_ASPNET"></a>

### <a name="aspnet-web-pages"></a><span data-ttu-id="42597-161">ASP.NET Web Pages</span><span class="sxs-lookup"><span data-stu-id="42597-161">ASP.NET Web Pages</span></span>

<span data-ttu-id="42597-162">Esta sección del documento describe nuevas características, los cambios y los problemas conocidos con la 1.0 versión de ASP.NET Web Pages con sintaxis Razor.</span><span class="sxs-lookup"><span data-stu-id="42597-162">This section of the document describes new features, changes, and known issues with the 1.0 release of ASP.NET Web Pages with Razor syntax.</span></span>

- [<span data-ttu-id="42597-163">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="42597-163">New features</span></span>](#NewFeatures)
- [<span data-ttu-id="42597-164">Cambios</span><span class="sxs-lookup"><span data-stu-id="42597-164">Changes</span></span>](#Changes)
- [<span data-ttu-id="42597-165">Problemas</span><span class="sxs-lookup"><span data-stu-id="42597-165">Issues</span></span>](#Issues)

#### <a id="NewFeatures"></a><span data-ttu-id="42597-166">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="42597-166">New Features</span></span>

#### <a name="new-configuration-setting-added-to-disable-the-package-manager"></a><span data-ttu-id="42597-167">Nuevo: Agrega la opción de configuración para deshabilitar al administrador de paquetes</span><span class="sxs-lookup"><span data-stu-id="42597-167">New: Configuration setting added to disable the package manager</span></span>

> <span data-ttu-id="42597-168">Un nuevo `asp:AdminManagerEnabled` clave está disponible para el `<appSettings>` elemento en el *web.config* archivo, que le permite deshabilitar por completo el Administrador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="42597-168">A new `asp:AdminManagerEnabled` key is available for the `<appSettings>` element in the *web.config* file, which lets you completely disable the package manager.</span></span> <span data-ttu-id="42597-169">El valor predeterminado de este elemento es true, lo que significa que si no se incluye en el *web.config* archivo, el Administrador de paquetes está habilitado.</span><span class="sxs-lookup"><span data-stu-id="42597-169">The default value for this element is true, meaning that if it is not included in the *web.config* file, the package manager is enabled.</span></span> <span data-ttu-id="42597-170">Para deshabilitar el Administrador de paquetes, agregue el siguiente elemento en el *web.config* archivo en la raíz del sitio Web:</span><span class="sxs-lookup"><span data-stu-id="42597-170">To disable the package manager, add the following element to the *web.config* file in the root of the website:</span></span>
> 
> [!code-xml[Main](overview/samples/sample1.xml)]


#### <a id="Changes"></a><span data-ttu-id="42597-171">Cambios</span><span class="sxs-lookup"><span data-stu-id="42597-171">Changes</span></span>

#### <a name="change-webpagesadminfoldervirtualpath-key-renamed-to-aspadminfoldervirtualpath"></a><span data-ttu-id="42597-172">Cambiar: la clave de "webPages:AdminFolderVirtualPath" cambiada a "asp: AdminFolderVirtualPath"</span><span class="sxs-lookup"><span data-stu-id="42597-172">Change: "webPages:AdminFolderVirtualPath" key renamed to "asp:AdminFolderVirtualPath"</span></span>

> <span data-ttu-id="42597-173">El `webPages:AdminFolderVirtualPath` clave que puede agregarse a la *web.config* archivo para especificar la ubicación del Administrador de paquetes se cambió para usar el `asp:` espacio de nombres en lugar de la `webPages` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="42597-173">The `webPages:AdminFolderVirtualPath` key that can be added to the *web.config* file to specify the location of the package manager has been renamed to use the `asp:` namespace instead of the `webPages` namespace.</span></span> <span data-ttu-id="42597-174">Si ha usado este elemento, debe cambiar el nombre del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="42597-174">If you have used this element, you must rename it in the configuration file.</span></span>


#### <a id="Issues"></a><span data-ttu-id="42597-175">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="42597-175">Known Issues</span></span>

#### <a name="issue-passwords-for-membership-users-no-longer-recognized"></a><span data-ttu-id="42597-176">Problema: Contraseñas para los usuarios de pertenencia que ya no se reconoce</span><span class="sxs-lookup"><span data-stu-id="42597-176">Issue: Passwords for membership users no longer recognized</span></span>

> <span data-ttu-id="42597-177">El algoritmo para crear y almacenar contraseñas de pertenencia (inicio de sesión) se cambió para que sea más seguro.</span><span class="sxs-lookup"><span data-stu-id="42597-177">The algorithm for creating and storing membership (login) passwords has been changed to be more secure.</span></span> <span data-ttu-id="42597-178">Como resultado, no se reconocerá las contraseñas almacenadas para los miembros (usuarios) creados en las versiones Beta de ASP.NET Razor.</span><span class="sxs-lookup"><span data-stu-id="42597-178">As a result, the passwords stored for members (users) created in Beta versions of ASP.NET Razor will not be recognized.</span></span> 
> 
> <span data-ttu-id="42597-179">**Solución alternativa** si el sitio aún no se han colocado en producción, quite los registros de usuario de la base de datos de pertenencia.</span><span class="sxs-lookup"><span data-stu-id="42597-179">**Workaround** If the site has not yet been put into production, remove the user records from the membership database.</span></span> <span data-ttu-id="42597-180">Si activa la base de datos, volver a generar mediante programación las contraseñas existentes en la base de datos de pertenencia.</span><span class="sxs-lookup"><span data-stu-id="42597-180">If database is live, programmatically regenerate existing passwords in the membership database.</span></span>


#### <a name="issue-unexpected-behavior-when-using-a-custom-user-table-for-membership"></a><span data-ttu-id="42597-181">Problema: Un comportamiento inesperado cuando se usa una tabla de usuario personalizada para la suscripción</span><span class="sxs-lookup"><span data-stu-id="42597-181">Issue: Unexpected behavior when using a custom user table for membership</span></span>

> <span data-ttu-id="42597-182">Para inicializar el proveedor de pertenencia para un sitio Web de ASP.NET Razor, se llama a la `WebSecurity.InitializeDatabaseConnection` método.</span><span class="sxs-lookup"><span data-stu-id="42597-182">To initialize the membership provider for an ASP.NET Razor website, you call the `WebSecurity.InitializeDatabaseConnection` method.</span></span> <span data-ttu-id="42597-183">(En WebMatrix, la plantilla de sitio de inicio incluye una llamada a este método en el  *\_AppStart.cshtml* archivo.) Si el `autoCreateTables` parámetro de este método se establece en true (de forma predeterminada, se establece en true en la plantilla de sitio de inicio), y si se pasa un nombre de tabla no reconocida para el método (el segundo parámetro), el método no produce un error.</span><span class="sxs-lookup"><span data-stu-id="42597-183">(In WebMatrix, the Starter Site template includes a call to this method in the *\_AppStart.cshtml* file.) If the `autoCreateTables` parameter of this method is set to true (by default, it is set to true in the Starter Site template), and if an unrecognized table name is passed to the method (the second parameter), the method does not throw an error.</span></span> <span data-ttu-id="42597-184">En su lugar, crea automáticamente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="42597-184">Instead, it automatically creates the table.</span></span>
> 
> <span data-ttu-id="42597-185">Esto puede ser un problema si va a utilizar una tabla de usuario personalizada para la pertenencia a pero pase el nombre de tabla incorrecto para el `WebSecurity.InitializeDatabaseConnection` método.</span><span class="sxs-lookup"><span data-stu-id="42597-185">This can be a problem if you intend to use a custom user table for membership but pass the wrong table name to the `WebSecurity.InitializeDatabaseConnection` method.</span></span> <span data-ttu-id="42597-186">Dado que el método no predeterminada genera un error si no existe en la tabla que especifique, y porque en su lugar, crea una nueva tabla, la aplicación puede parecer que va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="42597-186">Because the method does not by default raise an error if the table you specify does not exist, and because it instead creates a new table, the application can appear to be working.</span></span> <span data-ttu-id="42597-187">Sin embargo, código de aplicación que se basa en una tabla de usuario personalizada (y en los campos de él) puede producir un error con errores inesperados.</span><span class="sxs-lookup"><span data-stu-id="42597-187">However, application code that relies on your custom user table (and on fields in it) can eventually fail with unexpected errors.</span></span>
> 
> <span data-ttu-id="42597-188">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-188">**Workaround**</span></span>  
> <span data-ttu-id="42597-189">Asegúrese de que el nombre se pasa en el `InitializeDatabaseConnection` coincidencias de método, el perfil de usuario de la tabla en la base de datos de pertenencia, o asegúrese de que el `autoCreateTables` parámetro se establece en false.</span><span class="sxs-lookup"><span data-stu-id="42597-189">Make sure that the name passed in the `InitializeDatabaseConnection` method matches the user profile table in the membership database, or make sure that the `autoCreateTables` parameter is set to false.</span></span>


#### <a name="issue-error-message-the-admin-module-requires-access-to-appdata"></a><span data-ttu-id="42597-190">Problema: Mensaje de Error "el módulo de administración requiere acceso a ~/App\_datos"</span><span class="sxs-lookup"><span data-stu-id="42597-190">Issue: Error message "The Admin Module requires access to ~/App\_Data"</span></span>

> <span data-ttu-id="42597-191">En algunas circunstancias, intenta crear usuarios o en caso contrario, trabajar con el sistema de pertenencia ASP.NET puede dar lugar a la página para mostrar el error *el módulo de administración requiere acceso a ~/App\_datos*.</span><span class="sxs-lookup"><span data-stu-id="42597-191">Under some circumstances, trying to create users or otherwise work with the ASP.NET membership system can cause the page to display the error *The Admin Module requires access to ~/App\_Data*.</span></span> <span data-ttu-id="42597-192">Esto ocurre si la cuenta que se está ejecutando IIS o IIS Express no tiene permisos para crear y escribir en el *aplicación\_datos* carpeta bajo la raíz del sitio Web.</span><span class="sxs-lookup"><span data-stu-id="42597-192">This occurs if the account that IIS or IIS Express is running under does not have permissions to create and write to the *App\_Data* folder under the website root.</span></span> 
> 
> <span data-ttu-id="42597-193">**Solución alternativa** crear manualmente un *aplicación\_datos* carpeta para el sitio Web.</span><span class="sxs-lookup"><span data-stu-id="42597-193">**Workaround** Manually create an *App\_Data* folder for the website.</span></span> <span data-ttu-id="42597-194">Asegúrese de que la cuenta de Windows que se ejecuta la aplicación (normalmente el servicio de red) tiene permisos de lectura/escritura para las carpetas raíz de la aplicación y para las subcarpetas, como aplicación\_datos.</span><span class="sxs-lookup"><span data-stu-id="42597-194">Then make sure that the Windows account that the application runs under (typically NETWORK SERVICE) has read/write permissions for root folders of the application and for subfolders such as App\_Data.</span></span> <span data-ttu-id="42597-195">Hay información más detallada en el artículo de Knowledge Base [problemas con instancias de usuario de SQL Server Express y proyectos de aplicación Web de ASP.net](https://support.microsoft.com/kb/2002980).</span><span class="sxs-lookup"><span data-stu-id="42597-195">More detailed information is available in the KnowledgeBase article [Problems with SQL Server Express user instancing and ASP.net Web Application Projects](https://support.microsoft.com/kb/2002980).</span></span>


#### <a name="issue-failed-to-generate-a-user-instance-of-sql-server-error"></a><span data-ttu-id="42597-196">Problema: "error no se pudo generar una instancia de usuario de SQL Server"</span><span class="sxs-lookup"><span data-stu-id="42597-196">Issue: "Failed to generate a user instance of SQL Server" error</span></span>

> <span data-ttu-id="42597-197">Si una aplicación WebMatrix Web usa SQL Server Express y ejecuta IIS 7.5 en Windows 7 o Windows Server 2008 R2, verá un error que indica que SQL Server no se puede recuperar la ruta de acceso de aplicación local del usuario en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="42597-197">If a WebMatrix Web application uses SQL Server Express and is running IIS 7.5 on Windows 7 or Windows Server 2008 R2, you might see an error that indicates that SQL Server cannot retrieve the user's local application path at run time.</span></span>
> 
> <span data-ttu-id="42597-198">**Solución alternativa** Asegúrese de que la cuenta de Windows que se ejecuta la aplicación (normalmente el servicio de red) tiene permisos de lectura/escritura para las carpetas raíz de la aplicación y para las subcarpetas como *aplicación\_datos*.</span><span class="sxs-lookup"><span data-stu-id="42597-198">**Workaround** Make sure that the Windows account that the application runs under (typically NETWORK SERVICE) has read/write permissions for root folders of the application and for subfolders such as *App\_Data*.</span></span> <span data-ttu-id="42597-199">Hay información más detallada en el artículo de Knowledge Base [problemas con instancias de usuario de SQL Server Express y proyectos de aplicación Web de ASP.net](https://support.microsoft.com/kb/2002980).</span><span class="sxs-lookup"><span data-stu-id="42597-199">More detailed information is available in the KnowledgeBase article [Problems with SQL Server Express user instancing and ASP.net Web Application Projects](https://support.microsoft.com/kb/2002980).</span></span>


#### <a name="issue-files-that-contains-package-manager-resources-or-package-manager-passwords-are-servable-under-iis-60-and-earlier"></a><span data-ttu-id="42597-200">Problema: Los archivos que contiene recursos del Administrador de paquetes o las contraseñas de administrador de paquetes son servable en IIS 6.0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="42597-200">Issue: Files that contains package-manager resources or package-manager passwords are servable under IIS 6.0 and earlier</span></span>

> <span data-ttu-id="42597-201">Si implementa una aplicación de ASP.NET Web Pages (Razor) que se compiló con la versión de RC2, y si la aplicación contiene un *password.txt* o *packagesources.txt* de archivos en   */App\_ Datos/admin*, IIS 6.0 se usará el archivo si se solicita, puede exponer las contraseñas para la instancia del Administrador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="42597-201">If you deploy an ASP.NET Web Pages (Razor) application that was built using the RC2 release, and if the application contains a *password.txt* or *packagesources.txt* file under */App\_Data/admin*, IIS 6.0 will serve the file if requested, potentially exposing the passwords for your package manager instance.</span></span> 
> 
> <span data-ttu-id="42597-202">**Solución alternativa** cambiar el nombre de la *password.txt* o *packagesources.txt* del archivo a *password.config* o *packagesources.config*. De forma predeterminada, IIS 6.0 no sirve a archivos que tienen la *.config* extensión.</span><span class="sxs-lookup"><span data-stu-id="42597-202">**Workaround** Rename the *password.txt* or *packagesources.txt* file to *password.config* or *packagesources.config*. By default, IIS 6.0 does not serve files that have the *.config* extension.</span></span> <span data-ttu-id="42597-203">(En IIS 7, no hay archivos en el *aplicación\_datos* carpeta se atienden, por lo que no es necesario cambiar el nombre de los archivos.)</span><span class="sxs-lookup"><span data-stu-id="42597-203">(In IIS 7, no files in the *App\_Data* folder are served, so you do not need to rename the files.)</span></span>


#### <a name="issue-uninstalling-packages-installed-using-the-beta-3-release-does-not-completely-remove-package-components"></a><span data-ttu-id="42597-204">Problema: Desinstalación de paquetes instalados con la versión Beta 3 no quitar completamente los componentes de paquete</span><span class="sxs-lookup"><span data-stu-id="42597-204">Issue: Uninstalling packages installed using the Beta 3 release does not completely remove package components</span></span>

> <span data-ttu-id="42597-205">Si instaló un paquete mediante el Administrador de paquetes en la versión Beta 3 y, a continuación, intentar desinstalar mediante la versión actual, el paquete no se desinstaló totalmente.</span><span class="sxs-lookup"><span data-stu-id="42597-205">If you installed a package using the package manager in the Beta 3 release and then try to uninstall it using the current release, the package is not completely uninstalled.</span></span> <span data-ttu-id="42597-206">Mediante el Administrador de paquetes **desinstalar** botón quita algunos componentes, pero deje el código de biblioteca del paquete y no actualiza el *package.config* archivo.</span><span class="sxs-lookup"><span data-stu-id="42597-206">Using the package manager's **Uninstall** button removes some components, but leaves the package's library code and does not update the *package.config* file.</span></span>
> 
> <span data-ttu-id="42597-207">**Solución alternativa** </span><span class="sxs-lookup"><span data-stu-id="42597-207">**Workaround** </span></span>  
> <span data-ttu-id="42597-208">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="42597-208">Perform these steps:</span></span>  
> 1. <span data-ttu-id="42597-209">Eliminar el *aplicación\_Data\packages* carpeta.</span><span class="sxs-lookup"><span data-stu-id="42597-209">Delete the *App\_Data\packages* folder.</span></span> <span data-ttu-id="42597-210">Esto quita todos los paquetes.</span><span class="sxs-lookup"><span data-stu-id="42597-210">This removes all packages.</span></span>   
> 2. <span data-ttu-id="42597-211">Eliminar el *packages.config* archivo en la raíz del sitio Web.</span><span class="sxs-lookup"><span data-stu-id="42597-211">Delete the *packages.config* file in the root of the website.</span></span>


#### <a name="issue-in-visual-studio-invoking-the-web-based-package-manager-takes-the-application-offline"></a><span data-ttu-id="42597-212">Problema: En Visual Studio, invocar el Administrador de paquetes basados en web requiere la aplicación sin conexión</span><span class="sxs-lookup"><span data-stu-id="42597-212">Issue: In Visual Studio, invoking the web-based package manager takes the application offline</span></span>

> <span data-ttu-id="42597-213">Si está trabajando en Visual Studio (no WebMatrix) y use la  *\_administración* funcionalidad para iniciar el Administrador de paquetes, Visual Studio deja sin conexión la aplicación y registra el *aplicación\_ offline.htm* en la raíz del sitio Web, que interrumpen su capacidad para usar el Administrador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="42597-213">If you are working in Visual Studio (not WebMatrix) and use the *\_admin* functionality to start the package manager, Visual Studio takes the application offline and posts the *app\_offline.htm* into the website root, which disrupts your ability to use the package manager.</span></span>
> 
> [!NOTE]
> <span data-ttu-id="42597-214">Aunque normalmente verá este comportamiento cuando se usa la interfaz del Administrador de paquetes basada en web, el mismo comportamiento se produce si agregar, quitar o modificar los archivos de la *aplicación\_datos* carpeta.</span><span class="sxs-lookup"><span data-stu-id="42597-214">Although you would most typically see this behavior when using the web-based package manager interface, the same behavior occurs if you add, remove, or modify any files in the *App\_Data* folder.</span></span>
> 
> <span data-ttu-id="42597-215">**Solución alternativa** </span><span class="sxs-lookup"><span data-stu-id="42597-215">**Workaround** </span></span>  
> <span data-ttu-id="42597-216">Para trabajar con paquetes en Visual Studio, utilice la extensión de NuGet en lugar del Administrador de paquetes basados en web.</span><span class="sxs-lookup"><span data-stu-id="42597-216">To work with packages in Visual Studio, use the NuGet extension instead of the web-based package manager.</span></span> <span data-ttu-id="42597-217">Para obtener información, consulte el [documentación de NuGet](https://docs.microsoft.com/nuget/).</span><span class="sxs-lookup"><span data-stu-id="42597-217">For information, see the [NuGet documentation](https://docs.microsoft.com/nuget/).</span></span> <span data-ttu-id="42597-218">Si está trabajando con otros archivos en el *aplicación\_datos* carpeta, considere la posibilidad de mantener los archivos en otro lugar para evitar este problema.</span><span class="sxs-lookup"><span data-stu-id="42597-218">If you are working with other files in the *App\_Data* folder, consider keeping the files elsewhere to avoid this issue.</span></span> <span data-ttu-id="42597-219">Si esto no es práctico, elimine la *aplicación\_offline.htm* archivo manualmente o espere a que el sitio vuelve a conectarse automáticamente (de forma predeterminada, después de 30 segundos).</span><span class="sxs-lookup"><span data-stu-id="42597-219">If that's not practical, delete the *app\_offline.htm* file manually or wait until the site comes back online automatically (by default, after 30 seconds).</span></span>


#### <a name="issue-visual-studio-intellisense-and-project-templates-available-only-in-aspnet-mvc-version-3"></a><span data-ttu-id="42597-220">Problema: Visual Studio IntelliSense y proyecto de plantillas disponibles solo en ASP.NET MVC versión 3</span><span class="sxs-lookup"><span data-stu-id="42597-220">Issue: Visual Studio IntelliSense and project templates available only in ASP.NET MVC version 3</span></span>

> <span data-ttu-id="42597-221">Instalar ASP.NET Web Pages no instalar herramientas para Visual Studio como IntelliSense y proyecto de plantillas para aplicaciones de ASP.NET Web Pages.</span><span class="sxs-lookup"><span data-stu-id="42597-221">Installing ASP.NET Web Pages does not also install tools for Visual Studio such as IntelliSense and project templates for ASP.NET Web Pages applications.</span></span>
> 
> <span data-ttu-id="42597-222">**Solución alternativa** para usar las plantillas de proyecto y de IntelliSense para las aplicaciones de ASP.NET Web Pages en Visual Studio, instale ASP.NET MVC 3 RC ya sea mediante el instalador de plataforma Web o la [instalador independiente](https://go.microsoft.com/fwlink/?LinkID=191797).</span><span class="sxs-lookup"><span data-stu-id="42597-222">**Workaround** To use IntelliSense and project templates for ASP.NET Web Pages applications in Visual Studio, install ASP.NET MVC 3 RC either through the Web Platform Installer or the [stand-alone installer](https://go.microsoft.com/fwlink/?LinkID=191797).</span></span>


#### <a name="issue-reading-feeds-or-other-external-data-via-a-proxy-server"></a><span data-ttu-id="42597-223">Problema: Leer fuentes u otros datos externos a través de un servidor proxy</span><span class="sxs-lookup"><span data-stu-id="42597-223">Issue: Reading feeds or other external data via a proxy server</span></span>

> <span data-ttu-id="42597-224">Si el servidor que ejecuta el sitio está detrás de un servidor proxy, tendrá que configurar la información de proxy en el *web.config* archivo para poder leer la información que procede de fuera de su sitio.</span><span class="sxs-lookup"><span data-stu-id="42597-224">If the server running the site is behind a proxy server, you might need to configure proxy information in the *web.config* file in order to be able to read information that comes from outside your site.</span></span> <span data-ttu-id="42597-225">Por ejemplo, si usa el `ReCaptcha` auxiliar, el Ayudante se comunica con el servicio de reCAPTCHA, pero puede estar bloqueado por el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="42597-225">For example, if you use the `ReCaptcha` helper, the helper communicates with the reCAPTCHA service, but might be blocked by your proxy server.</span></span> <span data-ttu-id="42597-226">De forma similar, las fuentes que se utilizan en ASP.NET Web Pages, como la fuente utilizada por el Administrador de paquetes, podrían requerir configuración de proxy.</span><span class="sxs-lookup"><span data-stu-id="42597-226">Similarly, feeds that are used in ASP.NET Web Pages, such as the feed used by the package manager, might require proxy configuration.</span></span>
> 
> <span data-ttu-id="42597-227">Si tiene problemas de trabajar con un servicio externo o para trabajar con el paquete de fuente, coloque los elementos siguientes en la raíz de la aplicación *web.config* archivo:</span><span class="sxs-lookup"><span data-stu-id="42597-227">If you experience problems in working with an external service or working with the package feed, put the following elements into your application's root *web.config* file:</span></span>
> 
> [!code-xml[Main](overview/samples/sample2.xml)]
> 
> <span data-ttu-id="42597-228">Para obtener más información acerca de cómo configurar un servidor proxy, consulte [ &lt;proxy&gt; Element (Network Settings)](https://msdn.microsoft.com/en-us/library/sa91de1e.aspx) en el sitio Web de MSDN.</span><span class="sxs-lookup"><span data-stu-id="42597-228">For more information about configuring a proxy server, see [&lt;proxy&gt; Element (Network Settings)](https://msdn.microsoft.com/en-us/library/sa91de1e.aspx) on the MSDN Web site.</span></span>


#### <a name="issue-uninstalling-the-net-framework-version-4-disables-aspnet-web-pages-with-razor-syntax"></a><span data-ttu-id="42597-229">Problema: Desinstalar .NET Framework versión 4 deshabilita ASP.NET Web Pages con sintaxis Razor</span><span class="sxs-lookup"><span data-stu-id="42597-229">Issue: Uninstalling the .NET Framework version 4 disables ASP.NET Web Pages with Razor Syntax</span></span>

> <span data-ttu-id="42597-230">Si desinstala la versión 4 de .NET Framework y, a continuación, vuelva a instalarlo, se deshabilita ASP.NET Web Pages con sintaxis Razor.</span><span class="sxs-lookup"><span data-stu-id="42597-230">If you uninstall the .NET Framework version 4 and then reinstall it, ASP.NET Web Pages with Razor syntax is disabled.</span></span> <span data-ttu-id="42597-231">Páginas con la *.cshtml* extensión no se ejecutan correctamente.</span><span class="sxs-lookup"><span data-stu-id="42597-231">Pages with the *.cshtml* extension do not run correctly.</span></span> <span data-ttu-id="42597-232">Las páginas Web ASP.NET registra un ensamblado en la raíz de la máquina *web.config* archivo y quitar .NET Framework se elimina el archivo.</span><span class="sxs-lookup"><span data-stu-id="42597-232">ASP.NET Web Pages registers an assembly in the machine root *web.config* file, and removing the .NET Framework removes that file.</span></span> <span data-ttu-id="42597-233">Volver a instalar .NET Framework instala una nueva versión del archivo de configuración, pero no agrega la referencia del ensamblado de ASP.NET Web Pages.</span><span class="sxs-lookup"><span data-stu-id="42597-233">Reinstalling the .NET Framework installs a new version of the configuration file, but does not add the reference for the ASP.NET Web Pages assembly.</span></span>
> 
> <span data-ttu-id="42597-234">**Solución alternativa** después de reinstalar .NET Framework, vuelva a instalar ASP.NET Web Pages con sintaxis Razor.</span><span class="sxs-lookup"><span data-stu-id="42597-234">**Workaround** After reinstalling the .NET Framework, reinstall ASP.NET Web Pages with Razor syntax.</span></span> <span data-ttu-id="42597-235">Esto agrega el siguiente elemento a la *web.config* archivo en la raíz de la máquina, que se encuentra normalmente en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="42597-235">This adds the following element to the *web.config* file in the machine root, which is typically in the following location:</span></span>  
>   
> `C:\Windows\Microsoft.NET\Framework\v4.0.30319\Config (32-bit)`  
> `C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config (64-bit)`
> 
> [!code-xml[Main](overview/samples/sample3.xml)]


#### <a name="issue-extensionless-urls-do-not-find-cshtmlvbhtml-files-on-iis-7-or-iis-75"></a><span data-ttu-id="42597-236">Problema: Direcciones URL sin extensión no encuentran archivos.cshtml/.vbhtml en IIS 7 o IIS 7.5</span><span class="sxs-lookup"><span data-stu-id="42597-236">Issue: Extensionless URLs do not find .cshtml/.vbhtml files on IIS 7 or IIS 7.5</span></span>

> <span data-ttu-id="42597-237">En IIS 7 o IIS 7.5, las solicitudes con una dirección URL similar a la siguiente no están posible encontrar las páginas que tienen la *.cshtml* o *.vbhtml* extensión:</span><span class="sxs-lookup"><span data-stu-id="42597-237">On IIS 7 or IIS 7.5, requests with a URL like the following are not able to find pages that have the *.cshtml* or *.vbhtml* extension:</span></span>  
>   
> `http://www.example.com/ExampleSite/ExampleFile`  
>   
> <span data-ttu-id="42597-238">El problema se produce porque la reescritura de direcciones URL no está habilitada de forma predeterminada para IIS 7 o IIS 7.5.</span><span class="sxs-lookup"><span data-stu-id="42597-238">The issue arises because URL rewriting is not enabled by default for IIS 7 or IIS 7.5.</span></span> <span data-ttu-id="42597-239">El escenario más probable es que no se ve el problema al probar localmente mediante IIS Express, pero experimenta al implementar el sitio Web en un sitio Web de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="42597-239">The likeliest scenario is that you do not see the problem when testing locally using IIS Express, but you experience it when you deploy your website to a hosting website.</span></span>
> 
> <span data-ttu-id="42597-240">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-240">**Workaround**</span></span>
> 
> - <span data-ttu-id="42597-241">Si tiene control sobre el equipo del servidor, en el equipo servidor instale la actualización que se describe en [hay una actualización disponible que permite determinados controladores de IIS 7.0 o IIS 7.5 para controlar las solicitudes de direcciones URL no termina con un período](https://support.microsoft.com/kb/980368).</span><span class="sxs-lookup"><span data-stu-id="42597-241">If you have control over the server computer, on the server computer install the update that is described in [A update is available that enables certain IIS 7.0 or IIS 7.5 handlers to handle requests whose URLs do not end with a period](https://support.microsoft.com/kb/980368).</span></span>
> - <span data-ttu-id="42597-242">Si no tiene control sobre el equipo del servidor (por ejemplo, va a implementar en un sitio Web de hospedaje), agregue lo siguiente del sitio Web *web.config* archivo:</span><span class="sxs-lookup"><span data-stu-id="42597-242">If you do not have control over the server computer (for example, you are deploying to a hosting website), add the following to the website's *web.config* file:</span></span> 
> 
>     [!code-xml[Main](overview/samples/sample4.xml)]


#### <a name="issue-deploying-an-application-to-a-computer-that-does-not-have-sql-server-compact-installed"></a><span data-ttu-id="42597-243">Problema: Implementar una aplicación en un equipo que no tiene SQL Server Compact instalado</span><span class="sxs-lookup"><span data-stu-id="42597-243">Issue: Deploying an application to a computer that does not have SQL Server Compact installed</span></span>

> <span data-ttu-id="42597-244">Las aplicaciones que incluyen bases de datos de SQL Server Compact se pueden ejecutar en un equipo donde SQL Server Compact no está instalado.</span><span class="sxs-lookup"><span data-stu-id="42597-244">Applications that include SQL Server Compact databases can run on a computer where SQL Server Compact is not installed.</span></span> <span data-ttu-id="42597-245">Microsoft WebMatrix 1.0 automáticamente copia estos archivos binarios para usted y realiza la correspondiente *web.config* transformaciones de archivos.</span><span class="sxs-lookup"><span data-stu-id="42597-245">Microsoft WebMatrix 1.0 automatically copies these binaries for you and performs the appropriate *web.config* file transforms.</span></span>
> 
> <span data-ttu-id="42597-246">**Solución alternativa** si necesita copiar estos archivos y realizar la *web.config* cambios en los archivos manualmente, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="42597-246">**Workaround** If you need to copy these files and make the *web.config* file changes manually, do the following:</span></span>
> 
> 1. <span data-ttu-id="42597-247">Copie los ensamblados de motor de base de datos a la *Bin* carpeta (y sus subcarpetas) de la aplicación en el equipo de destino:</span><span class="sxs-lookup"><span data-stu-id="42597-247">Copy the database engine assemblies to the *Bin* folder (and subfolders) of the application on the target computer:</span></span>  
> 
>     - <span data-ttu-id="42597-248">Copia *C:\Program Files\Microsoft SQL Server Edition\v4.0\Desktop\System.Data.SqlServerCe.dll* </span><span class="sxs-lookup"><span data-stu-id="42597-248">Copy *C:\Program Files\Microsoft SQL Server Edition\v4.0\Desktop\System.Data.SqlServerCe.dll* </span></span>  
>         <span data-ttu-id="42597-249">**para** *\Bin*</span><span class="sxs-lookup"><span data-stu-id="42597-249">**to** *\Bin*</span></span>
>     - <span data-ttu-id="42597-250">Copia *C:\Program Files\Microsoft SQL Server Compact Edition\v4.0\Private\x86\\*** a***\Bin\x86*</span><span class="sxs-lookup"><span data-stu-id="42597-250">Copy *C:\Program Files\Microsoft SQL Server Compact Edition\v4.0\Private\x86\\****to***\Bin\x86*</span></span>
>     - <span data-ttu-id="42597-251">Copia *C:\Program Files\Microsoft SQL Server Compact Edition\v4.0\Private\amd64\\** **a***\Bin\amd64*</span><span class="sxs-lookup"><span data-stu-id="42597-251">Copy *C:\Program Files\Microsoft SQL Server Compact Edition\v4.0\Private\amd64\\** **to***\Bin\amd64*</span></span>
> 2. <span data-ttu-id="42597-252">En la carpeta raíz del sitio Web, cree o abra un *web.config* archivo.</span><span class="sxs-lookup"><span data-stu-id="42597-252">In the root folder of the website, create or open a *web.config* file.</span></span> <span data-ttu-id="42597-253">(En WebMatrix 1.0, está disponible si hace clic en este tipo de archivo **todos los** en el **elegir un tipo de archivo** cuadro de diálogo.)</span><span class="sxs-lookup"><span data-stu-id="42597-253">(In WebMatrix 1.0, this file type is available if you click **All** in the **Choose a File Type** dialog box.)</span></span>
> 3. <span data-ttu-id="42597-254">Agregue el siguiente elemento como elemento secundario de la `<configuration>` elemento (no en el `<system.web>` elemento):</span><span class="sxs-lookup"><span data-stu-id="42597-254">Add the following element as a child of the `<configuration>` element (not inside the `<system.web>` element):</span></span>
> 
>     [!code-xml[Main](overview/samples/sample5.xml)]


#### <a name="issue-database-and-webgrid-helpers-do-not-work-in-medium-trust-in-visual-basic"></a><span data-ttu-id="42597-255">Problema: "Base de datos" y "WebGrid" aplicaciones auxiliares no funcionan en el nivel de confianza medio en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="42597-255">Issue: "Database" and "WebGrid" helpers do not work in Medium Trust in Visual Basic</span></span>

> <span data-ttu-id="42597-256">Si está utilizando Visual Basic (crear *vbhtml* archivos), el `Database` y `WebGrid` aplicaciones auxiliares no funcionará si la aplicación está configurada para usar el nivel de confianza medio.</span><span class="sxs-lookup"><span data-stu-id="42597-256">If you are using Visual Basic (creating *.vbhtml* files), the `Database` and `WebGrid` helpers will not work if the application is set to use Medium Trust.</span></span>
> 
> <span data-ttu-id="42597-257">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-257">**Workaround**</span></span>  
> <span data-ttu-id="42597-258">Si usa Visual Studio 2010, puede resolver este problema mediante la instalación de la versión de Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="42597-258">If you use Visual Studio 2010, you can resolve this problem by installing the Service Pack 1 release.</span></span> <span data-ttu-id="42597-259">Hasta que esté disponible la versión final de la versión de SP1, puede descargar la versión Beta de SP1 desde el [Microsoft Visual Studio 2010 Service Pack 1 Beta](https://www.microsoft.com/downloads/en/details.aspx?FamilyID=11ea69cb-cf12-4842-a3d7-b32a1e5642e2&amp;displaylang=en) página en Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="42597-259">Until the final version of the SP1 release is available, you can download the Beta version of SP1 from the [Microsoft Visual Studio 2010 Service Pack 1 Beta](https://www.microsoft.com/downloads/en/details.aspx?FamilyID=11ea69cb-cf12-4842-a3d7-b32a1e5642e2&amp;displaylang=en) page on the Microsoft Download Center.</span></span>   
>   
> <span data-ttu-id="42597-260">Si esto no es práctico, o si no usa Visual Studio 2010, puede establece la aplicación para utilizar plena confianza.</span><span class="sxs-lookup"><span data-stu-id="42597-260">If this is not practical, or if you do not use Visual Studio 2010, you can temporarily set the application to use Full Trust.</span></span>


#### <a name="issue-applicationpart-resources-are-externally-accessible"></a><span data-ttu-id="42597-261">Problema: "ApplicationPart" recursos son accesibles desde el exterior</span><span class="sxs-lookup"><span data-stu-id="42597-261">Issue: "ApplicationPart" resources are externally accessible</span></span>

> <span data-ttu-id="42597-262">Si un ensamblado contiene objetos que se deriva de la `ApplicationPart` de la clase, que se exponen los recursos del ensamblado por el `ResourceRouteHandler` clase.</span><span class="sxs-lookup"><span data-stu-id="42597-262">If an assembly contains objects that derives from the `ApplicationPart` class, that assembly's resources are exposed by the `ResourceRouteHandler` class.</span></span> <span data-ttu-id="42597-263">Por ejemplo, considere la siguiente dirección URL:</span><span class="sxs-lookup"><span data-stu-id="42597-263">For example, consider the following URL:</span></span>  
>   
> `~/r.ashx/System.Web.WebPages.Administration/Resources/AdminResources.resources`  
>   
> <span data-ttu-id="42597-264">Esta solicitud de descarga todas las cadenas de recursos en el *System.Web.WebPages.Administration.dll* ensamblado.</span><span class="sxs-lookup"><span data-stu-id="42597-264">This request downloads all of the resource strings in the *System.Web.WebPages.Administration.dll* assembly.</span></span> <span data-ttu-id="42597-265">Se descargan todos los recursos incrustados (incluso aquellos que no están diseñados para ser sirve como contenido estático).</span><span class="sxs-lookup"><span data-stu-id="42597-265">All of the embedded resources (even those that are not intended to be served as static content) are downloaded.</span></span> <span data-ttu-id="42597-266">Si los recursos incrustados contienen información confidencial, esto puede representar un riesgo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="42597-266">If the embedded resources contain sensitive information, this can represent a security risk.</span></span> 
> 
> <span data-ttu-id="42597-267">**Solución alternativa** </span><span class="sxs-lookup"><span data-stu-id="42597-267">**Workaround** </span></span>  
> <span data-ttu-id="42597-268">Si crea un **ApplicationPart** de objetos, asegúrese de que los recursos incrustados asociados a ese **ApplicationPart** ensamblado del objeto no contienen información confidencial.</span><span class="sxs-lookup"><span data-stu-id="42597-268">If you create an **ApplicationPart** object, make sure that the embedded resources associated with that **ApplicationPart** object's assembly do not contain sensitive information.</span></span>


<a id="Known_Issues_WebMatrix"></a>

### <a name="webmatrix"></a><span data-ttu-id="42597-269">WebMatrix</span><span class="sxs-lookup"><span data-stu-id="42597-269">WebMatrix</span></span>

> [!NOTE]
> <span data-ttu-id="42597-270">Para obtener información acerca de los problemas de instalación de WebMatrix, consulte [problemas de instalación de WebMatrix](#Known_Issues_Installation) anteriormente en este documento.</span><span class="sxs-lookup"><span data-stu-id="42597-270">For information about installation issues for WebMatrix, see [WebMatrix Installation Issues](#Known_Issues_Installation) earlier in this document.</span></span>


<span data-ttu-id="42597-271">Esta sección del documento describen los problemas conocidos para el entorno de desarrollo de WebMatrix.</span><span class="sxs-lookup"><span data-stu-id="42597-271">This section of the document describes known issues for the WebMatrix development environment.</span></span>

#### <a name="issue-changes-in-the-username-or-password-of-a-database-connection-string-in-a-webconfig-file-are-not-reflected-in-the-databases-workspace"></a><span data-ttu-id="42597-272">Problema: No se reflejan los cambios en el nombre de usuario o la contraseña de una cadena de conexión de base de datos en un archivo web.config en el área de trabajo de las bases de datos</span><span class="sxs-lookup"><span data-stu-id="42597-272">Issue: Changes in the username or password of a database connection string in a web.config file are not reflected in the Databases workspace</span></span>

> <span data-ttu-id="42597-273">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-273">**Workaround**</span></span>  
> 
> 1. <span data-ttu-id="42597-274">En el *web.config* de archivo, cambie el nombre de la base de datos en la cadena de conexión (por ejemplo, agregar "1" a él).</span><span class="sxs-lookup"><span data-stu-id="42597-274">In the *web.config* file, change the database name in the connection string (for example, add "1" to it).</span></span>
> 2. <span data-ttu-id="42597-275">Guardar el *web.config* archivo.</span><span class="sxs-lookup"><span data-stu-id="42597-275">Save the *web.config* file.</span></span>
> 3. <span data-ttu-id="42597-276">Haga clic en **bases de datos** y actualizar.</span><span class="sxs-lookup"><span data-stu-id="42597-276">Click **Databases** and refresh.</span></span>
> 4. <span data-ttu-id="42597-277">Cambiar el nombre de la base de datos en la cadena de conexión en el *web.config* archivo por el nombre de base de datos original.</span><span class="sxs-lookup"><span data-stu-id="42597-277">Change the database name in the connection string in the *web.config* file back to the original database name.</span></span>
> 5. <span data-ttu-id="42597-278">Guardar el *web.config* archivo.</span><span class="sxs-lookup"><span data-stu-id="42597-278">Save the *web.config* file.</span></span>
> 6. <span data-ttu-id="42597-279">Haga clic en **bases de datos** y actualizar.</span><span class="sxs-lookup"><span data-stu-id="42597-279">Click **Databases** and refresh.</span></span>


#### <a name="issue-folders-created-by-webmatrix-cannot-be-deleted"></a><span data-ttu-id="42597-280">Problema: No se puede eliminar carpetas que creó WebMatrix</span><span class="sxs-lookup"><span data-stu-id="42597-280">Issue: Folders created by WebMatrix cannot be deleted</span></span>

> <span data-ttu-id="42597-281">Si WebMatrix se ejecuta con permisos elevados (es decir, ha empezado a usar WebMatrix el **ejecutar como administrador** opción en Windows), no se puede eliminar las carpetas que se crean mediante WebMatrix mediante el Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="42597-281">If WebMatrix is running using elevated permissions (that is, you started WebMatrix using the **Run as Administrator** option in Windows), folders that are created by WebMatrix cannot be deleted using Windows Explorer.</span></span>
> 
> <span data-ttu-id="42597-282">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-282">**Workaround**</span></span>  
> <span data-ttu-id="42597-283">Ejecute el Explorador de Windows con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="42597-283">Run Windows Explorer using elevated permissions.</span></span> <span data-ttu-id="42597-284">Siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="42597-284">Follow these steps:</span></span>  
> 
> 1. <span data-ttu-id="42597-285">En Windows, haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="42597-285">In Windows, click **Start**.</span></span>
> 2. <span data-ttu-id="42597-286">Escriba "Explorador de Windows" y haga clic en la entrada de **el Explorador de Windows**.</span><span class="sxs-lookup"><span data-stu-id="42597-286">Enter "Windows Explorer" and right-click the entry for **Windows Explorer**.</span></span>
> 3. <span data-ttu-id="42597-287">Haga clic en **ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="42597-287">Click **Run as Administrator**.</span></span> <span data-ttu-id="42597-288">A continuación, puede eliminar las carpetas.</span><span class="sxs-lookup"><span data-stu-id="42597-288">You can then delete the folders.</span></span>


#### <a name="issue-webmatrix-10-is-unable-to-perform-certain-tasks-that-require-elevation"></a><span data-ttu-id="42597-289">Problema: WebMatrix 1.0 es no se puede realizar ciertas tareas que requieren elevación</span><span class="sxs-lookup"><span data-stu-id="42597-289">Issue: WebMatrix 1.0 is unable to perform certain tasks that require elevation</span></span>

> <span data-ttu-id="42597-290">WebMatrix 1.0 es no se puede realizar ciertas tareas que requieren elevación, tales como instalar componentes adicionales en las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="42597-290">WebMatrix 1.0 is unable to perform certain tasks that require elevation, such as installing additional components in the following situations:</span></span>
> 
> - <span data-ttu-id="42597-291">En Windows Vista o Windows 7, está iniciando sesión con una cuenta que no tiene privilegios administrativos y Control de cuentas de usuario (UAC) está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="42597-291">On Windows Vista or Windows 7, you are logged in with an account that does not have administrative privileges and User Account Control (UAC) is disabled.</span></span>
> - <span data-ttu-id="42597-292">Está utilizando Microsoft Windows XP o Microsoft Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="42597-292">You are using Microsoft Windows XP or Microsoft Windows Server 2003.</span></span>
> 
> <span data-ttu-id="42597-293">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-293">**Workaround**</span></span>  
> <span data-ttu-id="42597-294">Mayoría de las tareas en WebMatrix 1.0 no requiere permisos administrativos.</span><span class="sxs-lookup"><span data-stu-id="42597-294">Most tasks in WebMatrix 1.0 do not require administrative permission.</span></span> <span data-ttu-id="42597-295">Para aquellos que lo hacen, puede realizar la operación porque un administrador o siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="42597-295">For those that do, you can perform the operation as an administrator, or follow these steps:</span></span>
> 
> - <span data-ttu-id="42597-296">En Windows Vista o Windows 7, habilitar UAC.</span><span class="sxs-lookup"><span data-stu-id="42597-296">On Windows Vista or Windows 7, enable UAC.</span></span>
> - <span data-ttu-id="42597-297">En Windows XP, agregue el usuario al grupo de seguridad Administradores.</span><span class="sxs-lookup"><span data-stu-id="42597-297">On Windows XP, add the user to the Administrators security group.</span></span>


#### <a name="issue-site-from-web-gallery-is-disabled"></a><span data-ttu-id="42597-298">Problema: El "Sitio de la galería Web" está deshabilitada</span><span class="sxs-lookup"><span data-stu-id="42597-298">Issue: "Site from Web Gallery" is disabled</span></span>

> <span data-ttu-id="42597-299">El **sitio desde galería Web** opción está deshabilitada si el instalador de plataforma Web 3.0 no está instalado.</span><span class="sxs-lookup"><span data-stu-id="42597-299">The **Site from Web Gallery** option is disabled if the Web Platform Installer 3.0 is not installed.</span></span>
> 
> <span data-ttu-id="42597-300">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-300">**Workaround**</span></span>  
> <span data-ttu-id="42597-301">Instalar el [instalador de plataforma Web de Microsoft 3.0](https://go.microsoft.com/fwlink/?LinkID=194638).</span><span class="sxs-lookup"><span data-stu-id="42597-301">Install the [Microsoft Web Platform Installer 3.0](https://go.microsoft.com/fwlink/?LinkID=194638).</span></span>


#### <a name="issue-google-chrome-is-not-available-as-a-run-option"></a><span data-ttu-id="42597-302">Problema: Google Chrome no está disponible como una opción de ejecución</span><span class="sxs-lookup"><span data-stu-id="42597-302">Issue: Google Chrome is not available as a Run option</span></span>

> <span data-ttu-id="42597-303">Google Chrome no aparece en la lista de exploradores en **ejecutar** en el **inicio** ficha.</span><span class="sxs-lookup"><span data-stu-id="42597-303">Google Chrome is not displayed in the list of browsers under **Run** on the **Home** tab.</span></span>
> 
> <span data-ttu-id="42597-304">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-304">**Workaround**</span></span>  
> <span data-ttu-id="42597-305">Algunas versiones de Google Chrome no se registran correctamente con la característica de programas predeterminados de Windows.</span><span class="sxs-lookup"><span data-stu-id="42597-305">Some versions of Google Chrome do not register themselves correctly with the Default Programs feature in Windows.</span></span> <span data-ttu-id="42597-306">Como alternativa, inicie Google Chrome, haga clic en el *control Google Chrome y personalizar* menú, haga clic en *opciones*y, a continuación, haga clic en *Asegúrese de Google Chrome mi explorador predeterminado*.</span><span class="sxs-lookup"><span data-stu-id="42597-306">As a workaround, start Google Chrome, click the *Customize and control Google Chrome* menu, click *Options*, and then click *Make Google Chrome my default browser*.</span></span>


#### <a name="issue-the-foreign-key-dialog-box-doesnt-allow-entering-a-primary-key"></a><span data-ttu-id="42597-307">Problema: El cuadro de diálogo "Foreign Key" no permite especificar una clave principal</span><span class="sxs-lookup"><span data-stu-id="42597-307">Issue: The "Foreign Key" dialog box doesn't allow entering a primary key</span></span>

> <span data-ttu-id="42597-308">El **Foreign Key** cuadro de diálogo no permite especificar el nombre de clave principal de la tabla de clave principal.</span><span class="sxs-lookup"><span data-stu-id="42597-308">The **Foreign Key** dialog box does not allow you to enter the primary key name from the primary key table.</span></span>
> 
> <span data-ttu-id="42597-309">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-309">**Workaround**</span></span>  
> <span data-ttu-id="42597-310">Esto tiene su porqué.</span><span class="sxs-lookup"><span data-stu-id="42597-310">This is intentional.</span></span> <span data-ttu-id="42597-311">No es necesario que escriba el nombre de la clave principal de la tabla de clave principal.</span><span class="sxs-lookup"><span data-stu-id="42597-311">You do not need to enter the name of the primary key from the primary key table.</span></span>


#### <a name="issue-intellisense-is-not-available-in-webmatrix-for-razor-syntax-c-or-visual-basic"></a><span data-ttu-id="42597-312">Problema: IntelliSense no está disponible en WebMatrix para Razor sintaxis, C# o Visual Basic</span><span class="sxs-lookup"><span data-stu-id="42597-312">Issue: IntelliSense is not available in WebMatrix for Razor syntax, C#, or Visual Basic</span></span>

> <span data-ttu-id="42597-313">IntelliSense se admite en WebMatrix para HTML y CSS.</span><span class="sxs-lookup"><span data-stu-id="42597-313">IntelliSense is supported in WebMatrix for HTML and CSS.</span></span> <span data-ttu-id="42597-314">Sin embargo, no está disponible para otros idiomas.</span><span class="sxs-lookup"><span data-stu-id="42597-314">However, it is not available for other languages.</span></span> 
> 
> <span data-ttu-id="42597-315">**Solución alternativa** </span><span class="sxs-lookup"><span data-stu-id="42597-315">**Workaround** </span></span>  
> <span data-ttu-id="42597-316">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="42597-316">None.</span></span>


#### <a name="issue-intellisense-for-html-and-css-suggests-elements-that-are-not-contextually-appropriate"></a><span data-ttu-id="42597-317">Problema: IntelliSense para HTML y CSS sugiere elementos que no son adecuados como</span><span class="sxs-lookup"><span data-stu-id="42597-317">Issue: IntelliSense for HTML and CSS suggests elements that are not contextually appropriate</span></span>

> <span data-ttu-id="42597-318">IntelliSense para el marcado en WebMatrix es compatible con HTML utilizando el [esquema XHTML 1.0 Transitional](http://www.w3.org/TR/2002/NOTE-xhtml1-schema-20020902/#xhtml1-transitional) y el uso de CSS el [esquema CSS 2.1](http://www.w3.org/TR/CSS2/).</span><span class="sxs-lookup"><span data-stu-id="42597-318">IntelliSense for markup in WebMatrix supports HTML using the [XHTML 1.0 Transitional schema](http://www.w3.org/TR/2002/NOTE-xhtml1-schema-20020902/#xhtml1-transitional) and CSS using the [CSS 2.1 schema](http://www.w3.org/TR/CSS2/).</span></span> <span data-ttu-id="42597-319">Dado que IntelliSense se basa en estos esquemas específicos, determinadas etiquetas, atributos o propiedades podrían sugiere que no son adecuadas para la definición de estilo o la página actual.</span><span class="sxs-lookup"><span data-stu-id="42597-319">Because IntelliSense is based on these specific schemas, certain tags, attributes, or properties might be suggested that are not appropriate for the current page or style definition.</span></span> <span data-ttu-id="42597-320">Para HTML, también se pueden producir en sugerencias inesperados en el contenido que se puede interpretar como XHTML con formato incorrecto (por ejemplo, cuando no se cierran las etiquetas).</span><span class="sxs-lookup"><span data-stu-id="42597-320">For HTML, it can also lead to unexpected suggestions in content that might be interpreted as malformed XHTML (for example, when tags are not closed).</span></span> <span data-ttu-id="42597-321">Este problema podría ser más evidente si el punto de inserción está dentro de una etiqueta incompleta; en ese caso, IntelliSense puede sugerir nuevas etiquetas de apertura u ofrecen otras sugerencias incorrectas.</span><span class="sxs-lookup"><span data-stu-id="42597-321">This issue might be more noticeable if the insertion point is inside an incomplete tag; in that case, IntelliSense might suggest new opening tags or offer other incorrect suggestions.</span></span> 
> 
> <span data-ttu-id="42597-322">**Solución alternativa** </span><span class="sxs-lookup"><span data-stu-id="42597-322">**Workaround** </span></span>  
> <span data-ttu-id="42597-323">Para HTML, asegúrese de que está trabajando en una página XHTML con formato correcto, completa.</span><span class="sxs-lookup"><span data-stu-id="42597-323">For HTML, make sure that you are working within a well-formed, complete XHTML page.</span></span> <span data-ttu-id="42597-324">CSS, no hay ninguna solución alternativa.</span><span class="sxs-lookup"><span data-stu-id="42597-324">For CSS, there is no workaround.</span></span>


#### <a name="issue-intellisense-is-not-invoked-while-you-type"></a><span data-ttu-id="42597-325">Problema: No se invoca IntelliSense mientras se escribe</span><span class="sxs-lookup"><span data-stu-id="42597-325">Issue: IntelliSense is not invoked while you type</span></span>

> <span data-ttu-id="42597-326">En ocasiones, IntelliSense no puede invocar como HTML o CSS que se va a se escribe en el editor.</span><span class="sxs-lookup"><span data-stu-id="42597-326">At times, IntelliSense might not be invoked as HTML or CSS is being entered in the editor.</span></span> <span data-ttu-id="42597-327">En concreto, esto puede ocurrir cuando el punto de inserción está directamente al lado de otro elemento o al final de un archivo.</span><span class="sxs-lookup"><span data-stu-id="42597-327">In particular, this might happen when the insertion point is directly next to another element or at the end of a file.</span></span> 
> 
> <span data-ttu-id="42597-328">**Solución alternativa** </span><span class="sxs-lookup"><span data-stu-id="42597-328">**Workaround** </span></span>  
> <span data-ttu-id="42597-329">Asegúrese de que hay espacio en blanco alrededor del punto de inserción y que el punto de inserción no está al final de un archivo.</span><span class="sxs-lookup"><span data-stu-id="42597-329">Make sure that there is whitespace around the insertion point and that the insertion point is not at the end of a file.</span></span> <span data-ttu-id="42597-330">También puede invocar IntelliSense manualmente presionando Ctrl + barra espaciadora.</span><span class="sxs-lookup"><span data-stu-id="42597-330">You can also invoke IntelliSense manually by pressing Ctrl+Space.</span></span>


#### <a name="issue-no-ui-is-available-for-disabling-intellisense"></a><span data-ttu-id="42597-331">Problema: Ninguna interfaz de usuario está disponible para deshabilitar IntelliSense</span><span class="sxs-lookup"><span data-stu-id="42597-331">Issue: No UI is available for disabling IntelliSense</span></span>

> <span data-ttu-id="42597-332">WebMatrix 1.0 se proporciona ninguna interfaz de usuario o de gestos para deshabilitar IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="42597-332">WebMatrix 1.0 provides no UI or gesture for disabling IntelliSense.</span></span> 
> 
> <span data-ttu-id="42597-333">**Solución alternativa** </span><span class="sxs-lookup"><span data-stu-id="42597-333">**Workaround** </span></span>  
> <span data-ttu-id="42597-334">Iniciar WebMatrix mediante el comando siguiente, que incluye un modificador que deshabilita IntelliSense:</span><span class="sxs-lookup"><span data-stu-id="42597-334">Start WebMatrix using the following command, which includes a switch that disables IntelliSense:</span></span>  
>   
> `WebMatrix.exe #ExecuteCommand# EditorIntelliSense off`


<a id="Known_Issues_IISExpress"></a>
### <a name="iis-express"></a><span data-ttu-id="42597-335">IIS Express</span><span class="sxs-lookup"><span data-stu-id="42597-335">IIS Express</span></span>

<span data-ttu-id="42597-336">IIS Express tiene su propio archivo Léame, que está disponible en la siguiente URL:</span><span class="sxs-lookup"><span data-stu-id="42597-336">IIS Express has its own readme file, which is available at the following URL:</span></span>

[<span data-ttu-id="42597-337">https://go.Microsoft.com/fwlink/?LinkId=207675&amp;clcid = 0 x 409</span><span class="sxs-lookup"><span data-stu-id="42597-337">https://go.microsoft.com/fwlink/?LinkID=207675&amp;clcid=0x409</span></span>](https://go.microsoft.com/fwlink/?LinkID=207675&amp;clcid=0x409)

<a id="Known_Issues_SQLServerCompact"></a>

### <a name="sql-server-compact"></a><span data-ttu-id="42597-338">SQL Server Compact</span><span class="sxs-lookup"><span data-stu-id="42597-338">SQL Server Compact</span></span>

<span data-ttu-id="42597-339">SQL Server Compact tiene su propio archivo Léame, que está disponible en la siguiente URL:</span><span class="sxs-lookup"><span data-stu-id="42597-339">SQL Server Compact has its own readme file, which is available at the following URL:</span></span>

[<span data-ttu-id="42597-340">https://go.Microsoft.com/fwlink/?LinkId=208545</span><span class="sxs-lookup"><span data-stu-id="42597-340">https://go.microsoft.com/fwlink/?LinkID=208545</span></span>](https://go.microsoft.com/fwlink/?LinkID=208545&amp;clcid=0x409)

<span data-ttu-id="42597-341">Para obtener información acerca de los problemas que implican la instalación de SQL Server Compact como parte de WebMatrix, consulte [problemas de instalación de WebMatrix](#Known_Issues_Installation) anteriormente en este documento.</span><span class="sxs-lookup"><span data-stu-id="42597-341">For information about issues that involve installing SQL Server Compact as part of WebMatrix, see [WebMatrix Installation Issues](#Known_Issues_Installation) earlier in this document.</span></span>

### <a id="Known_Issues_Installing_Applications"></a><span data-ttu-id="42597-342">Instalación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="42597-342">Installing Applications</span></span>

#### <a name="issue-installing-an-application-can-take-a-long-time-if-the-users-my-documents-folder-is-redirected-to-a-network-share"></a><span data-ttu-id="42597-343">Problema: Instalar una aplicación puede tardar mucho tiempo si se redirige la carpeta Mis documentos del usuario a un recurso compartido de red</span><span class="sxs-lookup"><span data-stu-id="42597-343">Issue: Installing an application can take a long time if the user's My Documents folder is redirected to a network share</span></span>

> <span data-ttu-id="42597-344">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-344">**Workaround**</span></span>  
> <span data-ttu-id="42597-345">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="42597-345">None.</span></span> <span data-ttu-id="42597-346">La aplicación puede tardar bastante tiempo en instalar, pero se instalará correctamente.</span><span class="sxs-lookup"><span data-stu-id="42597-346">The application might take a while to install, but will install correctly.</span></span>


### <a id="Known_Issues_Publishing_Applications"></a><span data-ttu-id="42597-347">Publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="42597-347">Publishing Applications</span></span>

#### <a name="issue-required-permissions-cannot-be-acquired-error-when-publishing-a-sql-compact-database"></a><span data-ttu-id="42597-348">Problema: "requerido no se puede obtener permisos" error al publicar una base de datos de SQL Compact</span><span class="sxs-lookup"><span data-stu-id="42597-348">Issue: "Required permissions cannot be acquired" error when publishing a SQL Compact Database</span></span>

> <span data-ttu-id="42597-349">WebMatrix no admite totalmente la implementación auxiliares de los archivos binarios de SQL Server Compact a un servidor que está ejecutando la versión 3.5 de .NET Framework con una configuración de nivel de confianza medio.</span><span class="sxs-lookup"><span data-stu-id="42597-349">WebMatrix does not fully support deploying supporting binaries for SQL Server Compact to a server that is running .NET Framework version 3.5 with a medium trust configuration.</span></span>
> 
> <span data-ttu-id="42597-350">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-350">**Workaround**</span></span>  
> <span data-ttu-id="42597-351">Es la solución preferida instalar .NET Framework 4 en el servidor.</span><span class="sxs-lookup"><span data-stu-id="42597-351">The preferred workaround is to install the .NET Framework 4 on the server.</span></span> <span data-ttu-id="42597-352">Como alternativa, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="42597-352">Alternatively, do the following:</span></span>
> 
> 1. <span data-ttu-id="42597-353">Agregue los siguientes elementos para la `SecurityClasses` sección *Web\_MediumTrust.config* archivo:</span><span class="sxs-lookup"><span data-stu-id="42597-353">Add the following elements to the `SecurityClasses` section in *Web\_MediumTrust.config* file:</span></span>
> 
>     [!code-html[Main](overview/samples/sample6.html)]
> 2. <span data-ttu-id="42597-354">Crear un nuevo conjunto de permisos en el *Web\_MediumTrust.config* archivo con los permisos siguientes:</span><span class="sxs-lookup"><span data-stu-id="42597-354">Create a new permission set in the *Web\_MediumTrust.config* file with the following required permissions:</span></span>
> 
>     [!code-html[Main](overview/samples/sample7.html)]
> 3. <span data-ttu-id="42597-355">Aplicar el permiso establecido en SQL Server Compact colocando los siguientes elementos el *Web\_MediumTrust.config* archivo:</span><span class="sxs-lookup"><span data-stu-id="42597-355">Apply the permission set to SQL Server Compact by putting the following elements in the *Web\_MediumTrust.config* file:</span></span>
> 
>     [!code-html[Main](overview/samples/sample8.html)]


#### <a name="issue-gallery-and-phpbb-web-applications-display-a-service-is-unavailable-error-after-publishing"></a><span data-ttu-id="42597-356">Problema: Las aplicaciones web de galería y PhpBB mostrarán un error "El servicio no está disponible" después de publicar</span><span class="sxs-lookup"><span data-stu-id="42597-356">Issue: Gallery and PhpBB web applications display a "Service is unavailable" error after publishing</span></span>

> <span data-ttu-id="42597-357">En algunas circunstancias, al publicar una aplicación produce un error "el servicio no está disponible".</span><span class="sxs-lookup"><span data-stu-id="42597-357">Under some circumstances, publishing an application causes a "service is unavailable" error.</span></span>
> 
> <span data-ttu-id="42597-358">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-358">**Workaround**</span></span>  
> <span data-ttu-id="42597-359">En WebMatrix, agregue una barra diagonal inversa (\) al final del nombre del servidor en el **configuración de publicación** ventana y, a continuación, publicar la aplicación de nuevo.</span><span class="sxs-lookup"><span data-stu-id="42597-359">In WebMatrix, add a backslash (\) to the end of the server name in the **Publish Settings** window and then publish the application again.</span></span>


#### <a name="issue-moodle-website-layout-and-links-are-broken-after-publishing"></a><span data-ttu-id="42597-360">Problema: Vínculos y el diseño del sitio Web de Moodle se interrumpen después de publicar</span><span class="sxs-lookup"><span data-stu-id="42597-360">Issue: Moodle website layout and links are broken after publishing</span></span>

> <span data-ttu-id="42597-361">Después de publicar una aplicación Moodle, la aplicación no funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="42597-361">After you publish a Moodle application, the application does not work correctly.</span></span>
> 
> <span data-ttu-id="42597-362">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-362">**Workaround**</span></span>  
> <span data-ttu-id="42597-363">En WebMatrix, agregue una barra diagonal (/) al final de la **nombre del sitio** campo el **configuración de publicación** ventana y, a continuación, publicar la aplicación de nuevo.</span><span class="sxs-lookup"><span data-stu-id="42597-363">In WebMatrix, add a slash (/) to the end of the **Site Name** field in the **Publish Settings** window and then publish the application again.</span></span>


#### <a name="issue-publishing-nopcommerce-fails-with-a-database-error"></a><span data-ttu-id="42597-364">Problema: Publicación nopCommerce se produce un error de base de datos</span><span class="sxs-lookup"><span data-stu-id="42597-364">Issue: Publishing nopCommerce fails with a database error</span></span>

> <span data-ttu-id="42597-365">Publicación nopCommerce se produce un error y notifica un error de base de datos como "insertar en la instrucción nop\_tabla del registro de error."</span><span class="sxs-lookup"><span data-stu-id="42597-365">Publishing nopCommerce fails and reports a database error like "Insert into the nop\_log table failed."</span></span>
> 
> <span data-ttu-id="42597-366">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-366">**Workaround**</span></span>  
> 
> 1. <span data-ttu-id="42597-367">En WebMatrix, haga clic en **ejecutar** para iniciar nopCommerce localmente.</span><span class="sxs-lookup"><span data-stu-id="42597-367">In WebMatrix, click **Run** to launch nopCommerce locally.</span></span>
> 2. <span data-ttu-id="42597-368">Inicie sesión en la página de administración.</span><span class="sxs-lookup"><span data-stu-id="42597-368">Log into the administration page.</span></span>
> 3. <span data-ttu-id="42597-369">Haga clic en el **System** menú.</span><span class="sxs-lookup"><span data-stu-id="42597-369">Click the **System** menu.</span></span>
> 4. <span data-ttu-id="42597-370">Haga clic en el **registro** opción.</span><span class="sxs-lookup"><span data-stu-id="42597-370">Click the **Log** option.</span></span>
> 5. <span data-ttu-id="42597-371">Haga clic en el **Vaciar registro** botón.</span><span class="sxs-lookup"><span data-stu-id="42597-371">Click the **Clear Log** button.</span></span>
> 6. <span data-ttu-id="42597-372">Vuelva a publicar nopCommerce.</span><span class="sxs-lookup"><span data-stu-id="42597-372">Publish nopCommerce again.</span></span>


#### <a name="issue-silverstripe-cms-displays-a-http-500-php-fcgi-error-when-you-download-a-published-site"></a><span data-ttu-id="42597-373">Problema: Silverstripe CMS muestra un "Error FCGI PHP HTTP 500" al descargar un sitio publicado</span><span class="sxs-lookup"><span data-stu-id="42597-373">Issue: Silverstripe CMS displays a "HTTP 500 PHP FCGI Error" when you download a published site</span></span>

> <span data-ttu-id="42597-374">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-374">**Workaround**</span></span>  
> <span data-ttu-id="42597-375">Tras hacer clic en **descarga publicado sitio**, omitir `silverstripe-cache/manifest_main` en **vista previa de publicación**.</span><span class="sxs-lookup"><span data-stu-id="42597-375">After you click **Download published site**, skip `silverstripe-cache/manifest_main` in **Publish Preview**.</span></span> <span data-ttu-id="42597-376">Este archivo se usa para el almacenamiento en caché y es específico de cada equipo.</span><span class="sxs-lookup"><span data-stu-id="42597-376">This file is used for caching purposes and is specific to each computer.</span></span>


#### <a name="issue-subtext-displays-server-error-in--application-when-you-download-a-published-site"></a><span data-ttu-id="42597-377">Problema: Subtext muestra "Error de servidor en la aplicación '/'" cuando se descarga un sitio publicado</span><span class="sxs-lookup"><span data-stu-id="42597-377">Issue: Subtext displays "Server Error in '/' Application" when you download a published site</span></span>

> <span data-ttu-id="42597-378">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-378">**Workaround**</span></span>  
> <span data-ttu-id="42597-379">Abra el sitio *web.config* archivo y reemplace el Id. de usuario y la contraseña en la cadena de conexión de base de datos con las credenciales de administrador de SQL Server (las credenciales "sa").</span><span class="sxs-lookup"><span data-stu-id="42597-379">Open the site's *web.config* file and replace the user ID and password in the database connection string with the SQL Server administrator credentials (the "sa" credentials).</span></span>
> 
> <span data-ttu-id="42597-380">Como alternativa, siga estos pasos para conceder a la cuenta de usuario que ha iniciado sesión con `db_owner` permisos:</span><span class="sxs-lookup"><span data-stu-id="42597-380">Alternatively, follow these steps in order to give the user account you are logged in with `db_owner` permissions:</span></span>
> 
> 1. <span data-ttu-id="42597-381">Instalar SQL Server Management Studio con el instalador de plataforma Web.</span><span class="sxs-lookup"><span data-stu-id="42597-381">Install SQL Server Management Studio using the Web Platform Installer.</span></span>
> 2. <span data-ttu-id="42597-382">Conéctese a la instancia local de SQL Server Express (de forma predeterminada, `.\SQLEXPRESS`).</span><span class="sxs-lookup"><span data-stu-id="42597-382">Connect to the local SQL Server Express instance (by default, `.\SQLEXPRESS`).</span></span>
> 3. <span data-ttu-id="42597-383">Haga clic en **bases de datos** &gt; *[localSubtextDatabase]* &gt; **seguridad** &gt; **usuarios** &gt; *[localSubtextUser*] (valor predeterminado es `subtextuser`], menú contextual y haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="42597-383">Click **Databases** &gt; *[localSubtextDatabase]* &gt; **Security** &gt; **Users** &gt; *[localSubtextUser*] (default is `subtextuser`], right-click, and click **Properties**.</span></span>
> 4. <span data-ttu-id="42597-384">Seleccione **db\_propietario** en la sección de la pertenencia al rol.</span><span class="sxs-lookup"><span data-stu-id="42597-384">Select **db\_owner** in the role membership section.</span></span>


#### <a name="issue-site-might-not-work-after-publishing-if-the-destination-url-field-is-not-prefixed-with-http-or-https"></a><span data-ttu-id="42597-385">Problema: Sitio no funcionen después de publicar si el campo "Dirección URL de destino" no es el prefijo http:// o https://</span><span class="sxs-lookup"><span data-stu-id="42597-385">Issue: Site might not work after publishing if the "Destination URL" field is not prefixed with http:// or https://</span></span>

> <span data-ttu-id="42597-386">En el **configuración de publicación** cuadro de diálogo, si la dirección URL de destino no comienza con `http://` o `https://`, el sitio no funcionen después de la implementación.</span><span class="sxs-lookup"><span data-stu-id="42597-386">In the **Publishing Settings** dialog box, if the destination URL does not begin with `http://` or `https://`, the site might not work after deployment.</span></span>
> 
> <span data-ttu-id="42597-387">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-387">**Workaround**</span></span>  
> <span data-ttu-id="42597-388">Asegúrese de que antes de publicar un sitio, la dirección URL de destino en la **configuración de publicación** inicia el cuadro de diálogo con `http://` o `https://`.</span><span class="sxs-lookup"><span data-stu-id="42597-388">Make sure that before you publish a site, the destination URL in the **Publish Settings** dialog box starts with `http://` or `https://`.</span></span>


#### <a name="issue-publishing-a-mysql-database-fails-with-the-error-failed-to-publish-the-database-this-can-happen-if-the-remote-database-cannot-run-the-script"></a><span data-ttu-id="42597-389">Problema: Publicar una base de datos de MySQL produce el error "no se pudo publicar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="42597-389">Issue: Publishing a MySQL database fails with the error "Failed to publish the database.</span></span> <span data-ttu-id="42597-390">Esto puede ocurrir si la base de datos remota no puede ejecutar la secuencia de comandos."</span><span class="sxs-lookup"><span data-stu-id="42597-390">This can happen if the remote database cannot run the script."</span></span>

> <span data-ttu-id="42597-391">El error puede producirse por una serie de motivos.</span><span class="sxs-lookup"><span data-stu-id="42597-391">The error can occur for a number of reasons.</span></span> <span data-ttu-id="42597-392">Un motivo que puede ver este error es si la secuencia de comandos de base de datos contiene un carácter de comillas simples (') y juego de caracteres de destino MySQL la base de datos predeterminada no es UTF-8.</span><span class="sxs-lookup"><span data-stu-id="42597-392">One reason you can see this error is if the database script contains a single quotation character (') and the destination MySQL database's default character set is not to UTF-8.</span></span>
> 
> <span data-ttu-id="42597-393">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-393">**Workaround**</span></span>  
> <span data-ttu-id="42597-394">Establecer el carácter predeterminado establecido para la base de datos MySQL remota en UTF-8.</span><span class="sxs-lookup"><span data-stu-id="42597-394">Set the default character set for the remote MySQL database to UTF-8.</span></span>


#### <a name="issue-some-links-are-not-visible-in-dotnetnuke-after-publishing-or-downloading-the-site"></a><span data-ttu-id="42597-395">Problema: Algunos vínculos no están visibles en DotNetNuke tras publicar o descargando el sitio</span><span class="sxs-lookup"><span data-stu-id="42597-395">Issue: Some links are not visible in DotNetNuke after publishing or downloading the site</span></span>

> <span data-ttu-id="42597-396">Si se publica o descarga un sitio de DotNetNuke, tendrá que borrar la memoria caché para obtener los nuevos vínculos que aparecerá en el sitio.</span><span class="sxs-lookup"><span data-stu-id="42597-396">If you publish or download a DotNetNuke site, you might need to clear the cache to get the new links to appear on the site.</span></span>
> 
> <span data-ttu-id="42597-397">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-397">**Workaround**</span></span>
> 
> 1. <span data-ttu-id="42597-398">Inicie sesión como "Host".</span><span class="sxs-lookup"><span data-stu-id="42597-398">Log in as "Host".</span></span>
> 2. <span data-ttu-id="42597-399">Vaya al menú de host y seleccione **configuración de Host**.</span><span class="sxs-lookup"><span data-stu-id="42597-399">Go to the host menu and select **Host Settings**.</span></span>
> 3. <span data-ttu-id="42597-400">Desplácese hacia abajo y en **configuración avanzada**, expanda **configuración de rendimiento**.</span><span class="sxs-lookup"><span data-stu-id="42597-400">Scroll down and under **Advanced Settings**, expand **Performance Settings**.</span></span>
> 4. <span data-ttu-id="42597-401">Haga clic en el **Borrar caché** vínculo para las páginas.</span><span class="sxs-lookup"><span data-stu-id="42597-401">Click the **Clear Cache** link for pages.</span></span>
> 5. <span data-ttu-id="42597-402">Vaya a la parte inferior de la página y reiniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="42597-402">Go to the bottom of the page and restart the application.</span></span>


#### <a name="issue-some-links-in-atomsite-are-broken-after-you-download-a-published-site"></a><span data-ttu-id="42597-403">Problema: Algunos vínculos en AtomSite se interrumpen después de descargar un sitio publicado</span><span class="sxs-lookup"><span data-stu-id="42597-403">Issue: Some links in AtomSite are broken after you download a published site</span></span>

> <span data-ttu-id="42597-404">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-404">**Workaround**</span></span>  
> <span data-ttu-id="42597-405">En el *service.config* archivo *users.config* archivo y todos los *.xml* archivos, reemplace la cadena de dirección URL (por ejemplo, `http://myhost.com/atomsite`) con el local (por ejemplo, `http://localhost:1239`).</span><span class="sxs-lookup"><span data-stu-id="42597-405">In the *service.config* file, *users.config* file, and all *.xml* files, replace the URL string (for example, `http://myhost.com/atomsite`) with the local one (for example, `http://localhost:1239`).</span></span>


#### <a name="issue-mysql-based-applications-like-wordpress-fail-to-publish-and-report-a-database-error"></a><span data-ttu-id="42597-406">Problema: Aplicaciones basadas en MySQL como WordPress no pueden publicar e informar de un error de base de datos</span><span class="sxs-lookup"><span data-stu-id="42597-406">Issue: MySQL-based applications like WordPress fail to publish and report a database error</span></span>

> <span data-ttu-id="42597-407">De manera predeterminada, WebMatrix instala MySQL con el juego de caracteres UTF-8.</span><span class="sxs-lookup"><span data-stu-id="42597-407">By default, WebMatrix installs MySQL with the UTF-8 character set.</span></span> <span data-ttu-id="42597-408">Si instala MySQL en su propio y el juego de caracteres no es UTF-8 (por ejemplo, es Latin1), podría producir un error en el proceso de publicación para las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="42597-408">If you install MySQL on your own, and the character set is not UTF-8 (for example, it is Latin1), the publish process for databases might fail.</span></span>
> 
> <span data-ttu-id="42597-409">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-409">**Workaround**</span></span>
> 
> 1. <span data-ttu-id="42597-410">Cambiar el juego de caracteres para MySQL a UTF-8.</span><span class="sxs-lookup"><span data-stu-id="42597-410">Change the character set for MySQL to UTF-8.</span></span> <span data-ttu-id="42597-411">(Para obtener más información, consulte [Server del juego de caracteres y la intercalación](http://dev.mysql.com/doc/refman/5.0/en/charset-server.html) en el sitio Web de MySQL.)</span><span class="sxs-lookup"><span data-stu-id="42597-411">(For details, see [Server Character Set and Collation](http://dev.mysql.com/doc/refman/5.0/en/charset-server.html) on the MySQL website.)</span></span>
> 2. <span data-ttu-id="42597-412">Vuelva a instalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="42597-412">Reinstall the application.</span></span>
> 3. <span data-ttu-id="42597-413">Volver a publicar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="42597-413">Republish the application.</span></span>


#### <a name="issue-download-published-site-fails-for-applications-that-have-browser-based-setup"></a><span data-ttu-id="42597-414">Problema: "Sitio de descarga publicado" se produce un error para las aplicaciones que tienen el programa de instalación basada en explorador</span><span class="sxs-lookup"><span data-stu-id="42597-414">Issue: "Download published site" fails for applications that have browser-based setup</span></span>

> <span data-ttu-id="42597-415">Algunas aplicaciones (por ejemplo, Kentico CMS) requieren que se inicie en el explorador para llevar a cabo el programa de instalación posteriores a la instalación como la creación de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="42597-415">Some applications (for example, Kentico CMS) require you to launch them in the browser in order to perform post-installation setup such as creating a database.</span></span> <span data-ttu-id="42597-416">Si publica una aplicación similar al siguiente sin completar la instalación basada en explorador, intenta descargar el mismo sitio desde un servidor remoto generará un error.</span><span class="sxs-lookup"><span data-stu-id="42597-416">If you publish an application like this without completing the browser-based setup, attempting to download the same site from a remote server will fail.</span></span>
> 
> <span data-ttu-id="42597-417">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-417">**Workaround**</span></span>  
> <span data-ttu-id="42597-418">Finalizar el programa de instalación basada en explorador antes de publicar el sitio.</span><span class="sxs-lookup"><span data-stu-id="42597-418">Finish browser-based setup before publishing the site.</span></span>


#### <a name="issue-download-published-site-fails-with-a-database-error-for-dotnetnuke-and-kooboo-cms"></a><span data-ttu-id="42597-419">Problema: "Sitio de descarga publicado" produce un error de base de datos de DotNetNuke y Kooboo CMS</span><span class="sxs-lookup"><span data-stu-id="42597-419">Issue: "Download published site" fails with a database error for DotNetNuke and Kooboo CMS</span></span>

> <span data-ttu-id="42597-420">Si intenta descargar una aplicación de un servidor y tener credenciales de administrador en la cadena de conexión de base de datos en el **configuración de publicación** cuadro de diálogo, puede aparecer el siguiente error en el registro de la publicación:</span><span class="sxs-lookup"><span data-stu-id="42597-420">If you try to download an application from a server and you have administrator credentials in the database connection string in the **Publish Settings** dialog, you might see the following error in the publish log:</span></span>
> 
> [!code-console[Main](overview/samples/sample9.cmd)]
> 
> <span data-ttu-id="42597-421">**Solución alternativa**</span><span class="sxs-lookup"><span data-stu-id="42597-421">**Workaround**</span></span>  
> <span data-ttu-id="42597-422">Si es factible, vuelva a publicar el sitio (o publicarlo) con credenciales sin privilegios de administrador para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="42597-422">If practical, republish the site (or have it published) using non-administrator credentials for the database.</span></span>


<a id="More_Info"></a>

## <a name="for-more-information"></a><span data-ttu-id="42597-423">Para obtener más información</span><span class="sxs-lookup"><span data-stu-id="42597-423">For More Information</span></span>

<span data-ttu-id="42597-424">Para obtener más información acerca de WebMatrix 1.0, vea los siguientes sitios Web:</span><span class="sxs-lookup"><span data-stu-id="42597-424">For more information about WebMatrix 1.0, see the following websites:</span></span>

- [<span data-ttu-id="42597-425">IIS.net</span><span class="sxs-lookup"><span data-stu-id="42597-425">IIS.net</span></span>](http://iis.net/)
- [<span data-ttu-id="42597-426">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="42597-426">ASP.NET</span></span>](https://asp.net/webmatrix)
- [<span data-ttu-id="42597-427">Web de Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="42597-427">Microsoft.com/web</span></span>](https://www.microsoft.com/web)

<span data-ttu-id="42597-428">© 2011 Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="42597-428">© 2011 Microsoft Corporation.</span></span> <span data-ttu-id="42597-429">Reservados todos los derechos.</span><span class="sxs-lookup"><span data-stu-id="42597-429">All Rights Reserved.</span></span> <span data-ttu-id="42597-430">[Términos de uso](https://msdn.microsoft.com/en-us/cc300389.aspx).</span><span class="sxs-lookup"><span data-stu-id="42597-430">[Terms of Use](https://msdn.microsoft.com/en-us/cc300389.aspx).</span></span>
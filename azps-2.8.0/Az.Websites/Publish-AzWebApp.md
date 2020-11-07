---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793166"
---
# <span data-ttu-id="a444c-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a444c-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="a444c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a444c-102">SYNOPSIS</span></span>
<span data-ttu-id="a444c-103">使用 zipdeploy 從 ZIP、JAR 或 WAR 檔案部署 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="a444c-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="a444c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a444c-104">SYNTAX</span></span>

### <span data-ttu-id="a444c-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a444c-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a444c-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a444c-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a444c-107">說明</span><span class="sxs-lookup"><span data-stu-id="a444c-107">DESCRIPTION</span></span>
<span data-ttu-id="a444c-108">**Publish AzWebApp** Cmdlet 會將內容上傳到現有的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="a444c-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="a444c-109">如果使用的是 .NET、Python 或 Node 等堆疊，請將內容封裝在 ZIP 檔案中，或在使用 JAVA 時使用 WAR 或 JAR 檔案。</span><span class="sxs-lookup"><span data-stu-id="a444c-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="a444c-110">在部署期間，必須預先建立內容並準備好執行，而不需要任何額外的建立步驟。</span><span class="sxs-lookup"><span data-stu-id="a444c-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="a444c-111">這個 Cmdlet 使用 Kudu zipdeploy 和 wardeploy 功能來部署內容。</span><span class="sxs-lookup"><span data-stu-id="a444c-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="a444c-112">請參閱 Kudu wiki，以取得有關 zipdeploy 和 wardeploy 運作方式的詳細資料，以及如何正確地封裝 web 應用程式以進行部署。</span><span class="sxs-lookup"><span data-stu-id="a444c-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="a444c-113"> https://aka.ms/kuduzipdeploy 以及 https://aka.ms/kuduwardeploy 包含有關 zipdeploy 和 wardeploy 的有用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a444c-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="a444c-114">示例</span><span class="sxs-lookup"><span data-stu-id="a444c-114">EXAMPLES</span></span>

### <span data-ttu-id="a444c-115">範例1</span><span class="sxs-lookup"><span data-stu-id="a444c-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="a444c-116">將 app.zip 的內容上傳到屬於資源群組的 web app （預設為 [網站-WestUS]）。</span><span class="sxs-lookup"><span data-stu-id="a444c-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="a444c-117">範例2</span><span class="sxs-lookup"><span data-stu-id="a444c-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="a444c-118">將 javaproject 的內容上傳到屬於資源群組 ContosoRG 之名為 ContosoApp 之 web app 的分段槽。</span><span class="sxs-lookup"><span data-stu-id="a444c-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="a444c-119">範例3</span><span class="sxs-lookup"><span data-stu-id="a444c-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="a444c-120">將 app.zip 的內容上傳到屬於資源群組 ContosoRG 的名為 ContosoApp 的 web app。</span><span class="sxs-lookup"><span data-stu-id="a444c-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="a444c-121">此 Cmdlet 將在背景作業中執行。</span><span class="sxs-lookup"><span data-stu-id="a444c-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="a444c-122">範例4</span><span class="sxs-lookup"><span data-stu-id="a444c-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="a444c-123">將 java_app .jar 的內容上傳到屬於資源群組 ContosoRG 的名為 ContosoApp 的 web app。</span><span class="sxs-lookup"><span data-stu-id="a444c-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="a444c-124">參數</span><span class="sxs-lookup"><span data-stu-id="a444c-124">PARAMETERS</span></span>

### <span data-ttu-id="a444c-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="a444c-125">-ArchivePath</span></span>
<span data-ttu-id="a444c-126">封存檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a444c-126">The path of the archive file.</span></span> <span data-ttu-id="a444c-127">支援 ZIP、WAR 和 JAR。</span><span class="sxs-lookup"><span data-stu-id="a444c-127">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a444c-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a444c-128">-AsJob</span></span>
<span data-ttu-id="a444c-129">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a444c-129">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a444c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a444c-130">-DefaultProfile</span></span>
<span data-ttu-id="a444c-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a444c-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a444c-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="a444c-132">-Name</span></span>
<span data-ttu-id="a444c-133">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a444c-133">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a444c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a444c-134">-ResourceGroupName</span></span>
<span data-ttu-id="a444c-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a444c-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a444c-136">-槽</span><span class="sxs-lookup"><span data-stu-id="a444c-136">-Slot</span></span>
<span data-ttu-id="a444c-137">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="a444c-137">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a444c-138">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a444c-138">-WebApp</span></span>
<span data-ttu-id="a444c-139">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="a444c-139">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a444c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a444c-140">CommonParameters</span></span>
<span data-ttu-id="a444c-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a444c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a444c-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a444c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a444c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a444c-143">INPUTS</span></span>

### <span data-ttu-id="a444c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="a444c-144">System.String</span></span>

### <span data-ttu-id="a444c-145">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a444c-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a444c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a444c-146">OUTPUTS</span></span>

### <span data-ttu-id="a444c-147">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a444c-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a444c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a444c-148">NOTES</span></span>

## <span data-ttu-id="a444c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a444c-149">RELATED LINKS</span></span>

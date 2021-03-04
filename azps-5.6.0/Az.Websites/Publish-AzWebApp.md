---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 726f991f5e51b6196b61a6e977ba1c5d4a1debf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917537"
---
# <span data-ttu-id="f4e9d-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f4e9d-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="f4e9d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f4e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e9d-103">使用 zipdeploy 從 ZIP、JAR 或 WAR 檔案部署 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="f4e9d-104">語法</span><span class="sxs-lookup"><span data-stu-id="f4e9d-104">SYNTAX</span></span>

### <span data-ttu-id="f4e9d-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f4e9d-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4e9d-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f4e9d-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="f4e9d-107">描述</span><span class="sxs-lookup"><span data-stu-id="f4e9d-107">DESCRIPTION</span></span>
<span data-ttu-id="f4e9d-108">**Publish-AzWebApp** Cmdlet 會上傳內容至現有的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="f4e9d-109">如果使用堆疊 ，例如 .NET、JAVA 或 Node，則內容應封裝在 ZIP 檔案中;如果使用 JAVA，則應封裝為 WAR 或 JAR 檔案。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="f4e9d-110">內容應預先建立並可供執行，而不需要在部署期間執行任何其他的建立步驟。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="f4e9d-111">此 Cmdlet 會使用 Kudu zipdeploy 和loy 功能來部署內容。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="f4e9d-112">請參閱 Kudu Wiki，以瞭解有關 zipdeploy 和eploy 如何運作，以及如何正確封裝 Web 應用程式進行部署的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="f4e9d-113"> https://aka.ms/kuduzipdeploy 並 https://aka.ms/kuduwardeploy 包含有關 zipdeploy 和eploy 的實用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="f4e9d-114">例子</span><span class="sxs-lookup"><span data-stu-id="f4e9d-114">EXAMPLES</span></span>

### <span data-ttu-id="f4e9d-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="f4e9d-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="f4e9d-116">將檔內容上傳到app.zip資源群組 Default-Web-WestUS 的名為 MyApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="f4e9d-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="f4e9d-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="f4e9d-118">將 javaproject.war 的內容上傳到屬於資源群組 ContosoRG 的 Web App 的暫存時段。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="f4e9d-119">範例 3</span><span class="sxs-lookup"><span data-stu-id="f4e9d-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="f4e9d-120">將檔內容上傳到app.zip ContosoApp 屬於資源群組 ContosoRG 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="f4e9d-121">Cmdlet 會以背景工作執行。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="f4e9d-122">範例 4</span><span class="sxs-lookup"><span data-stu-id="f4e9d-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="f4e9d-123">範例 5</span><span class="sxs-lookup"><span data-stu-id="f4e9d-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="f4e9d-124">將 java_app.jar 的內容上傳到屬於資源群組 ContosoRG 的名為 ContosoApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="f4e9d-125">範例 6</span><span class="sxs-lookup"><span data-stu-id="f4e9d-125">Example 6</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Timeout 300000 -Force
```

<span data-ttu-id="f4e9d-126">將 java_app.jar 的內容上傳到屬於資源群組 ContosoRG 的名為 ContosoApp 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-126">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="f4e9d-127">使用者可以將時間範圍設定為以毫秒為單位，等待要求時間過長。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-127">User can Sets the timespan in Milliseconds to wait before the request times out.</span></span>

## <span data-ttu-id="f4e9d-128">參數</span><span class="sxs-lookup"><span data-stu-id="f4e9d-128">PARAMETERS</span></span>

### <span data-ttu-id="f4e9d-129">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="f4e9d-129">-ArchivePath</span></span>
<span data-ttu-id="f4e9d-130">該檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-130">The path of the archive file.</span></span> <span data-ttu-id="f4e9d-131">支援 ZIP、WAR 和 JAR。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-131">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="f4e9d-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4e9d-132">-AsJob</span></span>
<span data-ttu-id="f4e9d-133">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4e9d-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4e9d-134">-強制</span><span class="sxs-lookup"><span data-stu-id="f4e9d-134">-Force</span></span>
<span data-ttu-id="f4e9d-135">強制移除選項</span><span class="sxs-lookup"><span data-stu-id="f4e9d-135">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="f4e9d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e9d-136">-DefaultProfile</span></span>
<span data-ttu-id="f4e9d-137">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e9d-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4e9d-138">-Name</span></span>
<span data-ttu-id="f4e9d-139">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-139">The name of the web app.</span></span>

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

### <span data-ttu-id="f4e9d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e9d-140">-ResourceGroupName</span></span>
<span data-ttu-id="f4e9d-141">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4e9d-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="f4e9d-142">-Slot</span></span>
<span data-ttu-id="f4e9d-143">Web App 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-143">The name of the web app slot.</span></span>

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

### <span data-ttu-id="f4e9d-144">-Timeout</span><span class="sxs-lookup"><span data-stu-id="f4e9d-144">-Timeout</span></span>
<span data-ttu-id="f4e9d-145">將時間範圍設定為以毫秒為單位，等待要求時間過長。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-145">Sets the timespan in Milliseconds to wait before the request times out.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e9d-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f4e9d-146">-WebApp</span></span>
<span data-ttu-id="f4e9d-147">Web App 物件</span><span class="sxs-lookup"><span data-stu-id="f4e9d-147">The web app object</span></span>

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

### <span data-ttu-id="f4e9d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e9d-148">CommonParameters</span></span>
<span data-ttu-id="f4e9d-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e9d-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f4e9d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e9d-151">輸入</span><span class="sxs-lookup"><span data-stu-id="f4e9d-151">INPUTS</span></span>

### <span data-ttu-id="f4e9d-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f4e9d-152">System.String</span></span>

### <span data-ttu-id="f4e9d-153">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f4e9d-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f4e9d-154">輸出</span><span class="sxs-lookup"><span data-stu-id="f4e9d-154">OUTPUTS</span></span>

### <span data-ttu-id="f4e9d-155">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f4e9d-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f4e9d-156">筆記</span><span class="sxs-lookup"><span data-stu-id="f4e9d-156">NOTES</span></span>

## <span data-ttu-id="f4e9d-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4e9d-157">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 9d544d48a430aa671c0c18721e6dece6f1351424
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793205"
---
# <span data-ttu-id="256d0-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="256d0-101">New-AzWebApp</span></span>

## <span data-ttu-id="256d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="256d0-102">SYNOPSIS</span></span>
<span data-ttu-id="256d0-103">建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="256d0-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="256d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="256d0-104">SYNTAX</span></span>

### <span data-ttu-id="256d0-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="256d0-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="256d0-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="256d0-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="256d0-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="256d0-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="256d0-108">說明</span><span class="sxs-lookup"><span data-stu-id="256d0-108">DESCRIPTION</span></span>
<span data-ttu-id="256d0-109">**AzWebApp** Cmdlet 會在指定的資源群組中，使用指定的應用程式服務方案和資料中心來建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="256d0-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="256d0-110">示例</span><span class="sxs-lookup"><span data-stu-id="256d0-110">EXAMPLES</span></span>

### <span data-ttu-id="256d0-111">範例1：建立 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="256d0-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="256d0-112">這個命令會在資料中心的名為「預設-Web-WestUS」的現有資源群組中，建立名為 ContosoSite 的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="256d0-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="256d0-113">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="256d0-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="256d0-114">參數</span><span class="sxs-lookup"><span data-stu-id="256d0-114">PARAMETERS</span></span>

### <span data-ttu-id="256d0-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="256d0-115">-AppServicePlan</span></span>
<span data-ttu-id="256d0-116">應用程式服務計畫名稱或應用程式服務方案識別碼。如果 WebApp 和 App 服務方案位於不同的資源群組中，請使用 ID 而不是名稱。</span><span class="sxs-lookup"><span data-stu-id="256d0-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="256d0-117">您可以使用下列方法來檢索 App 服務方案識別碼： $asp = Get-AzAppServicePlan ResourceGroup myRG-Name MyWebapp $asp。 Id 會傳回應用程式服務方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="256d0-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="256d0-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="256d0-119">應用程式設定會覆寫 HashTable</span><span class="sxs-lookup"><span data-stu-id="256d0-119">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="256d0-120">-AseName</span></span>
<span data-ttu-id="256d0-121">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="256d0-121">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="256d0-122">-AseResourceGroupName</span></span>
<span data-ttu-id="256d0-123">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="256d0-123">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="256d0-124">-AsJob</span></span>
<span data-ttu-id="256d0-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="256d0-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="256d0-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="256d0-126">-ContainerImageName</span></span>
<span data-ttu-id="256d0-127">容器影像名稱和選用的標籤，例如 (影像： tag) </span><span class="sxs-lookup"><span data-stu-id="256d0-127">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="256d0-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="256d0-129">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="256d0-129">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="256d0-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="256d0-131">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="256d0-131">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="256d0-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="256d0-133">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="256d0-133">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="256d0-134">-DefaultProfile</span></span>
<span data-ttu-id="256d0-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="256d0-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="256d0-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="256d0-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="256d0-137">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="256d0-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="256d0-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="256d0-138">-GitRepositoryPath</span></span>
<span data-ttu-id="256d0-139">包含要部署之 web 應用程式之 GitHub 儲存庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="256d0-139">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="256d0-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="256d0-141">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="256d0-141">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="256d0-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="256d0-143">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="256d0-143">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="256d0-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="256d0-145">[包括來源 WebApp 槽] 選項</span><span class="sxs-lookup"><span data-stu-id="256d0-145">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-146">-位置</span><span class="sxs-lookup"><span data-stu-id="256d0-146">-Location</span></span>
<span data-ttu-id="256d0-147">位於</span><span class="sxs-lookup"><span data-stu-id="256d0-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="256d0-148">-Name</span></span>
<span data-ttu-id="256d0-149">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="256d0-149">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="256d0-150">-ResourceGroupName</span></span>
<span data-ttu-id="256d0-151">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="256d0-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="256d0-152">-SourceWebApp</span></span>
<span data-ttu-id="256d0-153">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="256d0-153">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="256d0-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="256d0-155">現有流量管理器設定檔的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="256d0-155">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-156">-確認</span><span class="sxs-lookup"><span data-stu-id="256d0-156">-Confirm</span></span>
<span data-ttu-id="256d0-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="256d0-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="256d0-158">-WhatIf</span></span>
<span data-ttu-id="256d0-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="256d0-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="256d0-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="256d0-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256d0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256d0-161">CommonParameters</span></span>
<span data-ttu-id="256d0-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="256d0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256d0-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="256d0-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256d0-164">輸入</span><span class="sxs-lookup"><span data-stu-id="256d0-164">INPUTS</span></span>

### <span data-ttu-id="256d0-165">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="256d0-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="256d0-166">輸出</span><span class="sxs-lookup"><span data-stu-id="256d0-166">OUTPUTS</span></span>

### <span data-ttu-id="256d0-167">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="256d0-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="256d0-168">筆記</span><span class="sxs-lookup"><span data-stu-id="256d0-168">NOTES</span></span>

## <span data-ttu-id="256d0-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="256d0-169">RELATED LINKS</span></span>

[<span data-ttu-id="256d0-170">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="256d0-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="256d0-171">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="256d0-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="256d0-172">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="256d0-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="256d0-173">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="256d0-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="256d0-174">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="256d0-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: e09c2660f37a7b737d137c0907ff74ef9e39a5ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907013"
---
# <span data-ttu-id="5455a-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5455a-101">New-AzWebApp</span></span>

## <span data-ttu-id="5455a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5455a-102">SYNOPSIS</span></span>
<span data-ttu-id="5455a-103">建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="5455a-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="5455a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5455a-104">SYNTAX</span></span>

### <span data-ttu-id="5455a-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5455a-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5455a-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="5455a-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5455a-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="5455a-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5455a-108">描述</span><span class="sxs-lookup"><span data-stu-id="5455a-108">DESCRIPTION</span></span>
<span data-ttu-id="5455a-109">**New-AzWebApp** Cmdlet 會使用指定的應用程式服務計畫和資料中心，在指定的資源群組中建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="5455a-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="5455a-110">例子</span><span class="sxs-lookup"><span data-stu-id="5455a-110">EXAMPLES</span></span>

### <span data-ttu-id="5455a-111">範例 1：建立 Web App</span><span class="sxs-lookup"><span data-stu-id="5455a-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="5455a-112">此命令會在美國西部資料中心名為 Default-Web-WestUS 的現有資源群組中，建立名為 ContosoSite 的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="5455a-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="5455a-113">該命令使用名為 ContosoServicePlan 的現有應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="5455a-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="5455a-114">參數</span><span class="sxs-lookup"><span data-stu-id="5455a-114">PARAMETERS</span></span>

### <span data-ttu-id="5455a-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5455a-115">-AppServicePlan</span></span>
<span data-ttu-id="5455a-116">應用程式服務方案名稱或應用程式服務方案識別碼。如果 WebApp 與 App 服務方案在不同的資源群組中，請使用識別碼而非名稱。</span><span class="sxs-lookup"><span data-stu-id="5455a-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="5455a-117">您可以使用：$asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id 會返回應用程式服務方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="5455a-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="5455a-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="5455a-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="5455a-119">應用程式設定會覆蓋雜湊表</span><span class="sxs-lookup"><span data-stu-id="5455a-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="5455a-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="5455a-120">-AseName</span></span>
<span data-ttu-id="5455a-121">應用程式服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="5455a-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="5455a-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5455a-122">-AseResourceGroupName</span></span>
<span data-ttu-id="5455a-123">應用程式服務環境資源組名</span><span class="sxs-lookup"><span data-stu-id="5455a-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="5455a-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5455a-124">-AsJob</span></span>
<span data-ttu-id="5455a-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5455a-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5455a-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="5455a-126">-ContainerImageName</span></span>
<span data-ttu-id="5455a-127">容器圖像名稱及選擇性標記，例如 (：標記) </span><span class="sxs-lookup"><span data-stu-id="5455a-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="5455a-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="5455a-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="5455a-129">私人容器登錄密碼</span><span class="sxs-lookup"><span data-stu-id="5455a-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="5455a-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="5455a-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="5455a-131">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="5455a-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="5455a-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="5455a-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="5455a-133">私人容器登錄使用者名稱</span><span class="sxs-lookup"><span data-stu-id="5455a-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="5455a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5455a-134">-DefaultProfile</span></span>
<span data-ttu-id="5455a-135">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5455a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5455a-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="5455a-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="5455a-137">啟用/停用容器連續部署網頁元件</span><span class="sxs-lookup"><span data-stu-id="5455a-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="5455a-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="5455a-138">-GitRepositoryPath</span></span>
<span data-ttu-id="5455a-139">包含要部署的 Web 應用程式之 GitHub 存放庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="5455a-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="5455a-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="5455a-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="5455a-141">忽略自訂主機名稱選項</span><span class="sxs-lookup"><span data-stu-id="5455a-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="5455a-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="5455a-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="5455a-143">忽略原始程式碼管理選項</span><span class="sxs-lookup"><span data-stu-id="5455a-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="5455a-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="5455a-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="5455a-145">包含來源 WebApp 插槽選項</span><span class="sxs-lookup"><span data-stu-id="5455a-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="5455a-146">-位置</span><span class="sxs-lookup"><span data-stu-id="5455a-146">-Location</span></span>
<span data-ttu-id="5455a-147">位置</span><span class="sxs-lookup"><span data-stu-id="5455a-147">Location</span></span>

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

### <span data-ttu-id="5455a-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="5455a-148">-Name</span></span>
<span data-ttu-id="5455a-149">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="5455a-149">WebApp Name</span></span>

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

### <span data-ttu-id="5455a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5455a-150">-ResourceGroupName</span></span>
<span data-ttu-id="5455a-151">資源組名</span><span class="sxs-lookup"><span data-stu-id="5455a-151">Resource Group Name</span></span>

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

### <span data-ttu-id="5455a-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="5455a-152">-SourceWebApp</span></span>
<span data-ttu-id="5455a-153">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="5455a-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="5455a-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5455a-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="5455a-155">現有流量管理員設定檔的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5455a-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="5455a-156">-確認</span><span class="sxs-lookup"><span data-stu-id="5455a-156">-Confirm</span></span>
<span data-ttu-id="5455a-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5455a-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5455a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5455a-158">-WhatIf</span></span>
<span data-ttu-id="5455a-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5455a-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5455a-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5455a-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5455a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5455a-161">CommonParameters</span></span>
<span data-ttu-id="5455a-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5455a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5455a-163">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5455a-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5455a-164">輸入</span><span class="sxs-lookup"><span data-stu-id="5455a-164">INPUTS</span></span>

### <span data-ttu-id="5455a-165">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5455a-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5455a-166">輸出</span><span class="sxs-lookup"><span data-stu-id="5455a-166">OUTPUTS</span></span>

### <span data-ttu-id="5455a-167">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5455a-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5455a-168">筆記</span><span class="sxs-lookup"><span data-stu-id="5455a-168">NOTES</span></span>

## <span data-ttu-id="5455a-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="5455a-169">RELATED LINKS</span></span>

[<span data-ttu-id="5455a-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5455a-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="5455a-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5455a-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="5455a-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5455a-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="5455a-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5455a-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="5455a-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5455a-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)



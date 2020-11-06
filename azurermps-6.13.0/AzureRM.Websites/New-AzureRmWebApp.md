---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443624"
---
# <span data-ttu-id="017c2-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="017c2-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="017c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="017c2-102">SYNOPSIS</span></span>
<span data-ttu-id="017c2-103">建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="017c2-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="017c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="017c2-104">SYNTAX</span></span>

### <span data-ttu-id="017c2-105">SimpleParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="017c2-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="017c2-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="017c2-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="017c2-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="017c2-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="017c2-108">說明</span><span class="sxs-lookup"><span data-stu-id="017c2-108">DESCRIPTION</span></span>
<span data-ttu-id="017c2-109">**AzureRmWebApp** Cmdlet 會在指定的資源群組中，使用指定的應用程式服務方案和資料中心來建立 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="017c2-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="017c2-110">示例</span><span class="sxs-lookup"><span data-stu-id="017c2-110">EXAMPLES</span></span>

### <span data-ttu-id="017c2-111">範例1：建立 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="017c2-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="017c2-112">這個命令會在資料中心的名為「預設-Web-WestUS」的現有資源群組中，建立名為 ContosoSite 的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="017c2-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="017c2-113">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="017c2-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="017c2-114">參數</span><span class="sxs-lookup"><span data-stu-id="017c2-114">PARAMETERS</span></span>

### <span data-ttu-id="017c2-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="017c2-115">-AppServicePlan</span></span>
<span data-ttu-id="017c2-116">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="017c2-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="017c2-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="017c2-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="017c2-118">應用程式設定會覆寫 HashTable</span><span class="sxs-lookup"><span data-stu-id="017c2-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="017c2-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="017c2-119">-AseName</span></span>
<span data-ttu-id="017c2-120">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="017c2-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="017c2-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017c2-121">-AseResourceGroupName</span></span>
<span data-ttu-id="017c2-122">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="017c2-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="017c2-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="017c2-123">-AsJob</span></span>
<span data-ttu-id="017c2-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="017c2-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="017c2-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="017c2-125">-ContainerImageName</span></span>
<span data-ttu-id="017c2-126">容器影像名稱和選用的標籤，例如 (影像： tag) </span><span class="sxs-lookup"><span data-stu-id="017c2-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="017c2-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="017c2-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="017c2-128">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="017c2-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="017c2-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="017c2-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="017c2-130">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="017c2-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="017c2-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="017c2-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="017c2-132">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="017c2-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="017c2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017c2-133">-DefaultProfile</span></span>
<span data-ttu-id="017c2-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="017c2-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017c2-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="017c2-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="017c2-136">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="017c2-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="017c2-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="017c2-137">-GitRepositoryPath</span></span>
<span data-ttu-id="017c2-138">GitHub 知識庫的路徑 containign 要部署的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="017c2-138">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="017c2-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="017c2-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="017c2-140">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="017c2-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="017c2-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="017c2-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="017c2-142">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="017c2-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="017c2-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="017c2-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="017c2-144">[包括來源 WebApp 槽] 選項</span><span class="sxs-lookup"><span data-stu-id="017c2-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="017c2-145">-位置</span><span class="sxs-lookup"><span data-stu-id="017c2-145">-Location</span></span>
<span data-ttu-id="017c2-146">位於</span><span class="sxs-lookup"><span data-stu-id="017c2-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="017c2-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="017c2-147">-Name</span></span>
<span data-ttu-id="017c2-148">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="017c2-148">WebApp Name</span></span>

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

### <span data-ttu-id="017c2-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017c2-149">-ResourceGroupName</span></span>
<span data-ttu-id="017c2-150">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="017c2-150">Resource Group Name</span></span>

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

### <span data-ttu-id="017c2-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="017c2-151">-SourceWebApp</span></span>
<span data-ttu-id="017c2-152">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="017c2-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="017c2-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="017c2-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="017c2-154">現有流量管理器設定檔的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="017c2-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="017c2-155">-確認</span><span class="sxs-lookup"><span data-stu-id="017c2-155">-Confirm</span></span>
<span data-ttu-id="017c2-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="017c2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="017c2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="017c2-157">-WhatIf</span></span>
<span data-ttu-id="017c2-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="017c2-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="017c2-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="017c2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="017c2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017c2-160">CommonParameters</span></span>
<span data-ttu-id="017c2-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="017c2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017c2-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="017c2-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017c2-163">輸入</span><span class="sxs-lookup"><span data-stu-id="017c2-163">INPUTS</span></span>

### <span data-ttu-id="017c2-164">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="017c2-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="017c2-165">參數： SourceWebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="017c2-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="017c2-166">輸出</span><span class="sxs-lookup"><span data-stu-id="017c2-166">OUTPUTS</span></span>

### <span data-ttu-id="017c2-167">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="017c2-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="017c2-168">筆記</span><span class="sxs-lookup"><span data-stu-id="017c2-168">NOTES</span></span>

## <span data-ttu-id="017c2-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="017c2-169">RELATED LINKS</span></span>

[<span data-ttu-id="017c2-170">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="017c2-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="017c2-171">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="017c2-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="017c2-172">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="017c2-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="017c2-173">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="017c2-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="017c2-174">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="017c2-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)



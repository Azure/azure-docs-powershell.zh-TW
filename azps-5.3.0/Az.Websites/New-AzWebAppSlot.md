---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 2228eb7562ed7a0ffa1c0098086c085985e45fee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435992"
---
# <span data-ttu-id="f6a65-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6a65-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="f6a65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6a65-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a65-103">建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="f6a65-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="f6a65-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6a65-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6a65-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6a65-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a65-106">**AzWebAppSlot** Cmdlet 會在指定的資源群組中使用指定的應用程式服務方案和資料中心來建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="f6a65-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="f6a65-107">示例</span><span class="sxs-lookup"><span data-stu-id="f6a65-107">EXAMPLES</span></span>

### <span data-ttu-id="f6a65-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f6a65-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="f6a65-109">這個命令會在已有的 Web App 名稱 ContosoSite 中，建立一個名為 Slot001 的槽，在「資料中心」的現有資源群組中的 [預設-網路-WestUS] 西部我們。</span><span class="sxs-lookup"><span data-stu-id="f6a65-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="f6a65-110">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="f6a65-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="f6a65-111">參數</span><span class="sxs-lookup"><span data-stu-id="f6a65-111">PARAMETERS</span></span>

### <span data-ttu-id="f6a65-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f6a65-112">-AppServicePlan</span></span>
<span data-ttu-id="f6a65-113">應用程式服務計畫名稱或應用程式服務方案識別碼。如果槽位和 App 服務方案位於不同的資源群組中，請使用 ID 而不是名稱。</span><span class="sxs-lookup"><span data-stu-id="f6a65-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="f6a65-114">您可以使用下列方法來檢索 App 服務方案識別碼： $asp = Get-AzAppServicePlan ResourceGroup myRG-Name MyWebapp $asp。 Id 會傳回應用程式服務方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6a65-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="f6a65-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="f6a65-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="f6a65-116">應用程式設定會覆寫 Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6a65-116">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="f6a65-117">-AseName</span></span>
<span data-ttu-id="f6a65-118">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="f6a65-118">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a65-119">-AseResourceGroupName</span></span>
<span data-ttu-id="f6a65-120">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f6a65-120">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6a65-121">-AsJob</span></span>
<span data-ttu-id="f6a65-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6a65-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6a65-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="f6a65-123">-ContainerImageName</span></span>
<span data-ttu-id="f6a65-124">容器影像名稱和選用的標籤，例如 (影像： tag) </span><span class="sxs-lookup"><span data-stu-id="f6a65-124">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="f6a65-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="f6a65-126">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="f6a65-126">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="f6a65-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="f6a65-128">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="f6a65-128">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="f6a65-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="f6a65-130">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="f6a65-130">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a65-131">-DefaultProfile</span></span>
<span data-ttu-id="f6a65-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6a65-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6a65-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="f6a65-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="f6a65-134">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="f6a65-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="f6a65-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="f6a65-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="f6a65-136">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="f6a65-136">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="f6a65-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="f6a65-138">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="f6a65-138">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6a65-139">-Name</span></span>
<span data-ttu-id="f6a65-140">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="f6a65-140">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a65-141">-ResourceGroupName</span></span>
<span data-ttu-id="f6a65-142">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f6a65-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-143">-槽</span><span class="sxs-lookup"><span data-stu-id="f6a65-143">-Slot</span></span>
<span data-ttu-id="f6a65-144">Webapp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="f6a65-144">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="f6a65-145">-SourceWebApp</span></span>
<span data-ttu-id="f6a65-146">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="f6a65-146">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6a65-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a65-147">CommonParameters</span></span>
<span data-ttu-id="f6a65-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6a65-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a65-149">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6a65-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a65-150">輸入</span><span class="sxs-lookup"><span data-stu-id="f6a65-150">INPUTS</span></span>

### <span data-ttu-id="f6a65-151">System.object</span><span class="sxs-lookup"><span data-stu-id="f6a65-151">System.String</span></span>

### <span data-ttu-id="f6a65-152">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="f6a65-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f6a65-153">輸出</span><span class="sxs-lookup"><span data-stu-id="f6a65-153">OUTPUTS</span></span>

### <span data-ttu-id="f6a65-154">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="f6a65-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f6a65-155">筆記</span><span class="sxs-lookup"><span data-stu-id="f6a65-155">NOTES</span></span>

## <span data-ttu-id="f6a65-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6a65-156">RELATED LINKS</span></span>

[<span data-ttu-id="f6a65-157">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6a65-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f6a65-158">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6a65-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="f6a65-159">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6a65-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="f6a65-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6a65-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="f6a65-161">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6a65-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="f6a65-162">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6a65-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="f6a65-163">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f6a65-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="f6a65-164">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f6a65-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

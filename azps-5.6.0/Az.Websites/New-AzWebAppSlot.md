---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 283b3dd7ec57150d1c93a6e01a85251ed94fbdf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907186"
---
# <span data-ttu-id="55f08-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="55f08-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="55f08-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55f08-102">SYNOPSIS</span></span>
<span data-ttu-id="55f08-103">建立 Azure Web App 插槽。</span><span class="sxs-lookup"><span data-stu-id="55f08-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="55f08-104">語法</span><span class="sxs-lookup"><span data-stu-id="55f08-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55f08-105">描述</span><span class="sxs-lookup"><span data-stu-id="55f08-105">DESCRIPTION</span></span>
<span data-ttu-id="55f08-106">**New-AzWebAppSlot** Cmdlet 會使用指定的應用程式服務計畫和資料中心，在指定的資源群組中建立 Azure Web App Slot。</span><span class="sxs-lookup"><span data-stu-id="55f08-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="55f08-107">例子</span><span class="sxs-lookup"><span data-stu-id="55f08-107">EXAMPLES</span></span>

### <span data-ttu-id="55f08-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="55f08-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="55f08-109">此命令會在美國西部資料中心名為 Default-Web-WestUS 的現有資源群組中，根據現有的 Web App 名稱 ContosoSite，建立一個名為 Slot001 的 Slot。</span><span class="sxs-lookup"><span data-stu-id="55f08-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="55f08-110">該命令使用名為 ContosoServicePlan 的現有應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="55f08-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="55f08-111">參數</span><span class="sxs-lookup"><span data-stu-id="55f08-111">PARAMETERS</span></span>

### <span data-ttu-id="55f08-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="55f08-112">-AppServicePlan</span></span>
<span data-ttu-id="55f08-113">應用程式服務方案名稱或應用程式服務方案識別碼。如果 Slot 與 App 服務方案在不同的資源群組中，請使用識別碼而非名稱。</span><span class="sxs-lookup"><span data-stu-id="55f08-113">App Service Plan Name or App Service Plan Id. If the Slot and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="55f08-114">您可以使用：$asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id 會返回應用程式服務方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="55f08-114">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>

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

### <span data-ttu-id="55f08-115">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="55f08-115">-AppSettingsOverrides</span></span>
<span data-ttu-id="55f08-116">應用程式設定會覆蓋雜湊表</span><span class="sxs-lookup"><span data-stu-id="55f08-116">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="55f08-117">-AseName</span><span class="sxs-lookup"><span data-stu-id="55f08-117">-AseName</span></span>
<span data-ttu-id="55f08-118">應用程式服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="55f08-118">App Service Environment Name</span></span>

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

### <span data-ttu-id="55f08-119">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f08-119">-AseResourceGroupName</span></span>
<span data-ttu-id="55f08-120">應用程式服務環境資源組名</span><span class="sxs-lookup"><span data-stu-id="55f08-120">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="55f08-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55f08-121">-AsJob</span></span>
<span data-ttu-id="55f08-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="55f08-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55f08-123">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="55f08-123">-ContainerImageName</span></span>
<span data-ttu-id="55f08-124">容器圖像名稱及選擇性標記，例如 (：標記) </span><span class="sxs-lookup"><span data-stu-id="55f08-124">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="55f08-125">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="55f08-125">-ContainerRegistryPassword</span></span>
<span data-ttu-id="55f08-126">私人容器登錄密碼</span><span class="sxs-lookup"><span data-stu-id="55f08-126">Private Container Registry Password</span></span>

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

### <span data-ttu-id="55f08-127">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="55f08-127">-ContainerRegistryUrl</span></span>
<span data-ttu-id="55f08-128">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="55f08-128">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="55f08-129">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="55f08-129">-ContainerRegistryUser</span></span>
<span data-ttu-id="55f08-130">私人容器登錄使用者名稱</span><span class="sxs-lookup"><span data-stu-id="55f08-130">Private Container Registry Username</span></span>

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

### <span data-ttu-id="55f08-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f08-131">-DefaultProfile</span></span>
<span data-ttu-id="55f08-132">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55f08-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55f08-133">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="55f08-133">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="55f08-134">啟用/停用容器連續部署網頁元件</span><span class="sxs-lookup"><span data-stu-id="55f08-134">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="55f08-135">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="55f08-135">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="55f08-136">忽略自訂主機名稱選項</span><span class="sxs-lookup"><span data-stu-id="55f08-136">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="55f08-137">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="55f08-137">-IgnoreSourceControl</span></span>
<span data-ttu-id="55f08-138">忽略原始程式碼管理選項</span><span class="sxs-lookup"><span data-stu-id="55f08-138">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="55f08-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="55f08-139">-Name</span></span>
<span data-ttu-id="55f08-140">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="55f08-140">Webapp Name</span></span>

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

### <span data-ttu-id="55f08-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f08-141">-ResourceGroupName</span></span>
<span data-ttu-id="55f08-142">資源組名</span><span class="sxs-lookup"><span data-stu-id="55f08-142">Resource Group Name</span></span>

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

### <span data-ttu-id="55f08-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="55f08-143">-Slot</span></span>
<span data-ttu-id="55f08-144">Webapp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="55f08-144">Webapp Slot Name</span></span>

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

### <span data-ttu-id="55f08-145">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="55f08-145">-SourceWebApp</span></span>
<span data-ttu-id="55f08-146">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="55f08-146">Source WebApp Object</span></span>

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

### <span data-ttu-id="55f08-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f08-147">CommonParameters</span></span>
<span data-ttu-id="55f08-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55f08-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f08-149">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="55f08-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f08-150">輸入</span><span class="sxs-lookup"><span data-stu-id="55f08-150">INPUTS</span></span>

### <span data-ttu-id="55f08-151">System.String</span><span class="sxs-lookup"><span data-stu-id="55f08-151">System.String</span></span>

### <span data-ttu-id="55f08-152">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="55f08-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="55f08-153">輸出</span><span class="sxs-lookup"><span data-stu-id="55f08-153">OUTPUTS</span></span>

### <span data-ttu-id="55f08-154">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="55f08-154">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="55f08-155">筆記</span><span class="sxs-lookup"><span data-stu-id="55f08-155">NOTES</span></span>

## <span data-ttu-id="55f08-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="55f08-156">RELATED LINKS</span></span>

[<span data-ttu-id="55f08-157">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="55f08-157">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="55f08-158">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="55f08-158">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="55f08-159">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="55f08-159">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="55f08-160">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="55f08-160">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="55f08-161">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="55f08-161">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="55f08-162">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="55f08-162">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="55f08-163">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="55f08-163">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="55f08-164">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="55f08-164">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

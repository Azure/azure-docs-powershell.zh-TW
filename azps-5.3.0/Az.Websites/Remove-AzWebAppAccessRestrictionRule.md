---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435986"
---
# <span data-ttu-id="3d0e4-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3d0e4-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="3d0e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="3d0e4-103">從 Azure Web App 移除訪問限制規則。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="3d0e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d0e4-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d0e4-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d0e4-105">DESCRIPTION</span></span>
<span data-ttu-id="3d0e4-106">**AzWebAppAccessRestrictionRule** Cmdlet 會從 Azure Web App 中移除訪問限制規則</span><span class="sxs-lookup"><span data-stu-id="3d0e4-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="3d0e4-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d0e4-107">EXAMPLES</span></span>

### <span data-ttu-id="3d0e4-108">範例1：移除 Web 應用程式存取限制規則</span><span class="sxs-lookup"><span data-stu-id="3d0e4-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="3d0e4-109">這個命令會從 Azure Web App 中移除名為「Default-Web-WestUS」的資源群組的 IpRule 存取限制規則。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="3d0e4-110">範例2：移除 Service 標記 Web App 存取限制規則</span><span class="sxs-lookup"><span data-stu-id="3d0e4-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="3d0e4-111">這個命令會從 Azure Web App 中移除名為 ServiceTag 等於 AzureFrontDoor 的 access 限制規則，該 ContosoSite 屬於名為 [預設-Web-WestUS] 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3d0e4-112">參數</span><span class="sxs-lookup"><span data-stu-id="3d0e4-112">PARAMETERS</span></span>

### <span data-ttu-id="3d0e4-113">-動作</span><span class="sxs-lookup"><span data-stu-id="3d0e4-113">-Action</span></span>
<span data-ttu-id="3d0e4-114">[允許] 或 [拒絕] 規則。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d0e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d0e4-115">-DefaultProfile</span></span>
<span data-ttu-id="3d0e4-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d0e4-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="3d0e4-117">-IpAddress</span></span>
<span data-ttu-id="3d0e4-118">Ip 位址 v4 或 v6 CIDR 範圍。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="3d0e4-119">例如： 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="3d0e4-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="3d0e4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d0e4-120">-Name</span></span>
<span data-ttu-id="3d0e4-121">Access 限制規則名稱</span><span class="sxs-lookup"><span data-stu-id="3d0e4-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="3d0e4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d0e4-122">-PassThru</span></span>
<span data-ttu-id="3d0e4-123">傳回 [存取限制] 設定物件。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="3d0e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d0e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d0e4-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3d0e4-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d0e4-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="3d0e4-126">-ServiceTag</span></span>
<span data-ttu-id="3d0e4-127">服務標記的名稱</span><span class="sxs-lookup"><span data-stu-id="3d0e4-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="3d0e4-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="3d0e4-128">-SlotName</span></span>
<span data-ttu-id="3d0e4-129">部署槽名稱。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="3d0e4-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3d0e4-130">-SubnetId</span></span>
<span data-ttu-id="3d0e4-131">子網上的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="3d0e4-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3d0e4-132">-SubnetName</span></span>
<span data-ttu-id="3d0e4-133">子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="3d0e4-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="3d0e4-134">-TargetScmSite</span></span>
<span data-ttu-id="3d0e4-135">規則主要針對主網站或 Scm 網站。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="3d0e4-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3d0e4-136">-VirtualNetworkName</span></span>
<span data-ttu-id="3d0e4-137">虛擬網路 (的名稱必須與 Web App) 在相同的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="3d0e4-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="3d0e4-138">-WebAppName</span></span>
<span data-ttu-id="3d0e4-139">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-139">The name of the web app.</span></span>

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

### <span data-ttu-id="3d0e4-140">-確認</span><span class="sxs-lookup"><span data-stu-id="3d0e4-140">-Confirm</span></span>
<span data-ttu-id="3d0e4-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d0e4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d0e4-142">-WhatIf</span></span>
<span data-ttu-id="3d0e4-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d0e4-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d0e4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d0e4-145">CommonParameters</span></span>
<span data-ttu-id="3d0e4-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d0e4-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d0e4-148">輸入</span><span class="sxs-lookup"><span data-stu-id="3d0e4-148">INPUTS</span></span>

### <span data-ttu-id="3d0e4-149">System.object</span><span class="sxs-lookup"><span data-stu-id="3d0e4-149">System.String</span></span>

## <span data-ttu-id="3d0e4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="3d0e4-150">OUTPUTS</span></span>

### <span data-ttu-id="3d0e4-151">PSAccessRestrictionConfig 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="3d0e4-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="3d0e4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="3d0e4-152">NOTES</span></span>

## <span data-ttu-id="3d0e4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d0e4-153">RELATED LINKS</span></span>

[<span data-ttu-id="3d0e4-154">AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3d0e4-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3d0e4-155">更新-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3d0e4-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3d0e4-156">附加 AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3d0e4-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

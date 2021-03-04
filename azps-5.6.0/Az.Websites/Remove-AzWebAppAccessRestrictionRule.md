---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913286"
---
# <span data-ttu-id="62d1b-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="62d1b-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="62d1b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="62d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="62d1b-103">從 Azure Web App 移除存取限制規則。</span><span class="sxs-lookup"><span data-stu-id="62d1b-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="62d1b-104">語法</span><span class="sxs-lookup"><span data-stu-id="62d1b-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62d1b-105">描述</span><span class="sxs-lookup"><span data-stu-id="62d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="62d1b-106">**Remove-AzWebAppAccessRestrictionRule** Cmdlet 會從 Azure Web App 移除存取限制規則</span><span class="sxs-lookup"><span data-stu-id="62d1b-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="62d1b-107">例子</span><span class="sxs-lookup"><span data-stu-id="62d1b-107">EXAMPLES</span></span>

### <span data-ttu-id="62d1b-108">範例 1：移除 Web App 存取限制規則</span><span class="sxs-lookup"><span data-stu-id="62d1b-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="62d1b-109">此命令會從名稱為 ContosoSite 的 Azure Web App 移除屬於 Default-Web-WestUS 資源群組的 IpRule 存取限制規則。</span><span class="sxs-lookup"><span data-stu-id="62d1b-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="62d1b-110">範例 2：移除服務標記 Web App 存取限制規則</span><span class="sxs-lookup"><span data-stu-id="62d1b-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="62d1b-111">此命令會從名稱為 ContosoSite 的 Azure Web App 移除 Access 限制規則，而 ServiceTag 等於 AzureFrontDoor.後端，該 Web App 屬於 Default-Web-WestUS 資源群組。</span><span class="sxs-lookup"><span data-stu-id="62d1b-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="62d1b-112">參數</span><span class="sxs-lookup"><span data-stu-id="62d1b-112">PARAMETERS</span></span>

### <span data-ttu-id="62d1b-113">-動作</span><span class="sxs-lookup"><span data-stu-id="62d1b-113">-Action</span></span>
<span data-ttu-id="62d1b-114">允許或拒絕規則。</span><span class="sxs-lookup"><span data-stu-id="62d1b-114">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="62d1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d1b-115">-DefaultProfile</span></span>
<span data-ttu-id="62d1b-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="62d1b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62d1b-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="62d1b-117">-IpAddress</span></span>
<span data-ttu-id="62d1b-118">Ip Address v4 或 v6 CIDR 範圍。</span><span class="sxs-lookup"><span data-stu-id="62d1b-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="62d1b-119">例如：192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="62d1b-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="62d1b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="62d1b-120">-Name</span></span>
<span data-ttu-id="62d1b-121">存取限制規則名稱</span><span class="sxs-lookup"><span data-stu-id="62d1b-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="62d1b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62d1b-122">-PassThru</span></span>
<span data-ttu-id="62d1b-123">返回存取限制 config 物件。</span><span class="sxs-lookup"><span data-stu-id="62d1b-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="62d1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62d1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="62d1b-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="62d1b-125">Resource Group Name</span></span>

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

### <span data-ttu-id="62d1b-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="62d1b-126">-ServiceTag</span></span>
<span data-ttu-id="62d1b-127">服務標記名稱</span><span class="sxs-lookup"><span data-stu-id="62d1b-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="62d1b-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="62d1b-128">-SlotName</span></span>
<span data-ttu-id="62d1b-129">部署插槽名稱。</span><span class="sxs-lookup"><span data-stu-id="62d1b-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="62d1b-130">-子網Id</span><span class="sxs-lookup"><span data-stu-id="62d1b-130">-SubnetId</span></span>
<span data-ttu-id="62d1b-131">子網的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="62d1b-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="62d1b-132">-子網名稱</span><span class="sxs-lookup"><span data-stu-id="62d1b-132">-SubnetName</span></span>
<span data-ttu-id="62d1b-133">子網名稱。</span><span class="sxs-lookup"><span data-stu-id="62d1b-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="62d1b-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="62d1b-134">-TargetScmSite</span></span>
<span data-ttu-id="62d1b-135">規則適用于主要網站或 Scm 網站。</span><span class="sxs-lookup"><span data-stu-id="62d1b-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="62d1b-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="62d1b-136">-VirtualNetworkName</span></span>
<span data-ttu-id="62d1b-137">虛擬網路名稱 (與 Web App 應用程式名稱必須在同一個資源) 。</span><span class="sxs-lookup"><span data-stu-id="62d1b-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="62d1b-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="62d1b-138">-WebAppName</span></span>
<span data-ttu-id="62d1b-139">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="62d1b-139">The name of the web app.</span></span>

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

### <span data-ttu-id="62d1b-140">-確認</span><span class="sxs-lookup"><span data-stu-id="62d1b-140">-Confirm</span></span>
<span data-ttu-id="62d1b-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="62d1b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62d1b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62d1b-142">-WhatIf</span></span>
<span data-ttu-id="62d1b-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62d1b-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62d1b-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62d1b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62d1b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d1b-145">CommonParameters</span></span>
<span data-ttu-id="62d1b-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="62d1b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d1b-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62d1b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d1b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="62d1b-148">INPUTS</span></span>

### <span data-ttu-id="62d1b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="62d1b-149">System.String</span></span>

## <span data-ttu-id="62d1b-150">輸出</span><span class="sxs-lookup"><span data-stu-id="62d1b-150">OUTPUTS</span></span>

### <span data-ttu-id="62d1b-151">Microsoft.Azure.Commands.WebApps.models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="62d1b-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="62d1b-152">筆記</span><span class="sxs-lookup"><span data-stu-id="62d1b-152">NOTES</span></span>

## <span data-ttu-id="62d1b-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="62d1b-153">RELATED LINKS</span></span>

[<span data-ttu-id="62d1b-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="62d1b-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="62d1b-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="62d1b-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="62d1b-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="62d1b-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140700"
---
# <span data-ttu-id="a1706-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a1706-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="a1706-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1706-102">SYNOPSIS</span></span>
<span data-ttu-id="a1706-103">從 Azure Web App 移除訪問限制規則。</span><span class="sxs-lookup"><span data-stu-id="a1706-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="a1706-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1706-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1706-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1706-105">DESCRIPTION</span></span>
<span data-ttu-id="a1706-106">**AzWebAppAccessRestrictionRule** Cmdlet 會從 Azure Web App 中移除訪問限制規則</span><span class="sxs-lookup"><span data-stu-id="a1706-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="a1706-107">示例</span><span class="sxs-lookup"><span data-stu-id="a1706-107">EXAMPLES</span></span>

### <span data-ttu-id="a1706-108">範例1：移除 Web 應用程式存取限制規則</span><span class="sxs-lookup"><span data-stu-id="a1706-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="a1706-109">這個命令會從 Azure Web App 中移除名為「Default-Web-WestUS」的資源群組的 IpRule 存取限制規則。</span><span class="sxs-lookup"><span data-stu-id="a1706-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a1706-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1706-110">PARAMETERS</span></span>

### <span data-ttu-id="a1706-111">-動作</span><span class="sxs-lookup"><span data-stu-id="a1706-111">-Action</span></span>
<span data-ttu-id="a1706-112">[允許] 或 [拒絕] 規則。</span><span class="sxs-lookup"><span data-stu-id="a1706-112">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1706-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1706-113">-DefaultProfile</span></span>
<span data-ttu-id="a1706-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1706-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1706-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a1706-115">-IpAddress</span></span>
<span data-ttu-id="a1706-116">Ip 位址 v4 或 v6 CIDR 範圍。</span><span class="sxs-lookup"><span data-stu-id="a1706-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="a1706-117">例如： 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="a1706-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="a1706-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1706-118">-Name</span></span>
<span data-ttu-id="a1706-119">Access 限制規則名稱</span><span class="sxs-lookup"><span data-stu-id="a1706-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="a1706-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1706-120">-PassThru</span></span>
<span data-ttu-id="a1706-121">傳回 [存取限制] 設定物件。</span><span class="sxs-lookup"><span data-stu-id="a1706-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="a1706-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1706-122">-ResourceGroupName</span></span>
<span data-ttu-id="a1706-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a1706-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a1706-124">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a1706-124">-SlotName</span></span>
<span data-ttu-id="a1706-125">部署槽名稱。</span><span class="sxs-lookup"><span data-stu-id="a1706-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="a1706-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a1706-126">-SubnetId</span></span>
<span data-ttu-id="a1706-127">子網上的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a1706-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="a1706-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a1706-128">-SubnetName</span></span>
<span data-ttu-id="a1706-129">子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1706-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="a1706-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="a1706-130">-TargetScmSite</span></span>
<span data-ttu-id="a1706-131">規則主要針對主網站或 Scm 網站。</span><span class="sxs-lookup"><span data-stu-id="a1706-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="a1706-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a1706-132">-VirtualNetworkName</span></span>
<span data-ttu-id="a1706-133">虛擬網路 (的名稱必須與 Web App) 在相同的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="a1706-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="a1706-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a1706-134">-WebAppName</span></span>
<span data-ttu-id="a1706-135">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1706-135">The name of the web app.</span></span>

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

### <span data-ttu-id="a1706-136">-確認</span><span class="sxs-lookup"><span data-stu-id="a1706-136">-Confirm</span></span>
<span data-ttu-id="a1706-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1706-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1706-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1706-138">-WhatIf</span></span>
<span data-ttu-id="a1706-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1706-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1706-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1706-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1706-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1706-141">CommonParameters</span></span>
<span data-ttu-id="a1706-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1706-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1706-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1706-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1706-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a1706-144">INPUTS</span></span>

### <span data-ttu-id="a1706-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a1706-145">System.String</span></span>

## <span data-ttu-id="a1706-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a1706-146">OUTPUTS</span></span>

### <span data-ttu-id="a1706-147">PSAccessRestrictionConfig 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a1706-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="a1706-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a1706-148">NOTES</span></span>

## <span data-ttu-id="a1706-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1706-149">RELATED LINKS</span></span>

[<span data-ttu-id="a1706-150">AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a1706-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a1706-151">更新-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a1706-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a1706-152">附加 AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a1706-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970759"
---
# <span data-ttu-id="71614-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="71614-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="71614-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71614-102">SYNOPSIS</span></span>
<span data-ttu-id="71614-103">從 Azure Web App 移除訪問限制規則。</span><span class="sxs-lookup"><span data-stu-id="71614-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="71614-104">句法</span><span class="sxs-lookup"><span data-stu-id="71614-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71614-105">說明</span><span class="sxs-lookup"><span data-stu-id="71614-105">DESCRIPTION</span></span>
<span data-ttu-id="71614-106">**AzWebAppAccessRestrictionRule** Cmdlet 會從 Azure Web App 中移除訪問限制規則</span><span class="sxs-lookup"><span data-stu-id="71614-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="71614-107">示例</span><span class="sxs-lookup"><span data-stu-id="71614-107">EXAMPLES</span></span>

### <span data-ttu-id="71614-108">範例1：移除 Web 應用程式存取限制規則</span><span class="sxs-lookup"><span data-stu-id="71614-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="71614-109">這個命令會從 Azure Web App 中移除名為「Default-Web-WestUS」的資源群組的 IpRule 存取限制規則。</span><span class="sxs-lookup"><span data-stu-id="71614-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="71614-110">參數</span><span class="sxs-lookup"><span data-stu-id="71614-110">PARAMETERS</span></span>

### <span data-ttu-id="71614-111">-動作</span><span class="sxs-lookup"><span data-stu-id="71614-111">-Action</span></span>
<span data-ttu-id="71614-112">[允許] 或 [拒絕] 規則。</span><span class="sxs-lookup"><span data-stu-id="71614-112">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="71614-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71614-113">-DefaultProfile</span></span>
<span data-ttu-id="71614-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71614-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71614-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="71614-115">-IpAddress</span></span>
<span data-ttu-id="71614-116">Ip 位址 v4 或 v6 CIDR 範圍。</span><span class="sxs-lookup"><span data-stu-id="71614-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="71614-117">例如： 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="71614-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="71614-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="71614-118">-Name</span></span>
<span data-ttu-id="71614-119">Access 限制規則名稱</span><span class="sxs-lookup"><span data-stu-id="71614-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="71614-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71614-120">-PassThru</span></span>
<span data-ttu-id="71614-121">傳回 [存取限制] 設定物件。</span><span class="sxs-lookup"><span data-stu-id="71614-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="71614-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71614-122">-ResourceGroupName</span></span>
<span data-ttu-id="71614-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="71614-123">Resource Group Name</span></span>

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

### <span data-ttu-id="71614-124">-SlotName</span><span class="sxs-lookup"><span data-stu-id="71614-124">-SlotName</span></span>
<span data-ttu-id="71614-125">部署槽名稱。</span><span class="sxs-lookup"><span data-stu-id="71614-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="71614-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="71614-126">-SubnetId</span></span>
<span data-ttu-id="71614-127">子網上的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="71614-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="71614-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="71614-128">-SubnetName</span></span>
<span data-ttu-id="71614-129">子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="71614-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="71614-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="71614-130">-TargetScmSite</span></span>
<span data-ttu-id="71614-131">規則主要針對主網站或 Scm 網站。</span><span class="sxs-lookup"><span data-stu-id="71614-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="71614-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="71614-132">-VirtualNetworkName</span></span>
<span data-ttu-id="71614-133">虛擬網路 (的名稱必須與 Web App) 在相同的資源群組中。</span><span class="sxs-lookup"><span data-stu-id="71614-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="71614-134">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="71614-134">-WebAppName</span></span>
<span data-ttu-id="71614-135">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="71614-135">The name of the web app.</span></span>

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

### <span data-ttu-id="71614-136">-確認</span><span class="sxs-lookup"><span data-stu-id="71614-136">-Confirm</span></span>
<span data-ttu-id="71614-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71614-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71614-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71614-138">-WhatIf</span></span>
<span data-ttu-id="71614-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71614-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71614-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71614-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71614-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71614-141">CommonParameters</span></span>
<span data-ttu-id="71614-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71614-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71614-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71614-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71614-144">輸入</span><span class="sxs-lookup"><span data-stu-id="71614-144">INPUTS</span></span>

### <span data-ttu-id="71614-145">System.object</span><span class="sxs-lookup"><span data-stu-id="71614-145">System.String</span></span>

## <span data-ttu-id="71614-146">輸出</span><span class="sxs-lookup"><span data-stu-id="71614-146">OUTPUTS</span></span>

### <span data-ttu-id="71614-147">PSAccessRestrictionConfig 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="71614-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="71614-148">筆記</span><span class="sxs-lookup"><span data-stu-id="71614-148">NOTES</span></span>

## <span data-ttu-id="71614-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="71614-149">RELATED LINKS</span></span>

[<span data-ttu-id="71614-150">AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="71614-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="71614-151">更新-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="71614-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="71614-152">附加 AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="71614-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

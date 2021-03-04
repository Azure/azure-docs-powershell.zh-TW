---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 3bb2a2d7c8e53cc7ba336234e3c5b24ad58e2faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913146"
---
# <span data-ttu-id="c9264-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c9264-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="c9264-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c9264-102">SYNOPSIS</span></span>
<span data-ttu-id="c9264-103">建立 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="c9264-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="c9264-104">語法</span><span class="sxs-lookup"><span data-stu-id="c9264-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9264-105">描述</span><span class="sxs-lookup"><span data-stu-id="c9264-105">DESCRIPTION</span></span>
<span data-ttu-id="c9264-106">建立新的 Azure VirtualWAN 資源。</span><span class="sxs-lookup"><span data-stu-id="c9264-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="c9264-107">例子</span><span class="sxs-lookup"><span data-stu-id="c9264-107">EXAMPLES</span></span>

### <span data-ttu-id="c9264-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c9264-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="c9264-109">上述步驟將在「西部美國」地區建立資源群組「testRG」，以及 Azure 虛擬 WAN，其分支至 Azure 資源群組中允許的分支流量。</span><span class="sxs-lookup"><span data-stu-id="c9264-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="c9264-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9264-110">PARAMETERS</span></span>

### <span data-ttu-id="c9264-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="c9264-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="c9264-112">允許分支到 VirtualWan 的分支流量。</span><span class="sxs-lookup"><span data-stu-id="c9264-112">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="c9264-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="c9264-114">允許 vnet 到 VirtualWan 的 vnet 流量。</span><span class="sxs-lookup"><span data-stu-id="c9264-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9264-115">-AsJob</span></span>
<span data-ttu-id="c9264-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c9264-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9264-117">-DefaultProfile</span></span>
<span data-ttu-id="c9264-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9264-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-119">-位置</span><span class="sxs-lookup"><span data-stu-id="c9264-119">-Location</span></span>
<span data-ttu-id="c9264-120">VirtualWAN 資源的位置。</span><span class="sxs-lookup"><span data-stu-id="c9264-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9264-121">-Name</span></span>
<span data-ttu-id="c9264-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c9264-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9264-123">-ResourceGroupName</span></span>
<span data-ttu-id="c9264-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c9264-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-125">-標記</span><span class="sxs-lookup"><span data-stu-id="c9264-125">-Tag</span></span>
<span data-ttu-id="c9264-126">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c9264-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="c9264-127">-VirtualWANType</span></span>
<span data-ttu-id="c9264-128">虛擬 Wan 的類型。</span><span class="sxs-lookup"><span data-stu-id="c9264-128">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c9264-129">-Confirm</span></span>
<span data-ttu-id="c9264-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c9264-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9264-131">-WhatIf</span></span>
<span data-ttu-id="c9264-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9264-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9264-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9264-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9264-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9264-134">CommonParameters</span></span>
<span data-ttu-id="c9264-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c9264-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9264-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9264-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9264-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c9264-137">INPUTS</span></span>

### <span data-ttu-id="c9264-138">沒有</span><span class="sxs-lookup"><span data-stu-id="c9264-138">None</span></span>

## <span data-ttu-id="c9264-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c9264-139">OUTPUTS</span></span>

### <span data-ttu-id="c9264-140">Microsoft.Azure.Commands.Network.models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c9264-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="c9264-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c9264-141">NOTES</span></span>

## <span data-ttu-id="c9264-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9264-142">RELATED LINKS</span></span>

[<span data-ttu-id="c9264-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c9264-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="c9264-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c9264-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="c9264-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="c9264-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)

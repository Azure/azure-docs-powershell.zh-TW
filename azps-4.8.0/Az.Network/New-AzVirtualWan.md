---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126442"
---
# <span data-ttu-id="b8fdb-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b8fdb-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="b8fdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fdb-103">建立 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="b8fdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8fdb-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8fdb-105">說明</span><span class="sxs-lookup"><span data-stu-id="b8fdb-105">DESCRIPTION</span></span>
<span data-ttu-id="b8fdb-106">建立新的 Azure VirtualWAN 資源。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="b8fdb-107">示例</span><span class="sxs-lookup"><span data-stu-id="b8fdb-107">EXAMPLES</span></span>

### <span data-ttu-id="b8fdb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b8fdb-108">Example 1</span></span>

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

<span data-ttu-id="b8fdb-109">上述將會在 [West 西部] 區域中建立資源群組 "testRG"，並在 Azure 中的 [該資源群組] 中使用分支來分支流量。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="b8fdb-110">參數</span><span class="sxs-lookup"><span data-stu-id="b8fdb-110">PARAMETERS</span></span>

### <span data-ttu-id="b8fdb-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="b8fdb-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="b8fdb-112">允許分支分支機搆 VirtualWan 的流量。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="b8fdb-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="b8fdb-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="b8fdb-114">允許 vnet 至 vnet 流量以進行 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="b8fdb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8fdb-115">-AsJob</span></span>
<span data-ttu-id="b8fdb-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b8fdb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8fdb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fdb-117">-DefaultProfile</span></span>
<span data-ttu-id="b8fdb-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8fdb-119">-位置</span><span class="sxs-lookup"><span data-stu-id="b8fdb-119">-Location</span></span>
<span data-ttu-id="b8fdb-120">VirtualWAN 資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="b8fdb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8fdb-121">-Name</span></span>
<span data-ttu-id="b8fdb-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-122">The resource name.</span></span>

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

### <span data-ttu-id="b8fdb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8fdb-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8fdb-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-124">The resource group name.</span></span>

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

### <span data-ttu-id="b8fdb-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b8fdb-125">-Tag</span></span>
<span data-ttu-id="b8fdb-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b8fdb-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="b8fdb-127">-VirtualWANType</span></span>
<span data-ttu-id="b8fdb-128">虛擬 Wan 的類型。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="b8fdb-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b8fdb-129">-Confirm</span></span>
<span data-ttu-id="b8fdb-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fdb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fdb-131">-WhatIf</span></span>
<span data-ttu-id="b8fdb-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8fdb-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fdb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fdb-134">CommonParameters</span></span>
<span data-ttu-id="b8fdb-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fdb-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8fdb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fdb-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b8fdb-137">INPUTS</span></span>

### <span data-ttu-id="b8fdb-138">所有</span><span class="sxs-lookup"><span data-stu-id="b8fdb-138">None</span></span>

## <span data-ttu-id="b8fdb-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b8fdb-139">OUTPUTS</span></span>

### <span data-ttu-id="b8fdb-140">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b8fdb-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="b8fdb-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b8fdb-141">NOTES</span></span>

## <span data-ttu-id="b8fdb-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8fdb-142">RELATED LINKS</span></span>

[<span data-ttu-id="b8fdb-143">AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b8fdb-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="b8fdb-144">移除-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b8fdb-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="b8fdb-145">更新-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b8fdb-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
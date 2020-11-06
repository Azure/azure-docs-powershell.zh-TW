---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
ms.openlocfilehash: 8d514ae4f01709d499c7685958cf13671e9b0c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455983"
---
# <span data-ttu-id="9cbb6-101">New-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="9cbb6-101">New-AzureRmVirtualWan</span></span>

## <span data-ttu-id="9cbb6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cbb6-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbb6-103">建立 Azure 虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-103">Creates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cbb6-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cbb6-104">SYNTAX</span></span>

```
New-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cbb6-105">說明</span><span class="sxs-lookup"><span data-stu-id="9cbb6-105">DESCRIPTION</span></span>
<span data-ttu-id="9cbb6-106">建立新的 Azure VirtualWAN 資源。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="9cbb6-107">示例</span><span class="sxs-lookup"><span data-stu-id="9cbb6-107">EXAMPLES</span></span>

### <span data-ttu-id="9cbb6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9cbb6-108">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="9cbb6-109">上述將會在 [West 西部] 區域中建立資源群組 "testRG"，並在 Azure 中的 [該資源群組] 中使用分支來分支流量。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="9cbb6-110">參數</span><span class="sxs-lookup"><span data-stu-id="9cbb6-110">PARAMETERS</span></span>

### <span data-ttu-id="9cbb6-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="9cbb6-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="9cbb6-112">允許分支分支機搆 VirtualWan 的流量。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="9cbb6-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="9cbb6-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="9cbb6-114">允許 vnet 至 vnet 流量以進行 VirtualWan。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="9cbb6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cbb6-115">-AsJob</span></span>
<span data-ttu-id="9cbb6-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9cbb6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cbb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbb6-117">-DefaultProfile</span></span>
<span data-ttu-id="9cbb6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cbb6-119">-位置</span><span class="sxs-lookup"><span data-stu-id="9cbb6-119">-Location</span></span>
<span data-ttu-id="9cbb6-120">VirtualWAN 資源的位置。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbb6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9cbb6-121">-Name</span></span>
<span data-ttu-id="9cbb6-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbb6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbb6-123">-ResourceGroupName</span></span>
<span data-ttu-id="9cbb6-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbb6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cbb6-125">-Tag</span></span>
<span data-ttu-id="9cbb6-126">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbb6-127">-確認</span><span class="sxs-lookup"><span data-stu-id="9cbb6-127">-Confirm</span></span>
<span data-ttu-id="9cbb6-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cbb6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cbb6-129">-WhatIf</span></span>
<span data-ttu-id="9cbb6-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cbb6-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cbb6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbb6-132">CommonParameters</span></span>
<span data-ttu-id="9cbb6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbb6-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9cbb6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbb6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9cbb6-135">INPUTS</span></span>

### <span data-ttu-id="9cbb6-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9cbb6-136">System.String</span></span>

### <span data-ttu-id="9cbb6-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9cbb6-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9cbb6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9cbb6-138">OUTPUTS</span></span>

### <span data-ttu-id="9cbb6-139">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9cbb6-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="9cbb6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9cbb6-140">NOTES</span></span>

## <span data-ttu-id="9cbb6-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cbb6-141">RELATED LINKS</span></span>
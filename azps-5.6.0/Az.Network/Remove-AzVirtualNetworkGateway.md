---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: c4841678a1e1f318da36b506cc56e586244c233f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915962"
---
# <span data-ttu-id="28e87-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28e87-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="28e87-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28e87-102">SYNOPSIS</span></span>
<span data-ttu-id="28e87-103">刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="28e87-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="28e87-104">語法</span><span class="sxs-lookup"><span data-stu-id="28e87-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28e87-105">描述</span><span class="sxs-lookup"><span data-stu-id="28e87-105">DESCRIPTION</span></span>
<span data-ttu-id="28e87-106">虛擬網路閘道是代表 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="28e87-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="28e87-107">**Get-AzVirtualNetworkGateway** Cmdlet 會根據名稱和資源組名，在 Azure 中會返回閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="28e87-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="28e87-108">例子</span><span class="sxs-lookup"><span data-stu-id="28e87-108">EXAMPLES</span></span>

### <span data-ttu-id="28e87-109">範例 1：刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="28e87-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="28e87-110">刪除資源群組「myRG」內名稱為「myGateway」的虛擬網路閘道物件：您必須先刪除使用 **Remove-AzVirtualNetworkGatewayConnection** Cmdlet 之虛擬網路閘道的所有連結。</span><span class="sxs-lookup"><span data-stu-id="28e87-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="28e87-111">參數</span><span class="sxs-lookup"><span data-stu-id="28e87-111">PARAMETERS</span></span>

### <span data-ttu-id="28e87-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28e87-112">-AsJob</span></span>
<span data-ttu-id="28e87-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="28e87-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28e87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e87-114">-DefaultProfile</span></span>
<span data-ttu-id="28e87-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e87-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28e87-116">-強制</span><span class="sxs-lookup"><span data-stu-id="28e87-116">-Force</span></span>
<span data-ttu-id="28e87-117">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="28e87-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28e87-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="28e87-118">-Name</span></span>
<span data-ttu-id="28e87-119">指定此 Cmdlet 移除的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="28e87-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28e87-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28e87-120">-PassThru</span></span>
<span data-ttu-id="28e87-121">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="28e87-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28e87-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="28e87-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28e87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28e87-123">-ResourceGroupName</span></span>
<span data-ttu-id="28e87-124">指定包含虛擬網路閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="28e87-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28e87-125">-確認</span><span class="sxs-lookup"><span data-stu-id="28e87-125">-Confirm</span></span>
<span data-ttu-id="28e87-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28e87-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e87-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e87-127">-WhatIf</span></span>
<span data-ttu-id="28e87-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28e87-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28e87-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28e87-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e87-130">CommonParameters</span></span>
<span data-ttu-id="28e87-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28e87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e87-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="28e87-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e87-133">輸入</span><span class="sxs-lookup"><span data-stu-id="28e87-133">INPUTS</span></span>

### <span data-ttu-id="28e87-134">System.String</span><span class="sxs-lookup"><span data-stu-id="28e87-134">System.String</span></span>

## <span data-ttu-id="28e87-135">輸出</span><span class="sxs-lookup"><span data-stu-id="28e87-135">OUTPUTS</span></span>

### <span data-ttu-id="28e87-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28e87-136">System.Boolean</span></span>

## <span data-ttu-id="28e87-137">筆記</span><span class="sxs-lookup"><span data-stu-id="28e87-137">NOTES</span></span>

## <span data-ttu-id="28e87-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="28e87-138">RELATED LINKS</span></span>

[<span data-ttu-id="28e87-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28e87-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="28e87-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28e87-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="28e87-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28e87-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="28e87-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28e87-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="28e87-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28e87-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

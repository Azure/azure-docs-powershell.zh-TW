---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 777e03a570f3915d6e0ebe4cbb5c84f9c1824120
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135790"
---
# <span data-ttu-id="ac52d-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ac52d-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="ac52d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac52d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac52d-103">移除虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="ac52d-103">Removes a virtual network.</span></span>

## <span data-ttu-id="ac52d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac52d-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac52d-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac52d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac52d-106">**AzVirtualNetwork** Cmdlet 會移除 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="ac52d-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="ac52d-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac52d-107">EXAMPLES</span></span>

### <span data-ttu-id="ac52d-108">1：建立和刪除虛擬網路</span><span class="sxs-lookup"><span data-stu-id="ac52d-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="ac52d-109">這個範例會在資源群組中建立虛擬網路，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="ac52d-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="ac52d-110">若要在刪除虛擬網路時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="ac52d-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="ac52d-111">參數</span><span class="sxs-lookup"><span data-stu-id="ac52d-111">PARAMETERS</span></span>

### <span data-ttu-id="ac52d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac52d-112">-AsJob</span></span>
<span data-ttu-id="ac52d-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ac52d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac52d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac52d-114">-DefaultProfile</span></span>
<span data-ttu-id="ac52d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac52d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac52d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ac52d-116">-Force</span></span>
<span data-ttu-id="ac52d-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ac52d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac52d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac52d-118">-Name</span></span>
<span data-ttu-id="ac52d-119">指定此 Cmdlet 移除之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac52d-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ac52d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac52d-120">-PassThru</span></span>
<span data-ttu-id="ac52d-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ac52d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac52d-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ac52d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac52d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac52d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac52d-124">指定包含此 Cmdlet 移除之虛擬網路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac52d-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ac52d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ac52d-125">-Confirm</span></span>
<span data-ttu-id="ac52d-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac52d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac52d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac52d-127">-WhatIf</span></span>
<span data-ttu-id="ac52d-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac52d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac52d-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac52d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac52d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac52d-130">CommonParameters</span></span>
<span data-ttu-id="ac52d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac52d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac52d-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac52d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac52d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ac52d-133">INPUTS</span></span>

### <span data-ttu-id="ac52d-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ac52d-134">System.String</span></span>

## <span data-ttu-id="ac52d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ac52d-135">OUTPUTS</span></span>

### <span data-ttu-id="ac52d-136">System.object</span><span class="sxs-lookup"><span data-stu-id="ac52d-136">System.Boolean</span></span>

## <span data-ttu-id="ac52d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ac52d-137">NOTES</span></span>

## <span data-ttu-id="ac52d-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac52d-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac52d-139">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ac52d-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="ac52d-140">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ac52d-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="ac52d-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ac52d-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: b65fcbc132923f18c0a70187403e4c4ba2cef52a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795486"
---
# <span data-ttu-id="88462-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="88462-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="88462-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88462-102">SYNOPSIS</span></span>
<span data-ttu-id="88462-103">移除虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="88462-103">Removes a virtual network.</span></span>

## <span data-ttu-id="88462-104">句法</span><span class="sxs-lookup"><span data-stu-id="88462-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88462-105">說明</span><span class="sxs-lookup"><span data-stu-id="88462-105">DESCRIPTION</span></span>
<span data-ttu-id="88462-106">**AzVirtualNetwork** Cmdlet 會移除 Azure 虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="88462-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="88462-107">示例</span><span class="sxs-lookup"><span data-stu-id="88462-107">EXAMPLES</span></span>

### <span data-ttu-id="88462-108">1：建立和刪除虛擬網路</span><span class="sxs-lookup"><span data-stu-id="88462-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="88462-109">這個範例會在資源群組中建立虛擬網路，然後立即將它刪除。</span><span class="sxs-lookup"><span data-stu-id="88462-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="88462-110">若要在刪除虛擬網路時取消提示，請使用-Force 標誌。</span><span class="sxs-lookup"><span data-stu-id="88462-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="88462-111">參數</span><span class="sxs-lookup"><span data-stu-id="88462-111">PARAMETERS</span></span>

### <span data-ttu-id="88462-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88462-112">-AsJob</span></span>
<span data-ttu-id="88462-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88462-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88462-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88462-114">-DefaultProfile</span></span>
<span data-ttu-id="88462-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88462-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88462-116">-Force</span><span class="sxs-lookup"><span data-stu-id="88462-116">-Force</span></span>
<span data-ttu-id="88462-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="88462-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88462-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="88462-118">-Name</span></span>
<span data-ttu-id="88462-119">指定此 Cmdlet 移除之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="88462-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88462-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88462-120">-PassThru</span></span>
<span data-ttu-id="88462-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="88462-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="88462-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="88462-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="88462-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88462-123">-ResourceGroupName</span></span>
<span data-ttu-id="88462-124">指定包含此 Cmdlet 移除之虛擬網路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88462-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88462-125">-確認</span><span class="sxs-lookup"><span data-stu-id="88462-125">-Confirm</span></span>
<span data-ttu-id="88462-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="88462-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88462-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88462-127">-WhatIf</span></span>
<span data-ttu-id="88462-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88462-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88462-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88462-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88462-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88462-130">CommonParameters</span></span>
<span data-ttu-id="88462-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88462-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88462-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="88462-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88462-133">輸入</span><span class="sxs-lookup"><span data-stu-id="88462-133">INPUTS</span></span>

## <span data-ttu-id="88462-134">輸出</span><span class="sxs-lookup"><span data-stu-id="88462-134">OUTPUTS</span></span>

## <span data-ttu-id="88462-135">筆記</span><span class="sxs-lookup"><span data-stu-id="88462-135">NOTES</span></span>

## <span data-ttu-id="88462-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="88462-136">RELATED LINKS</span></span>

[<span data-ttu-id="88462-137">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="88462-137">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="88462-138">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="88462-138">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="88462-139">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="88462-139">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)



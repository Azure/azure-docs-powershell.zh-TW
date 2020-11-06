---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: df4da43c1a8edf0c3c887e4acdd009593984c048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621911"
---
# <span data-ttu-id="0c184-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0c184-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="0c184-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c184-102">SYNOPSIS</span></span>
<span data-ttu-id="0c184-103">取得虛擬網路攻絲</span><span class="sxs-lookup"><span data-stu-id="0c184-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="0c184-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c184-104">SYNTAX</span></span>

### <span data-ttu-id="0c184-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0c184-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c184-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c184-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c184-107">說明</span><span class="sxs-lookup"><span data-stu-id="0c184-107">DESCRIPTION</span></span>
<span data-ttu-id="0c184-108">**AzVirtualNetworkTap** Cmdlet 會取得 azure 虛擬網路點或 azure 虛擬網路的清單，點擊 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="0c184-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="0c184-109">示例</span><span class="sxs-lookup"><span data-stu-id="0c184-109">EXAMPLES</span></span>

### <span data-ttu-id="0c184-110">範例1：取得虛擬網路分流</span><span class="sxs-lookup"><span data-stu-id="0c184-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="0c184-111">這個命令會在「ResourceGroup1」中取得指定「VirtualTap1」的 VirtualNetwork 攻絲參照。</span><span class="sxs-lookup"><span data-stu-id="0c184-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="0c184-112">範例2：使用篩選來取得所有虛擬網路分路器</span><span class="sxs-lookup"><span data-stu-id="0c184-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="0c184-113">這個命令會取得以 "VirtualTap" 為開頭的所有 VirtualNetwork 攻絲參照。</span><span class="sxs-lookup"><span data-stu-id="0c184-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="0c184-114">參數</span><span class="sxs-lookup"><span data-stu-id="0c184-114">PARAMETERS</span></span>

### <span data-ttu-id="0c184-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c184-115">-DefaultProfile</span></span>
<span data-ttu-id="0c184-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c184-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c184-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c184-117">-Name</span></span>
<span data-ttu-id="0c184-118">攻絲的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c184-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0c184-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c184-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c184-120">虛擬網路的 [資源] 群組名稱。</span><span class="sxs-lookup"><span data-stu-id="0c184-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0c184-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c184-121">-ResourceId</span></span>
<span data-ttu-id="0c184-122">VirtualNetworkTap 資源的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c184-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c184-123">-確認</span><span class="sxs-lookup"><span data-stu-id="0c184-123">-Confirm</span></span>
<span data-ttu-id="0c184-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0c184-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c184-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c184-125">-WhatIf</span></span>
<span data-ttu-id="0c184-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c184-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c184-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c184-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c184-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c184-128">CommonParameters</span></span>
<span data-ttu-id="0c184-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c184-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c184-130">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0c184-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c184-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0c184-131">INPUTS</span></span>

### <span data-ttu-id="0c184-132">System.object</span><span class="sxs-lookup"><span data-stu-id="0c184-132">System.String</span></span>

## <span data-ttu-id="0c184-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0c184-133">OUTPUTS</span></span>

### <span data-ttu-id="0c184-134">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0c184-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="0c184-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0c184-135">NOTES</span></span>

## <span data-ttu-id="0c184-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c184-136">RELATED LINKS</span></span>

[<span data-ttu-id="0c184-137">新-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0c184-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="0c184-138">移除-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0c184-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="0c184-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0c184-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455972"
---
# <span data-ttu-id="d3945-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d3945-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="d3945-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3945-102">SYNOPSIS</span></span>
<span data-ttu-id="d3945-103">設定虛擬網路攻絲的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="d3945-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3945-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3945-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3945-105">說明</span><span class="sxs-lookup"><span data-stu-id="d3945-105">DESCRIPTION</span></span>
<span data-ttu-id="d3945-106">[ **設定] AzureRmVirtualNetworkTap** 會設定 Azure 虛擬網路的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="d3945-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="d3945-107">示例</span><span class="sxs-lookup"><span data-stu-id="d3945-107">EXAMPLES</span></span>

### <span data-ttu-id="d3945-108">範例1：設定虛擬網路分流</span><span class="sxs-lookup"><span data-stu-id="d3945-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="d3945-109">此命令會更新目的地 IpConfiguration，並更新虛擬網路路器。</span><span class="sxs-lookup"><span data-stu-id="d3945-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="d3945-110">如果有任何的攻絲配置引用它，則所有來源流量都不會啟動，因此無法在新的目的地 ip 配置更新後進行鏡像。</span><span class="sxs-lookup"><span data-stu-id="d3945-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="d3945-111">參數</span><span class="sxs-lookup"><span data-stu-id="d3945-111">PARAMETERS</span></span>

### <span data-ttu-id="d3945-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3945-112">-AsJob</span></span>
<span data-ttu-id="d3945-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d3945-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3945-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3945-114">-DefaultProfile</span></span>
<span data-ttu-id="d3945-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3945-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3945-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d3945-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="d3945-117">虛擬網路分流</span><span class="sxs-lookup"><span data-stu-id="d3945-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3945-118">-確認</span><span class="sxs-lookup"><span data-stu-id="d3945-118">-Confirm</span></span>
<span data-ttu-id="d3945-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3945-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3945-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3945-120">-WhatIf</span></span>
<span data-ttu-id="d3945-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3945-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3945-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3945-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3945-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3945-123">CommonParameters</span></span>
<span data-ttu-id="d3945-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3945-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3945-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d3945-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3945-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d3945-126">INPUTS</span></span>

### <span data-ttu-id="d3945-127">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d3945-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="d3945-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d3945-128">OUTPUTS</span></span>

### <span data-ttu-id="d3945-129">PSVirtualNetworkTap 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d3945-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="d3945-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d3945-130">NOTES</span></span>

## <span data-ttu-id="d3945-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3945-131">RELATED LINKS</span></span>

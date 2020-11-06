---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 6f9fd09aa87c8a812bf43a14068feb1604d8de8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443804"
---
# <span data-ttu-id="4e71b-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4e71b-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="4e71b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e71b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e71b-103">句法</span><span class="sxs-lookup"><span data-stu-id="4e71b-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e71b-104">說明</span><span class="sxs-lookup"><span data-stu-id="4e71b-104">DESCRIPTION</span></span>

## <span data-ttu-id="4e71b-105">示例</span><span class="sxs-lookup"><span data-stu-id="4e71b-105">EXAMPLES</span></span>

### <span data-ttu-id="4e71b-106">1：移除</span><span class="sxs-lookup"><span data-stu-id="4e71b-106">1: Remove</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="4e71b-107">參數</span><span class="sxs-lookup"><span data-stu-id="4e71b-107">PARAMETERS</span></span>

### <span data-ttu-id="4e71b-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e71b-108">-DefaultProfile</span></span>
<span data-ttu-id="4e71b-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e71b-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e71b-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4e71b-110">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e71b-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e71b-111">-Name</span></span>
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

### <span data-ttu-id="4e71b-112">-確認</span><span class="sxs-lookup"><span data-stu-id="4e71b-112">-Confirm</span></span>
<span data-ttu-id="4e71b-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e71b-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e71b-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e71b-114">-WhatIf</span></span>
<span data-ttu-id="4e71b-115">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e71b-115">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e71b-116">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e71b-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e71b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e71b-117">CommonParameters</span></span>
<span data-ttu-id="4e71b-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e71b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e71b-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e71b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e71b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4e71b-120">INPUTS</span></span>

### <span data-ttu-id="4e71b-121">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e71b-121">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="4e71b-122">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4e71b-122">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="4e71b-123">輸出</span><span class="sxs-lookup"><span data-stu-id="4e71b-123">OUTPUTS</span></span>

### <span data-ttu-id="4e71b-124">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4e71b-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4e71b-125">筆記</span><span class="sxs-lookup"><span data-stu-id="4e71b-125">NOTES</span></span>

## <span data-ttu-id="4e71b-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e71b-126">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dbd49a948108d23c0f824adaea2e06105152a36b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450245"
---
# <span data-ttu-id="22cb1-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="22cb1-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="22cb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22cb1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22cb1-103">句法</span><span class="sxs-lookup"><span data-stu-id="22cb1-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22cb1-104">說明</span><span class="sxs-lookup"><span data-stu-id="22cb1-104">DESCRIPTION</span></span>

## <span data-ttu-id="22cb1-105">示例</span><span class="sxs-lookup"><span data-stu-id="22cb1-105">EXAMPLES</span></span>

### <span data-ttu-id="22cb1-106">1：取得</span><span class="sxs-lookup"><span data-stu-id="22cb1-106">1: Get</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzureRmLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="22cb1-107">參數</span><span class="sxs-lookup"><span data-stu-id="22cb1-107">PARAMETERS</span></span>

### <span data-ttu-id="22cb1-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cb1-108">-DefaultProfile</span></span>
<span data-ttu-id="22cb1-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22cb1-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22cb1-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22cb1-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="22cb1-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="22cb1-111">-Name</span></span>
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

### <span data-ttu-id="22cb1-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cb1-112">CommonParameters</span></span>
<span data-ttu-id="22cb1-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22cb1-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cb1-114">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22cb1-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cb1-115">輸入</span><span class="sxs-lookup"><span data-stu-id="22cb1-115">INPUTS</span></span>

### <span data-ttu-id="22cb1-116">PSLoadBalancer 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="22cb1-116">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="22cb1-117">參數： LoadBalancer (ByValue) </span><span class="sxs-lookup"><span data-stu-id="22cb1-117">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="22cb1-118">輸出</span><span class="sxs-lookup"><span data-stu-id="22cb1-118">OUTPUTS</span></span>

### <span data-ttu-id="22cb1-119">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="22cb1-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="22cb1-120">筆記</span><span class="sxs-lookup"><span data-stu-id="22cb1-120">NOTES</span></span>

## <span data-ttu-id="22cb1-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="22cb1-121">RELATED LINKS</span></span>

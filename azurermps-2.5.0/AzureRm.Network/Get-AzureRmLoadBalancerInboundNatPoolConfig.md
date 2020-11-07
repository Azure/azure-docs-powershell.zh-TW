---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 20837f96bc17d2cfd71abc359ff4114b44e6c062
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800446"
---
# <span data-ttu-id="c345f-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c345f-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="c345f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c345f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c345f-103">句法</span><span class="sxs-lookup"><span data-stu-id="c345f-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c345f-104">說明</span><span class="sxs-lookup"><span data-stu-id="c345f-104">DESCRIPTION</span></span>

## <span data-ttu-id="c345f-105">示例</span><span class="sxs-lookup"><span data-stu-id="c345f-105">EXAMPLES</span></span>

### <span data-ttu-id="c345f-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="c345f-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c345f-107">參數</span><span class="sxs-lookup"><span data-stu-id="c345f-107">PARAMETERS</span></span>

### <span data-ttu-id="c345f-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c345f-108">-DefaultProfile</span></span>
<span data-ttu-id="c345f-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c345f-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c345f-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c345f-110">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c345f-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="c345f-111">-Name</span></span>
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

### <span data-ttu-id="c345f-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c345f-112">CommonParameters</span></span>
<span data-ttu-id="c345f-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c345f-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c345f-114">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c345f-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c345f-115">輸入</span><span class="sxs-lookup"><span data-stu-id="c345f-115">INPUTS</span></span>

### <span data-ttu-id="c345f-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c345f-116">PSLoadBalancer</span></span>
<span data-ttu-id="c345f-117">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="c345f-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c345f-118">輸出</span><span class="sxs-lookup"><span data-stu-id="c345f-118">OUTPUTS</span></span>

### <span data-ttu-id="c345f-119">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c345f-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="c345f-120">筆記</span><span class="sxs-lookup"><span data-stu-id="c345f-120">NOTES</span></span>

## <span data-ttu-id="c345f-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="c345f-121">RELATED LINKS</span></span>


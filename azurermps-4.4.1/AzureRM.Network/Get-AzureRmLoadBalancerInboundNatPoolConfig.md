---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9f9e14b94cbe38ba643d2c39beca5e1fe52138b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624551"
---
# <span data-ttu-id="52a7b-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="52a7b-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="52a7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52a7b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52a7b-103">句法</span><span class="sxs-lookup"><span data-stu-id="52a7b-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a7b-104">說明</span><span class="sxs-lookup"><span data-stu-id="52a7b-104">DESCRIPTION</span></span>

## <span data-ttu-id="52a7b-105">示例</span><span class="sxs-lookup"><span data-stu-id="52a7b-105">EXAMPLES</span></span>

### <span data-ttu-id="52a7b-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="52a7b-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="52a7b-107">參數</span><span class="sxs-lookup"><span data-stu-id="52a7b-107">PARAMETERS</span></span>

### <span data-ttu-id="52a7b-108">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="52a7b-108">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52a7b-109">-名稱</span><span class="sxs-lookup"><span data-stu-id="52a7b-109">-Name</span></span>
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

### <span data-ttu-id="52a7b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a7b-110">-DefaultProfile</span></span>
<span data-ttu-id="52a7b-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52a7b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a7b-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a7b-112">CommonParameters</span></span>
<span data-ttu-id="52a7b-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52a7b-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a7b-114">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52a7b-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a7b-115">輸入</span><span class="sxs-lookup"><span data-stu-id="52a7b-115">INPUTS</span></span>

### <span data-ttu-id="52a7b-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="52a7b-116">PSLoadBalancer</span></span>
<span data-ttu-id="52a7b-117">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="52a7b-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="52a7b-118">輸出</span><span class="sxs-lookup"><span data-stu-id="52a7b-118">OUTPUTS</span></span>

### <span data-ttu-id="52a7b-119">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="52a7b-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="52a7b-120">筆記</span><span class="sxs-lookup"><span data-stu-id="52a7b-120">NOTES</span></span>

## <span data-ttu-id="52a7b-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="52a7b-121">RELATED LINKS</span></span>


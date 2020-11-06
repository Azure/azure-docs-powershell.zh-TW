---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: f2fd08abbc9a01f1a6cacb9891d82fe1c89d13ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457131"
---
# <span data-ttu-id="1a629-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1a629-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="1a629-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a629-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a629-103">句法</span><span class="sxs-lookup"><span data-stu-id="1a629-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a629-104">說明</span><span class="sxs-lookup"><span data-stu-id="1a629-104">DESCRIPTION</span></span>

## <span data-ttu-id="1a629-105">示例</span><span class="sxs-lookup"><span data-stu-id="1a629-105">EXAMPLES</span></span>

### <span data-ttu-id="1a629-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="1a629-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1a629-107">參數</span><span class="sxs-lookup"><span data-stu-id="1a629-107">PARAMETERS</span></span>

### <span data-ttu-id="1a629-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a629-108">-DefaultProfile</span></span>
<span data-ttu-id="1a629-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a629-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a629-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a629-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="1a629-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a629-111">-Name</span></span>
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

### <span data-ttu-id="1a629-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a629-112">CommonParameters</span></span>
<span data-ttu-id="1a629-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a629-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a629-114">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1a629-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a629-115">輸入</span><span class="sxs-lookup"><span data-stu-id="1a629-115">INPUTS</span></span>

### <span data-ttu-id="1a629-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a629-116">PSLoadBalancer</span></span>
<span data-ttu-id="1a629-117">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1a629-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1a629-118">輸出</span><span class="sxs-lookup"><span data-stu-id="1a629-118">OUTPUTS</span></span>

### <span data-ttu-id="1a629-119">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1a629-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="1a629-120">筆記</span><span class="sxs-lookup"><span data-stu-id="1a629-120">NOTES</span></span>

## <span data-ttu-id="1a629-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a629-121">RELATED LINKS</span></span>


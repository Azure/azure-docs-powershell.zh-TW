---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: d3dcdabc84eca5efa7e52e61f4beafd23eb67b05
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794420"
---
# <span data-ttu-id="94573-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="94573-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="94573-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94573-102">SYNOPSIS</span></span>

## <span data-ttu-id="94573-103">句法</span><span class="sxs-lookup"><span data-stu-id="94573-103">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94573-104">說明</span><span class="sxs-lookup"><span data-stu-id="94573-104">DESCRIPTION</span></span>

## <span data-ttu-id="94573-105">示例</span><span class="sxs-lookup"><span data-stu-id="94573-105">EXAMPLES</span></span>

### <span data-ttu-id="94573-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="94573-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="94573-107">參數</span><span class="sxs-lookup"><span data-stu-id="94573-107">PARAMETERS</span></span>

### <span data-ttu-id="94573-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94573-108">-DefaultProfile</span></span>
<span data-ttu-id="94573-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94573-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94573-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94573-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="94573-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="94573-111">-Name</span></span>
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

### <span data-ttu-id="94573-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94573-112">CommonParameters</span></span>
<span data-ttu-id="94573-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94573-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94573-114">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94573-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94573-115">輸入</span><span class="sxs-lookup"><span data-stu-id="94573-115">INPUTS</span></span>

### <span data-ttu-id="94573-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94573-116">PSLoadBalancer</span></span>
<span data-ttu-id="94573-117">形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="94573-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="94573-118">輸出</span><span class="sxs-lookup"><span data-stu-id="94573-118">OUTPUTS</span></span>

### <span data-ttu-id="94573-119">PSInboundNatPool 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="94573-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="94573-120">筆記</span><span class="sxs-lookup"><span data-stu-id="94573-120">NOTES</span></span>

## <span data-ttu-id="94573-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="94573-121">RELATED LINKS</span></span>


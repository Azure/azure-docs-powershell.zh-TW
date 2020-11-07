---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
ms.openlocfilehash: ed33d1a683e10e0e39d0b722dec92b7f7ba11254
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800425"
---
# <span data-ttu-id="c2c1c-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="c2c1c-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="c2c1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c1c-103">列出適用于位置的端點服務。</span><span class="sxs-lookup"><span data-stu-id="c2c1c-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2c1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2c1c-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2c1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="c2c1c-106">Get-AzureRmVirtualNetworkAvailableEndpointService 列出指定位置中可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="c2c1c-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="c2c1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="c2c1c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c2c1c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="c2c1c-109">在 westus 區域中取得可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="c2c1c-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="c2c1c-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2c1c-110">PARAMETERS</span></span>

### <span data-ttu-id="c2c1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c1c-111">-DefaultProfile</span></span>
<span data-ttu-id="c2c1c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2c1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2c1c-113">-位置</span><span class="sxs-lookup"><span data-stu-id="c2c1c-113">-Location</span></span>
<span data-ttu-id="c2c1c-114">要從中檢索端點服務的位置。</span><span class="sxs-lookup"><span data-stu-id="c2c1c-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="c2c1c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c1c-115">CommonParameters</span></span>
<span data-ttu-id="c2c1c-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2c1c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c1c-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2c1c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c1c-118">輸入</span><span class="sxs-lookup"><span data-stu-id="c2c1c-118">INPUTS</span></span>

### <span data-ttu-id="c2c1c-119">System.object</span><span class="sxs-lookup"><span data-stu-id="c2c1c-119">System.String</span></span>

## <span data-ttu-id="c2c1c-120">輸出</span><span class="sxs-lookup"><span data-stu-id="c2c1c-120">OUTPUTS</span></span>

### <span data-ttu-id="c2c1c-121">[System.object]. 清單 ' 1 [PSEndpointServiceResult，4.2.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="c2c1c-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c2c1c-122">筆記</span><span class="sxs-lookup"><span data-stu-id="c2c1c-122">NOTES</span></span>

## <span data-ttu-id="c2c1c-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2c1c-123">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: a1c28622a4bb3a43d9d91b2f991c402a3572a3f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904998"
---
# <span data-ttu-id="fae3e-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="fae3e-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="fae3e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fae3e-102">SYNOPSIS</span></span>
<span data-ttu-id="fae3e-103">列出位置的可用端點服務。</span><span class="sxs-lookup"><span data-stu-id="fae3e-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="fae3e-104">語法</span><span class="sxs-lookup"><span data-stu-id="fae3e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fae3e-105">描述</span><span class="sxs-lookup"><span data-stu-id="fae3e-105">DESCRIPTION</span></span>
<span data-ttu-id="fae3e-106">Get-AzVirtualNetworkAvailableEndpointService會列出指定位置提供的端點服務。</span><span class="sxs-lookup"><span data-stu-id="fae3e-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="fae3e-107">例子</span><span class="sxs-lookup"><span data-stu-id="fae3e-107">EXAMPLES</span></span>

### <span data-ttu-id="fae3e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fae3e-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="fae3e-109">在西部地區獲得可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="fae3e-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="fae3e-110">參數</span><span class="sxs-lookup"><span data-stu-id="fae3e-110">PARAMETERS</span></span>

### <span data-ttu-id="fae3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae3e-111">-DefaultProfile</span></span>
<span data-ttu-id="fae3e-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fae3e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae3e-113">-位置</span><span class="sxs-lookup"><span data-stu-id="fae3e-113">-Location</span></span>
<span data-ttu-id="fae3e-114">從中取回端點服務的位置。</span><span class="sxs-lookup"><span data-stu-id="fae3e-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fae3e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae3e-115">CommonParameters</span></span>
<span data-ttu-id="fae3e-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fae3e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae3e-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fae3e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae3e-118">輸入</span><span class="sxs-lookup"><span data-stu-id="fae3e-118">INPUTS</span></span>

### <span data-ttu-id="fae3e-119">System.String</span><span class="sxs-lookup"><span data-stu-id="fae3e-119">System.String</span></span>

## <span data-ttu-id="fae3e-120">輸出</span><span class="sxs-lookup"><span data-stu-id="fae3e-120">OUTPUTS</span></span>

### <span data-ttu-id="fae3e-121">Microsoft.Azure.Commands.network.models.PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="fae3e-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="fae3e-122">筆記</span><span class="sxs-lookup"><span data-stu-id="fae3e-122">NOTES</span></span>

## <span data-ttu-id="fae3e-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="fae3e-123">RELATED LINKS</span></span>

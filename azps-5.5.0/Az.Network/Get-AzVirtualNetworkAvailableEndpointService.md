---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128943"
---
# <span data-ttu-id="a3f23-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="a3f23-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="a3f23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3f23-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f23-103">列出適用于位置的端點服務。</span><span class="sxs-lookup"><span data-stu-id="a3f23-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="a3f23-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3f23-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3f23-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3f23-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f23-106">Get-AzVirtualNetworkAvailableEndpointService 列出指定位置中可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="a3f23-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="a3f23-107">示例</span><span class="sxs-lookup"><span data-stu-id="a3f23-107">EXAMPLES</span></span>

### <span data-ttu-id="a3f23-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a3f23-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="a3f23-109">在 westus 區域中取得可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="a3f23-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="a3f23-110">參數</span><span class="sxs-lookup"><span data-stu-id="a3f23-110">PARAMETERS</span></span>

### <span data-ttu-id="a3f23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f23-111">-DefaultProfile</span></span>
<span data-ttu-id="a3f23-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3f23-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f23-113">-位置</span><span class="sxs-lookup"><span data-stu-id="a3f23-113">-Location</span></span>
<span data-ttu-id="a3f23-114">要從中檢索端點服務的位置。</span><span class="sxs-lookup"><span data-stu-id="a3f23-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="a3f23-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f23-115">CommonParameters</span></span>
<span data-ttu-id="a3f23-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3f23-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f23-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a3f23-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f23-118">輸入</span><span class="sxs-lookup"><span data-stu-id="a3f23-118">INPUTS</span></span>

### <span data-ttu-id="a3f23-119">System.object</span><span class="sxs-lookup"><span data-stu-id="a3f23-119">System.String</span></span>

## <span data-ttu-id="a3f23-120">輸出</span><span class="sxs-lookup"><span data-stu-id="a3f23-120">OUTPUTS</span></span>

### <span data-ttu-id="a3f23-121">PSEndpointServiceResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3f23-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="a3f23-122">筆記</span><span class="sxs-lookup"><span data-stu-id="a3f23-122">NOTES</span></span>

## <span data-ttu-id="a3f23-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3f23-123">RELATED LINKS</span></span>

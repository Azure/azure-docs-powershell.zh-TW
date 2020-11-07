---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 2de970201456f941d8b35d40c569c41e114468c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789510"
---
# <span data-ttu-id="f9e20-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="f9e20-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="f9e20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9e20-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e20-103">列出適用于位置的端點服務。</span><span class="sxs-lookup"><span data-stu-id="f9e20-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="f9e20-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9e20-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9e20-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9e20-105">DESCRIPTION</span></span>
<span data-ttu-id="f9e20-106">Get-AzVirtualNetworkAvailableEndpointService 列出指定位置中可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="f9e20-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="f9e20-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9e20-107">EXAMPLES</span></span>

### <span data-ttu-id="f9e20-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f9e20-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="f9e20-109">在 westus 區域中取得可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="f9e20-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="f9e20-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9e20-110">PARAMETERS</span></span>

### <span data-ttu-id="f9e20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e20-111">-DefaultProfile</span></span>
<span data-ttu-id="f9e20-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9e20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9e20-113">-位置</span><span class="sxs-lookup"><span data-stu-id="f9e20-113">-Location</span></span>
<span data-ttu-id="f9e20-114">要從中檢索端點服務的位置。</span><span class="sxs-lookup"><span data-stu-id="f9e20-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="f9e20-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e20-115">CommonParameters</span></span>
<span data-ttu-id="f9e20-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9e20-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e20-117">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f9e20-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e20-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f9e20-118">INPUTS</span></span>

### <span data-ttu-id="f9e20-119">System.object</span><span class="sxs-lookup"><span data-stu-id="f9e20-119">System.String</span></span>

## <span data-ttu-id="f9e20-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f9e20-120">OUTPUTS</span></span>

### <span data-ttu-id="f9e20-121">PSEndpointServiceResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f9e20-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="f9e20-122">筆記</span><span class="sxs-lookup"><span data-stu-id="f9e20-122">NOTES</span></span>

## <span data-ttu-id="f9e20-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9e20-123">RELATED LINKS</span></span>

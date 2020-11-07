---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: bcd4ba14a14fdacdcdaa0ea85ec8059d2639bdc6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794365"
---
# <span data-ttu-id="49e83-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="49e83-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="49e83-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49e83-102">SYNOPSIS</span></span>
<span data-ttu-id="49e83-103">列出適用于位置的端點服務。</span><span class="sxs-lookup"><span data-stu-id="49e83-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="49e83-104">句法</span><span class="sxs-lookup"><span data-stu-id="49e83-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49e83-105">說明</span><span class="sxs-lookup"><span data-stu-id="49e83-105">DESCRIPTION</span></span>
<span data-ttu-id="49e83-106">Get-AzVirtualNetworkAvailableEndpointService 列出指定位置中可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="49e83-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="49e83-107">示例</span><span class="sxs-lookup"><span data-stu-id="49e83-107">EXAMPLES</span></span>

### <span data-ttu-id="49e83-108">範例1</span><span class="sxs-lookup"><span data-stu-id="49e83-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="49e83-109">在 westus 區域中取得可用的端點服務。</span><span class="sxs-lookup"><span data-stu-id="49e83-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="49e83-110">參數</span><span class="sxs-lookup"><span data-stu-id="49e83-110">PARAMETERS</span></span>

### <span data-ttu-id="49e83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e83-111">-DefaultProfile</span></span>
<span data-ttu-id="49e83-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49e83-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49e83-113">-位置</span><span class="sxs-lookup"><span data-stu-id="49e83-113">-Location</span></span>
<span data-ttu-id="49e83-114">要從中檢索端點服務的位置。</span><span class="sxs-lookup"><span data-stu-id="49e83-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="49e83-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e83-115">CommonParameters</span></span>
<span data-ttu-id="49e83-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49e83-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e83-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49e83-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e83-118">輸入</span><span class="sxs-lookup"><span data-stu-id="49e83-118">INPUTS</span></span>

### <span data-ttu-id="49e83-119">System.object</span><span class="sxs-lookup"><span data-stu-id="49e83-119">System.String</span></span>

## <span data-ttu-id="49e83-120">輸出</span><span class="sxs-lookup"><span data-stu-id="49e83-120">OUTPUTS</span></span>

### <span data-ttu-id="49e83-121">[System.object]. 清單 ' 1 [PSEndpointServiceResult，4.2.1.0，，system.object，版本 =，Culture = 中性，PublicKeyToken = null]」）。</span><span class="sxs-lookup"><span data-stu-id="49e83-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="49e83-122">筆記</span><span class="sxs-lookup"><span data-stu-id="49e83-122">NOTES</span></span>

## <span data-ttu-id="49e83-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="49e83-123">RELATED LINKS</span></span>


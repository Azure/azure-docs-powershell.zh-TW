---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: daea57cb0e8c910fca4fedabad0e4583354c4072
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906785"
---
# <span data-ttu-id="dfc9d-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="dfc9d-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="dfc9d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dfc9d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc9d-103">獲得 CDN 端點的可用性狀態。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="dfc9d-104">語法</span><span class="sxs-lookup"><span data-stu-id="dfc9d-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfc9d-105">描述</span><span class="sxs-lookup"><span data-stu-id="dfc9d-105">DESCRIPTION</span></span>
<span data-ttu-id="dfc9d-106">**Get-AzCdnEndpointNameAvailability** Cmdlet 會取得 Azure 內容傳遞網路 (CDN) 的可用性狀態。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="dfc9d-107">例子</span><span class="sxs-lookup"><span data-stu-id="dfc9d-107">EXAMPLES</span></span>

## <span data-ttu-id="dfc9d-108">參數</span><span class="sxs-lookup"><span data-stu-id="dfc9d-108">PARAMETERS</span></span>

### <span data-ttu-id="dfc9d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc9d-109">-DefaultProfile</span></span>
<span data-ttu-id="dfc9d-110">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="dfc9d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfc9d-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dfc9d-111">-EndpointName</span></span>
<span data-ttu-id="dfc9d-112">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc9d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc9d-113">CommonParameters</span></span>
<span data-ttu-id="dfc9d-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dfc9d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc9d-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfc9d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc9d-116">輸入</span><span class="sxs-lookup"><span data-stu-id="dfc9d-116">INPUTS</span></span>

### <span data-ttu-id="dfc9d-117">沒有</span><span class="sxs-lookup"><span data-stu-id="dfc9d-117">None</span></span>

## <span data-ttu-id="dfc9d-118">輸出</span><span class="sxs-lookup"><span data-stu-id="dfc9d-118">OUTPUTS</span></span>

### <span data-ttu-id="dfc9d-119">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="dfc9d-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="dfc9d-120">筆記</span><span class="sxs-lookup"><span data-stu-id="dfc9d-120">NOTES</span></span>

## <span data-ttu-id="dfc9d-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfc9d-121">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: d39bd2d3a10f1ff8512b54cdf45902fb10f6810d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917774"
---
# <span data-ttu-id="1f60f-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="1f60f-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="1f60f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f60f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f60f-103">獲得 CDN 端點的資源使用量。</span><span class="sxs-lookup"><span data-stu-id="1f60f-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="1f60f-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f60f-104">SYNTAX</span></span>

### <span data-ttu-id="1f60f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1f60f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f60f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f60f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f60f-107">描述</span><span class="sxs-lookup"><span data-stu-id="1f60f-107">DESCRIPTION</span></span>
<span data-ttu-id="1f60f-108">{{填寫 Description}}</span><span class="sxs-lookup"><span data-stu-id="1f60f-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1f60f-109">例子</span><span class="sxs-lookup"><span data-stu-id="1f60f-109">EXAMPLES</span></span>

### <span data-ttu-id="1f60f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="1f60f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1f60f-111">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="1f60f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="1f60f-112">參數</span><span class="sxs-lookup"><span data-stu-id="1f60f-112">PARAMETERS</span></span>

### <span data-ttu-id="1f60f-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f60f-113">-CdnEndpoint</span></span>
<span data-ttu-id="1f60f-114">CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="1f60f-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f60f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f60f-115">-DefaultProfile</span></span>
<span data-ttu-id="1f60f-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1f60f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f60f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1f60f-117">-EndpointName</span></span>
<span data-ttu-id="1f60f-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="1f60f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1f60f-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1f60f-119">-ProfileName</span></span>
<span data-ttu-id="1f60f-120">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="1f60f-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f60f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f60f-121">-ResourceGroupName</span></span>
<span data-ttu-id="1f60f-122">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1f60f-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f60f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f60f-123">CommonParameters</span></span>
<span data-ttu-id="1f60f-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f60f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f60f-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f60f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f60f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1f60f-126">INPUTS</span></span>

### <span data-ttu-id="1f60f-127">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f60f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1f60f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1f60f-128">OUTPUTS</span></span>

### <span data-ttu-id="1f60f-129">Microsoft.Azure.Commands.Cdn.models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="1f60f-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="1f60f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="1f60f-130">NOTES</span></span>

## <span data-ttu-id="1f60f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f60f-131">RELATED LINKS</span></span>

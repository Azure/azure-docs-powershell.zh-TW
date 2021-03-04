---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: e1c436a76a3fc98714798bc938f0de987906e7d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916778"
---
# <span data-ttu-id="b43fe-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b43fe-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="b43fe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b43fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b43fe-103">獲得 CDN 自訂網域。</span><span class="sxs-lookup"><span data-stu-id="b43fe-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="b43fe-104">語法</span><span class="sxs-lookup"><span data-stu-id="b43fe-104">SYNTAX</span></span>

### <span data-ttu-id="b43fe-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b43fe-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b43fe-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b43fe-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b43fe-107">描述</span><span class="sxs-lookup"><span data-stu-id="b43fe-107">DESCRIPTION</span></span>
<span data-ttu-id="b43fe-108">**Get-AzCdnCustomDomain Cmdlet** 會取得 Azure 內容傳遞網路 (CDN) 自訂網域及其相關設定。</span><span class="sxs-lookup"><span data-stu-id="b43fe-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="b43fe-109">例子</span><span class="sxs-lookup"><span data-stu-id="b43fe-109">EXAMPLES</span></span>

## <span data-ttu-id="b43fe-110">參數</span><span class="sxs-lookup"><span data-stu-id="b43fe-110">PARAMETERS</span></span>

### <span data-ttu-id="b43fe-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b43fe-111">-CdnEndpoint</span></span>
<span data-ttu-id="b43fe-112">指定自訂網域為成員之 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="b43fe-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="b43fe-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="b43fe-113">-CustomDomainName</span></span>
<span data-ttu-id="b43fe-114">指定自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="b43fe-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="b43fe-115">自訂網域的名稱與自訂網域的主機名稱不同。</span><span class="sxs-lookup"><span data-stu-id="b43fe-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="b43fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43fe-116">-DefaultProfile</span></span>
<span data-ttu-id="b43fe-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b43fe-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b43fe-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b43fe-118">-EndpointName</span></span>
<span data-ttu-id="b43fe-119">指定自訂網域所屬的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="b43fe-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b43fe-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b43fe-120">-ProfileName</span></span>
<span data-ttu-id="b43fe-121">指定自訂網域所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b43fe-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b43fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="b43fe-123">指定自訂網域所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b43fe-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="b43fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43fe-124">CommonParameters</span></span>
<span data-ttu-id="b43fe-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b43fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43fe-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b43fe-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43fe-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b43fe-127">INPUTS</span></span>

### <span data-ttu-id="b43fe-128">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b43fe-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b43fe-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b43fe-129">OUTPUTS</span></span>

### <span data-ttu-id="b43fe-130">Microsoft.Azure.Commands.Cdn.models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b43fe-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="b43fe-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b43fe-131">NOTES</span></span>

## <span data-ttu-id="b43fe-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b43fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="b43fe-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b43fe-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="b43fe-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b43fe-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)



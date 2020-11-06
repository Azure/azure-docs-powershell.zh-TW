---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e0c1d2e49cce4798499506352811d1e341bf47e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456151"
---
# <span data-ttu-id="60ed1-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="60ed1-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="60ed1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="60ed1-103">取得 CDN 自訂網域。</span><span class="sxs-lookup"><span data-stu-id="60ed1-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ed1-104">句法</span><span class="sxs-lookup"><span data-stu-id="60ed1-104">SYNTAX</span></span>

### <span data-ttu-id="60ed1-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="60ed1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60ed1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60ed1-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60ed1-107">說明</span><span class="sxs-lookup"><span data-stu-id="60ed1-107">DESCRIPTION</span></span>
<span data-ttu-id="60ed1-108">**AzureRmCdnCustomDomain** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 自訂網域及其相關設定。</span><span class="sxs-lookup"><span data-stu-id="60ed1-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="60ed1-109">示例</span><span class="sxs-lookup"><span data-stu-id="60ed1-109">EXAMPLES</span></span>

## <span data-ttu-id="60ed1-110">參數</span><span class="sxs-lookup"><span data-stu-id="60ed1-110">PARAMETERS</span></span>

### <span data-ttu-id="60ed1-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60ed1-111">-CdnEndpoint</span></span>
<span data-ttu-id="60ed1-112">指定自訂網域是其成員的 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="60ed1-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="60ed1-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="60ed1-113">-CustomDomainName</span></span>
<span data-ttu-id="60ed1-114">指定自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="60ed1-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="60ed1-115">自訂網域的名稱與自訂網域的主機名稱不同。</span><span class="sxs-lookup"><span data-stu-id="60ed1-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="60ed1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ed1-116">-DefaultProfile</span></span>
<span data-ttu-id="60ed1-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="60ed1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ed1-118">-終結點</span><span class="sxs-lookup"><span data-stu-id="60ed1-118">-EndpointName</span></span>
<span data-ttu-id="60ed1-119">指定自訂網域所屬之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="60ed1-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="60ed1-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="60ed1-120">-ProfileName</span></span>
<span data-ttu-id="60ed1-121">指定自訂網域所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="60ed1-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="60ed1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ed1-122">-ResourceGroupName</span></span>
<span data-ttu-id="60ed1-123">指定自訂網域所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60ed1-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="60ed1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ed1-124">CommonParameters</span></span>
<span data-ttu-id="60ed1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60ed1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ed1-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60ed1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ed1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="60ed1-127">INPUTS</span></span>

### <span data-ttu-id="60ed1-128">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="60ed1-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="60ed1-129">參數： CdnEndpoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="60ed1-129">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="60ed1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="60ed1-130">OUTPUTS</span></span>

### <span data-ttu-id="60ed1-131">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="60ed1-131">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="60ed1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="60ed1-132">NOTES</span></span>

## <span data-ttu-id="60ed1-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="60ed1-133">RELATED LINKS</span></span>

[<span data-ttu-id="60ed1-134">新-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="60ed1-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="60ed1-135">移除-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="60ed1-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


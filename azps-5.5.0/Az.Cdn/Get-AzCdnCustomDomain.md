---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136602"
---
# <span data-ttu-id="60d51-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="60d51-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="60d51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60d51-102">SYNOPSIS</span></span>
<span data-ttu-id="60d51-103">取得 CDN 自訂網域。</span><span class="sxs-lookup"><span data-stu-id="60d51-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="60d51-104">句法</span><span class="sxs-lookup"><span data-stu-id="60d51-104">SYNTAX</span></span>

### <span data-ttu-id="60d51-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="60d51-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60d51-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60d51-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60d51-107">說明</span><span class="sxs-lookup"><span data-stu-id="60d51-107">DESCRIPTION</span></span>
<span data-ttu-id="60d51-108">**AzCdnCustomDomain** Cmdlet 會取得 Azure 內容傳遞網路， (CDN) 自訂網域及其相關設定。</span><span class="sxs-lookup"><span data-stu-id="60d51-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="60d51-109">示例</span><span class="sxs-lookup"><span data-stu-id="60d51-109">EXAMPLES</span></span>

## <span data-ttu-id="60d51-110">參數</span><span class="sxs-lookup"><span data-stu-id="60d51-110">PARAMETERS</span></span>

### <span data-ttu-id="60d51-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60d51-111">-CdnEndpoint</span></span>
<span data-ttu-id="60d51-112">指定自訂網域是其成員的 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="60d51-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="60d51-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="60d51-113">-CustomDomainName</span></span>
<span data-ttu-id="60d51-114">指定自訂網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="60d51-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="60d51-115">自訂網域的名稱與自訂網域的主機名稱不同。</span><span class="sxs-lookup"><span data-stu-id="60d51-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="60d51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d51-116">-DefaultProfile</span></span>
<span data-ttu-id="60d51-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="60d51-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60d51-118">-終結點</span><span class="sxs-lookup"><span data-stu-id="60d51-118">-EndpointName</span></span>
<span data-ttu-id="60d51-119">指定自訂網域所屬之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="60d51-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="60d51-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="60d51-120">-ProfileName</span></span>
<span data-ttu-id="60d51-121">指定自訂網域所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="60d51-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="60d51-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d51-122">-ResourceGroupName</span></span>
<span data-ttu-id="60d51-123">指定自訂網域所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60d51-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="60d51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d51-124">CommonParameters</span></span>
<span data-ttu-id="60d51-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60d51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d51-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="60d51-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d51-127">輸入</span><span class="sxs-lookup"><span data-stu-id="60d51-127">INPUTS</span></span>

### <span data-ttu-id="60d51-128">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="60d51-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="60d51-129">輸出</span><span class="sxs-lookup"><span data-stu-id="60d51-129">OUTPUTS</span></span>

### <span data-ttu-id="60d51-130">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="60d51-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="60d51-131">筆記</span><span class="sxs-lookup"><span data-stu-id="60d51-131">NOTES</span></span>

## <span data-ttu-id="60d51-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="60d51-132">RELATED LINKS</span></span>

[<span data-ttu-id="60d51-133">新-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="60d51-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="60d51-134">移除-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="60d51-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)



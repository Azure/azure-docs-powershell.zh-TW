---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 58e4d922d74f36f6f472cf3bfef8e0d0d45155d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916775"
---
# <span data-ttu-id="83b8f-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83b8f-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="83b8f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="83b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="83b8f-103">為 CDN 端點建立自訂網域。</span><span class="sxs-lookup"><span data-stu-id="83b8f-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="83b8f-104">語法</span><span class="sxs-lookup"><span data-stu-id="83b8f-104">SYNTAX</span></span>

### <span data-ttu-id="83b8f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="83b8f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83b8f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83b8f-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b8f-107">描述</span><span class="sxs-lookup"><span data-stu-id="83b8f-107">DESCRIPTION</span></span>
<span data-ttu-id="83b8f-108">**New-AzCdnCustomDomain** Cmdlet 會為 AZURE 內容傳遞網路與 CDN 端點 (自訂) 網域。</span><span class="sxs-lookup"><span data-stu-id="83b8f-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="83b8f-109">例子</span><span class="sxs-lookup"><span data-stu-id="83b8f-109">EXAMPLES</span></span>

## <span data-ttu-id="83b8f-110">參數</span><span class="sxs-lookup"><span data-stu-id="83b8f-110">PARAMETERS</span></span>

### <span data-ttu-id="83b8f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="83b8f-111">-CdnEndpoint</span></span>
<span data-ttu-id="83b8f-112">指定新增自訂網域的 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="83b8f-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="83b8f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="83b8f-113">-CustomDomainName</span></span>
<span data-ttu-id="83b8f-114">指定自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="83b8f-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="83b8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b8f-115">-DefaultProfile</span></span>
<span data-ttu-id="83b8f-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="83b8f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83b8f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="83b8f-117">-EndpointName</span></span>
<span data-ttu-id="83b8f-118">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="83b8f-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="83b8f-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="83b8f-119">-HostName</span></span>
<span data-ttu-id="83b8f-120">指定自訂網域的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="83b8f-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="83b8f-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="83b8f-121">-ProfileName</span></span>
<span data-ttu-id="83b8f-122">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="83b8f-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="83b8f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b8f-123">-ResourceGroupName</span></span>
<span data-ttu-id="83b8f-124">指定自訂網域所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="83b8f-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="83b8f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="83b8f-125">-Confirm</span></span>
<span data-ttu-id="83b8f-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="83b8f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b8f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b8f-127">-WhatIf</span></span>
<span data-ttu-id="83b8f-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83b8f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b8f-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83b8f-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b8f-130">CommonParameters</span></span>
<span data-ttu-id="83b8f-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="83b8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b8f-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83b8f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b8f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="83b8f-133">INPUTS</span></span>

### <span data-ttu-id="83b8f-134">Microsoft.Azure.Commands.Cdn.models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="83b8f-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="83b8f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="83b8f-135">OUTPUTS</span></span>

### <span data-ttu-id="83b8f-136">Microsoft.Azure.Commands.Cdn.models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83b8f-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="83b8f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="83b8f-137">NOTES</span></span>

## <span data-ttu-id="83b8f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="83b8f-138">RELATED LINKS</span></span>

[<span data-ttu-id="83b8f-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83b8f-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="83b8f-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83b8f-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="83b8f-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83b8f-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)



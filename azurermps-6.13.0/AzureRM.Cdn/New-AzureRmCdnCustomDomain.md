---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: a3d92c095173d9eeb0b5e84812d42656e414b9d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451363"
---
# <span data-ttu-id="83f87-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83f87-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="83f87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83f87-102">SYNOPSIS</span></span>
<span data-ttu-id="83f87-103">為 CDN 端點建立自訂網域。</span><span class="sxs-lookup"><span data-stu-id="83f87-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83f87-104">句法</span><span class="sxs-lookup"><span data-stu-id="83f87-104">SYNTAX</span></span>

### <span data-ttu-id="83f87-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="83f87-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f87-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83f87-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f87-107">說明</span><span class="sxs-lookup"><span data-stu-id="83f87-107">DESCRIPTION</span></span>
<span data-ttu-id="83f87-108">**新的-AzureRmCdnCustomDomain** Cmdlet 會針對 Azure 內容傳遞網路 (CDN) 端點建立自訂網域。</span><span class="sxs-lookup"><span data-stu-id="83f87-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="83f87-109">示例</span><span class="sxs-lookup"><span data-stu-id="83f87-109">EXAMPLES</span></span>

## <span data-ttu-id="83f87-110">參數</span><span class="sxs-lookup"><span data-stu-id="83f87-110">PARAMETERS</span></span>

### <span data-ttu-id="83f87-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="83f87-111">-CdnEndpoint</span></span>
<span data-ttu-id="83f87-112">指定將自訂網域新增到哪個 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="83f87-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="83f87-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="83f87-113">-CustomDomainName</span></span>
<span data-ttu-id="83f87-114">指定自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="83f87-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="83f87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f87-115">-DefaultProfile</span></span>
<span data-ttu-id="83f87-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="83f87-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83f87-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="83f87-117">-EndpointName</span></span>
<span data-ttu-id="83f87-118">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="83f87-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="83f87-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="83f87-119">-HostName</span></span>
<span data-ttu-id="83f87-120">指定自訂網域的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="83f87-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="83f87-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="83f87-121">-ProfileName</span></span>
<span data-ttu-id="83f87-122">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="83f87-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="83f87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f87-123">-ResourceGroupName</span></span>
<span data-ttu-id="83f87-124">指定自訂網域所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83f87-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="83f87-125">-確認</span><span class="sxs-lookup"><span data-stu-id="83f87-125">-Confirm</span></span>
<span data-ttu-id="83f87-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83f87-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f87-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f87-127">-WhatIf</span></span>
<span data-ttu-id="83f87-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83f87-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f87-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83f87-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f87-130">CommonParameters</span></span>
<span data-ttu-id="83f87-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83f87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f87-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83f87-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f87-133">輸入</span><span class="sxs-lookup"><span data-stu-id="83f87-133">INPUTS</span></span>

### <span data-ttu-id="83f87-134">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="83f87-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="83f87-135">參數： CdnEndpoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="83f87-135">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="83f87-136">輸出</span><span class="sxs-lookup"><span data-stu-id="83f87-136">OUTPUTS</span></span>

### <span data-ttu-id="83f87-137">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="83f87-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="83f87-138">筆記</span><span class="sxs-lookup"><span data-stu-id="83f87-138">NOTES</span></span>

## <span data-ttu-id="83f87-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="83f87-139">RELATED LINKS</span></span>

[<span data-ttu-id="83f87-140">AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83f87-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="83f87-141">移除-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83f87-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="83f87-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="83f87-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)



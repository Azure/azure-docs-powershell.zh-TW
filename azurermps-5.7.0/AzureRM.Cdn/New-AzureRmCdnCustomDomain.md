---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2788c135f7c93d0ca2f3a8dbb17228e4118625c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446435"
---
# <span data-ttu-id="5d3c2-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5d3c2-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="5d3c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d3c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3c2-103">為 CDN 端點建立自訂網域。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d3c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d3c2-104">SYNTAX</span></span>

### <span data-ttu-id="5d3c2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5d3c2-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3c2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3c2-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d3c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="5d3c2-107">DESCRIPTION</span></span>
<span data-ttu-id="5d3c2-108">**新的-AzureRmCdnCustomDomain** Cmdlet 會針對 Azure 內容傳遞網路 (CDN) 端點建立自訂網域。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5d3c2-109">示例</span><span class="sxs-lookup"><span data-stu-id="5d3c2-109">EXAMPLES</span></span>

## <span data-ttu-id="5d3c2-110">參數</span><span class="sxs-lookup"><span data-stu-id="5d3c2-110">PARAMETERS</span></span>

### <span data-ttu-id="5d3c2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d3c2-111">-CdnEndpoint</span></span>
<span data-ttu-id="5d3c2-112">指定將自訂網域新增到哪個 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="5d3c2-113">-CustomDomainName</span></span>
<span data-ttu-id="5d3c2-114">指定自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3c2-115">-DefaultProfile</span></span>
<span data-ttu-id="5d3c2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5d3c2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d3c2-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="5d3c2-117">-EndpointName</span></span>
<span data-ttu-id="5d3c2-118">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="5d3c2-119">-HostName</span></span>
<span data-ttu-id="5d3c2-120">指定自訂網域的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5d3c2-121">-ProfileName</span></span>
<span data-ttu-id="5d3c2-122">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-122">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d3c2-124">指定自訂網域所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="5d3c2-125">-Confirm</span></span>
<span data-ttu-id="5d3c2-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d3c2-127">-WhatIf</span></span>
<span data-ttu-id="5d3c2-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d3c2-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3c2-130">CommonParameters</span></span>
<span data-ttu-id="5d3c2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3c2-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d3c2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3c2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5d3c2-133">INPUTS</span></span>

### <span data-ttu-id="5d3c2-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5d3c2-134">PSEndpoint</span></span>
<span data-ttu-id="5d3c2-135">形參 "CdnEndpoint" 接受管線中 "PSEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5d3c2-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="5d3c2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5d3c2-136">OUTPUTS</span></span>

### <span data-ttu-id="5d3c2-137">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="5d3c2-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="5d3c2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5d3c2-138">NOTES</span></span>

## <span data-ttu-id="5d3c2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d3c2-139">RELATED LINKS</span></span>

[<span data-ttu-id="5d3c2-140">AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5d3c2-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="5d3c2-141">移除-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5d3c2-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="5d3c2-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5d3c2-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)



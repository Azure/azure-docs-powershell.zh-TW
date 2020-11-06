---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: bc37d6c6c9be6278cc2e27782000ad242ac07a2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613535"
---
# <span data-ttu-id="0d56d-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d56d-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="0d56d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d56d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d56d-103">為 CDN 端點建立自訂網域。</span><span class="sxs-lookup"><span data-stu-id="0d56d-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="0d56d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d56d-104">SYNTAX</span></span>

### <span data-ttu-id="0d56d-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0d56d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d56d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d56d-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d56d-107">說明</span><span class="sxs-lookup"><span data-stu-id="0d56d-107">DESCRIPTION</span></span>
<span data-ttu-id="0d56d-108">**新的-AzCdnCustomDomain** Cmdlet 會針對 Azure 內容傳遞網路 (CDN) 端點建立自訂網域。</span><span class="sxs-lookup"><span data-stu-id="0d56d-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0d56d-109">示例</span><span class="sxs-lookup"><span data-stu-id="0d56d-109">EXAMPLES</span></span>

## <span data-ttu-id="0d56d-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d56d-110">PARAMETERS</span></span>

### <span data-ttu-id="0d56d-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d56d-111">-CdnEndpoint</span></span>
<span data-ttu-id="0d56d-112">指定將自訂網域新增到哪個 CDN 端點物件。</span><span class="sxs-lookup"><span data-stu-id="0d56d-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="0d56d-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0d56d-113">-CustomDomainName</span></span>
<span data-ttu-id="0d56d-114">指定自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0d56d-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="0d56d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d56d-115">-DefaultProfile</span></span>
<span data-ttu-id="0d56d-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0d56d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d56d-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="0d56d-117">-EndpointName</span></span>
<span data-ttu-id="0d56d-118">指定端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d56d-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="0d56d-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="0d56d-119">-HostName</span></span>
<span data-ttu-id="0d56d-120">指定自訂網域的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="0d56d-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="0d56d-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0d56d-121">-ProfileName</span></span>
<span data-ttu-id="0d56d-122">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d56d-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="0d56d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d56d-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d56d-124">指定自訂網域所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d56d-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="0d56d-125">-確認</span><span class="sxs-lookup"><span data-stu-id="0d56d-125">-Confirm</span></span>
<span data-ttu-id="0d56d-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d56d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d56d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d56d-127">-WhatIf</span></span>
<span data-ttu-id="0d56d-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d56d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d56d-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d56d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d56d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d56d-130">CommonParameters</span></span>
<span data-ttu-id="0d56d-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d56d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d56d-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d56d-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d56d-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0d56d-133">INPUTS</span></span>

### <span data-ttu-id="0d56d-134">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="0d56d-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="0d56d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0d56d-135">OUTPUTS</span></span>

### <span data-ttu-id="0d56d-136">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="0d56d-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="0d56d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0d56d-137">NOTES</span></span>

## <span data-ttu-id="0d56d-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d56d-138">RELATED LINKS</span></span>

[<span data-ttu-id="0d56d-139">AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d56d-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="0d56d-140">移除-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d56d-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="0d56d-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d56d-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


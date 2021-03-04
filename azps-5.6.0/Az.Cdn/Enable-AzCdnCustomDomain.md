---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 82d980768147bb82332dae2dfa8965d962cc882e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902926"
---
# <span data-ttu-id="e16e0-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e16e0-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="e16e0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e16e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e16e0-103">啟用自訂網域 HTTPS (已) 。</span><span class="sxs-lookup"><span data-stu-id="e16e0-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="e16e0-104">語法</span><span class="sxs-lookup"><span data-stu-id="e16e0-104">SYNTAX</span></span>

### <span data-ttu-id="e16e0-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e16e0-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e16e0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e16e0-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e16e0-107">描述</span><span class="sxs-lookup"><span data-stu-id="e16e0-107">DESCRIPTION</span></span>
<span data-ttu-id="e16e0-108">**Enable-AzCdnCustomDomain** Cmdlet 可讓 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="e16e0-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="e16e0-109">例子</span><span class="sxs-lookup"><span data-stu-id="e16e0-109">EXAMPLES</span></span>

### <span data-ttu-id="e16e0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e16e0-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="e16e0-111">啟用自訂網域的 HTTPs 傳遞。</span><span class="sxs-lookup"><span data-stu-id="e16e0-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="e16e0-112">參數</span><span class="sxs-lookup"><span data-stu-id="e16e0-112">PARAMETERS</span></span>

### <span data-ttu-id="e16e0-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e16e0-113">-CustomDomainName</span></span>
<span data-ttu-id="e16e0-114">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e16e0-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="e16e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16e0-115">-DefaultProfile</span></span>
<span data-ttu-id="e16e0-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e16e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e16e0-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e16e0-117">-EndpointName</span></span>
<span data-ttu-id="e16e0-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="e16e0-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e16e0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e16e0-119">-InputObject</span></span>
<span data-ttu-id="e16e0-120">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="e16e0-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e16e0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e16e0-121">-PassThru</span></span>
<span data-ttu-id="e16e0-122">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="e16e0-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16e0-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e16e0-123">-ProfileName</span></span>
<span data-ttu-id="e16e0-124">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="e16e0-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e16e0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e16e0-125">-ResourceGroupName</span></span>
<span data-ttu-id="e16e0-126">Azure CDN 設定檔的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e16e0-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="e16e0-127">-確認</span><span class="sxs-lookup"><span data-stu-id="e16e0-127">-Confirm</span></span>
<span data-ttu-id="e16e0-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e16e0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16e0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16e0-129">-WhatIf</span></span>
<span data-ttu-id="e16e0-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e16e0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e16e0-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e16e0-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16e0-132">CommonParameters</span></span>
<span data-ttu-id="e16e0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e16e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16e0-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e16e0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16e0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="e16e0-135">INPUTS</span></span>

### <span data-ttu-id="e16e0-136">Microsoft.Azure.Commands.Cdn.models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e16e0-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="e16e0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e16e0-137">OUTPUTS</span></span>

### <span data-ttu-id="e16e0-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e16e0-138">System.Boolean</span></span>

## <span data-ttu-id="e16e0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e16e0-139">NOTES</span></span>

## <span data-ttu-id="e16e0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e16e0-140">RELATED LINKS</span></span>

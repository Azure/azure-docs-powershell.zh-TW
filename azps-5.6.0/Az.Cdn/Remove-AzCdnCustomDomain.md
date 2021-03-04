---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: c76e8d9da78fed592f506ba9aca39b68d4d119c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907813"
---
# <span data-ttu-id="6bc51-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6bc51-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="6bc51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6bc51-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc51-103">移除自訂網域。</span><span class="sxs-lookup"><span data-stu-id="6bc51-103">Removes a custom domain.</span></span>

## <span data-ttu-id="6bc51-104">語法</span><span class="sxs-lookup"><span data-stu-id="6bc51-104">SYNTAX</span></span>

### <span data-ttu-id="6bc51-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6bc51-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bc51-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bc51-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc51-107">描述</span><span class="sxs-lookup"><span data-stu-id="6bc51-107">DESCRIPTION</span></span>
<span data-ttu-id="6bc51-108">**Remove-AzCdnCustomDomain Cmdlet** 會從 Azure 內容傳遞網路或 CDN 端點 (自訂) 網域。</span><span class="sxs-lookup"><span data-stu-id="6bc51-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6bc51-109">例子</span><span class="sxs-lookup"><span data-stu-id="6bc51-109">EXAMPLES</span></span>

## <span data-ttu-id="6bc51-110">參數</span><span class="sxs-lookup"><span data-stu-id="6bc51-110">PARAMETERS</span></span>

### <span data-ttu-id="6bc51-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6bc51-111">-CdnCustomDomain</span></span>
<span data-ttu-id="6bc51-112">指定此 Cmdlet 移除的自訂網域。</span><span class="sxs-lookup"><span data-stu-id="6bc51-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6bc51-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="6bc51-113">-CustomDomainName</span></span>
<span data-ttu-id="6bc51-114">指定此 Cmdlet 移除之自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6bc51-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6bc51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc51-115">-DefaultProfile</span></span>
<span data-ttu-id="6bc51-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6bc51-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bc51-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6bc51-117">-EndpointName</span></span>
<span data-ttu-id="6bc51-118">指定此 Cmdlet 移除自訂網域的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="6bc51-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6bc51-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bc51-119">-PassThru</span></span>
<span data-ttu-id="6bc51-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6bc51-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6bc51-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6bc51-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bc51-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6bc51-122">-ProfileName</span></span>
<span data-ttu-id="6bc51-123">指定此 Cmdlet 移除自訂網域的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="6bc51-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6bc51-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bc51-124">-ResourceGroupName</span></span>
<span data-ttu-id="6bc51-125">指定此 Cmdlet 移除自訂網域的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6bc51-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="6bc51-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6bc51-126">-Confirm</span></span>
<span data-ttu-id="6bc51-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6bc51-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc51-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc51-128">-WhatIf</span></span>
<span data-ttu-id="6bc51-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bc51-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bc51-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bc51-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc51-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc51-131">CommonParameters</span></span>
<span data-ttu-id="6bc51-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6bc51-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc51-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bc51-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc51-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6bc51-134">INPUTS</span></span>

### <span data-ttu-id="6bc51-135">Microsoft.Azure.Commands.Cdn.models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6bc51-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="6bc51-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bc51-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bc51-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6bc51-137">OUTPUTS</span></span>

### <span data-ttu-id="6bc51-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6bc51-138">System.Boolean</span></span>

## <span data-ttu-id="6bc51-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6bc51-139">NOTES</span></span>

## <span data-ttu-id="6bc51-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bc51-140">RELATED LINKS</span></span>

[<span data-ttu-id="6bc51-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6bc51-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="6bc51-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6bc51-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="6bc51-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6bc51-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)



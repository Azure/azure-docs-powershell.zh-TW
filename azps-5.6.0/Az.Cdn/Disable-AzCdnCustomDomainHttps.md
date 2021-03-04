---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 837def99279905e3c647ecd8805ed0284840f5a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908630"
---
# <span data-ttu-id="ec1a4-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="ec1a4-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="ec1a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ec1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ec1a4-103">停用自訂網域 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="ec1a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="ec1a4-104">SYNTAX</span></span>

### <span data-ttu-id="ec1a4-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ec1a4-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec1a4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec1a4-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec1a4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec1a4-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec1a4-108">描述</span><span class="sxs-lookup"><span data-stu-id="ec1a4-108">DESCRIPTION</span></span>
<span data-ttu-id="ec1a4-109">**Disable-AzCdnCustomDomainHttps** Cmdlet 會停用 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="ec1a4-110">例子</span><span class="sxs-lookup"><span data-stu-id="ec1a4-110">EXAMPLES</span></span>

### <span data-ttu-id="ec1a4-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ec1a4-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="ec1a4-112">停用自訂網域的安全傳遞。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="ec1a4-113">參數</span><span class="sxs-lookup"><span data-stu-id="ec1a4-113">PARAMETERS</span></span>

### <span data-ttu-id="ec1a4-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ec1a4-114">-CustomDomainName</span></span>
<span data-ttu-id="ec1a4-115">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="ec1a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec1a4-116">-DefaultProfile</span></span>
<span data-ttu-id="ec1a4-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec1a4-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ec1a4-118">-EndpointName</span></span>
<span data-ttu-id="ec1a4-119">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="ec1a4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec1a4-120">-InputObject</span></span>
<span data-ttu-id="ec1a4-121">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-121">The custom domain object.</span></span>

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

### <span data-ttu-id="ec1a4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec1a4-122">-PassThru</span></span>
<span data-ttu-id="ec1a4-123">如果指定，則 Return 物件。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-123">Return object if specified.</span></span>

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

### <span data-ttu-id="ec1a4-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ec1a4-124">-ProfileName</span></span>
<span data-ttu-id="ec1a4-125">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="ec1a4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec1a4-126">-ResourceGroupName</span></span>
<span data-ttu-id="ec1a4-127">Azure CDN 設定檔的資源群組</span><span class="sxs-lookup"><span data-stu-id="ec1a4-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="ec1a4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec1a4-128">-ResourceId</span></span>
<span data-ttu-id="ec1a4-129">自訂網域的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec1a4-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1a4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ec1a4-130">-Confirm</span></span>
<span data-ttu-id="ec1a4-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec1a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec1a4-132">-WhatIf</span></span>
<span data-ttu-id="ec1a4-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec1a4-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec1a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec1a4-135">CommonParameters</span></span>
<span data-ttu-id="ec1a4-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ec1a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec1a4-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec1a4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec1a4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ec1a4-138">INPUTS</span></span>

### <span data-ttu-id="ec1a4-139">Microsoft.Azure.Commands.Cdn.models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ec1a4-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="ec1a4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ec1a4-140">System.String</span></span>

## <span data-ttu-id="ec1a4-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ec1a4-141">OUTPUTS</span></span>

### <span data-ttu-id="ec1a4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec1a4-142">System.Boolean</span></span>

## <span data-ttu-id="ec1a4-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ec1a4-143">NOTES</span></span>

## <span data-ttu-id="ec1a4-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec1a4-144">RELATED LINKS</span></span>

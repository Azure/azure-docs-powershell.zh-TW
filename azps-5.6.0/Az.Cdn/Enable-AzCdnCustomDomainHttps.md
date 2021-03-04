---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 598dd0f386e82f7b195a57c72044756343ef9f56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907162"
---
# <span data-ttu-id="a5145-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="a5145-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="a5145-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5145-102">SYNOPSIS</span></span>
<span data-ttu-id="a5145-103">啟用自訂 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="a5145-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="a5145-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5145-104">SYNTAX</span></span>

### <span data-ttu-id="a5145-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a5145-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5145-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5145-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5145-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5145-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5145-108">描述</span><span class="sxs-lookup"><span data-stu-id="a5145-108">DESCRIPTION</span></span>
<span data-ttu-id="a5145-109">**Enable-AzCdnCustomDomainHttps** Cmdlet 可讓 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="a5145-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="a5145-110">例子</span><span class="sxs-lookup"><span data-stu-id="a5145-110">EXAMPLES</span></span>

### <span data-ttu-id="a5145-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5145-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="a5145-112">啟用自訂網域的安全傳遞。</span><span class="sxs-lookup"><span data-stu-id="a5145-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="a5145-113">參數</span><span class="sxs-lookup"><span data-stu-id="a5145-113">PARAMETERS</span></span>

### <span data-ttu-id="a5145-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a5145-114">-CustomDomainName</span></span>
<span data-ttu-id="a5145-115">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a5145-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="a5145-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5145-116">-DefaultProfile</span></span>
<span data-ttu-id="a5145-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5145-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5145-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a5145-118">-EndpointName</span></span>
<span data-ttu-id="a5145-119">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="a5145-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a5145-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5145-120">-InputObject</span></span>
<span data-ttu-id="a5145-121">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="a5145-121">The custom domain object.</span></span>

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

### <span data-ttu-id="a5145-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5145-122">-PassThru</span></span>
<span data-ttu-id="a5145-123">如果指定，則 Return 物件。</span><span class="sxs-lookup"><span data-stu-id="a5145-123">Return object if specified.</span></span>

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

### <span data-ttu-id="a5145-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a5145-124">-ProfileName</span></span>
<span data-ttu-id="a5145-125">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="a5145-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a5145-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5145-126">-ResourceGroupName</span></span>
<span data-ttu-id="a5145-127">Azure CDN 設定檔的資源群組</span><span class="sxs-lookup"><span data-stu-id="a5145-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="a5145-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5145-128">-ResourceId</span></span>
<span data-ttu-id="a5145-129">自訂網域的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5145-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="a5145-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a5145-130">-Confirm</span></span>
<span data-ttu-id="a5145-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5145-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5145-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5145-132">-WhatIf</span></span>
<span data-ttu-id="a5145-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5145-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5145-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5145-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5145-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5145-135">CommonParameters</span></span>
<span data-ttu-id="a5145-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5145-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5145-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5145-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5145-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a5145-138">INPUTS</span></span>

### <span data-ttu-id="a5145-139">Microsoft.Azure.Commands.Cdn.models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a5145-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="a5145-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a5145-140">System.String</span></span>

## <span data-ttu-id="a5145-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a5145-141">OUTPUTS</span></span>

### <span data-ttu-id="a5145-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5145-142">System.Boolean</span></span>

## <span data-ttu-id="a5145-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a5145-143">NOTES</span></span>

## <span data-ttu-id="a5145-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5145-144">RELATED LINKS</span></span>

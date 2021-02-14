---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: cb11377c4ee18278dee2a3dc97c16bb58a02f5d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129954"
---
# <span data-ttu-id="cc797-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="cc797-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="cc797-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc797-102">SYNOPSIS</span></span>
<span data-ttu-id="cc797-103">啟用自訂 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="cc797-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="cc797-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc797-104">SYNTAX</span></span>

### <span data-ttu-id="cc797-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cc797-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc797-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc797-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc797-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc797-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc797-108">說明</span><span class="sxs-lookup"><span data-stu-id="cc797-108">DESCRIPTION</span></span>
<span data-ttu-id="cc797-109">**Enable-AzCdnCustomDomainHttps** Cmdlet 可啟用 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="cc797-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="cc797-110">示例</span><span class="sxs-lookup"><span data-stu-id="cc797-110">EXAMPLES</span></span>

### <span data-ttu-id="cc797-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cc797-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="cc797-112">允許安全傳送自訂網域。</span><span class="sxs-lookup"><span data-stu-id="cc797-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="cc797-113">參數</span><span class="sxs-lookup"><span data-stu-id="cc797-113">PARAMETERS</span></span>

### <span data-ttu-id="cc797-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="cc797-114">-CustomDomainName</span></span>
<span data-ttu-id="cc797-115">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cc797-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="cc797-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc797-116">-DefaultProfile</span></span>
<span data-ttu-id="cc797-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc797-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc797-118">-終結點</span><span class="sxs-lookup"><span data-stu-id="cc797-118">-EndpointName</span></span>
<span data-ttu-id="cc797-119">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="cc797-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="cc797-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc797-120">-InputObject</span></span>
<span data-ttu-id="cc797-121">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="cc797-121">The custom domain object.</span></span>

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

### <span data-ttu-id="cc797-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc797-122">-PassThru</span></span>
<span data-ttu-id="cc797-123">傳回物件（如果已指定）。</span><span class="sxs-lookup"><span data-stu-id="cc797-123">Return object if specified.</span></span>

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

### <span data-ttu-id="cc797-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cc797-124">-ProfileName</span></span>
<span data-ttu-id="cc797-125">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="cc797-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="cc797-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc797-126">-ResourceGroupName</span></span>
<span data-ttu-id="cc797-127">Azure CDN 設定檔的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="cc797-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="cc797-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc797-128">-ResourceId</span></span>
<span data-ttu-id="cc797-129">自訂網域的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc797-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="cc797-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cc797-130">-Confirm</span></span>
<span data-ttu-id="cc797-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc797-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc797-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc797-132">-WhatIf</span></span>
<span data-ttu-id="cc797-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc797-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc797-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc797-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc797-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc797-135">CommonParameters</span></span>
<span data-ttu-id="cc797-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc797-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc797-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc797-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc797-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cc797-138">INPUTS</span></span>

### <span data-ttu-id="cc797-139">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="cc797-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="cc797-140">System.object</span><span class="sxs-lookup"><span data-stu-id="cc797-140">System.String</span></span>

## <span data-ttu-id="cc797-141">輸出</span><span class="sxs-lookup"><span data-stu-id="cc797-141">OUTPUTS</span></span>

### <span data-ttu-id="cc797-142">System.object</span><span class="sxs-lookup"><span data-stu-id="cc797-142">System.Boolean</span></span>

## <span data-ttu-id="cc797-143">筆記</span><span class="sxs-lookup"><span data-stu-id="cc797-143">NOTES</span></span>

## <span data-ttu-id="cc797-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc797-144">RELATED LINKS</span></span>

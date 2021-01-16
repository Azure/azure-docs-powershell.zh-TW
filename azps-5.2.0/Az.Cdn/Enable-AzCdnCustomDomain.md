---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: eebc75ba8f8f1a55fb4c1db2e7929ce233d93a23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280461"
---
# <span data-ttu-id="d2229-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d2229-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="d2229-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2229-102">SYNOPSIS</span></span>
<span data-ttu-id="d2229-103">啟用 (過時的自訂網域 HTTPS) 。</span><span class="sxs-lookup"><span data-stu-id="d2229-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="d2229-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2229-104">SYNTAX</span></span>

### <span data-ttu-id="d2229-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d2229-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2229-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2229-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2229-107">說明</span><span class="sxs-lookup"><span data-stu-id="d2229-107">DESCRIPTION</span></span>
<span data-ttu-id="d2229-108">**Enable-AzCdnCustomDomain** Cmdlet 可啟用 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="d2229-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d2229-109">示例</span><span class="sxs-lookup"><span data-stu-id="d2229-109">EXAMPLES</span></span>

### <span data-ttu-id="d2229-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d2229-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="d2229-111">啟用自訂網域的 HTTPs 傳送。</span><span class="sxs-lookup"><span data-stu-id="d2229-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="d2229-112">參數</span><span class="sxs-lookup"><span data-stu-id="d2229-112">PARAMETERS</span></span>

### <span data-ttu-id="d2229-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d2229-113">-CustomDomainName</span></span>
<span data-ttu-id="d2229-114">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d2229-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d2229-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2229-115">-DefaultProfile</span></span>
<span data-ttu-id="d2229-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2229-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2229-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="d2229-117">-EndpointName</span></span>
<span data-ttu-id="d2229-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="d2229-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d2229-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2229-119">-InputObject</span></span>
<span data-ttu-id="d2229-120">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="d2229-120">The custom domain object.</span></span>

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

### <span data-ttu-id="d2229-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2229-121">-PassThru</span></span>
<span data-ttu-id="d2229-122">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="d2229-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="d2229-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d2229-123">-ProfileName</span></span>
<span data-ttu-id="d2229-124">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="d2229-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d2229-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2229-125">-ResourceGroupName</span></span>
<span data-ttu-id="d2229-126">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="d2229-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="d2229-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d2229-127">-Confirm</span></span>
<span data-ttu-id="d2229-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2229-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2229-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2229-129">-WhatIf</span></span>
<span data-ttu-id="d2229-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2229-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2229-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2229-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2229-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2229-132">CommonParameters</span></span>
<span data-ttu-id="d2229-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2229-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2229-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d2229-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2229-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d2229-135">INPUTS</span></span>

### <span data-ttu-id="d2229-136">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="d2229-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="d2229-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d2229-137">OUTPUTS</span></span>

### <span data-ttu-id="d2229-138">System.object</span><span class="sxs-lookup"><span data-stu-id="d2229-138">System.Boolean</span></span>

## <span data-ttu-id="d2229-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d2229-139">NOTES</span></span>

## <span data-ttu-id="d2229-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2229-140">RELATED LINKS</span></span>

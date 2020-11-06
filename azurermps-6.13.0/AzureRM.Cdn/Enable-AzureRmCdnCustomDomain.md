---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/enable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 50c1bf02a8952bbbddd2bbb82e55441adacd6a2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443992"
---
# <span data-ttu-id="fc145-101">Enable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fc145-101">Enable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="fc145-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc145-102">SYNOPSIS</span></span>
<span data-ttu-id="fc145-103">啟用自訂 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="fc145-103">Enables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc145-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc145-104">SYNTAX</span></span>

### <span data-ttu-id="fc145-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc145-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc145-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc145-106">ByObjectParameterSet</span></span>
```
Enable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc145-107">說明</span><span class="sxs-lookup"><span data-stu-id="fc145-107">DESCRIPTION</span></span>
<span data-ttu-id="fc145-108">**Enable-AzureRmCdnCustomDomain** Cmdlet 可啟用 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="fc145-108">The **Enable-AzureRmCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="fc145-109">示例</span><span class="sxs-lookup"><span data-stu-id="fc145-109">EXAMPLES</span></span>

### <span data-ttu-id="fc145-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fc145-110">Example 1</span></span>
```powershell
Enable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="fc145-111">啟用自訂網域的 HTTPs 傳送。</span><span class="sxs-lookup"><span data-stu-id="fc145-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="fc145-112">參數</span><span class="sxs-lookup"><span data-stu-id="fc145-112">PARAMETERS</span></span>

### <span data-ttu-id="fc145-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="fc145-113">-CustomDomainName</span></span>
<span data-ttu-id="fc145-114">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="fc145-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="fc145-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc145-115">-DefaultProfile</span></span>
<span data-ttu-id="fc145-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc145-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc145-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="fc145-117">-EndpointName</span></span>
<span data-ttu-id="fc145-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="fc145-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="fc145-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc145-119">-InputObject</span></span>
<span data-ttu-id="fc145-120">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="fc145-120">The custom domain object.</span></span>

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

### <span data-ttu-id="fc145-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc145-121">-PassThru</span></span>
<span data-ttu-id="fc145-122">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="fc145-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="fc145-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fc145-123">-ProfileName</span></span>
<span data-ttu-id="fc145-124">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="fc145-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="fc145-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc145-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc145-126">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="fc145-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="fc145-127">-確認</span><span class="sxs-lookup"><span data-stu-id="fc145-127">-Confirm</span></span>
<span data-ttu-id="fc145-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc145-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc145-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc145-129">-WhatIf</span></span>
<span data-ttu-id="fc145-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc145-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc145-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc145-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc145-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc145-132">CommonParameters</span></span>
<span data-ttu-id="fc145-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc145-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc145-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc145-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc145-135">輸入</span><span class="sxs-lookup"><span data-stu-id="fc145-135">INPUTS</span></span>

### <span data-ttu-id="fc145-136">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="fc145-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="fc145-137">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fc145-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fc145-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fc145-138">OUTPUTS</span></span>

### <span data-ttu-id="fc145-139">System.object</span><span class="sxs-lookup"><span data-stu-id="fc145-139">System.Boolean</span></span>

## <span data-ttu-id="fc145-140">筆記</span><span class="sxs-lookup"><span data-stu-id="fc145-140">NOTES</span></span>

## <span data-ttu-id="fc145-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc145-141">RELATED LINKS</span></span>

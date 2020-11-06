---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 4107ae55b42e35ae600766deb037c8c0590c8731
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613561"
---
# <span data-ttu-id="b1038-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b1038-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="b1038-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1038-102">SYNOPSIS</span></span>
<span data-ttu-id="b1038-103">停用 (過時的自訂網域 HTTPS) 。</span><span class="sxs-lookup"><span data-stu-id="b1038-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="b1038-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1038-104">SYNTAX</span></span>

### <span data-ttu-id="b1038-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b1038-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1038-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1038-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1038-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1038-107">DESCRIPTION</span></span>
<span data-ttu-id="b1038-108">**Disable AzCdnCustomDomain** Cmdlet 會停用 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="b1038-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="b1038-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1038-109">EXAMPLES</span></span>

### <span data-ttu-id="b1038-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b1038-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="b1038-111">停用 HTTPs 傳送自訂網域。</span><span class="sxs-lookup"><span data-stu-id="b1038-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="b1038-112">參數</span><span class="sxs-lookup"><span data-stu-id="b1038-112">PARAMETERS</span></span>

### <span data-ttu-id="b1038-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="b1038-113">-CustomDomainName</span></span>
<span data-ttu-id="b1038-114">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b1038-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="b1038-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1038-115">-DefaultProfile</span></span>
<span data-ttu-id="b1038-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1038-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1038-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="b1038-117">-EndpointName</span></span>
<span data-ttu-id="b1038-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="b1038-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="b1038-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1038-119">-InputObject</span></span>
<span data-ttu-id="b1038-120">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="b1038-120">The custom domain object.</span></span>

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

### <span data-ttu-id="b1038-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1038-121">-PassThru</span></span>
<span data-ttu-id="b1038-122">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="b1038-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="b1038-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b1038-123">-ProfileName</span></span>
<span data-ttu-id="b1038-124">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b1038-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="b1038-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1038-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1038-126">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="b1038-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="b1038-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b1038-127">-Confirm</span></span>
<span data-ttu-id="b1038-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1038-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1038-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1038-129">-WhatIf</span></span>
<span data-ttu-id="b1038-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1038-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1038-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1038-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1038-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1038-132">CommonParameters</span></span>
<span data-ttu-id="b1038-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1038-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1038-134">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1038-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1038-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b1038-135">INPUTS</span></span>

### <span data-ttu-id="b1038-136">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="b1038-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="b1038-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b1038-137">OUTPUTS</span></span>

### <span data-ttu-id="b1038-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b1038-138">System.Boolean</span></span>

## <span data-ttu-id="b1038-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b1038-139">NOTES</span></span>

## <span data-ttu-id="b1038-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1038-140">RELATED LINKS</span></span>
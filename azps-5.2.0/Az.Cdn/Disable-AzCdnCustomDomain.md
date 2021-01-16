---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280469"
---
# <span data-ttu-id="3dd0c-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="3dd0c-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="3dd0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3dd0c-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd0c-103">停用 (過時的自訂網域 HTTPS) 。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="3dd0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3dd0c-104">SYNTAX</span></span>

### <span data-ttu-id="3dd0c-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3dd0c-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dd0c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dd0c-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd0c-107">說明</span><span class="sxs-lookup"><span data-stu-id="3dd0c-107">DESCRIPTION</span></span>
<span data-ttu-id="3dd0c-108">**Disable AzCdnCustomDomain** Cmdlet 會停用 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="3dd0c-109">示例</span><span class="sxs-lookup"><span data-stu-id="3dd0c-109">EXAMPLES</span></span>

### <span data-ttu-id="3dd0c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3dd0c-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="3dd0c-111">停用 HTTPs 傳送自訂網域。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="3dd0c-112">參數</span><span class="sxs-lookup"><span data-stu-id="3dd0c-112">PARAMETERS</span></span>

### <span data-ttu-id="3dd0c-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="3dd0c-113">-CustomDomainName</span></span>
<span data-ttu-id="3dd0c-114">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="3dd0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd0c-115">-DefaultProfile</span></span>
<span data-ttu-id="3dd0c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd0c-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="3dd0c-117">-EndpointName</span></span>
<span data-ttu-id="3dd0c-118">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="3dd0c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dd0c-119">-InputObject</span></span>
<span data-ttu-id="3dd0c-120">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-120">The custom domain object.</span></span>

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

### <span data-ttu-id="3dd0c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dd0c-121">-PassThru</span></span>
<span data-ttu-id="3dd0c-122">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="3dd0c-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3dd0c-123">-ProfileName</span></span>
<span data-ttu-id="3dd0c-124">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="3dd0c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd0c-125">-ResourceGroupName</span></span>
<span data-ttu-id="3dd0c-126">Azure CDN 設定檔的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="3dd0c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="3dd0c-127">-Confirm</span></span>
<span data-ttu-id="3dd0c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd0c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd0c-129">-WhatIf</span></span>
<span data-ttu-id="3dd0c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dd0c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd0c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd0c-132">CommonParameters</span></span>
<span data-ttu-id="3dd0c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd0c-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3dd0c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd0c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3dd0c-135">INPUTS</span></span>

### <span data-ttu-id="3dd0c-136">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="3dd0c-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="3dd0c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3dd0c-137">OUTPUTS</span></span>

### <span data-ttu-id="3dd0c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="3dd0c-138">System.Boolean</span></span>

## <span data-ttu-id="3dd0c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3dd0c-139">NOTES</span></span>

## <span data-ttu-id="3dd0c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3dd0c-140">RELATED LINKS</span></span>

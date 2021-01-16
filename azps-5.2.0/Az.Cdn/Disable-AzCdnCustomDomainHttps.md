---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280462"
---
# <span data-ttu-id="df6db-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="df6db-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="df6db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df6db-102">SYNOPSIS</span></span>
<span data-ttu-id="df6db-103">停用自訂網域 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="df6db-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="df6db-104">句法</span><span class="sxs-lookup"><span data-stu-id="df6db-104">SYNTAX</span></span>

### <span data-ttu-id="df6db-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="df6db-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df6db-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df6db-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df6db-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df6db-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df6db-108">說明</span><span class="sxs-lookup"><span data-stu-id="df6db-108">DESCRIPTION</span></span>
<span data-ttu-id="df6db-109">**Disable AzCdnCustomDomainHttps** Cmdlet 會停用 CDN 自訂網域的安全 HTTPS 傳遞。</span><span class="sxs-lookup"><span data-stu-id="df6db-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="df6db-110">示例</span><span class="sxs-lookup"><span data-stu-id="df6db-110">EXAMPLES</span></span>

### <span data-ttu-id="df6db-111">範例1</span><span class="sxs-lookup"><span data-stu-id="df6db-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="df6db-112">停用自訂網域的安全傳送。</span><span class="sxs-lookup"><span data-stu-id="df6db-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="df6db-113">參數</span><span class="sxs-lookup"><span data-stu-id="df6db-113">PARAMETERS</span></span>

### <span data-ttu-id="df6db-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="df6db-114">-CustomDomainName</span></span>
<span data-ttu-id="df6db-115">Azure CDN 自訂網域顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="df6db-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="df6db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6db-116">-DefaultProfile</span></span>
<span data-ttu-id="df6db-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df6db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df6db-118">-終結點</span><span class="sxs-lookup"><span data-stu-id="df6db-118">-EndpointName</span></span>
<span data-ttu-id="df6db-119">Azure CDN 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="df6db-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="df6db-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df6db-120">-InputObject</span></span>
<span data-ttu-id="df6db-121">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="df6db-121">The custom domain object.</span></span>

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

### <span data-ttu-id="df6db-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df6db-122">-PassThru</span></span>
<span data-ttu-id="df6db-123">傳回物件（如果已指定）。</span><span class="sxs-lookup"><span data-stu-id="df6db-123">Return object if specified.</span></span>

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

### <span data-ttu-id="df6db-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="df6db-124">-ProfileName</span></span>
<span data-ttu-id="df6db-125">Azure CDN 設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="df6db-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="df6db-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df6db-126">-ResourceGroupName</span></span>
<span data-ttu-id="df6db-127">Azure CDN 設定檔的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="df6db-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="df6db-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df6db-128">-ResourceId</span></span>
<span data-ttu-id="df6db-129">自訂網域的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="df6db-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="df6db-130">-確認</span><span class="sxs-lookup"><span data-stu-id="df6db-130">-Confirm</span></span>
<span data-ttu-id="df6db-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df6db-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df6db-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df6db-132">-WhatIf</span></span>
<span data-ttu-id="df6db-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df6db-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df6db-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df6db-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df6db-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6db-135">CommonParameters</span></span>
<span data-ttu-id="df6db-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df6db-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6db-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="df6db-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6db-138">輸入</span><span class="sxs-lookup"><span data-stu-id="df6db-138">INPUTS</span></span>

### <span data-ttu-id="df6db-139">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="df6db-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="df6db-140">System.object</span><span class="sxs-lookup"><span data-stu-id="df6db-140">System.String</span></span>

## <span data-ttu-id="df6db-141">輸出</span><span class="sxs-lookup"><span data-stu-id="df6db-141">OUTPUTS</span></span>

### <span data-ttu-id="df6db-142">System.object</span><span class="sxs-lookup"><span data-stu-id="df6db-142">System.Boolean</span></span>

## <span data-ttu-id="df6db-143">筆記</span><span class="sxs-lookup"><span data-stu-id="df6db-143">NOTES</span></span>

## <span data-ttu-id="df6db-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="df6db-144">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: c2259cdf42fc0f1065b37736dddea1d214b2ecb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613517"
---
# <span data-ttu-id="84126-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84126-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="84126-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84126-102">SYNOPSIS</span></span>
<span data-ttu-id="84126-103">移除自訂網域。</span><span class="sxs-lookup"><span data-stu-id="84126-103">Removes a custom domain.</span></span>

## <span data-ttu-id="84126-104">句法</span><span class="sxs-lookup"><span data-stu-id="84126-104">SYNTAX</span></span>

### <span data-ttu-id="84126-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="84126-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84126-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84126-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84126-107">說明</span><span class="sxs-lookup"><span data-stu-id="84126-107">DESCRIPTION</span></span>
<span data-ttu-id="84126-108">**AzCdnCustomDomain** Cmdlet 會將自訂網域從 Azure 內容傳遞網路 (CDN) 端點中移除。</span><span class="sxs-lookup"><span data-stu-id="84126-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="84126-109">示例</span><span class="sxs-lookup"><span data-stu-id="84126-109">EXAMPLES</span></span>

## <span data-ttu-id="84126-110">參數</span><span class="sxs-lookup"><span data-stu-id="84126-110">PARAMETERS</span></span>

### <span data-ttu-id="84126-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84126-111">-CdnCustomDomain</span></span>
<span data-ttu-id="84126-112">指定此 Cmdlet 移除的自訂網域。</span><span class="sxs-lookup"><span data-stu-id="84126-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="84126-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="84126-113">-CustomDomainName</span></span>
<span data-ttu-id="84126-114">指定此 Cmdlet 移除之自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="84126-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="84126-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84126-115">-DefaultProfile</span></span>
<span data-ttu-id="84126-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="84126-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84126-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="84126-117">-EndpointName</span></span>
<span data-ttu-id="84126-118">指定此 Cmdlet 從中移除自訂網域的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="84126-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="84126-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84126-119">-PassThru</span></span>
<span data-ttu-id="84126-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="84126-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84126-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="84126-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="84126-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="84126-122">-ProfileName</span></span>
<span data-ttu-id="84126-123">指定此 Cmdlet 從中移除自訂網域的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="84126-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="84126-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84126-124">-ResourceGroupName</span></span>
<span data-ttu-id="84126-125">指定此 Cmdlet 從中移除自訂網域的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84126-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="84126-126">-確認</span><span class="sxs-lookup"><span data-stu-id="84126-126">-Confirm</span></span>
<span data-ttu-id="84126-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84126-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84126-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84126-128">-WhatIf</span></span>
<span data-ttu-id="84126-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84126-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84126-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84126-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84126-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84126-131">CommonParameters</span></span>
<span data-ttu-id="84126-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84126-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84126-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84126-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84126-134">輸入</span><span class="sxs-lookup"><span data-stu-id="84126-134">INPUTS</span></span>

### <span data-ttu-id="84126-135">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="84126-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="84126-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="84126-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84126-137">輸出</span><span class="sxs-lookup"><span data-stu-id="84126-137">OUTPUTS</span></span>

### <span data-ttu-id="84126-138">System.object</span><span class="sxs-lookup"><span data-stu-id="84126-138">System.Boolean</span></span>

## <span data-ttu-id="84126-139">筆記</span><span class="sxs-lookup"><span data-stu-id="84126-139">NOTES</span></span>

## <span data-ttu-id="84126-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="84126-140">RELATED LINKS</span></span>

[<span data-ttu-id="84126-141">AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84126-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="84126-142">新-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84126-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="84126-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="84126-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)



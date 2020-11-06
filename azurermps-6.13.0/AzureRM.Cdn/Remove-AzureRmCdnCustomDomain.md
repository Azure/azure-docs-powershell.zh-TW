---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: fa0e3682d62f01d7d305d190c6765aab709bed15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450267"
---
# <span data-ttu-id="cc99b-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc99b-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="cc99b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc99b-102">SYNOPSIS</span></span>
<span data-ttu-id="cc99b-103">移除自訂網域。</span><span class="sxs-lookup"><span data-stu-id="cc99b-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc99b-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc99b-104">SYNTAX</span></span>

### <span data-ttu-id="cc99b-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cc99b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc99b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc99b-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc99b-107">說明</span><span class="sxs-lookup"><span data-stu-id="cc99b-107">DESCRIPTION</span></span>
<span data-ttu-id="cc99b-108">**AzureRmCdnCustomDomain** Cmdlet 會將自訂網域從 Azure 內容傳遞網路 (CDN) 端點中移除。</span><span class="sxs-lookup"><span data-stu-id="cc99b-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="cc99b-109">示例</span><span class="sxs-lookup"><span data-stu-id="cc99b-109">EXAMPLES</span></span>

## <span data-ttu-id="cc99b-110">參數</span><span class="sxs-lookup"><span data-stu-id="cc99b-110">PARAMETERS</span></span>

### <span data-ttu-id="cc99b-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc99b-111">-CdnCustomDomain</span></span>
<span data-ttu-id="cc99b-112">指定此 Cmdlet 移除的自訂網域。</span><span class="sxs-lookup"><span data-stu-id="cc99b-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cc99b-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="cc99b-113">-CustomDomainName</span></span>
<span data-ttu-id="cc99b-114">指定此 Cmdlet 移除之自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="cc99b-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cc99b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc99b-115">-DefaultProfile</span></span>
<span data-ttu-id="cc99b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cc99b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc99b-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="cc99b-117">-EndpointName</span></span>
<span data-ttu-id="cc99b-118">指定此 Cmdlet 從中移除自訂網域的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="cc99b-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="cc99b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc99b-119">-PassThru</span></span>
<span data-ttu-id="cc99b-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="cc99b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc99b-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cc99b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc99b-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cc99b-122">-ProfileName</span></span>
<span data-ttu-id="cc99b-123">指定此 Cmdlet 從中移除自訂網域的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="cc99b-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="cc99b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc99b-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc99b-125">指定此 Cmdlet 從中移除自訂網域的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc99b-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="cc99b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="cc99b-126">-Confirm</span></span>
<span data-ttu-id="cc99b-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc99b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc99b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc99b-128">-WhatIf</span></span>
<span data-ttu-id="cc99b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc99b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc99b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc99b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc99b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc99b-131">CommonParameters</span></span>
<span data-ttu-id="cc99b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc99b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc99b-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc99b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc99b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="cc99b-134">INPUTS</span></span>

### <span data-ttu-id="cc99b-135">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="cc99b-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="cc99b-136">參數： CdnCustomDomain (ByValue) </span><span class="sxs-lookup"><span data-stu-id="cc99b-136">Parameters: CdnCustomDomain (ByValue)</span></span>

### <span data-ttu-id="cc99b-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="cc99b-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cc99b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="cc99b-138">OUTPUTS</span></span>

### <span data-ttu-id="cc99b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="cc99b-139">System.Boolean</span></span>

## <span data-ttu-id="cc99b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="cc99b-140">NOTES</span></span>

## <span data-ttu-id="cc99b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc99b-141">RELATED LINKS</span></span>

[<span data-ttu-id="cc99b-142">AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc99b-142">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="cc99b-143">新-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc99b-143">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="cc99b-144">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc99b-144">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)



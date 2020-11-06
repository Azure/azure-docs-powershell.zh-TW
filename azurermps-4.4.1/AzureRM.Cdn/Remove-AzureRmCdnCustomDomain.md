---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2aa6b3932424f7a8375cca2584a7fc7916124c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452555"
---
# <span data-ttu-id="38550-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="38550-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="38550-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38550-102">SYNOPSIS</span></span>
<span data-ttu-id="38550-103">移除自訂網域。</span><span class="sxs-lookup"><span data-stu-id="38550-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38550-104">句法</span><span class="sxs-lookup"><span data-stu-id="38550-104">SYNTAX</span></span>

### <span data-ttu-id="38550-105">預設)  (欄位參數的參數集</span><span class="sxs-lookup"><span data-stu-id="38550-105">Parameter Set for fields parameters (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38550-106">為物件參數設定參數</span><span class="sxs-lookup"><span data-stu-id="38550-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38550-107">說明</span><span class="sxs-lookup"><span data-stu-id="38550-107">DESCRIPTION</span></span>
<span data-ttu-id="38550-108">**AzureRmCdnCustomDomain** Cmdlet 會將自訂網域從 Azure 內容傳遞網路 (CDN) 端點中移除。</span><span class="sxs-lookup"><span data-stu-id="38550-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="38550-109">示例</span><span class="sxs-lookup"><span data-stu-id="38550-109">EXAMPLES</span></span>

## <span data-ttu-id="38550-110">參數</span><span class="sxs-lookup"><span data-stu-id="38550-110">PARAMETERS</span></span>

### <span data-ttu-id="38550-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="38550-111">-CdnCustomDomain</span></span>
<span data-ttu-id="38550-112">指定此 Cmdlet 移除的自訂網域。</span><span class="sxs-lookup"><span data-stu-id="38550-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38550-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="38550-113">-CustomDomainName</span></span>
<span data-ttu-id="38550-114">指定此 Cmdlet 移除之自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="38550-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38550-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="38550-115">-EndpointName</span></span>
<span data-ttu-id="38550-116">指定此 Cmdlet 從中移除自訂網域的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="38550-116">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38550-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38550-117">-PassThru</span></span>
<span data-ttu-id="38550-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="38550-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="38550-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="38550-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="38550-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="38550-120">-ProfileName</span></span>
<span data-ttu-id="38550-121">指定此 Cmdlet 從中移除自訂網域的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="38550-121">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38550-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38550-122">-ResourceGroupName</span></span>
<span data-ttu-id="38550-123">指定此 Cmdlet 從中移除自訂網域的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="38550-123">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38550-124">-確認</span><span class="sxs-lookup"><span data-stu-id="38550-124">-Confirm</span></span>
<span data-ttu-id="38550-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38550-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38550-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38550-126">-WhatIf</span></span>
<span data-ttu-id="38550-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38550-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38550-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38550-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38550-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38550-129">-DefaultProfile</span></span>
<span data-ttu-id="38550-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38550-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38550-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38550-131">CommonParameters</span></span>
<span data-ttu-id="38550-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38550-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38550-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38550-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38550-134">輸入</span><span class="sxs-lookup"><span data-stu-id="38550-134">INPUTS</span></span>

### <span data-ttu-id="38550-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="38550-135">PSCustomDomain</span></span>
<span data-ttu-id="38550-136">形參 "CdnCustomDomain" 接受管線中 "PSCustomDomain" 類型的值</span><span class="sxs-lookup"><span data-stu-id="38550-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="38550-137">輸出</span><span class="sxs-lookup"><span data-stu-id="38550-137">OUTPUTS</span></span>

### <span data-ttu-id="38550-138">System.object</span><span class="sxs-lookup"><span data-stu-id="38550-138">System.Boolean</span></span>

## <span data-ttu-id="38550-139">筆記</span><span class="sxs-lookup"><span data-stu-id="38550-139">NOTES</span></span>

## <span data-ttu-id="38550-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="38550-140">RELATED LINKS</span></span>

[<span data-ttu-id="38550-141">AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="38550-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="38550-142">新-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="38550-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="38550-143">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="38550-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)



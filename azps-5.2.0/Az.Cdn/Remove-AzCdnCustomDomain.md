---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280964"
---
# <span data-ttu-id="5512e-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5512e-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="5512e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5512e-102">SYNOPSIS</span></span>
<span data-ttu-id="5512e-103">移除自訂網域。</span><span class="sxs-lookup"><span data-stu-id="5512e-103">Removes a custom domain.</span></span>

## <span data-ttu-id="5512e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5512e-104">SYNTAX</span></span>

### <span data-ttu-id="5512e-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5512e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5512e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5512e-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5512e-107">說明</span><span class="sxs-lookup"><span data-stu-id="5512e-107">DESCRIPTION</span></span>
<span data-ttu-id="5512e-108">**AzCdnCustomDomain** Cmdlet 會將自訂網域從 Azure 內容傳遞網路 (CDN) 端點中移除。</span><span class="sxs-lookup"><span data-stu-id="5512e-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5512e-109">示例</span><span class="sxs-lookup"><span data-stu-id="5512e-109">EXAMPLES</span></span>

## <span data-ttu-id="5512e-110">參數</span><span class="sxs-lookup"><span data-stu-id="5512e-110">PARAMETERS</span></span>

### <span data-ttu-id="5512e-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5512e-111">-CdnCustomDomain</span></span>
<span data-ttu-id="5512e-112">指定此 Cmdlet 移除的自訂網域。</span><span class="sxs-lookup"><span data-stu-id="5512e-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5512e-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="5512e-113">-CustomDomainName</span></span>
<span data-ttu-id="5512e-114">指定此 Cmdlet 移除之自訂網域的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5512e-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5512e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5512e-115">-DefaultProfile</span></span>
<span data-ttu-id="5512e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5512e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5512e-117">-終結點</span><span class="sxs-lookup"><span data-stu-id="5512e-117">-EndpointName</span></span>
<span data-ttu-id="5512e-118">指定此 Cmdlet 從中移除自訂網域的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="5512e-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="5512e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5512e-119">-PassThru</span></span>
<span data-ttu-id="5512e-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5512e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5512e-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5512e-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5512e-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5512e-122">-ProfileName</span></span>
<span data-ttu-id="5512e-123">指定此 Cmdlet 從中移除自訂網域的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="5512e-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="5512e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5512e-124">-ResourceGroupName</span></span>
<span data-ttu-id="5512e-125">指定此 Cmdlet 從中移除自訂網域的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5512e-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="5512e-126">-確認</span><span class="sxs-lookup"><span data-stu-id="5512e-126">-Confirm</span></span>
<span data-ttu-id="5512e-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5512e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5512e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5512e-128">-WhatIf</span></span>
<span data-ttu-id="5512e-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5512e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5512e-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5512e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5512e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5512e-131">CommonParameters</span></span>
<span data-ttu-id="5512e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5512e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5512e-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5512e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5512e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5512e-134">INPUTS</span></span>

### <span data-ttu-id="5512e-135">PSCustomDomain （CustomDomain）的</span><span class="sxs-lookup"><span data-stu-id="5512e-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="5512e-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5512e-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5512e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5512e-137">OUTPUTS</span></span>

### <span data-ttu-id="5512e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="5512e-138">System.Boolean</span></span>

## <span data-ttu-id="5512e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5512e-139">NOTES</span></span>

## <span data-ttu-id="5512e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5512e-140">RELATED LINKS</span></span>

[<span data-ttu-id="5512e-141">AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5512e-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="5512e-142">新-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5512e-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="5512e-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="5512e-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)



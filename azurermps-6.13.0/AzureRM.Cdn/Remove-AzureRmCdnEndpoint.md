---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 6feb7eb3f20e06c8dfffaa3dd9a1fb2bf3cc4c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450266"
---
# <span data-ttu-id="097e3-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="097e3-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="097e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="097e3-102">SYNOPSIS</span></span>
<span data-ttu-id="097e3-103">移除 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="097e3-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="097e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="097e3-104">SYNTAX</span></span>

### <span data-ttu-id="097e3-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="097e3-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="097e3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="097e3-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="097e3-107">說明</span><span class="sxs-lookup"><span data-stu-id="097e3-107">DESCRIPTION</span></span>
<span data-ttu-id="097e3-108">**AzureRmCdnEndpoint** Cmdlet 會將 Azure 內容傳遞網路 (CDN) 端點中移除。</span><span class="sxs-lookup"><span data-stu-id="097e3-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="097e3-109">示例</span><span class="sxs-lookup"><span data-stu-id="097e3-109">EXAMPLES</span></span>

## <span data-ttu-id="097e3-110">參數</span><span class="sxs-lookup"><span data-stu-id="097e3-110">PARAMETERS</span></span>

### <span data-ttu-id="097e3-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="097e3-111">-CdnEndpoint</span></span>
<span data-ttu-id="097e3-112">指定此 Cmdlet 移除的端點。</span><span class="sxs-lookup"><span data-stu-id="097e3-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="097e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097e3-113">-DefaultProfile</span></span>
<span data-ttu-id="097e3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="097e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="097e3-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="097e3-115">-EndpointName</span></span>
<span data-ttu-id="097e3-116">指定此 Cmdlet 移除之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="097e3-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="097e3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="097e3-117">-Force</span></span>
<span data-ttu-id="097e3-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="097e3-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="097e3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="097e3-119">-PassThru</span></span>
<span data-ttu-id="097e3-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="097e3-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="097e3-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="097e3-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="097e3-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="097e3-122">-ProfileName</span></span>
<span data-ttu-id="097e3-123">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="097e3-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="097e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="097e3-125">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="097e3-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="097e3-126">-確認</span><span class="sxs-lookup"><span data-stu-id="097e3-126">-Confirm</span></span>
<span data-ttu-id="097e3-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="097e3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="097e3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="097e3-128">-WhatIf</span></span>
<span data-ttu-id="097e3-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="097e3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="097e3-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="097e3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="097e3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097e3-131">CommonParameters</span></span>
<span data-ttu-id="097e3-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="097e3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097e3-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="097e3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097e3-134">輸入</span><span class="sxs-lookup"><span data-stu-id="097e3-134">INPUTS</span></span>

### <span data-ttu-id="097e3-135">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="097e3-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="097e3-136">參數： CdnEndpoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="097e3-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="097e3-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="097e3-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="097e3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="097e3-138">OUTPUTS</span></span>

### <span data-ttu-id="097e3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="097e3-139">System.Boolean</span></span>

## <span data-ttu-id="097e3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="097e3-140">NOTES</span></span>

## <span data-ttu-id="097e3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="097e3-141">RELATED LINKS</span></span>

[<span data-ttu-id="097e3-142">AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="097e3-142">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="097e3-143">新-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="097e3-143">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="097e3-144">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="097e3-144">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="097e3-145">開始-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="097e3-145">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="097e3-146">停止 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="097e3-146">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 8216d6404cb184767b03acd92f6549c2b8eda2e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788625"
---
# <span data-ttu-id="eb8bc-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8bc-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="eb8bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8bc-103">啟動 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="eb8bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb8bc-104">SYNTAX</span></span>

### <span data-ttu-id="eb8bc-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eb8bc-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8bc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb8bc-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb8bc-107">說明</span><span class="sxs-lookup"><span data-stu-id="eb8bc-107">DESCRIPTION</span></span>
<span data-ttu-id="eb8bc-108">**Start AzCdnEndpoint** Cmdlet 會啟動 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="eb8bc-109">示例</span><span class="sxs-lookup"><span data-stu-id="eb8bc-109">EXAMPLES</span></span>

## <span data-ttu-id="eb8bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb8bc-110">PARAMETERS</span></span>

### <span data-ttu-id="eb8bc-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8bc-111">-CdnEndpoint</span></span>
<span data-ttu-id="eb8bc-112">指定此 Cmdlet 啟動的端點。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="eb8bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8bc-113">-DefaultProfile</span></span>
<span data-ttu-id="eb8bc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="eb8bc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb8bc-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="eb8bc-115">-EndpointName</span></span>
<span data-ttu-id="eb8bc-116">指定此 Cmdlet 啟動之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="eb8bc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb8bc-117">-PassThru</span></span>
<span data-ttu-id="eb8bc-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb8bc-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb8bc-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="eb8bc-120">-ProfileName</span></span>
<span data-ttu-id="eb8bc-121">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="eb8bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb8bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="eb8bc-123">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="eb8bc-124">-確認</span><span class="sxs-lookup"><span data-stu-id="eb8bc-124">-Confirm</span></span>
<span data-ttu-id="eb8bc-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb8bc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8bc-126">-WhatIf</span></span>
<span data-ttu-id="eb8bc-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb8bc-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb8bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8bc-129">CommonParameters</span></span>
<span data-ttu-id="eb8bc-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8bc-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb8bc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8bc-132">輸入</span><span class="sxs-lookup"><span data-stu-id="eb8bc-132">INPUTS</span></span>

### <span data-ttu-id="eb8bc-133">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="eb8bc-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="eb8bc-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="eb8bc-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eb8bc-135">輸出</span><span class="sxs-lookup"><span data-stu-id="eb8bc-135">OUTPUTS</span></span>

### <span data-ttu-id="eb8bc-136">System.object</span><span class="sxs-lookup"><span data-stu-id="eb8bc-136">System.Boolean</span></span>

## <span data-ttu-id="eb8bc-137">筆記</span><span class="sxs-lookup"><span data-stu-id="eb8bc-137">NOTES</span></span>

## <span data-ttu-id="eb8bc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb8bc-138">RELATED LINKS</span></span>

[<span data-ttu-id="eb8bc-139">AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8bc-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="eb8bc-140">新-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8bc-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="eb8bc-141">移除-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8bc-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="eb8bc-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8bc-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="eb8bc-143">停止 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="eb8bc-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)



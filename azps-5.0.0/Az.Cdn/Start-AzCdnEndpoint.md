---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139082"
---
# <span data-ttu-id="ca99b-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca99b-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="ca99b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca99b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca99b-103">啟動 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="ca99b-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="ca99b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca99b-104">SYNTAX</span></span>

### <span data-ttu-id="ca99b-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ca99b-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca99b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca99b-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca99b-107">說明</span><span class="sxs-lookup"><span data-stu-id="ca99b-107">DESCRIPTION</span></span>
<span data-ttu-id="ca99b-108">**Start AzCdnEndpoint** Cmdlet 會啟動 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="ca99b-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ca99b-109">示例</span><span class="sxs-lookup"><span data-stu-id="ca99b-109">EXAMPLES</span></span>

## <span data-ttu-id="ca99b-110">參數</span><span class="sxs-lookup"><span data-stu-id="ca99b-110">PARAMETERS</span></span>

### <span data-ttu-id="ca99b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca99b-111">-CdnEndpoint</span></span>
<span data-ttu-id="ca99b-112">指定此 Cmdlet 啟動的端點。</span><span class="sxs-lookup"><span data-stu-id="ca99b-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ca99b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca99b-113">-DefaultProfile</span></span>
<span data-ttu-id="ca99b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ca99b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca99b-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="ca99b-115">-EndpointName</span></span>
<span data-ttu-id="ca99b-116">指定此 Cmdlet 啟動之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca99b-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ca99b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca99b-117">-PassThru</span></span>
<span data-ttu-id="ca99b-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ca99b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca99b-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ca99b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca99b-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ca99b-120">-ProfileName</span></span>
<span data-ttu-id="ca99b-121">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="ca99b-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ca99b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca99b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca99b-123">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca99b-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ca99b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ca99b-124">-Confirm</span></span>
<span data-ttu-id="ca99b-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca99b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca99b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca99b-126">-WhatIf</span></span>
<span data-ttu-id="ca99b-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca99b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca99b-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca99b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca99b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca99b-129">CommonParameters</span></span>
<span data-ttu-id="ca99b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca99b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca99b-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca99b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca99b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ca99b-132">INPUTS</span></span>

### <span data-ttu-id="ca99b-133">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="ca99b-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="ca99b-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="ca99b-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ca99b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ca99b-135">OUTPUTS</span></span>

### <span data-ttu-id="ca99b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="ca99b-136">System.Boolean</span></span>

## <span data-ttu-id="ca99b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ca99b-137">NOTES</span></span>

## <span data-ttu-id="ca99b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca99b-138">RELATED LINKS</span></span>

[<span data-ttu-id="ca99b-139">AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca99b-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="ca99b-140">新-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca99b-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="ca99b-141">移除-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca99b-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="ca99b-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca99b-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="ca99b-143">停止 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca99b-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)



---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/start-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Start-AzureRmCdnEndpoint.md
ms.openlocfilehash: 4a6f7b86d16e5b82cf6bf9e869ed74f688fc5950
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450259"
---
# <span data-ttu-id="24e45-101">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e45-101">Start-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="24e45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24e45-102">SYNOPSIS</span></span>
<span data-ttu-id="24e45-103">啟動 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="24e45-103">Starts a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24e45-104">句法</span><span class="sxs-lookup"><span data-stu-id="24e45-104">SYNTAX</span></span>

### <span data-ttu-id="24e45-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="24e45-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e45-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24e45-106">ByObjectParameterSet</span></span>
```
Start-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e45-107">說明</span><span class="sxs-lookup"><span data-stu-id="24e45-107">DESCRIPTION</span></span>
<span data-ttu-id="24e45-108">**Start AzureRmCdnEndpoint** Cmdlet 會啟動 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="24e45-108">The **Start-AzureRmCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="24e45-109">示例</span><span class="sxs-lookup"><span data-stu-id="24e45-109">EXAMPLES</span></span>

## <span data-ttu-id="24e45-110">參數</span><span class="sxs-lookup"><span data-stu-id="24e45-110">PARAMETERS</span></span>

### <span data-ttu-id="24e45-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e45-111">-CdnEndpoint</span></span>
<span data-ttu-id="24e45-112">指定此 Cmdlet 啟動的端點。</span><span class="sxs-lookup"><span data-stu-id="24e45-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="24e45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e45-113">-DefaultProfile</span></span>
<span data-ttu-id="24e45-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="24e45-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24e45-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="24e45-115">-EndpointName</span></span>
<span data-ttu-id="24e45-116">指定此 Cmdlet 啟動之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="24e45-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="24e45-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24e45-117">-PassThru</span></span>
<span data-ttu-id="24e45-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="24e45-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="24e45-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="24e45-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="24e45-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="24e45-120">-ProfileName</span></span>
<span data-ttu-id="24e45-121">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="24e45-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="24e45-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e45-122">-ResourceGroupName</span></span>
<span data-ttu-id="24e45-123">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24e45-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="24e45-124">-確認</span><span class="sxs-lookup"><span data-stu-id="24e45-124">-Confirm</span></span>
<span data-ttu-id="24e45-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24e45-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e45-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e45-126">-WhatIf</span></span>
<span data-ttu-id="24e45-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24e45-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e45-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24e45-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e45-129">CommonParameters</span></span>
<span data-ttu-id="24e45-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24e45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e45-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24e45-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e45-132">輸入</span><span class="sxs-lookup"><span data-stu-id="24e45-132">INPUTS</span></span>

### <span data-ttu-id="24e45-133">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="24e45-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="24e45-134">參數： CdnEndpoint (ByValue) </span><span class="sxs-lookup"><span data-stu-id="24e45-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="24e45-135">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="24e45-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24e45-136">輸出</span><span class="sxs-lookup"><span data-stu-id="24e45-136">OUTPUTS</span></span>

### <span data-ttu-id="24e45-137">System.object</span><span class="sxs-lookup"><span data-stu-id="24e45-137">System.Boolean</span></span>

## <span data-ttu-id="24e45-138">筆記</span><span class="sxs-lookup"><span data-stu-id="24e45-138">NOTES</span></span>

## <span data-ttu-id="24e45-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="24e45-139">RELATED LINKS</span></span>

[<span data-ttu-id="24e45-140">AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e45-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="24e45-141">新-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e45-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="24e45-142">移除-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e45-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="24e45-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e45-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="24e45-144">停止 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="24e45-144">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)



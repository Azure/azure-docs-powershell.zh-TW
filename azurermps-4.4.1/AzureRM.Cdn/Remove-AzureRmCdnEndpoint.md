---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 49afefc7b80b5475735f61cb0511366b7f27a466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457660"
---
# <span data-ttu-id="e1bae-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1bae-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="e1bae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1bae-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bae-103">移除 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="e1bae-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1bae-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1bae-104">SYNTAX</span></span>

### <span data-ttu-id="e1bae-105">欄位參數的參數集</span><span class="sxs-lookup"><span data-stu-id="e1bae-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1bae-106">為物件參數設定參數</span><span class="sxs-lookup"><span data-stu-id="e1bae-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1bae-107">說明</span><span class="sxs-lookup"><span data-stu-id="e1bae-107">DESCRIPTION</span></span>
<span data-ttu-id="e1bae-108">**AzureRmCdnEndpoint** Cmdlet 會將 Azure 內容傳遞網路 (CDN) 端點中移除。</span><span class="sxs-lookup"><span data-stu-id="e1bae-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e1bae-109">示例</span><span class="sxs-lookup"><span data-stu-id="e1bae-109">EXAMPLES</span></span>

## <span data-ttu-id="e1bae-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1bae-110">PARAMETERS</span></span>

### <span data-ttu-id="e1bae-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1bae-111">-CdnEndpoint</span></span>
<span data-ttu-id="e1bae-112">指定此 Cmdlet 移除的端點。</span><span class="sxs-lookup"><span data-stu-id="e1bae-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bae-113">-終結點</span><span class="sxs-lookup"><span data-stu-id="e1bae-113">-EndpointName</span></span>
<span data-ttu-id="e1bae-114">指定此 Cmdlet 移除之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bae-114">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e1bae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e1bae-115">-Force</span></span>
<span data-ttu-id="e1bae-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e1bae-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1bae-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1bae-117">-PassThru</span></span>
<span data-ttu-id="e1bae-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e1bae-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1bae-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e1bae-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1bae-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e1bae-120">-ProfileName</span></span>
<span data-ttu-id="e1bae-121">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bae-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e1bae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bae-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1bae-123">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1bae-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e1bae-124">-確認</span><span class="sxs-lookup"><span data-stu-id="e1bae-124">-Confirm</span></span>
<span data-ttu-id="e1bae-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1bae-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1bae-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1bae-126">-WhatIf</span></span>
<span data-ttu-id="e1bae-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1bae-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1bae-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1bae-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1bae-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bae-129">-DefaultProfile</span></span>
<span data-ttu-id="e1bae-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1bae-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1bae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bae-131">CommonParameters</span></span>
<span data-ttu-id="e1bae-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1bae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bae-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1bae-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bae-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e1bae-134">INPUTS</span></span>

### <span data-ttu-id="e1bae-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1bae-135">PSEndpoint</span></span>
<span data-ttu-id="e1bae-136">形參 "CdnEndpoint" 接受管線中 "PSEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e1bae-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e1bae-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e1bae-137">OUTPUTS</span></span>

### <span data-ttu-id="e1bae-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e1bae-138">System.Boolean</span></span>

## <span data-ttu-id="e1bae-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e1bae-139">NOTES</span></span>

## <span data-ttu-id="e1bae-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1bae-140">RELATED LINKS</span></span>

[<span data-ttu-id="e1bae-141">AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1bae-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e1bae-142">新-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1bae-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e1bae-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1bae-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e1bae-144">開始-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1bae-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e1bae-145">停止 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e1bae-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)



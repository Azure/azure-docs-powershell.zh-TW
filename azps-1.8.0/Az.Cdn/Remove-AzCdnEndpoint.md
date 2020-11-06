---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 4dca00cf4b1746590591301657eb3ac0cbc7c17e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622847"
---
# <span data-ttu-id="067a7-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="067a7-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="067a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="067a7-102">SYNOPSIS</span></span>
<span data-ttu-id="067a7-103">移除 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="067a7-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="067a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="067a7-104">SYNTAX</span></span>

### <span data-ttu-id="067a7-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="067a7-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="067a7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="067a7-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="067a7-107">說明</span><span class="sxs-lookup"><span data-stu-id="067a7-107">DESCRIPTION</span></span>
<span data-ttu-id="067a7-108">**AzCdnEndpoint** Cmdlet 會將 Azure 內容傳遞網路 (CDN) 端點中移除。</span><span class="sxs-lookup"><span data-stu-id="067a7-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="067a7-109">示例</span><span class="sxs-lookup"><span data-stu-id="067a7-109">EXAMPLES</span></span>

## <span data-ttu-id="067a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="067a7-110">PARAMETERS</span></span>

### <span data-ttu-id="067a7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="067a7-111">-CdnEndpoint</span></span>
<span data-ttu-id="067a7-112">指定此 Cmdlet 移除的端點。</span><span class="sxs-lookup"><span data-stu-id="067a7-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="067a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="067a7-113">-DefaultProfile</span></span>
<span data-ttu-id="067a7-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="067a7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="067a7-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="067a7-115">-EndpointName</span></span>
<span data-ttu-id="067a7-116">指定此 Cmdlet 移除之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="067a7-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="067a7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="067a7-117">-Force</span></span>
<span data-ttu-id="067a7-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="067a7-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="067a7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="067a7-119">-PassThru</span></span>
<span data-ttu-id="067a7-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="067a7-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="067a7-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="067a7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="067a7-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="067a7-122">-ProfileName</span></span>
<span data-ttu-id="067a7-123">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="067a7-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="067a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="067a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="067a7-125">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="067a7-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="067a7-126">-確認</span><span class="sxs-lookup"><span data-stu-id="067a7-126">-Confirm</span></span>
<span data-ttu-id="067a7-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="067a7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="067a7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="067a7-128">-WhatIf</span></span>
<span data-ttu-id="067a7-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="067a7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="067a7-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="067a7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="067a7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="067a7-131">CommonParameters</span></span>
<span data-ttu-id="067a7-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="067a7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="067a7-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="067a7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="067a7-134">輸入</span><span class="sxs-lookup"><span data-stu-id="067a7-134">INPUTS</span></span>

### <span data-ttu-id="067a7-135">[PSEndpoint] 的 [Cdn] 命令</span><span class="sxs-lookup"><span data-stu-id="067a7-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="067a7-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="067a7-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="067a7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="067a7-137">OUTPUTS</span></span>

### <span data-ttu-id="067a7-138">System.object</span><span class="sxs-lookup"><span data-stu-id="067a7-138">System.Boolean</span></span>

## <span data-ttu-id="067a7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="067a7-139">NOTES</span></span>

## <span data-ttu-id="067a7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="067a7-140">RELATED LINKS</span></span>

[<span data-ttu-id="067a7-141">AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="067a7-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="067a7-142">新-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="067a7-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="067a7-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="067a7-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="067a7-144">開始-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="067a7-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="067a7-145">停止 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="067a7-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)



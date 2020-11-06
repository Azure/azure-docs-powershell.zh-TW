---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 8748806346baa4f84550d15749e7792ae928ad34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448773"
---
# <span data-ttu-id="1a560-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a560-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="1a560-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a560-102">SYNOPSIS</span></span>
<span data-ttu-id="1a560-103">移除 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="1a560-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a560-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a560-104">SYNTAX</span></span>

### <span data-ttu-id="1a560-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a560-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a560-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a560-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a560-107">說明</span><span class="sxs-lookup"><span data-stu-id="1a560-107">DESCRIPTION</span></span>
<span data-ttu-id="1a560-108">**AzureRmCdnEndpoint** Cmdlet 會將 Azure 內容傳遞網路 (CDN) 端點中移除。</span><span class="sxs-lookup"><span data-stu-id="1a560-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1a560-109">示例</span><span class="sxs-lookup"><span data-stu-id="1a560-109">EXAMPLES</span></span>

## <span data-ttu-id="1a560-110">參數</span><span class="sxs-lookup"><span data-stu-id="1a560-110">PARAMETERS</span></span>

### <span data-ttu-id="1a560-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a560-111">-CdnEndpoint</span></span>
<span data-ttu-id="1a560-112">指定此 Cmdlet 移除的端點。</span><span class="sxs-lookup"><span data-stu-id="1a560-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a560-113">-DefaultProfile</span></span>
<span data-ttu-id="1a560-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1a560-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="1a560-115">-EndpointName</span></span>
<span data-ttu-id="1a560-116">指定此 Cmdlet 移除之端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a560-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1a560-117">-Force</span></span>
<span data-ttu-id="1a560-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1a560-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a560-119">-PassThru</span></span>
<span data-ttu-id="1a560-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="1a560-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1a560-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1a560-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1a560-122">-ProfileName</span></span>
<span data-ttu-id="1a560-123">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="1a560-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a560-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a560-125">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a560-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-126">-確認</span><span class="sxs-lookup"><span data-stu-id="1a560-126">-Confirm</span></span>
<span data-ttu-id="1a560-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a560-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a560-128">-WhatIf</span></span>
<span data-ttu-id="1a560-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a560-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a560-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a560-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a560-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a560-131">CommonParameters</span></span>
<span data-ttu-id="1a560-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a560-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a560-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1a560-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a560-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1a560-134">INPUTS</span></span>

### <span data-ttu-id="1a560-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a560-135">PSEndpoint</span></span>
<span data-ttu-id="1a560-136">形參 "CdnEndpoint" 接受管線中 "PSEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1a560-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="1a560-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1a560-137">OUTPUTS</span></span>

### <span data-ttu-id="1a560-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1a560-138">System.Boolean</span></span>

## <span data-ttu-id="1a560-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1a560-139">NOTES</span></span>

## <span data-ttu-id="1a560-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a560-140">RELATED LINKS</span></span>

[<span data-ttu-id="1a560-141">AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a560-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="1a560-142">新-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a560-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="1a560-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a560-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="1a560-144">開始-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a560-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="1a560-145">停止 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a560-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)



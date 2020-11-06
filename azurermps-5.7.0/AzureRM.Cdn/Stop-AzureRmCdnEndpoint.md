---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 508465250489f2bcd0b031627258f11370fccfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446416"
---
# <span data-ttu-id="40e03-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="40e03-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="40e03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40e03-102">SYNOPSIS</span></span>
<span data-ttu-id="40e03-103">停止 CDN 端點。</span><span class="sxs-lookup"><span data-stu-id="40e03-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e03-104">句法</span><span class="sxs-lookup"><span data-stu-id="40e03-104">SYNTAX</span></span>

### <span data-ttu-id="40e03-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="40e03-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e03-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40e03-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e03-107">說明</span><span class="sxs-lookup"><span data-stu-id="40e03-107">DESCRIPTION</span></span>
<span data-ttu-id="40e03-108">**Stop-AzureRmCdnEndpoint** Cmdlet 會停止 Azure 內容傳遞網路 (CDN) 端點。</span><span class="sxs-lookup"><span data-stu-id="40e03-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="40e03-109">示例</span><span class="sxs-lookup"><span data-stu-id="40e03-109">EXAMPLES</span></span>

## <span data-ttu-id="40e03-110">參數</span><span class="sxs-lookup"><span data-stu-id="40e03-110">PARAMETERS</span></span>

### <span data-ttu-id="40e03-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="40e03-111">-CdnEndpoint</span></span>
<span data-ttu-id="40e03-112">指定此 Cmdlet 停止的端點物件。</span><span class="sxs-lookup"><span data-stu-id="40e03-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="40e03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e03-113">-DefaultProfile</span></span>
<span data-ttu-id="40e03-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="40e03-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40e03-115">-終結點</span><span class="sxs-lookup"><span data-stu-id="40e03-115">-EndpointName</span></span>
<span data-ttu-id="40e03-116">指定此 Cmdlet 停止的端點名稱。</span><span class="sxs-lookup"><span data-stu-id="40e03-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="40e03-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40e03-117">-PassThru</span></span>
<span data-ttu-id="40e03-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="40e03-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="40e03-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="40e03-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="40e03-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="40e03-120">-ProfileName</span></span>
<span data-ttu-id="40e03-121">指定端點所屬的設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="40e03-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="40e03-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e03-122">-ResourceGroupName</span></span>
<span data-ttu-id="40e03-123">指定端點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40e03-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="40e03-124">-確認</span><span class="sxs-lookup"><span data-stu-id="40e03-124">-Confirm</span></span>
<span data-ttu-id="40e03-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40e03-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e03-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e03-126">-WhatIf</span></span>
<span data-ttu-id="40e03-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40e03-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e03-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40e03-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e03-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e03-129">CommonParameters</span></span>
<span data-ttu-id="40e03-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40e03-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e03-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40e03-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e03-132">輸入</span><span class="sxs-lookup"><span data-stu-id="40e03-132">INPUTS</span></span>

### <span data-ttu-id="40e03-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="40e03-133">PSEndpoint</span></span>
<span data-ttu-id="40e03-134">形參 "CdnEndpoint" 接受管線中 "PSEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="40e03-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="40e03-135">輸出</span><span class="sxs-lookup"><span data-stu-id="40e03-135">OUTPUTS</span></span>

### <span data-ttu-id="40e03-136">System.object</span><span class="sxs-lookup"><span data-stu-id="40e03-136">System.Boolean</span></span>

## <span data-ttu-id="40e03-137">筆記</span><span class="sxs-lookup"><span data-stu-id="40e03-137">NOTES</span></span>

## <span data-ttu-id="40e03-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="40e03-138">RELATED LINKS</span></span>

[<span data-ttu-id="40e03-139">AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="40e03-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="40e03-140">新-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="40e03-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="40e03-141">移除-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="40e03-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="40e03-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="40e03-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="40e03-143">開始-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="40e03-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)



---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/switch-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Switch-AzureRmWebAppSlot.md
ms.openlocfilehash: e1cfb3e70ab8176cfd686dc404b13dbbfb23e4e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445888"
---
# <span data-ttu-id="41b1e-101">Switch-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41b1e-101">Switch-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="41b1e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="41b1e-103">使用 Web 應用程式交換兩個槽</span><span class="sxs-lookup"><span data-stu-id="41b1e-103">Swap two slots with a Web App</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41b1e-104">句法</span><span class="sxs-lookup"><span data-stu-id="41b1e-104">SYNTAX</span></span>

### <span data-ttu-id="41b1e-105">S1</span><span class="sxs-lookup"><span data-stu-id="41b1e-105">S1</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41b1e-106">S2</span><span class="sxs-lookup"><span data-stu-id="41b1e-106">S2</span></span>
```
Switch-AzureRmWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41b1e-107">說明</span><span class="sxs-lookup"><span data-stu-id="41b1e-107">DESCRIPTION</span></span>
<span data-ttu-id="41b1e-108">**AzureRmWebAppSlot** 會切換與 Azure Web App 相關聯的兩個槽。</span><span class="sxs-lookup"><span data-stu-id="41b1e-108">The **Switch-AzureRmWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="41b1e-109">示例</span><span class="sxs-lookup"><span data-stu-id="41b1e-109">EXAMPLES</span></span>

### <span data-ttu-id="41b1e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="41b1e-110">Example 1</span></span>
```
PS C:\> Switch-AzureRmWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="41b1e-111">這個命令會將 [sourceslot] 槽切換成與資源群組 [預設-WestUS] 相關聯的 Web App ContosoWebApp 的 "destinationslot"</span><span class="sxs-lookup"><span data-stu-id="41b1e-111">This command will switch slot "sourceslot" slot with "destinationslot" for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="41b1e-112">參數</span><span class="sxs-lookup"><span data-stu-id="41b1e-112">PARAMETERS</span></span>

### <span data-ttu-id="41b1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b1e-113">-DefaultProfile</span></span>
<span data-ttu-id="41b1e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41b1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b1e-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="41b1e-115">-DestinationSlotName</span></span>
<span data-ttu-id="41b1e-116">目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="41b1e-116">Destination Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="41b1e-117">-Name</span></span>
<span data-ttu-id="41b1e-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="41b1e-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="41b1e-119">-PreserveVnet</span></span>
<span data-ttu-id="41b1e-120">保留 Vnet 布林值</span><span class="sxs-lookup"><span data-stu-id="41b1e-120">Preserve Vnet Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="41b1e-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="41b1e-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="41b1e-123">-SourceSlotName</span></span>
<span data-ttu-id="41b1e-124">來源槽名稱</span><span class="sxs-lookup"><span data-stu-id="41b1e-124">Source Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="41b1e-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="41b1e-126">使用預覽動作進行交換</span><span class="sxs-lookup"><span data-stu-id="41b1e-126">Swap With Preview Action</span></span>

```yaml
Type: SwapWithPreviewAction
Parameter Sets: (All)
Aliases: 
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="41b1e-127">-WebApp</span></span>
<span data-ttu-id="41b1e-128">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="41b1e-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="41b1e-129">-Confirm</span></span>
<span data-ttu-id="41b1e-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41b1e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b1e-131">-WhatIf</span></span>
<span data-ttu-id="41b1e-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41b1e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41b1e-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41b1e-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b1e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b1e-134">CommonParameters</span></span>
<span data-ttu-id="41b1e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41b1e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b1e-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41b1e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b1e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="41b1e-137">INPUTS</span></span>

### <span data-ttu-id="41b1e-138">網站地圖</span><span class="sxs-lookup"><span data-stu-id="41b1e-138">Site</span></span>
<span data-ttu-id="41b1e-139">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="41b1e-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="41b1e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="41b1e-140">OUTPUTS</span></span>

## <span data-ttu-id="41b1e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="41b1e-141">NOTES</span></span>

## <span data-ttu-id="41b1e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="41b1e-142">RELATED LINKS</span></span>


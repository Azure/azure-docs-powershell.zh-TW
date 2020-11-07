---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/switch-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: e30179ce2e9198729771d406d1963ff0048e05b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794925"
---
# <span data-ttu-id="78ac4-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="78ac4-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="78ac4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="78ac4-103">使用 Web 應用程式交換兩個槽</span><span class="sxs-lookup"><span data-stu-id="78ac4-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="78ac4-104">句法</span><span class="sxs-lookup"><span data-stu-id="78ac4-104">SYNTAX</span></span>

### <span data-ttu-id="78ac4-105">S1</span><span class="sxs-lookup"><span data-stu-id="78ac4-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78ac4-106">S2</span><span class="sxs-lookup"><span data-stu-id="78ac4-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78ac4-107">說明</span><span class="sxs-lookup"><span data-stu-id="78ac4-107">DESCRIPTION</span></span>
<span data-ttu-id="78ac4-108">**AzWebAppSlot** 會切換與 Azure Web App 相關聯的兩個槽。</span><span class="sxs-lookup"><span data-stu-id="78ac4-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="78ac4-109">示例</span><span class="sxs-lookup"><span data-stu-id="78ac4-109">EXAMPLES</span></span>

### <span data-ttu-id="78ac4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="78ac4-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="78ac4-111">這個命令會針對與資源群組預設-WestUS 相關的 Web App ContosoWebApp，將 [sourceslot] 槽切換為 [destinationslot]。</span><span class="sxs-lookup"><span data-stu-id="78ac4-111">This command will switch slot "sourceslot" slot with "destinationslot" for for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="78ac4-112">參數</span><span class="sxs-lookup"><span data-stu-id="78ac4-112">PARAMETERS</span></span>

### <span data-ttu-id="78ac4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78ac4-113">-DefaultProfile</span></span>
<span data-ttu-id="78ac4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78ac4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78ac4-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="78ac4-115">-DestinationSlotName</span></span>
<span data-ttu-id="78ac4-116">目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="78ac4-116">Destination Slot Name</span></span>

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

### <span data-ttu-id="78ac4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="78ac4-117">-Name</span></span>
<span data-ttu-id="78ac4-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="78ac4-118">WebApp Name</span></span>

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

### <span data-ttu-id="78ac4-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="78ac4-119">-PreserveVnet</span></span>
<span data-ttu-id="78ac4-120">保留 Vnet 布林值</span><span class="sxs-lookup"><span data-stu-id="78ac4-120">Preserve Vnet Boolean</span></span>

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

### <span data-ttu-id="78ac4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78ac4-121">-ResourceGroupName</span></span>
<span data-ttu-id="78ac4-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="78ac4-122">Resource Group Name</span></span>

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

### <span data-ttu-id="78ac4-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="78ac4-123">-SourceSlotName</span></span>
<span data-ttu-id="78ac4-124">來源槽名稱</span><span class="sxs-lookup"><span data-stu-id="78ac4-124">Source Slot Name</span></span>

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

### <span data-ttu-id="78ac4-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="78ac4-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="78ac4-126">使用預覽動作進行交換</span><span class="sxs-lookup"><span data-stu-id="78ac4-126">Swap With Preview Action</span></span>

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

### <span data-ttu-id="78ac4-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="78ac4-127">-WebApp</span></span>
<span data-ttu-id="78ac4-128">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="78ac4-128">WebApp Object</span></span>

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

### <span data-ttu-id="78ac4-129">-確認</span><span class="sxs-lookup"><span data-stu-id="78ac4-129">-Confirm</span></span>
<span data-ttu-id="78ac4-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78ac4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78ac4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78ac4-131">-WhatIf</span></span>
<span data-ttu-id="78ac4-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78ac4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78ac4-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78ac4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78ac4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78ac4-134">CommonParameters</span></span>
<span data-ttu-id="78ac4-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78ac4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78ac4-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78ac4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78ac4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="78ac4-137">INPUTS</span></span>

### <span data-ttu-id="78ac4-138">網站地圖</span><span class="sxs-lookup"><span data-stu-id="78ac4-138">Site</span></span>
<span data-ttu-id="78ac4-139">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="78ac4-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="78ac4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="78ac4-140">OUTPUTS</span></span>

## <span data-ttu-id="78ac4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="78ac4-141">NOTES</span></span>

## <span data-ttu-id="78ac4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="78ac4-142">RELATED LINKS</span></span>


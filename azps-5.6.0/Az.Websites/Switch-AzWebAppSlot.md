---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 258A4EA9-B82C-4664-8DCE-30D47A623868
online version: https://docs.microsoft.com/powershell/module/az.websites/switch-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Switch-AzWebAppSlot.md
ms.openlocfilehash: 7cb74e6eec27df299206ee62264588a37dee3a2b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916800"
---
# <span data-ttu-id="143bf-101">Switch-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="143bf-101">Switch-AzWebAppSlot</span></span>

## <span data-ttu-id="143bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="143bf-102">SYNOPSIS</span></span>
<span data-ttu-id="143bf-103">使用 Web App 交換兩個插槽</span><span class="sxs-lookup"><span data-stu-id="143bf-103">Swap two slots with a Web App</span></span>

## <span data-ttu-id="143bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="143bf-104">SYNTAX</span></span>

### <span data-ttu-id="143bf-105">S1</span><span class="sxs-lookup"><span data-stu-id="143bf-105">S1</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="143bf-106">S2</span><span class="sxs-lookup"><span data-stu-id="143bf-106">S2</span></span>
```
Switch-AzWebAppSlot [-SourceSlotName] <String> [[-DestinationSlotName] <String>]
 [[-SwapWithPreviewAction] <SwapWithPreviewAction>] [[-PreserveVnet] <Boolean>] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="143bf-107">描述</span><span class="sxs-lookup"><span data-stu-id="143bf-107">DESCRIPTION</span></span>
<span data-ttu-id="143bf-108">**Switch-AzWebAppSlot** 會切換與 Azure Web App 相關聯的兩個插槽。</span><span class="sxs-lookup"><span data-stu-id="143bf-108">The **Switch-AzWebAppSlot** switches two slots associated with an Azure Web App.</span></span>

## <span data-ttu-id="143bf-109">例子</span><span class="sxs-lookup"><span data-stu-id="143bf-109">EXAMPLES</span></span>

### <span data-ttu-id="143bf-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="143bf-110">Example 1</span></span>
```
PS C:\> Switch-AzWebAppSlot -SourceSlotName "sourceslot" -DestinationSlotName "destinationslot" -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="143bf-111">此命令會切換與「destinationslot」相關聯的 Web App ContosoWebApp 與資源群組 Default-Web-WestUS 的插槽"sourceslot"插槽</span><span class="sxs-lookup"><span data-stu-id="143bf-111">This command will switch slot "sourceslot" slot with "destinationslot" the Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="143bf-112">參數</span><span class="sxs-lookup"><span data-stu-id="143bf-112">PARAMETERS</span></span>

### <span data-ttu-id="143bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="143bf-113">-DefaultProfile</span></span>
<span data-ttu-id="143bf-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="143bf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="143bf-115">-DestinationSlotName</span><span class="sxs-lookup"><span data-stu-id="143bf-115">-DestinationSlotName</span></span>
<span data-ttu-id="143bf-116">目的地插槽名稱</span><span class="sxs-lookup"><span data-stu-id="143bf-116">Destination Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="143bf-117">-Name</span></span>
<span data-ttu-id="143bf-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="143bf-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-119">-PreserveVnet</span><span class="sxs-lookup"><span data-stu-id="143bf-119">-PreserveVnet</span></span>
<span data-ttu-id="143bf-120">保留 Vnet 布林值</span><span class="sxs-lookup"><span data-stu-id="143bf-120">Preserve Vnet Boolean</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="143bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="143bf-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="143bf-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-123">-SourceSlotName</span><span class="sxs-lookup"><span data-stu-id="143bf-123">-SourceSlotName</span></span>
<span data-ttu-id="143bf-124">來源插槽名稱</span><span class="sxs-lookup"><span data-stu-id="143bf-124">Source Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-125">-SwapWithPreviewAction</span><span class="sxs-lookup"><span data-stu-id="143bf-125">-SwapWithPreviewAction</span></span>
<span data-ttu-id="143bf-126">使用預覽動作交換</span><span class="sxs-lookup"><span data-stu-id="143bf-126">Swap With Preview Action</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.WebApps.Utilities.SwapWithPreviewAction]
Parameter Sets: (All)
Aliases:
Accepted values: ApplySlotConfig, CompleteSlotSwap, ResetSlotSwap

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="143bf-127">-WebApp</span></span>
<span data-ttu-id="143bf-128">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="143bf-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-129">-確認</span><span class="sxs-lookup"><span data-stu-id="143bf-129">-Confirm</span></span>
<span data-ttu-id="143bf-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="143bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="143bf-131">-WhatIf</span></span>
<span data-ttu-id="143bf-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="143bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="143bf-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="143bf-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143bf-134">CommonParameters</span></span>
<span data-ttu-id="143bf-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="143bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143bf-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="143bf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143bf-137">輸入</span><span class="sxs-lookup"><span data-stu-id="143bf-137">INPUTS</span></span>

### <span data-ttu-id="143bf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="143bf-138">System.String</span></span>

### <span data-ttu-id="143bf-139">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="143bf-139">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="143bf-140">輸出</span><span class="sxs-lookup"><span data-stu-id="143bf-140">OUTPUTS</span></span>

### <span data-ttu-id="143bf-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="143bf-141">System.Void</span></span>

## <span data-ttu-id="143bf-142">筆記</span><span class="sxs-lookup"><span data-stu-id="143bf-142">NOTES</span></span>

## <span data-ttu-id="143bf-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="143bf-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b7b1cc38402e69b5783f76ec35445aae7b6944dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612407"
---
# <span data-ttu-id="e51f1-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e51f1-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="e51f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e51f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e51f1-103">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="e51f1-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="e51f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e51f1-104">SYNTAX</span></span>

### <span data-ttu-id="e51f1-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e51f1-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e51f1-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e51f1-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e51f1-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e51f1-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e51f1-108">說明</span><span class="sxs-lookup"><span data-stu-id="e51f1-108">DESCRIPTION</span></span>
<span data-ttu-id="e51f1-109">**AzEventHubGeoDRConfiguration** Cmdlet 會刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="e51f1-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="e51f1-110">示例</span><span class="sxs-lookup"><span data-stu-id="e51f1-110">EXAMPLES</span></span>

### <span data-ttu-id="e51f1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e51f1-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="e51f1-112">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="e51f1-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="e51f1-113">參數</span><span class="sxs-lookup"><span data-stu-id="e51f1-113">PARAMETERS</span></span>

### <span data-ttu-id="e51f1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e51f1-114">-AsJob</span></span>
<span data-ttu-id="e51f1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e51f1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e51f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51f1-116">-DefaultProfile</span></span>
<span data-ttu-id="e51f1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e51f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51f1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e51f1-118">-InputObject</span></span>
<span data-ttu-id="e51f1-119">Eventhub GeoDR Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="e51f1-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e51f1-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e51f1-120">-Name</span></span>
<span data-ttu-id="e51f1-121">別名 (GeoDR) </span><span class="sxs-lookup"><span data-stu-id="e51f1-121">Alias (GeoDR)</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51f1-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e51f1-122">-Namespace</span></span>
<span data-ttu-id="e51f1-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="e51f1-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51f1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e51f1-124">-PassThru</span></span>
<span data-ttu-id="e51f1-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e51f1-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e51f1-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e51f1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e51f1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e51f1-127">-ResourceGroupName</span></span>
<span data-ttu-id="e51f1-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e51f1-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51f1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e51f1-129">-ResourceId</span></span>
<span data-ttu-id="e51f1-130">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e51f1-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51f1-131">-確認</span><span class="sxs-lookup"><span data-stu-id="e51f1-131">-Confirm</span></span>
<span data-ttu-id="e51f1-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e51f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e51f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e51f1-133">-WhatIf</span></span>
<span data-ttu-id="e51f1-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e51f1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e51f1-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e51f1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e51f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51f1-136">CommonParameters</span></span>
<span data-ttu-id="e51f1-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e51f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51f1-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e51f1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51f1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e51f1-139">INPUTS</span></span>

### <span data-ttu-id="e51f1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e51f1-140">System.String</span></span>

### <span data-ttu-id="e51f1-141">PSEventHubDRConfigurationAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="e51f1-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="e51f1-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e51f1-142">OUTPUTS</span></span>

### <span data-ttu-id="e51f1-143">System.object</span><span class="sxs-lookup"><span data-stu-id="e51f1-143">System.Boolean</span></span>

## <span data-ttu-id="e51f1-144">筆記</span><span class="sxs-lookup"><span data-stu-id="e51f1-144">NOTES</span></span>

## <span data-ttu-id="e51f1-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="e51f1-145">RELATED LINKS</span></span>

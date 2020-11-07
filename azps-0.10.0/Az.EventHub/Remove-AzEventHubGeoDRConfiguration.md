---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 5bdc6e29ad55efd774f267af10b0f0652e513e43
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794751"
---
# <span data-ttu-id="7536f-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="7536f-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="7536f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7536f-102">SYNOPSIS</span></span>
<span data-ttu-id="7536f-103">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="7536f-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="7536f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7536f-104">SYNTAX</span></span>

### <span data-ttu-id="7536f-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7536f-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7536f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7536f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7536f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7536f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7536f-108">說明</span><span class="sxs-lookup"><span data-stu-id="7536f-108">DESCRIPTION</span></span>
<span data-ttu-id="7536f-109">**AzEventHubGeoDRConfiguration** Cmdlet 會刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="7536f-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="7536f-110">示例</span><span class="sxs-lookup"><span data-stu-id="7536f-110">EXAMPLES</span></span>

### <span data-ttu-id="7536f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7536f-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="7536f-112">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="7536f-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="7536f-113">參數</span><span class="sxs-lookup"><span data-stu-id="7536f-113">PARAMETERS</span></span>

### <span data-ttu-id="7536f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7536f-114">-AsJob</span></span>
<span data-ttu-id="7536f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7536f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7536f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7536f-116">-DefaultProfile</span></span>
<span data-ttu-id="7536f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7536f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7536f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7536f-118">-InputObject</span></span>
<span data-ttu-id="7536f-119">Eventhub GeoDR Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="7536f-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="7536f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7536f-120">-Name</span></span>
<span data-ttu-id="7536f-121">別名 (GeoDR) </span><span class="sxs-lookup"><span data-stu-id="7536f-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="7536f-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="7536f-122">-Namespace</span></span>
<span data-ttu-id="7536f-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="7536f-123">Namespace Name</span></span>

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

### <span data-ttu-id="7536f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7536f-124">-PassThru</span></span>
<span data-ttu-id="7536f-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7536f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7536f-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7536f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7536f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7536f-127">-ResourceGroupName</span></span>
<span data-ttu-id="7536f-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="7536f-128">Resource Group Name</span></span>

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

### <span data-ttu-id="7536f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7536f-129">-ResourceId</span></span>
<span data-ttu-id="7536f-130">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7536f-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="7536f-131">-確認</span><span class="sxs-lookup"><span data-stu-id="7536f-131">-Confirm</span></span>
<span data-ttu-id="7536f-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7536f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7536f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7536f-133">-WhatIf</span></span>
<span data-ttu-id="7536f-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7536f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7536f-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7536f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7536f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7536f-136">CommonParameters</span></span>
<span data-ttu-id="7536f-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7536f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7536f-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7536f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7536f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="7536f-139">INPUTS</span></span>

### <span data-ttu-id="7536f-140">System.object</span><span class="sxs-lookup"><span data-stu-id="7536f-140">System.String</span></span>

### <span data-ttu-id="7536f-141">PSEventHubDRConfigurationAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="7536f-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="7536f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="7536f-142">OUTPUTS</span></span>

### <span data-ttu-id="7536f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="7536f-143">System.Boolean</span></span>

## <span data-ttu-id="7536f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="7536f-144">NOTES</span></span>

## <span data-ttu-id="7536f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="7536f-145">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c4c23b877ae42703ade4b163c8c09d9156725e77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620619"
---
# <span data-ttu-id="43da4-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="43da4-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="43da4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43da4-102">SYNOPSIS</span></span>
<span data-ttu-id="43da4-103">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="43da4-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="43da4-104">句法</span><span class="sxs-lookup"><span data-stu-id="43da4-104">SYNTAX</span></span>

### <span data-ttu-id="43da4-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="43da4-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43da4-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43da4-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43da4-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43da4-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43da4-108">說明</span><span class="sxs-lookup"><span data-stu-id="43da4-108">DESCRIPTION</span></span>
<span data-ttu-id="43da4-109">**AzServiceBusGeoDRConfiguration** Cmdlet 會刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="43da4-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="43da4-110">示例</span><span class="sxs-lookup"><span data-stu-id="43da4-110">EXAMPLES</span></span>

### <span data-ttu-id="43da4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="43da4-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="43da4-112">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="43da4-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="43da4-113">參數</span><span class="sxs-lookup"><span data-stu-id="43da4-113">PARAMETERS</span></span>

### <span data-ttu-id="43da4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43da4-114">-AsJob</span></span>
<span data-ttu-id="43da4-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="43da4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43da4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43da4-116">-DefaultProfile</span></span>
<span data-ttu-id="43da4-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43da4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43da4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43da4-118">-InputObject</span></span>
<span data-ttu-id="43da4-119">服務匯流排 GeoDR 設定物件</span><span class="sxs-lookup"><span data-stu-id="43da4-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43da4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="43da4-120">-Name</span></span>
<span data-ttu-id="43da4-121">別名 (GeoDR) 名稱</span><span class="sxs-lookup"><span data-stu-id="43da4-121">Alias (GeoDR) Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43da4-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="43da4-122">-Namespace</span></span>
<span data-ttu-id="43da4-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="43da4-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43da4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43da4-124">-PassThru</span></span>
<span data-ttu-id="43da4-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="43da4-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43da4-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="43da4-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43da4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43da4-127">-ResourceGroupName</span></span>
<span data-ttu-id="43da4-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="43da4-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43da4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43da4-129">-ResourceId</span></span>
<span data-ttu-id="43da4-130">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="43da4-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="43da4-131">-確認</span><span class="sxs-lookup"><span data-stu-id="43da4-131">-Confirm</span></span>
<span data-ttu-id="43da4-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43da4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43da4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43da4-133">-WhatIf</span></span>
<span data-ttu-id="43da4-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43da4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43da4-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43da4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43da4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43da4-136">CommonParameters</span></span>
<span data-ttu-id="43da4-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43da4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43da4-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43da4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43da4-139">輸入</span><span class="sxs-lookup"><span data-stu-id="43da4-139">INPUTS</span></span>

### <span data-ttu-id="43da4-140">System.object</span><span class="sxs-lookup"><span data-stu-id="43da4-140">System.String</span></span>

### <span data-ttu-id="43da4-141">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43da4-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="43da4-142">輸出</span><span class="sxs-lookup"><span data-stu-id="43da4-142">OUTPUTS</span></span>

### <span data-ttu-id="43da4-143">System.object</span><span class="sxs-lookup"><span data-stu-id="43da4-143">System.Boolean</span></span>

## <span data-ttu-id="43da4-144">筆記</span><span class="sxs-lookup"><span data-stu-id="43da4-144">NOTES</span></span>

## <span data-ttu-id="43da4-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="43da4-145">RELATED LINKS</span></span>

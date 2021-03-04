---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 3fa1dd4c3f926e0c6011d8ffec3a510340a7eab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914385"
---
# <span data-ttu-id="5ce40-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ce40-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="5ce40-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ce40-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce40-103">刪除復原 (的別名) </span><span class="sxs-lookup"><span data-stu-id="5ce40-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5ce40-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ce40-104">SYNTAX</span></span>

### <span data-ttu-id="5ce40-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5ce40-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce40-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5ce40-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce40-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ce40-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce40-108">描述</span><span class="sxs-lookup"><span data-stu-id="5ce40-108">DESCRIPTION</span></span>
<span data-ttu-id="5ce40-109">**Remove-AzServiceBusGeoDRConfiguration Cmdlet** 會刪除 (復原組) </span><span class="sxs-lookup"><span data-stu-id="5ce40-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5ce40-110">例子</span><span class="sxs-lookup"><span data-stu-id="5ce40-110">EXAMPLES</span></span>

### <span data-ttu-id="5ce40-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="5ce40-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="5ce40-112">刪除復原 (的別名) </span><span class="sxs-lookup"><span data-stu-id="5ce40-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5ce40-113">參數</span><span class="sxs-lookup"><span data-stu-id="5ce40-113">PARAMETERS</span></span>

### <span data-ttu-id="5ce40-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ce40-114">-AsJob</span></span>
<span data-ttu-id="5ce40-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ce40-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ce40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce40-116">-DefaultProfile</span></span>
<span data-ttu-id="5ce40-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ce40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce40-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce40-118">-InputObject</span></span>
<span data-ttu-id="5ce40-119">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="5ce40-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="5ce40-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ce40-120">-Name</span></span>
<span data-ttu-id="5ce40-121">GeoDR (別名) 名稱</span><span class="sxs-lookup"><span data-stu-id="5ce40-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="5ce40-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="5ce40-122">-Namespace</span></span>
<span data-ttu-id="5ce40-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="5ce40-123">Namespace Name</span></span>

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

### <span data-ttu-id="5ce40-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ce40-124">-PassThru</span></span>
<span data-ttu-id="5ce40-125">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5ce40-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ce40-126">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5ce40-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ce40-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce40-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ce40-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="5ce40-128">Resource Group Name</span></span>

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

### <span data-ttu-id="5ce40-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ce40-129">-ResourceId</span></span>
<span data-ttu-id="5ce40-130">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5ce40-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="5ce40-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5ce40-131">-Confirm</span></span>
<span data-ttu-id="5ce40-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5ce40-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce40-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce40-133">-WhatIf</span></span>
<span data-ttu-id="5ce40-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ce40-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce40-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ce40-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce40-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce40-136">CommonParameters</span></span>
<span data-ttu-id="5ce40-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ce40-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce40-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5ce40-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce40-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5ce40-139">INPUTS</span></span>

### <span data-ttu-id="5ce40-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5ce40-140">System.String</span></span>

### <span data-ttu-id="5ce40-141">Microsoft.Azure.Commands.ServiceBus.models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5ce40-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="5ce40-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5ce40-142">OUTPUTS</span></span>

### <span data-ttu-id="5ce40-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ce40-143">System.Boolean</span></span>

## <span data-ttu-id="5ce40-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5ce40-144">NOTES</span></span>

## <span data-ttu-id="5ce40-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ce40-145">RELATED LINKS</span></span>

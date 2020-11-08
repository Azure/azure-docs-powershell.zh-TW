---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128098"
---
# <span data-ttu-id="f2b25-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2b25-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="f2b25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2b25-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b25-103">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="f2b25-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f2b25-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2b25-104">SYNTAX</span></span>

### <span data-ttu-id="f2b25-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f2b25-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2b25-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f2b25-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2b25-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2b25-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b25-108">說明</span><span class="sxs-lookup"><span data-stu-id="f2b25-108">DESCRIPTION</span></span>
<span data-ttu-id="f2b25-109">**AzServiceBusGeoDRConfiguration** Cmdlet 會刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="f2b25-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f2b25-110">示例</span><span class="sxs-lookup"><span data-stu-id="f2b25-110">EXAMPLES</span></span>

### <span data-ttu-id="f2b25-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f2b25-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="f2b25-112">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="f2b25-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f2b25-113">參數</span><span class="sxs-lookup"><span data-stu-id="f2b25-113">PARAMETERS</span></span>

### <span data-ttu-id="f2b25-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2b25-114">-AsJob</span></span>
<span data-ttu-id="f2b25-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f2b25-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2b25-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b25-116">-DefaultProfile</span></span>
<span data-ttu-id="f2b25-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2b25-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2b25-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2b25-118">-InputObject</span></span>
<span data-ttu-id="f2b25-119">服務匯流排 GeoDR 設定物件</span><span class="sxs-lookup"><span data-stu-id="f2b25-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="f2b25-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2b25-120">-Name</span></span>
<span data-ttu-id="f2b25-121">別名 (GeoDR) 名稱</span><span class="sxs-lookup"><span data-stu-id="f2b25-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="f2b25-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f2b25-122">-Namespace</span></span>
<span data-ttu-id="f2b25-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f2b25-123">Namespace Name</span></span>

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

### <span data-ttu-id="f2b25-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2b25-124">-PassThru</span></span>
<span data-ttu-id="f2b25-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f2b25-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f2b25-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f2b25-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f2b25-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b25-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2b25-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f2b25-128">Resource Group Name</span></span>

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

### <span data-ttu-id="f2b25-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2b25-129">-ResourceId</span></span>
<span data-ttu-id="f2b25-130">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f2b25-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="f2b25-131">-確認</span><span class="sxs-lookup"><span data-stu-id="f2b25-131">-Confirm</span></span>
<span data-ttu-id="f2b25-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f2b25-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b25-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b25-133">-WhatIf</span></span>
<span data-ttu-id="f2b25-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2b25-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b25-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2b25-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b25-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b25-136">CommonParameters</span></span>
<span data-ttu-id="f2b25-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2b25-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b25-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2b25-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b25-139">輸入</span><span class="sxs-lookup"><span data-stu-id="f2b25-139">INPUTS</span></span>

### <span data-ttu-id="f2b25-140">System.object</span><span class="sxs-lookup"><span data-stu-id="f2b25-140">System.String</span></span>

### <span data-ttu-id="f2b25-141">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2b25-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f2b25-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f2b25-142">OUTPUTS</span></span>

### <span data-ttu-id="f2b25-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f2b25-143">System.Boolean</span></span>

## <span data-ttu-id="f2b25-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f2b25-144">NOTES</span></span>

## <span data-ttu-id="f2b25-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2b25-145">RELATED LINKS</span></span>

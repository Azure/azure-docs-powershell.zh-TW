---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 9c5fe091e5e218c4e70ef1486f1211bc0be7894b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450487"
---
# <span data-ttu-id="107b6-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="107b6-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="107b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="107b6-102">SYNOPSIS</span></span>
<span data-ttu-id="107b6-103">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="107b6-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="107b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="107b6-104">SYNTAX</span></span>

### <span data-ttu-id="107b6-105">GeoDRBreakPairFailOverPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="107b6-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107b6-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="107b6-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="107b6-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="107b6-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="107b6-108">說明</span><span class="sxs-lookup"><span data-stu-id="107b6-108">DESCRIPTION</span></span>
<span data-ttu-id="107b6-109">**AzureRmServiceBusGeoDRConfiguration** Cmdlet 會刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="107b6-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="107b6-110">示例</span><span class="sxs-lookup"><span data-stu-id="107b6-110">EXAMPLES</span></span>

### <span data-ttu-id="107b6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="107b6-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="107b6-112">刪除 (災害復原設定的別名) </span><span class="sxs-lookup"><span data-stu-id="107b6-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="107b6-113">參數</span><span class="sxs-lookup"><span data-stu-id="107b6-113">PARAMETERS</span></span>

### <span data-ttu-id="107b6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="107b6-114">-AsJob</span></span>
<span data-ttu-id="107b6-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="107b6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="107b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107b6-116">-DefaultProfile</span></span>
<span data-ttu-id="107b6-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="107b6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="107b6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="107b6-118">-InputObject</span></span>
<span data-ttu-id="107b6-119">服務匯流排 GeoDR 設定物件</span><span class="sxs-lookup"><span data-stu-id="107b6-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="107b6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="107b6-120">-Name</span></span>
<span data-ttu-id="107b6-121">別名 (GeoDR) 名稱</span><span class="sxs-lookup"><span data-stu-id="107b6-121">Alias (GeoDR) Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107b6-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="107b6-122">-Namespace</span></span>
<span data-ttu-id="107b6-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="107b6-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107b6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="107b6-124">-PassThru</span></span>
<span data-ttu-id="107b6-125">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="107b6-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="107b6-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="107b6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="107b6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107b6-127">-ResourceGroupName</span></span>
<span data-ttu-id="107b6-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="107b6-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107b6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="107b6-129">-ResourceId</span></span>
<span data-ttu-id="107b6-130">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="107b6-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107b6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="107b6-131">-Confirm</span></span>
<span data-ttu-id="107b6-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="107b6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="107b6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="107b6-133">-WhatIf</span></span>
<span data-ttu-id="107b6-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="107b6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="107b6-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="107b6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="107b6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107b6-136">CommonParameters</span></span>
<span data-ttu-id="107b6-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="107b6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="107b6-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="107b6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107b6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="107b6-139">INPUTS</span></span>

### <span data-ttu-id="107b6-140">System.object</span><span class="sxs-lookup"><span data-stu-id="107b6-140">System.String</span></span>
<span data-ttu-id="107b6-141">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="107b6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="107b6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="107b6-142">OUTPUTS</span></span>

### <span data-ttu-id="107b6-143">System.object</span><span class="sxs-lookup"><span data-stu-id="107b6-143">System.Boolean</span></span>


## <span data-ttu-id="107b6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="107b6-144">NOTES</span></span>

## <span data-ttu-id="107b6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="107b6-145">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 1a6fc5bca4c31afe08591190c111649495555cde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450483"
---
# <span data-ttu-id="80f29-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="80f29-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="80f29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80f29-102">SYNOPSIS</span></span>
<span data-ttu-id="80f29-103">調用 GEO DR 容錯移轉，並重新設定別名以指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="80f29-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80f29-104">句法</span><span class="sxs-lookup"><span data-stu-id="80f29-104">SYNTAX</span></span>

### <span data-ttu-id="80f29-105">GeoDRBreakPairFailOverPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="80f29-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80f29-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="80f29-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80f29-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80f29-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80f29-108">說明</span><span class="sxs-lookup"><span data-stu-id="80f29-108">DESCRIPTION</span></span>
<span data-ttu-id="80f29-109">**AzureRmServiceBusGeoDRConfigurationFailOver** CMDLET ENVOKES GEO DR 容錯移轉，並將別名重新設定為指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="80f29-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="80f29-110">示例</span><span class="sxs-lookup"><span data-stu-id="80f29-110">EXAMPLES</span></span>

### <span data-ttu-id="80f29-111">範例1</span><span class="sxs-lookup"><span data-stu-id="80f29-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="80f29-112">針對別名 "SampleDRCongifName" 調用容錯移轉，重新配置並指向次要命名空間 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="80f29-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="80f29-113">參數</span><span class="sxs-lookup"><span data-stu-id="80f29-113">PARAMETERS</span></span>

### <span data-ttu-id="80f29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f29-114">-DefaultProfile</span></span>
<span data-ttu-id="80f29-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80f29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80f29-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80f29-116">-InputObject</span></span>
<span data-ttu-id="80f29-117">服務匯流排 GeoDR 設定物件</span><span class="sxs-lookup"><span data-stu-id="80f29-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="80f29-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="80f29-118">-Name</span></span>
<span data-ttu-id="80f29-119">DR 配置名稱-別名</span><span class="sxs-lookup"><span data-stu-id="80f29-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="80f29-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="80f29-120">-Namespace</span></span>
<span data-ttu-id="80f29-121">命名空間名稱-次要命名空間</span><span class="sxs-lookup"><span data-stu-id="80f29-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="80f29-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80f29-122">-PassThru</span></span>
<span data-ttu-id="80f29-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="80f29-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="80f29-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="80f29-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="80f29-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f29-125">-ResourceGroupName</span></span>
<span data-ttu-id="80f29-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="80f29-126">Resource Group Name</span></span>

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

### <span data-ttu-id="80f29-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80f29-127">-ResourceId</span></span>
<span data-ttu-id="80f29-128">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="80f29-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="80f29-129">-確認</span><span class="sxs-lookup"><span data-stu-id="80f29-129">-Confirm</span></span>
<span data-ttu-id="80f29-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="80f29-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80f29-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80f29-131">-WhatIf</span></span>
<span data-ttu-id="80f29-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="80f29-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80f29-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80f29-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80f29-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f29-134">CommonParameters</span></span>
<span data-ttu-id="80f29-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80f29-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="80f29-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80f29-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f29-137">輸入</span><span class="sxs-lookup"><span data-stu-id="80f29-137">INPUTS</span></span>

### <span data-ttu-id="80f29-138">System.object</span><span class="sxs-lookup"><span data-stu-id="80f29-138">System.String</span></span>
<span data-ttu-id="80f29-139">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="80f29-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="80f29-140">輸出</span><span class="sxs-lookup"><span data-stu-id="80f29-140">OUTPUTS</span></span>

### <span data-ttu-id="80f29-141">System.object</span><span class="sxs-lookup"><span data-stu-id="80f29-141">System.Boolean</span></span>


## <span data-ttu-id="80f29-142">筆記</span><span class="sxs-lookup"><span data-stu-id="80f29-142">NOTES</span></span>

## <span data-ttu-id="80f29-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="80f29-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e2f1edfa0d1b5fa081754457fa3fc53f310eb345
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624340"
---
# <span data-ttu-id="89e30-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="89e30-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="89e30-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89e30-102">SYNOPSIS</span></span>
<span data-ttu-id="89e30-103"> (災害復原設定建立新的別名) </span><span class="sxs-lookup"><span data-stu-id="89e30-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89e30-104">句法</span><span class="sxs-lookup"><span data-stu-id="89e30-104">SYNTAX</span></span>

### <span data-ttu-id="89e30-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="89e30-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89e30-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89e30-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89e30-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89e30-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89e30-108">說明</span><span class="sxs-lookup"><span data-stu-id="89e30-108">DESCRIPTION</span></span>
<span data-ttu-id="89e30-109">**新的-AzureRmServiceBusGeoDRConfiguration** Cmdlet 會建立新的別名 (災害復原配置) </span><span class="sxs-lookup"><span data-stu-id="89e30-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="89e30-110">示例</span><span class="sxs-lookup"><span data-stu-id="89e30-110">EXAMPLES</span></span>

### <span data-ttu-id="89e30-111">範例1</span><span class="sxs-lookup"><span data-stu-id="89e30-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="89e30-112">建立具有主要命名空間 "SampleNamespace_Primary" 的別名 "SampleDRCongifName" 與次要命名空間 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="89e30-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="89e30-113">參數</span><span class="sxs-lookup"><span data-stu-id="89e30-113">PARAMETERS</span></span>

### <span data-ttu-id="89e30-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="89e30-114">-AlternateName</span></span>
<span data-ttu-id="89e30-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="89e30-115">AlternateName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e30-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89e30-116">-AsJob</span></span>
<span data-ttu-id="89e30-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="89e30-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89e30-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e30-118">-DefaultProfile</span></span>
<span data-ttu-id="89e30-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89e30-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e30-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89e30-120">-InputObject</span></span>
<span data-ttu-id="89e30-121">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="89e30-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89e30-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="89e30-122">-Name</span></span>
<span data-ttu-id="89e30-123">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="89e30-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e30-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="89e30-124">-Namespace</span></span>
<span data-ttu-id="89e30-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="89e30-125">Namespace Name</span></span>

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

### <span data-ttu-id="89e30-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="89e30-126">-PartnerNamespace</span></span>
<span data-ttu-id="89e30-127">DR Configuration PartnerNamespace (ARM Id 為 PartnerNamespace [次要命名空間] ) </span><span class="sxs-lookup"><span data-stu-id="89e30-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e30-128">-ResourceGroupName</span></span>
<span data-ttu-id="89e30-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="89e30-129">Resource Group Name</span></span>

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

### <span data-ttu-id="89e30-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89e30-130">-ResourceId</span></span>
<span data-ttu-id="89e30-131">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="89e30-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e30-132">-確認</span><span class="sxs-lookup"><span data-stu-id="89e30-132">-Confirm</span></span>
<span data-ttu-id="89e30-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89e30-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e30-134">-WhatIf</span></span>
<span data-ttu-id="89e30-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89e30-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89e30-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89e30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e30-137">CommonParameters</span></span>
<span data-ttu-id="89e30-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89e30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e30-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89e30-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e30-140">輸入</span><span class="sxs-lookup"><span data-stu-id="89e30-140">INPUTS</span></span>

### <span data-ttu-id="89e30-141">System.object</span><span class="sxs-lookup"><span data-stu-id="89e30-141">System.String</span></span>

### <span data-ttu-id="89e30-142">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="89e30-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="89e30-143">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="89e30-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="89e30-144">輸出</span><span class="sxs-lookup"><span data-stu-id="89e30-144">OUTPUTS</span></span>

### <span data-ttu-id="89e30-145">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="89e30-145">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="89e30-146">筆記</span><span class="sxs-lookup"><span data-stu-id="89e30-146">NOTES</span></span>

## <span data-ttu-id="89e30-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="89e30-147">RELATED LINKS</span></span>

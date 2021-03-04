---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 02335868ca9984d4da57be905b9600b81333b484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903078"
---
# <span data-ttu-id="1af49-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="1af49-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="1af49-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1af49-102">SYNOPSIS</span></span>
<span data-ttu-id="1af49-103">建立新的別名 (復原組) </span><span class="sxs-lookup"><span data-stu-id="1af49-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="1af49-104">語法</span><span class="sxs-lookup"><span data-stu-id="1af49-104">SYNTAX</span></span>

### <span data-ttu-id="1af49-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1af49-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af49-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1af49-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af49-107">命名空間ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af49-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1af49-108">描述</span><span class="sxs-lookup"><span data-stu-id="1af49-108">DESCRIPTION</span></span>
<span data-ttu-id="1af49-109">**New-AzServiceBusGeoDRConfiguration** Cmdlet 會建立新的別名 (復原組) </span><span class="sxs-lookup"><span data-stu-id="1af49-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="1af49-110">例子</span><span class="sxs-lookup"><span data-stu-id="1af49-110">EXAMPLES</span></span>

### <span data-ttu-id="1af49-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1af49-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="1af49-112">使用次要命名空間 "SampleNamespace_Primary" 建立具有主要命名空間 "SampleNamespace_Secondary" 的別名 "sampleDRConfigName"</span><span class="sxs-lookup"><span data-stu-id="1af49-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="1af49-113">參數</span><span class="sxs-lookup"><span data-stu-id="1af49-113">PARAMETERS</span></span>

### <span data-ttu-id="1af49-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="1af49-114">-AlternateName</span></span>
<span data-ttu-id="1af49-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="1af49-115">AlternateName</span></span>

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

### <span data-ttu-id="1af49-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1af49-116">-AsJob</span></span>
<span data-ttu-id="1af49-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1af49-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1af49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af49-118">-DefaultProfile</span></span>
<span data-ttu-id="1af49-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1af49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af49-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1af49-120">-InputObject</span></span>
<span data-ttu-id="1af49-121">命名空間物件</span><span class="sxs-lookup"><span data-stu-id="1af49-121">Namespace Object</span></span>

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

### <span data-ttu-id="1af49-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1af49-122">-Name</span></span>
<span data-ttu-id="1af49-123">DR 組組名稱</span><span class="sxs-lookup"><span data-stu-id="1af49-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="1af49-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1af49-124">-Namespace</span></span>
<span data-ttu-id="1af49-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="1af49-125">Namespace Name</span></span>

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

### <span data-ttu-id="1af49-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="1af49-126">-PartnerNamespace</span></span>
<span data-ttu-id="1af49-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [次要命名空間]]) </span><span class="sxs-lookup"><span data-stu-id="1af49-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="1af49-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af49-128">-ResourceGroupName</span></span>
<span data-ttu-id="1af49-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="1af49-129">Resource Group Name</span></span>

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

### <span data-ttu-id="1af49-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af49-130">-ResourceId</span></span>
<span data-ttu-id="1af49-131">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1af49-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="1af49-132">-確認</span><span class="sxs-lookup"><span data-stu-id="1af49-132">-Confirm</span></span>
<span data-ttu-id="1af49-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1af49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af49-134">-WhatIf</span></span>
<span data-ttu-id="1af49-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1af49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af49-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1af49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af49-137">CommonParameters</span></span>
<span data-ttu-id="1af49-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1af49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af49-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1af49-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af49-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1af49-140">INPUTS</span></span>

### <span data-ttu-id="1af49-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1af49-141">System.String</span></span>

### <span data-ttu-id="1af49-142">Microsoft.Azure.Commands.ServiceBus.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1af49-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="1af49-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1af49-143">OUTPUTS</span></span>

### <span data-ttu-id="1af49-144">Microsoft.Azure.Commands.ServiceBus.models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1af49-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="1af49-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1af49-145">NOTES</span></span>

## <span data-ttu-id="1af49-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1af49-146">RELATED LINKS</span></span>

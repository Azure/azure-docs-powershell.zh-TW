---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959674"
---
# <span data-ttu-id="306af-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="306af-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="306af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="306af-102">SYNOPSIS</span></span>
<span data-ttu-id="306af-103"> (災害復原設定建立新的別名) </span><span class="sxs-lookup"><span data-stu-id="306af-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="306af-104">句法</span><span class="sxs-lookup"><span data-stu-id="306af-104">SYNTAX</span></span>

### <span data-ttu-id="306af-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="306af-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="306af-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="306af-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="306af-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="306af-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="306af-108">說明</span><span class="sxs-lookup"><span data-stu-id="306af-108">DESCRIPTION</span></span>
<span data-ttu-id="306af-109">**新的-AzServiceBusGeoDRConfiguration** Cmdlet 會建立新的別名 (災害復原配置) </span><span class="sxs-lookup"><span data-stu-id="306af-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="306af-110">示例</span><span class="sxs-lookup"><span data-stu-id="306af-110">EXAMPLES</span></span>

### <span data-ttu-id="306af-111">範例1</span><span class="sxs-lookup"><span data-stu-id="306af-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="306af-112">建立具有主要命名空間 "SampleNamespace_Primary" 的別名 "SampleDRConfigName" 與次要命名空間 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="306af-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="306af-113">參數</span><span class="sxs-lookup"><span data-stu-id="306af-113">PARAMETERS</span></span>

### <span data-ttu-id="306af-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="306af-114">-AlternateName</span></span>
<span data-ttu-id="306af-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="306af-115">AlternateName</span></span>

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

### <span data-ttu-id="306af-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="306af-116">-AsJob</span></span>
<span data-ttu-id="306af-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="306af-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="306af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="306af-118">-DefaultProfile</span></span>
<span data-ttu-id="306af-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="306af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="306af-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="306af-120">-InputObject</span></span>
<span data-ttu-id="306af-121">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="306af-121">Namespace Object</span></span>

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

### <span data-ttu-id="306af-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="306af-122">-Name</span></span>
<span data-ttu-id="306af-123">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="306af-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="306af-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="306af-124">-Namespace</span></span>
<span data-ttu-id="306af-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="306af-125">Namespace Name</span></span>

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

### <span data-ttu-id="306af-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="306af-126">-PartnerNamespace</span></span>
<span data-ttu-id="306af-127">DR Configuration PartnerNamespace (ARM Id 為 PartnerNamespace [次要命名空間] ) </span><span class="sxs-lookup"><span data-stu-id="306af-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="306af-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="306af-128">-ResourceGroupName</span></span>
<span data-ttu-id="306af-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="306af-129">Resource Group Name</span></span>

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

### <span data-ttu-id="306af-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="306af-130">-ResourceId</span></span>
<span data-ttu-id="306af-131">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="306af-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="306af-132">-確認</span><span class="sxs-lookup"><span data-stu-id="306af-132">-Confirm</span></span>
<span data-ttu-id="306af-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="306af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="306af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="306af-134">-WhatIf</span></span>
<span data-ttu-id="306af-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="306af-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="306af-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="306af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="306af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306af-137">CommonParameters</span></span>
<span data-ttu-id="306af-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="306af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306af-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="306af-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306af-140">輸入</span><span class="sxs-lookup"><span data-stu-id="306af-140">INPUTS</span></span>

### <span data-ttu-id="306af-141">System.object</span><span class="sxs-lookup"><span data-stu-id="306af-141">System.String</span></span>

### <span data-ttu-id="306af-142">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="306af-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="306af-143">輸出</span><span class="sxs-lookup"><span data-stu-id="306af-143">OUTPUTS</span></span>

### <span data-ttu-id="306af-144">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="306af-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="306af-145">筆記</span><span class="sxs-lookup"><span data-stu-id="306af-145">NOTES</span></span>

## <span data-ttu-id="306af-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="306af-146">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: d545883f1c4ce51d4e3efce15787a2e0fa144378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903198"
---
# <span data-ttu-id="f7264-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7264-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="f7264-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7264-102">SYNOPSIS</span></span>
<span data-ttu-id="f7264-103">建立新的別名 (復原組) </span><span class="sxs-lookup"><span data-stu-id="f7264-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f7264-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7264-104">SYNTAX</span></span>

### <span data-ttu-id="f7264-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f7264-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7264-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f7264-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7264-107">命名空間ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7264-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7264-108">描述</span><span class="sxs-lookup"><span data-stu-id="f7264-108">DESCRIPTION</span></span>
<span data-ttu-id="f7264-109">**New-AzEventHubGeoDRConfiguration** Cmdlet 會建立新的別名 (復原組) </span><span class="sxs-lookup"><span data-stu-id="f7264-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f7264-110">例子</span><span class="sxs-lookup"><span data-stu-id="f7264-110">EXAMPLES</span></span>

### <span data-ttu-id="f7264-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f7264-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="f7264-112">使用次要命名空間 "SampleNamespace_Primary" 建立具有主要命名空間 "SampleNamespace_Secondary" 的別名 "sampleDRConfigName"</span><span class="sxs-lookup"><span data-stu-id="f7264-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="f7264-113">參數</span><span class="sxs-lookup"><span data-stu-id="f7264-113">PARAMETERS</span></span>

### <span data-ttu-id="f7264-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="f7264-114">-AlternateName</span></span>
<span data-ttu-id="f7264-115">DR 組名與主要命名空間相同時，需要替代名稱</span><span class="sxs-lookup"><span data-stu-id="f7264-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="f7264-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7264-116">-AsJob</span></span>
<span data-ttu-id="f7264-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f7264-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7264-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7264-118">-DefaultProfile</span></span>
<span data-ttu-id="f7264-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7264-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7264-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7264-120">-InputObject</span></span>
<span data-ttu-id="f7264-121">命名空間物件</span><span class="sxs-lookup"><span data-stu-id="f7264-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7264-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7264-122">-Name</span></span>
<span data-ttu-id="f7264-123">DR 組組名稱</span><span class="sxs-lookup"><span data-stu-id="f7264-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="f7264-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f7264-124">-Namespace</span></span>
<span data-ttu-id="f7264-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f7264-125">Namespace Name</span></span>

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

### <span data-ttu-id="f7264-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="f7264-126">-PartnerNamespace</span></span>
<span data-ttu-id="f7264-127">DR Configuration PartnerNamespace ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="f7264-127">DR Configuration PartnerNamespace ARM ID</span></span>

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

### <span data-ttu-id="f7264-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7264-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7264-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="f7264-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f7264-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7264-130">-ResourceId</span></span>
<span data-ttu-id="f7264-131">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f7264-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f7264-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f7264-132">-Confirm</span></span>
<span data-ttu-id="f7264-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f7264-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7264-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7264-134">-WhatIf</span></span>
<span data-ttu-id="f7264-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7264-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7264-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7264-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7264-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7264-137">CommonParameters</span></span>
<span data-ttu-id="f7264-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7264-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7264-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f7264-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7264-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f7264-140">INPUTS</span></span>

### <span data-ttu-id="f7264-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f7264-141">System.String</span></span>

### <span data-ttu-id="f7264-142">Microsoft.Azure.Commands.EventHub.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f7264-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f7264-143">輸出</span><span class="sxs-lookup"><span data-stu-id="f7264-143">OUTPUTS</span></span>

### <span data-ttu-id="f7264-144">Microsoft.Azure.Commands.EventHub.models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f7264-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="f7264-145">筆記</span><span class="sxs-lookup"><span data-stu-id="f7264-145">NOTES</span></span>

## <span data-ttu-id="f7264-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7264-146">RELATED LINKS</span></span>

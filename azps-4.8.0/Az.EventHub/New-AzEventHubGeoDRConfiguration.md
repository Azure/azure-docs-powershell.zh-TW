---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: fe0d8f29650498e895e19e18bcb080107b2dbf35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136411"
---
# <span data-ttu-id="58b9b-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="58b9b-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="58b9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="58b9b-103"> (災害復原設定建立新的別名) </span><span class="sxs-lookup"><span data-stu-id="58b9b-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="58b9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="58b9b-104">SYNTAX</span></span>

### <span data-ttu-id="58b9b-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="58b9b-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58b9b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58b9b-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58b9b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58b9b-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58b9b-108">說明</span><span class="sxs-lookup"><span data-stu-id="58b9b-108">DESCRIPTION</span></span>
<span data-ttu-id="58b9b-109">**新的-AzEventHubGeoDRConfiguration** Cmdlet 會建立新的別名 (災害復原配置) </span><span class="sxs-lookup"><span data-stu-id="58b9b-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="58b9b-110">示例</span><span class="sxs-lookup"><span data-stu-id="58b9b-110">EXAMPLES</span></span>

### <span data-ttu-id="58b9b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="58b9b-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="58b9b-112">建立具有主要命名空間 "SampleNamespace_Primary" 的別名 "SampleDRConfigName" 與次要命名空間 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="58b9b-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="58b9b-113">參數</span><span class="sxs-lookup"><span data-stu-id="58b9b-113">PARAMETERS</span></span>

### <span data-ttu-id="58b9b-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="58b9b-114">-AlternateName</span></span>
<span data-ttu-id="58b9b-115">當 DR 設定名稱與主要命名空間相同時，需要 AlternateName</span><span class="sxs-lookup"><span data-stu-id="58b9b-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="58b9b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58b9b-116">-AsJob</span></span>
<span data-ttu-id="58b9b-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58b9b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58b9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b9b-118">-DefaultProfile</span></span>
<span data-ttu-id="58b9b-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58b9b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58b9b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58b9b-120">-InputObject</span></span>
<span data-ttu-id="58b9b-121">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="58b9b-121">Namespace Object</span></span>

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

### <span data-ttu-id="58b9b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="58b9b-122">-Name</span></span>
<span data-ttu-id="58b9b-123">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="58b9b-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="58b9b-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="58b9b-124">-Namespace</span></span>
<span data-ttu-id="58b9b-125">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="58b9b-125">Namespace Name</span></span>

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

### <span data-ttu-id="58b9b-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="58b9b-126">-PartnerNamespace</span></span>
<span data-ttu-id="58b9b-127">災害復原配置 PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="58b9b-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="58b9b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58b9b-128">-ResourceGroupName</span></span>
<span data-ttu-id="58b9b-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="58b9b-129">Resource Group Name</span></span>

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

### <span data-ttu-id="58b9b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58b9b-130">-ResourceId</span></span>
<span data-ttu-id="58b9b-131">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="58b9b-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="58b9b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="58b9b-132">-Confirm</span></span>
<span data-ttu-id="58b9b-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58b9b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b9b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b9b-134">-WhatIf</span></span>
<span data-ttu-id="58b9b-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58b9b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58b9b-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58b9b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b9b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b9b-137">CommonParameters</span></span>
<span data-ttu-id="58b9b-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58b9b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b9b-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58b9b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b9b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="58b9b-140">INPUTS</span></span>

### <span data-ttu-id="58b9b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="58b9b-141">System.String</span></span>

### <span data-ttu-id="58b9b-142">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="58b9b-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="58b9b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="58b9b-143">OUTPUTS</span></span>

### <span data-ttu-id="58b9b-144">PSEventHubDRConfigurationAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="58b9b-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="58b9b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="58b9b-145">NOTES</span></span>

## <span data-ttu-id="58b9b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="58b9b-146">RELATED LINKS</span></span>

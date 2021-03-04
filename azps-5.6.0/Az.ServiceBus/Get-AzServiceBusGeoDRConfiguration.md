---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 21ccb8a16ff3622e6661bd5548721d6d1227e7e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913718"
---
# <span data-ttu-id="cf716-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf716-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="cf716-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf716-102">SYNOPSIS</span></span>
<span data-ttu-id="cf716-103">針對主要或 (命名空間，) 復原組選的別名</span><span class="sxs-lookup"><span data-stu-id="cf716-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="cf716-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf716-104">SYNTAX</span></span>

### <span data-ttu-id="cf716-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cf716-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf716-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cf716-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf716-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf716-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf716-108">描述</span><span class="sxs-lookup"><span data-stu-id="cf716-108">DESCRIPTION</span></span>
<span data-ttu-id="cf716-109">**Get-AzServiceBusGeoDRConfiguration** 會針對主要或次要命名空間 (復原) 別名</span><span class="sxs-lookup"><span data-stu-id="cf716-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="cf716-110">例子</span><span class="sxs-lookup"><span data-stu-id="cf716-110">EXAMPLES</span></span>

### <span data-ttu-id="cf716-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="cf716-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="cf716-112">為主要命名空間 "SampleNamespace_Primary" 取用別名 "SampleDRConfigName" 組SampleNamespace_Primary</span><span class="sxs-lookup"><span data-stu-id="cf716-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="cf716-113">參數</span><span class="sxs-lookup"><span data-stu-id="cf716-113">PARAMETERS</span></span>

### <span data-ttu-id="cf716-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf716-114">-DefaultProfile</span></span>
<span data-ttu-id="cf716-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf716-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf716-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf716-116">-InputObject</span></span>
<span data-ttu-id="cf716-117">命名空間物件</span><span class="sxs-lookup"><span data-stu-id="cf716-117">Namespace Object</span></span>

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

### <span data-ttu-id="cf716-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf716-118">-Name</span></span>
<span data-ttu-id="cf716-119">DR 組組名稱</span><span class="sxs-lookup"><span data-stu-id="cf716-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="cf716-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="cf716-120">-Namespace</span></span>
<span data-ttu-id="cf716-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="cf716-121">Namespace Name</span></span>

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

### <span data-ttu-id="cf716-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf716-122">-ResourceGroupName</span></span>
<span data-ttu-id="cf716-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="cf716-123">Resource Group Name</span></span>

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

### <span data-ttu-id="cf716-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf716-124">-ResourceId</span></span>
<span data-ttu-id="cf716-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cf716-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf716-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf716-126">CommonParameters</span></span>
<span data-ttu-id="cf716-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf716-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf716-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cf716-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf716-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cf716-129">INPUTS</span></span>

### <span data-ttu-id="cf716-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cf716-130">System.String</span></span>

### <span data-ttu-id="cf716-131">Microsoft.Azure.Commands.ServiceBus.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cf716-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="cf716-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cf716-132">OUTPUTS</span></span>

### <span data-ttu-id="cf716-133">Microsoft.Azure.Commands.ServiceBus.models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cf716-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="cf716-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cf716-134">NOTES</span></span>

## <span data-ttu-id="cf716-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf716-135">RELATED LINKS</span></span>

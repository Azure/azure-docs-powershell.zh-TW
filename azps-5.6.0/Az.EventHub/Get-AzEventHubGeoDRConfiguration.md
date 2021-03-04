---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b2003821178875777240cb43bcdc1e9e53784fc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903234"
---
# <span data-ttu-id="ea1f7-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea1f7-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="ea1f7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1f7-103">針對主要或 (命名空間，) 復原組選的別名</span><span class="sxs-lookup"><span data-stu-id="ea1f7-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="ea1f7-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea1f7-104">SYNTAX</span></span>

### <span data-ttu-id="ea1f7-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ea1f7-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea1f7-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ea1f7-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea1f7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea1f7-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea1f7-108">描述</span><span class="sxs-lookup"><span data-stu-id="ea1f7-108">DESCRIPTION</span></span>
<span data-ttu-id="ea1f7-109">**Get-AzEventHubGeoDRConfiguration** 會針對主要或次要命名空間 (復原) 別名</span><span class="sxs-lookup"><span data-stu-id="ea1f7-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="ea1f7-110">例子</span><span class="sxs-lookup"><span data-stu-id="ea1f7-110">EXAMPLES</span></span>

### <span data-ttu-id="ea1f7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ea1f7-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="ea1f7-112">為主要命名空間 "SampleNamespace_Primary" 取用別名 "SampleDRConfigName" 組SampleNamespace_Primary</span><span class="sxs-lookup"><span data-stu-id="ea1f7-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="ea1f7-113">參數</span><span class="sxs-lookup"><span data-stu-id="ea1f7-113">PARAMETERS</span></span>

### <span data-ttu-id="ea1f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1f7-114">-DefaultProfile</span></span>
<span data-ttu-id="ea1f7-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea1f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea1f7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea1f7-116">-InputObject</span></span>
<span data-ttu-id="ea1f7-117">命名空間物件</span><span class="sxs-lookup"><span data-stu-id="ea1f7-117">Namespace Object</span></span>

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

### <span data-ttu-id="ea1f7-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea1f7-118">-Name</span></span>
<span data-ttu-id="ea1f7-119">DR 組組名稱</span><span class="sxs-lookup"><span data-stu-id="ea1f7-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="ea1f7-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ea1f7-120">-Namespace</span></span>
<span data-ttu-id="ea1f7-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="ea1f7-121">Namespace Name</span></span>

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

### <span data-ttu-id="ea1f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea1f7-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="ea1f7-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ea1f7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea1f7-124">-ResourceId</span></span>
<span data-ttu-id="ea1f7-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ea1f7-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="ea1f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1f7-126">CommonParameters</span></span>
<span data-ttu-id="ea1f7-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea1f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1f7-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ea1f7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1f7-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ea1f7-129">INPUTS</span></span>

### <span data-ttu-id="ea1f7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ea1f7-130">System.String</span></span>

### <span data-ttu-id="ea1f7-131">Microsoft.Azure.Commands.EventHub.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ea1f7-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ea1f7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ea1f7-132">OUTPUTS</span></span>

### <span data-ttu-id="ea1f7-133">Microsoft.Azure.Commands.EventHub.models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ea1f7-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="ea1f7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ea1f7-134">NOTES</span></span>

## <span data-ttu-id="ea1f7-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea1f7-135">RELATED LINKS</span></span>

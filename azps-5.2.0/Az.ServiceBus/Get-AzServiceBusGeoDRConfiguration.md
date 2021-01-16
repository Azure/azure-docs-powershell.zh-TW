---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279140"
---
# <span data-ttu-id="b38f9-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b38f9-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="b38f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b38f9-102">SYNOPSIS</span></span>
<span data-ttu-id="b38f9-103">檢索主要或次要命名空間的別名 (災害復原設定) </span><span class="sxs-lookup"><span data-stu-id="b38f9-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="b38f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="b38f9-104">SYNTAX</span></span>

### <span data-ttu-id="b38f9-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b38f9-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b38f9-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b38f9-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b38f9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b38f9-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b38f9-108">說明</span><span class="sxs-lookup"><span data-stu-id="b38f9-108">DESCRIPTION</span></span>
<span data-ttu-id="b38f9-109">**AzServiceBusGeoDRConfiguration** 會在主要或次要命名空間中檢索別名 (災害復原配置) </span><span class="sxs-lookup"><span data-stu-id="b38f9-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="b38f9-110">示例</span><span class="sxs-lookup"><span data-stu-id="b38f9-110">EXAMPLES</span></span>

### <span data-ttu-id="b38f9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b38f9-111">Example 1</span></span>
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

<span data-ttu-id="b38f9-112">針對主要命名空間 "SampleNamespace_Primary" 檢索別名 "SampleDRConfigName" 設定</span><span class="sxs-lookup"><span data-stu-id="b38f9-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="b38f9-113">參數</span><span class="sxs-lookup"><span data-stu-id="b38f9-113">PARAMETERS</span></span>

### <span data-ttu-id="b38f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b38f9-114">-DefaultProfile</span></span>
<span data-ttu-id="b38f9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b38f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b38f9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b38f9-116">-InputObject</span></span>
<span data-ttu-id="b38f9-117">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="b38f9-117">Namespace Object</span></span>

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

### <span data-ttu-id="b38f9-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b38f9-118">-Name</span></span>
<span data-ttu-id="b38f9-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="b38f9-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="b38f9-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b38f9-120">-Namespace</span></span>
<span data-ttu-id="b38f9-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="b38f9-121">Namespace Name</span></span>

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

### <span data-ttu-id="b38f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b38f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="b38f9-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b38f9-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b38f9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b38f9-124">-ResourceId</span></span>
<span data-ttu-id="b38f9-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b38f9-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="b38f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b38f9-126">CommonParameters</span></span>
<span data-ttu-id="b38f9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b38f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b38f9-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b38f9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b38f9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b38f9-129">INPUTS</span></span>

### <span data-ttu-id="b38f9-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b38f9-130">System.String</span></span>

### <span data-ttu-id="b38f9-131">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b38f9-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b38f9-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b38f9-132">OUTPUTS</span></span>

### <span data-ttu-id="b38f9-133">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b38f9-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="b38f9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b38f9-134">NOTES</span></span>

## <span data-ttu-id="b38f9-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b38f9-135">RELATED LINKS</span></span>

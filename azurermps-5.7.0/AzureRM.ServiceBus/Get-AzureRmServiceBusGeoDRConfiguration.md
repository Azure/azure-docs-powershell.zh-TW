---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: e5623ed840b9b1d2a7f75150fa686d6f488dc2ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447648"
---
# <span data-ttu-id="b0afc-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0afc-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="b0afc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0afc-102">SYNOPSIS</span></span>
<span data-ttu-id="b0afc-103">檢索主要或次要命名空間的別名 (災害復原設定) </span><span class="sxs-lookup"><span data-stu-id="b0afc-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0afc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0afc-104">SYNTAX</span></span>

### <span data-ttu-id="b0afc-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b0afc-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0afc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b0afc-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0afc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0afc-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0afc-108">說明</span><span class="sxs-lookup"><span data-stu-id="b0afc-108">DESCRIPTION</span></span>
<span data-ttu-id="b0afc-109">**AzureRmServiceBusGeoDRConfiguration** 會在主要或次要命名空間中檢索別名 (災害復原配置) </span><span class="sxs-lookup"><span data-stu-id="b0afc-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="b0afc-110">示例</span><span class="sxs-lookup"><span data-stu-id="b0afc-110">EXAMPLES</span></span>

### <span data-ttu-id="b0afc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b0afc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="b0afc-112">針對主要命名空間 "SampleNamespace_Primary" 檢索別名 "SampleDRCongifName" 設定</span><span class="sxs-lookup"><span data-stu-id="b0afc-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="b0afc-113">參數</span><span class="sxs-lookup"><span data-stu-id="b0afc-113">PARAMETERS</span></span>

### <span data-ttu-id="b0afc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0afc-114">-DefaultProfile</span></span>
<span data-ttu-id="b0afc-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b0afc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0afc-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0afc-116">-InputObject</span></span>
<span data-ttu-id="b0afc-117">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="b0afc-117">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0afc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0afc-118">-Name</span></span>
<span data-ttu-id="b0afc-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="b0afc-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0afc-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b0afc-120">-Namespace</span></span>
<span data-ttu-id="b0afc-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="b0afc-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0afc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0afc-122">-ResourceGroupName</span></span>
<span data-ttu-id="b0afc-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b0afc-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0afc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0afc-124">-ResourceId</span></span>
<span data-ttu-id="b0afc-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b0afc-125">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0afc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0afc-126">CommonParameters</span></span>
<span data-ttu-id="b0afc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0afc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b0afc-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0afc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0afc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b0afc-129">INPUTS</span></span>

### <span data-ttu-id="b0afc-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b0afc-130">System.String</span></span>
<span data-ttu-id="b0afc-131">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b0afc-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="b0afc-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b0afc-132">OUTPUTS</span></span>

### <span data-ttu-id="b0afc-133">[System.object]。清單 ' 1 [0.5.0.0，PSServiceBusDRConfigurationAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="b0afc-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="b0afc-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b0afc-134">NOTES</span></span>

## <span data-ttu-id="b0afc-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0afc-135">RELATED LINKS</span></span>

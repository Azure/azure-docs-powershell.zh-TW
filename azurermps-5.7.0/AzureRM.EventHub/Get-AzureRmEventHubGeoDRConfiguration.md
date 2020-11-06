---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 8c48e6dc8fb095258953a57498b76219dec4ef42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454239"
---
# <span data-ttu-id="3f342-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f342-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="3f342-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f342-102">SYNOPSIS</span></span>
<span data-ttu-id="3f342-103">檢索主要或次要命名空間的別名 (災害復原設定) </span><span class="sxs-lookup"><span data-stu-id="3f342-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f342-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f342-104">SYNTAX</span></span>

### <span data-ttu-id="3f342-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3f342-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f342-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f342-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f342-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f342-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f342-108">說明</span><span class="sxs-lookup"><span data-stu-id="3f342-108">DESCRIPTION</span></span>
<span data-ttu-id="3f342-109">**AzureRmEventHubGeoDRConfiguration** 會在主要或次要命名空間中檢索別名 (災害復原配置) </span><span class="sxs-lookup"><span data-stu-id="3f342-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="3f342-110">示例</span><span class="sxs-lookup"><span data-stu-id="3f342-110">EXAMPLES</span></span>

### <span data-ttu-id="3f342-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3f342-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="3f342-112">針對主要命名空間 "SampleNamespace_Primary" 檢索別名 "SampleDRCongifName" 設定</span><span class="sxs-lookup"><span data-stu-id="3f342-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="3f342-113">參數</span><span class="sxs-lookup"><span data-stu-id="3f342-113">PARAMETERS</span></span>

### <span data-ttu-id="3f342-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f342-114">-DefaultProfile</span></span>
<span data-ttu-id="3f342-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f342-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f342-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f342-116">-InputObject</span></span>
<span data-ttu-id="3f342-117">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="3f342-117">Namespace Object</span></span>

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

### <span data-ttu-id="3f342-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f342-118">-Name</span></span>
<span data-ttu-id="3f342-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="3f342-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f342-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="3f342-120">-Namespace</span></span>
<span data-ttu-id="3f342-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="3f342-121">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f342-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f342-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f342-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3f342-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f342-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f342-124">-ResourceId</span></span>
<span data-ttu-id="3f342-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3f342-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="3f342-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f342-126">CommonParameters</span></span>
<span data-ttu-id="3f342-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f342-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f342-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f342-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f342-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3f342-129">INPUTS</span></span>

### <span data-ttu-id="3f342-130">System.object</span><span class="sxs-lookup"><span data-stu-id="3f342-130">System.String</span></span>
<span data-ttu-id="3f342-131">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="3f342-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3f342-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3f342-132">OUTPUTS</span></span>

### <span data-ttu-id="3f342-133">[System.object]。清單 ' 1 [PSEventHubDRConfigurationAttributes，0.5.0.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="3f342-133">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3f342-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3f342-134">NOTES</span></span>

## <span data-ttu-id="3f342-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f342-135">RELATED LINKS</span></span>

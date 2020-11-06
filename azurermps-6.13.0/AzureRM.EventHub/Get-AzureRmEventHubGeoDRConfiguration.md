---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 40a80a975de56a867f0dcbc34aea0e46d42a155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448424"
---
# <span data-ttu-id="f81ec-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f81ec-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="f81ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f81ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f81ec-103">檢索主要或次要命名空間的別名 (災害復原設定) </span><span class="sxs-lookup"><span data-stu-id="f81ec-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f81ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="f81ec-104">SYNTAX</span></span>

### <span data-ttu-id="f81ec-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f81ec-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f81ec-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f81ec-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f81ec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f81ec-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f81ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="f81ec-108">DESCRIPTION</span></span>
<span data-ttu-id="f81ec-109">**AzureRmEventHubGeoDRConfiguration** 會在主要或次要命名空間中檢索別名 (災害復原配置) </span><span class="sxs-lookup"><span data-stu-id="f81ec-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="f81ec-110">示例</span><span class="sxs-lookup"><span data-stu-id="f81ec-110">EXAMPLES</span></span>

### <span data-ttu-id="f81ec-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f81ec-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="f81ec-112">針對主要命名空間 "SampleNamespace_Primary" 檢索別名 "SampleDRCongifName" 設定</span><span class="sxs-lookup"><span data-stu-id="f81ec-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="f81ec-113">參數</span><span class="sxs-lookup"><span data-stu-id="f81ec-113">PARAMETERS</span></span>

### <span data-ttu-id="f81ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81ec-114">-DefaultProfile</span></span>
<span data-ttu-id="f81ec-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f81ec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f81ec-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f81ec-116">-InputObject</span></span>
<span data-ttu-id="f81ec-117">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="f81ec-117">Namespace Object</span></span>

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

### <span data-ttu-id="f81ec-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f81ec-118">-Name</span></span>
<span data-ttu-id="f81ec-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="f81ec-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="f81ec-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f81ec-120">-Namespace</span></span>
<span data-ttu-id="f81ec-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f81ec-121">Namespace Name</span></span>

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

### <span data-ttu-id="f81ec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f81ec-122">-ResourceGroupName</span></span>
<span data-ttu-id="f81ec-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f81ec-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f81ec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f81ec-124">-ResourceId</span></span>
<span data-ttu-id="f81ec-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f81ec-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f81ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81ec-126">CommonParameters</span></span>
<span data-ttu-id="f81ec-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f81ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81ec-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f81ec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81ec-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f81ec-129">INPUTS</span></span>

### <span data-ttu-id="f81ec-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f81ec-130">System.String</span></span>

### <span data-ttu-id="f81ec-131">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="f81ec-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="f81ec-132">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f81ec-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f81ec-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f81ec-133">OUTPUTS</span></span>

### <span data-ttu-id="f81ec-134">PSEventHubDRConfigurationAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="f81ec-134">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="f81ec-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f81ec-135">NOTES</span></span>

## <span data-ttu-id="f81ec-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f81ec-136">RELATED LINKS</span></span>

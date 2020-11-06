---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449747"
---
# <span data-ttu-id="2337d-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2337d-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="2337d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2337d-102">SYNOPSIS</span></span>
<span data-ttu-id="2337d-103">檢索命名空間的 MigrationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2337d-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2337d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2337d-104">SYNTAX</span></span>

### <span data-ttu-id="2337d-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2337d-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2337d-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2337d-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2337d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2337d-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2337d-108">說明</span><span class="sxs-lookup"><span data-stu-id="2337d-108">DESCRIPTION</span></span>
<span data-ttu-id="2337d-109">**AzureRmServiceBusMigration** 會檢索命名空間的遷移設定</span><span class="sxs-lookup"><span data-stu-id="2337d-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="2337d-110">示例</span><span class="sxs-lookup"><span data-stu-id="2337d-110">EXAMPLES</span></span>

### <span data-ttu-id="2337d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2337d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="2337d-112">取得 ' TestingNamespaceStandardMirgation」的遷移設定屬性</span><span class="sxs-lookup"><span data-stu-id="2337d-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="2337d-113">參數</span><span class="sxs-lookup"><span data-stu-id="2337d-113">PARAMETERS</span></span>

### <span data-ttu-id="2337d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2337d-114">-DefaultProfile</span></span>
<span data-ttu-id="2337d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2337d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2337d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2337d-116">-InputObject</span></span>
<span data-ttu-id="2337d-117">Namespace 物件</span><span class="sxs-lookup"><span data-stu-id="2337d-117">Namespace Object</span></span>

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

### <span data-ttu-id="2337d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2337d-118">-Name</span></span>
<span data-ttu-id="2337d-119">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="2337d-119">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2337d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2337d-120">-ResourceGroupName</span></span>
<span data-ttu-id="2337d-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2337d-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2337d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2337d-122">-ResourceId</span></span>
<span data-ttu-id="2337d-123">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2337d-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2337d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2337d-124">CommonParameters</span></span>
<span data-ttu-id="2337d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2337d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2337d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2337d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2337d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2337d-127">INPUTS</span></span>

### <span data-ttu-id="2337d-128">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2337d-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="2337d-129">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2337d-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2337d-130">System.object</span><span class="sxs-lookup"><span data-stu-id="2337d-130">System.String</span></span>

## <span data-ttu-id="2337d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2337d-131">OUTPUTS</span></span>

### <span data-ttu-id="2337d-132">PSServiceBusMigrationConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2337d-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="2337d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2337d-133">NOTES</span></span>

## <span data-ttu-id="2337d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2337d-134">RELATED LINKS</span></span>

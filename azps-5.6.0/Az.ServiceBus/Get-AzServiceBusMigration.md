---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 29595722be5f7659d63828462ade0826ac85e610
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915862"
---
# <span data-ttu-id="2960f-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2960f-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="2960f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2960f-102">SYNOPSIS</span></span>
<span data-ttu-id="2960f-103">為命名空間取回 MigrationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2960f-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="2960f-104">語法</span><span class="sxs-lookup"><span data-stu-id="2960f-104">SYNTAX</span></span>

### <span data-ttu-id="2960f-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2960f-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2960f-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2960f-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2960f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2960f-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2960f-108">描述</span><span class="sxs-lookup"><span data-stu-id="2960f-108">DESCRIPTION</span></span>
<span data-ttu-id="2960f-109">**Get-AzServiceBusMigration** 會針對命名空間取得移移組</span><span class="sxs-lookup"><span data-stu-id="2960f-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="2960f-110">例子</span><span class="sxs-lookup"><span data-stu-id="2960f-110">EXAMPLES</span></span>

### <span data-ttu-id="2960f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2960f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="2960f-112">獲得 'TestingNamespaceStandardMigration' 的移入組定屬性</span><span class="sxs-lookup"><span data-stu-id="2960f-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="2960f-113">參數</span><span class="sxs-lookup"><span data-stu-id="2960f-113">PARAMETERS</span></span>

### <span data-ttu-id="2960f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2960f-114">-DefaultProfile</span></span>
<span data-ttu-id="2960f-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2960f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2960f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2960f-116">-InputObject</span></span>
<span data-ttu-id="2960f-117">命名空間物件</span><span class="sxs-lookup"><span data-stu-id="2960f-117">Namespace Object</span></span>

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

### <span data-ttu-id="2960f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2960f-118">-Name</span></span>
<span data-ttu-id="2960f-119">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="2960f-119">Namespace Name</span></span>

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

### <span data-ttu-id="2960f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2960f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2960f-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="2960f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2960f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2960f-122">-ResourceId</span></span>
<span data-ttu-id="2960f-123">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2960f-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2960f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2960f-124">CommonParameters</span></span>
<span data-ttu-id="2960f-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2960f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2960f-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2960f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2960f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2960f-127">INPUTS</span></span>

### <span data-ttu-id="2960f-128">Microsoft.Azure.Commands.ServiceBus.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2960f-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="2960f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2960f-129">System.String</span></span>

## <span data-ttu-id="2960f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2960f-130">OUTPUTS</span></span>

### <span data-ttu-id="2960f-131">Microsoft.Azure.Commands.ServiceBus.models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2960f-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="2960f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2960f-132">NOTES</span></span>

## <span data-ttu-id="2960f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2960f-133">RELATED LINKS</span></span>

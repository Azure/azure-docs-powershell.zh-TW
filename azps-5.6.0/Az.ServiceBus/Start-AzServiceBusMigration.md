---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 010e54b21d4abb3068f62e561c002fed6ca734d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911282"
---
# <span data-ttu-id="c5a93-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c5a93-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="c5a93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c5a93-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a93-103">建立新的移移組，並開始將實體從標準命名空間移為進級命名空間</span><span class="sxs-lookup"><span data-stu-id="c5a93-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="c5a93-104">語法</span><span class="sxs-lookup"><span data-stu-id="c5a93-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5a93-105">描述</span><span class="sxs-lookup"><span data-stu-id="c5a93-105">DESCRIPTION</span></span>
<span data-ttu-id="c5a93-106">**Start-AzServiceBusMigration Cmdlet** 會建立新的移轉組式，並開始從標準命名空間移轉實體到進級命名空間</span><span class="sxs-lookup"><span data-stu-id="c5a93-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="c5a93-107">例子</span><span class="sxs-lookup"><span data-stu-id="c5a93-107">EXAMPLES</span></span>

### <span data-ttu-id="c5a93-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c5a93-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="c5a93-109">為 'TestingNamespaceStandardMigration' 建立新移入組會至 'TestingNamespacePremiumMigration' 命名空間</span><span class="sxs-lookup"><span data-stu-id="c5a93-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="c5a93-110">參數</span><span class="sxs-lookup"><span data-stu-id="c5a93-110">PARAMETERS</span></span>

### <span data-ttu-id="c5a93-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5a93-111">-AsJob</span></span>
<span data-ttu-id="c5a93-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c5a93-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5a93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a93-113">-DefaultProfile</span></span>
<span data-ttu-id="c5a93-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5a93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5a93-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5a93-115">-Name</span></span>
<span data-ttu-id="c5a93-116">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c5a93-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a93-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="c5a93-117">-PostMigrationName</span></span>
<span data-ttu-id="c5a93-118">移移中標準命名空間的移後名稱</span><span class="sxs-lookup"><span data-stu-id="c5a93-118">Post Migration Name for Standard Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a93-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a93-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5a93-120">資源組名</span><span class="sxs-lookup"><span data-stu-id="c5a93-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a93-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="c5a93-121">-TargetNameSpace</span></span>
<span data-ttu-id="c5a93-122">進位命名空間 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="c5a93-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5a93-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c5a93-123">-Confirm</span></span>
<span data-ttu-id="c5a93-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c5a93-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5a93-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5a93-125">-WhatIf</span></span>
<span data-ttu-id="c5a93-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c5a93-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5a93-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c5a93-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5a93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a93-128">CommonParameters</span></span>
<span data-ttu-id="c5a93-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c5a93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a93-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c5a93-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a93-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c5a93-131">INPUTS</span></span>

### <span data-ttu-id="c5a93-132">沒有</span><span class="sxs-lookup"><span data-stu-id="c5a93-132">None</span></span>

## <span data-ttu-id="c5a93-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c5a93-133">OUTPUTS</span></span>

### <span data-ttu-id="c5a93-134">Microsoft.Azure.Commands.ServiceBus.models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c5a93-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="c5a93-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c5a93-135">NOTES</span></span>

## <span data-ttu-id="c5a93-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5a93-136">RELATED LINKS</span></span>

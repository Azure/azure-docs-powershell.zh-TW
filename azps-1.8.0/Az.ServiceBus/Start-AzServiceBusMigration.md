---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 66d8f15c58d1b4b92f19e23f5940ed7c8ba45d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620580"
---
# <span data-ttu-id="23e43-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="23e43-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="23e43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23e43-102">SYNOPSIS</span></span>
<span data-ttu-id="23e43-103">建立新的遷移設定，並開始從標準到 Premium 命名空間將實體遷移</span><span class="sxs-lookup"><span data-stu-id="23e43-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="23e43-104">句法</span><span class="sxs-lookup"><span data-stu-id="23e43-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23e43-105">說明</span><span class="sxs-lookup"><span data-stu-id="23e43-105">DESCRIPTION</span></span>
<span data-ttu-id="23e43-106">**AzServiceBusMigration** Cmdlet 會建立新的遷移設定，並開始從標準到 Premium 命名空間將實體遷移</span><span class="sxs-lookup"><span data-stu-id="23e43-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="23e43-107">示例</span><span class="sxs-lookup"><span data-stu-id="23e43-107">EXAMPLES</span></span>

### <span data-ttu-id="23e43-108">範例1</span><span class="sxs-lookup"><span data-stu-id="23e43-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="23e43-109">為 "TestingNamespaceStandardMirgation" 建立新的「TestingNamespacePremiumMirgation」命名空間的遷移設定</span><span class="sxs-lookup"><span data-stu-id="23e43-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="23e43-110">參數</span><span class="sxs-lookup"><span data-stu-id="23e43-110">PARAMETERS</span></span>

### <span data-ttu-id="23e43-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23e43-111">-AsJob</span></span>
<span data-ttu-id="23e43-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="23e43-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23e43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e43-113">-DefaultProfile</span></span>
<span data-ttu-id="23e43-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23e43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23e43-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="23e43-115">-Name</span></span>
<span data-ttu-id="23e43-116">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="23e43-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="23e43-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="23e43-117">-PostMigrationName</span></span>
<span data-ttu-id="23e43-118">在遷移中張貼 Standrad 命名空間的遷移名稱</span><span class="sxs-lookup"><span data-stu-id="23e43-118">Post Migration Name for Standrad Namespace in Migration</span></span>

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

### <span data-ttu-id="23e43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e43-119">-ResourceGroupName</span></span>
<span data-ttu-id="23e43-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="23e43-120">Resource Group Name</span></span>

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

### <span data-ttu-id="23e43-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="23e43-121">-TargetNameSpace</span></span>
<span data-ttu-id="23e43-122">Premium 命名空間 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="23e43-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="23e43-123">-確認</span><span class="sxs-lookup"><span data-stu-id="23e43-123">-Confirm</span></span>
<span data-ttu-id="23e43-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23e43-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e43-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e43-125">-WhatIf</span></span>
<span data-ttu-id="23e43-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23e43-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e43-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23e43-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e43-128">CommonParameters</span></span>
<span data-ttu-id="23e43-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23e43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e43-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23e43-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e43-131">輸入</span><span class="sxs-lookup"><span data-stu-id="23e43-131">INPUTS</span></span>

### <span data-ttu-id="23e43-132">所有</span><span class="sxs-lookup"><span data-stu-id="23e43-132">None</span></span>

## <span data-ttu-id="23e43-133">輸出</span><span class="sxs-lookup"><span data-stu-id="23e43-133">OUTPUTS</span></span>

### <span data-ttu-id="23e43-134">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="23e43-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="23e43-135">筆記</span><span class="sxs-lookup"><span data-stu-id="23e43-135">NOTES</span></span>

## <span data-ttu-id="23e43-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="23e43-136">RELATED LINKS</span></span>
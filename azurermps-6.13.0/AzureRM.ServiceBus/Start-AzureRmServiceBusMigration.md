---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/start-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
ms.openlocfilehash: 979db64fb11b4fffc901d96811b24be5c79f6b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449739"
---
# <span data-ttu-id="f91de-101">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f91de-101">Start-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="f91de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f91de-102">SYNOPSIS</span></span>
<span data-ttu-id="f91de-103">建立新的遷移設定，並開始從標準到 Premium 命名空間將實體遷移</span><span class="sxs-lookup"><span data-stu-id="f91de-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f91de-104">句法</span><span class="sxs-lookup"><span data-stu-id="f91de-104">SYNTAX</span></span>

```
Start-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f91de-105">說明</span><span class="sxs-lookup"><span data-stu-id="f91de-105">DESCRIPTION</span></span>
<span data-ttu-id="f91de-106">**AzureRmServiceBusMigration** Cmdlet 會建立新的遷移設定，並開始從標準到 Premium 命名空間將實體遷移</span><span class="sxs-lookup"><span data-stu-id="f91de-106">The **Start-AzureRmServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="f91de-107">示例</span><span class="sxs-lookup"><span data-stu-id="f91de-107">EXAMPLES</span></span>

### <span data-ttu-id="f91de-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f91de-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="f91de-109">為 "TestingNamespaceStandardMirgation" 建立新的「TestingNamespacePremiumMirgation」命名空間的遷移設定</span><span class="sxs-lookup"><span data-stu-id="f91de-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="f91de-110">參數</span><span class="sxs-lookup"><span data-stu-id="f91de-110">PARAMETERS</span></span>

### <span data-ttu-id="f91de-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f91de-111">-AsJob</span></span>
<span data-ttu-id="f91de-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f91de-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f91de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91de-113">-DefaultProfile</span></span>
<span data-ttu-id="f91de-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f91de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f91de-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f91de-115">-Name</span></span>
<span data-ttu-id="f91de-116">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f91de-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="f91de-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="f91de-117">-PostMigrationName</span></span>
<span data-ttu-id="f91de-118">在遷移中張貼 Standrad 命名空間的遷移名稱</span><span class="sxs-lookup"><span data-stu-id="f91de-118">Post Migration Name for Standrad Namespace in Migration</span></span>

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

### <span data-ttu-id="f91de-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91de-119">-ResourceGroupName</span></span>
<span data-ttu-id="f91de-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f91de-120">Resource Group Name</span></span>

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

### <span data-ttu-id="f91de-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="f91de-121">-TargetNameSpace</span></span>
<span data-ttu-id="f91de-122">Premium 命名空間 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="f91de-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="f91de-123">-確認</span><span class="sxs-lookup"><span data-stu-id="f91de-123">-Confirm</span></span>
<span data-ttu-id="f91de-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f91de-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f91de-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f91de-125">-WhatIf</span></span>
<span data-ttu-id="f91de-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f91de-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f91de-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f91de-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f91de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91de-128">CommonParameters</span></span>
<span data-ttu-id="f91de-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f91de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91de-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f91de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91de-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f91de-131">INPUTS</span></span>

### <span data-ttu-id="f91de-132">所有</span><span class="sxs-lookup"><span data-stu-id="f91de-132">None</span></span>

## <span data-ttu-id="f91de-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f91de-133">OUTPUTS</span></span>

### <span data-ttu-id="f91de-134">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f91de-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f91de-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f91de-135">NOTES</span></span>

## <span data-ttu-id="f91de-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f91de-136">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448384"
---
# <span data-ttu-id="62c1c-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="62c1c-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="62c1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="62c1c-103">Cmdlet 會刪除標準至 Premium 命名空間的遷移配置</span><span class="sxs-lookup"><span data-stu-id="62c1c-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="62c1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="62c1c-104">SYNTAX</span></span>

### <span data-ttu-id="62c1c-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="62c1c-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c1c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62c1c-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c1c-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62c1c-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62c1c-108">說明</span><span class="sxs-lookup"><span data-stu-id="62c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="62c1c-109">**AzServiceBusMigration** Cmdlet 會刪除標準到 Premium 命名空間的遷移配置</span><span class="sxs-lookup"><span data-stu-id="62c1c-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="62c1c-110">示例</span><span class="sxs-lookup"><span data-stu-id="62c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="62c1c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="62c1c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="62c1c-112">刪除 [TestingNamespaceStandardMigration] 遷移設定</span><span class="sxs-lookup"><span data-stu-id="62c1c-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="62c1c-113">參數</span><span class="sxs-lookup"><span data-stu-id="62c1c-113">PARAMETERS</span></span>

### <span data-ttu-id="62c1c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62c1c-114">-AsJob</span></span>
<span data-ttu-id="62c1c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="62c1c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62c1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c1c-116">-DefaultProfile</span></span>
<span data-ttu-id="62c1c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62c1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62c1c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62c1c-118">-InputObject</span></span>
<span data-ttu-id="62c1c-119">服務匯流排遷移標準命名空間物件</span><span class="sxs-lookup"><span data-stu-id="62c1c-119">Service Bus Migration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62c1c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="62c1c-120">-Name</span></span>
<span data-ttu-id="62c1c-121">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="62c1c-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="62c1c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62c1c-122">-PassThru</span></span>
<span data-ttu-id="62c1c-123">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="62c1c-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="62c1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="62c1c-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="62c1c-125">Resource Group Name</span></span>

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

### <span data-ttu-id="62c1c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62c1c-126">-ResourceId</span></span>
<span data-ttu-id="62c1c-127">服務匯流排遷移標準命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="62c1c-127">Service Bus Migration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c1c-128">-確認</span><span class="sxs-lookup"><span data-stu-id="62c1c-128">-Confirm</span></span>
<span data-ttu-id="62c1c-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62c1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c1c-130">-WhatIf</span></span>
<span data-ttu-id="62c1c-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62c1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c1c-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62c1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c1c-133">CommonParameters</span></span>
<span data-ttu-id="62c1c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62c1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c1c-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62c1c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c1c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="62c1c-136">INPUTS</span></span>

### <span data-ttu-id="62c1c-137">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="62c1c-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="62c1c-138">System.object</span><span class="sxs-lookup"><span data-stu-id="62c1c-138">System.String</span></span>

## <span data-ttu-id="62c1c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="62c1c-139">OUTPUTS</span></span>

### <span data-ttu-id="62c1c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="62c1c-140">System.Boolean</span></span>

## <span data-ttu-id="62c1c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="62c1c-141">NOTES</span></span>

## <span data-ttu-id="62c1c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="62c1c-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 9e53dab771486758cbd57c8f5c530a458df655d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901658"
---
# <span data-ttu-id="66901-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="66901-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="66901-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66901-102">SYNOPSIS</span></span>
<span data-ttu-id="66901-103">Cmdlet 會刪除標準到進一步命名空間的移轉組</span><span class="sxs-lookup"><span data-stu-id="66901-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="66901-104">語法</span><span class="sxs-lookup"><span data-stu-id="66901-104">SYNTAX</span></span>

### <span data-ttu-id="66901-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="66901-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66901-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66901-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66901-107">命名空間ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66901-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66901-108">描述</span><span class="sxs-lookup"><span data-stu-id="66901-108">DESCRIPTION</span></span>
<span data-ttu-id="66901-109">**Remove-AzServiceBusMigration Cmdlet** 會刪除標準到進一步命名空間的移轉組</span><span class="sxs-lookup"><span data-stu-id="66901-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="66901-110">例子</span><span class="sxs-lookup"><span data-stu-id="66901-110">EXAMPLES</span></span>

### <span data-ttu-id="66901-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="66901-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="66901-112">刪除 'TestingNamespaceStandardMigration' 移移組</span><span class="sxs-lookup"><span data-stu-id="66901-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="66901-113">參數</span><span class="sxs-lookup"><span data-stu-id="66901-113">PARAMETERS</span></span>

### <span data-ttu-id="66901-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66901-114">-AsJob</span></span>
<span data-ttu-id="66901-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="66901-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66901-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66901-116">-DefaultProfile</span></span>
<span data-ttu-id="66901-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="66901-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66901-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66901-118">-InputObject</span></span>
<span data-ttu-id="66901-119">Service Bus Migration 標準命名空間物件</span><span class="sxs-lookup"><span data-stu-id="66901-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="66901-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="66901-120">-Name</span></span>
<span data-ttu-id="66901-121">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="66901-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="66901-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66901-122">-PassThru</span></span>
<span data-ttu-id="66901-123">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="66901-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="66901-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66901-124">-ResourceGroupName</span></span>
<span data-ttu-id="66901-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="66901-125">Resource Group Name</span></span>

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

### <span data-ttu-id="66901-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66901-126">-ResourceId</span></span>
<span data-ttu-id="66901-127">Service Bus Migration 標準命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="66901-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="66901-128">-確認</span><span class="sxs-lookup"><span data-stu-id="66901-128">-Confirm</span></span>
<span data-ttu-id="66901-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="66901-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66901-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66901-130">-WhatIf</span></span>
<span data-ttu-id="66901-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66901-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66901-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66901-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66901-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66901-133">CommonParameters</span></span>
<span data-ttu-id="66901-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66901-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66901-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="66901-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66901-136">輸入</span><span class="sxs-lookup"><span data-stu-id="66901-136">INPUTS</span></span>

### <span data-ttu-id="66901-137">Microsoft.Azure.Commands.ServiceBus.models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="66901-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="66901-138">System.String</span><span class="sxs-lookup"><span data-stu-id="66901-138">System.String</span></span>

## <span data-ttu-id="66901-139">輸出</span><span class="sxs-lookup"><span data-stu-id="66901-139">OUTPUTS</span></span>

### <span data-ttu-id="66901-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66901-140">System.Boolean</span></span>

## <span data-ttu-id="66901-141">筆記</span><span class="sxs-lookup"><span data-stu-id="66901-141">NOTES</span></span>

## <span data-ttu-id="66901-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="66901-142">RELATED LINKS</span></span>

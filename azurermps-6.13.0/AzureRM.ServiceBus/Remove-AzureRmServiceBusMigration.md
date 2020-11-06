---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448215"
---
# <span data-ttu-id="caada-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="caada-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="caada-102">摘要</span><span class="sxs-lookup"><span data-stu-id="caada-102">SYNOPSIS</span></span>
<span data-ttu-id="caada-103">Cmdlet 會刪除標準至 Premium 命名空間的遷移配置</span><span class="sxs-lookup"><span data-stu-id="caada-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caada-104">句法</span><span class="sxs-lookup"><span data-stu-id="caada-104">SYNTAX</span></span>

### <span data-ttu-id="caada-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="caada-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caada-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="caada-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caada-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="caada-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caada-108">說明</span><span class="sxs-lookup"><span data-stu-id="caada-108">DESCRIPTION</span></span>
<span data-ttu-id="caada-109">**AzureRmServiceBusMigration** Cmdlet 會刪除標準到 Premium 命名空間的遷移配置</span><span class="sxs-lookup"><span data-stu-id="caada-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="caada-110">示例</span><span class="sxs-lookup"><span data-stu-id="caada-110">EXAMPLES</span></span>

### <span data-ttu-id="caada-111">範例1</span><span class="sxs-lookup"><span data-stu-id="caada-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="caada-112">刪除 [TestingNamespaceStandardMirgation] 遷移設定</span><span class="sxs-lookup"><span data-stu-id="caada-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="caada-113">參數</span><span class="sxs-lookup"><span data-stu-id="caada-113">PARAMETERS</span></span>

### <span data-ttu-id="caada-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="caada-114">-AsJob</span></span>
<span data-ttu-id="caada-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="caada-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="caada-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caada-116">-DefaultProfile</span></span>
<span data-ttu-id="caada-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="caada-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caada-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caada-118">-InputObject</span></span>
<span data-ttu-id="caada-119">服務匯流排遷移標準命名空間物件</span><span class="sxs-lookup"><span data-stu-id="caada-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="caada-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="caada-120">-Name</span></span>
<span data-ttu-id="caada-121">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="caada-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="caada-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="caada-122">-PassThru</span></span>
<span data-ttu-id="caada-123">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="caada-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="caada-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caada-124">-ResourceGroupName</span></span>
<span data-ttu-id="caada-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="caada-125">Resource Group Name</span></span>

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

### <span data-ttu-id="caada-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="caada-126">-ResourceId</span></span>
<span data-ttu-id="caada-127">服務匯流排遷移標準命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="caada-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="caada-128">-確認</span><span class="sxs-lookup"><span data-stu-id="caada-128">-Confirm</span></span>
<span data-ttu-id="caada-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="caada-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caada-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caada-130">-WhatIf</span></span>
<span data-ttu-id="caada-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="caada-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caada-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="caada-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caada-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caada-133">CommonParameters</span></span>
<span data-ttu-id="caada-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="caada-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caada-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="caada-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caada-136">輸入</span><span class="sxs-lookup"><span data-stu-id="caada-136">INPUTS</span></span>

### <span data-ttu-id="caada-137">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="caada-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="caada-138">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="caada-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="caada-139">System.object</span><span class="sxs-lookup"><span data-stu-id="caada-139">System.String</span></span>

## <span data-ttu-id="caada-140">輸出</span><span class="sxs-lookup"><span data-stu-id="caada-140">OUTPUTS</span></span>

### <span data-ttu-id="caada-141">System.object</span><span class="sxs-lookup"><span data-stu-id="caada-141">System.Boolean</span></span>

## <span data-ttu-id="caada-142">筆記</span><span class="sxs-lookup"><span data-stu-id="caada-142">NOTES</span></span>

## <span data-ttu-id="caada-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="caada-143">RELATED LINKS</span></span>

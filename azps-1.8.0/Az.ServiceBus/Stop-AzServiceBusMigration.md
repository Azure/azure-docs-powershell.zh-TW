---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: c507caa0ce6697132876309a7ae816802a682683
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620578"
---
# <span data-ttu-id="99ecb-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="99ecb-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="99ecb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="99ecb-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="99ecb-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="99ecb-104">句法</span><span class="sxs-lookup"><span data-stu-id="99ecb-104">SYNTAX</span></span>

### <span data-ttu-id="99ecb-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="99ecb-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ecb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="99ecb-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99ecb-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99ecb-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99ecb-108">說明</span><span class="sxs-lookup"><span data-stu-id="99ecb-108">DESCRIPTION</span></span>
<span data-ttu-id="99ecb-109">**Stop AzServiceBusMigration** Cmdlet 會終止從標準到 premium 命名空間之間的遷移</span><span class="sxs-lookup"><span data-stu-id="99ecb-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="99ecb-110">示例</span><span class="sxs-lookup"><span data-stu-id="99ecb-110">EXAMPLES</span></span>

### <span data-ttu-id="99ecb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="99ecb-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="99ecb-112">Cmdlet 會在建立遷移設定時，終止標準命名空間與 Premium 命名空間之間的遷移。</span><span class="sxs-lookup"><span data-stu-id="99ecb-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="99ecb-113">參數</span><span class="sxs-lookup"><span data-stu-id="99ecb-113">PARAMETERS</span></span>

### <span data-ttu-id="99ecb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ecb-114">-DefaultProfile</span></span>
<span data-ttu-id="99ecb-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99ecb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99ecb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99ecb-116">-InputObject</span></span>
<span data-ttu-id="99ecb-117">服務匯流排遷移設定標準命名空間物件</span><span class="sxs-lookup"><span data-stu-id="99ecb-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="99ecb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="99ecb-118">-Name</span></span>
<span data-ttu-id="99ecb-119">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="99ecb-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="99ecb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99ecb-120">-PassThru</span></span>
<span data-ttu-id="99ecb-121">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="99ecb-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="99ecb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ecb-122">-ResourceGroupName</span></span>
<span data-ttu-id="99ecb-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="99ecb-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ecb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99ecb-124">-ResourceId</span></span>
<span data-ttu-id="99ecb-125">服務匯流排遷移設定標準命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="99ecb-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="99ecb-126">-確認</span><span class="sxs-lookup"><span data-stu-id="99ecb-126">-Confirm</span></span>
<span data-ttu-id="99ecb-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99ecb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ecb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ecb-128">-WhatIf</span></span>
<span data-ttu-id="99ecb-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99ecb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ecb-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99ecb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ecb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ecb-131">CommonParameters</span></span>
<span data-ttu-id="99ecb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99ecb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ecb-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99ecb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ecb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="99ecb-134">INPUTS</span></span>

### <span data-ttu-id="99ecb-135">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="99ecb-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="99ecb-136">System.object</span><span class="sxs-lookup"><span data-stu-id="99ecb-136">System.String</span></span>

## <span data-ttu-id="99ecb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="99ecb-137">OUTPUTS</span></span>

### <span data-ttu-id="99ecb-138">System.object</span><span class="sxs-lookup"><span data-stu-id="99ecb-138">System.Boolean</span></span>

## <span data-ttu-id="99ecb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="99ecb-139">NOTES</span></span>

## <span data-ttu-id="99ecb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="99ecb-140">RELATED LINKS</span></span>

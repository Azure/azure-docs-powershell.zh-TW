---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 843ca61427d8aa5c2eea3d91f0dd8e5c22bb847f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620661"
---
# <span data-ttu-id="26f92-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="26f92-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="26f92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26f92-102">SYNOPSIS</span></span>
<span data-ttu-id="26f92-103">Cmdlet 將 [從標準到 premium] 命名空間的遷移設定為完成，而標準命名空間的連線字串現在指向 [Premium 命名空間]</span><span class="sxs-lookup"><span data-stu-id="26f92-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="26f92-104">句法</span><span class="sxs-lookup"><span data-stu-id="26f92-104">SYNTAX</span></span>

### <span data-ttu-id="26f92-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="26f92-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f92-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="26f92-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f92-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f92-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26f92-108">說明</span><span class="sxs-lookup"><span data-stu-id="26f92-108">DESCRIPTION</span></span>
<span data-ttu-id="26f92-109">**完整 AzServiceBusMigration** Cmdlet 會將從標準命名空間遷移到 premium 命名空間，因為標準命名空間的完整和連接字串現在指向 premium 命名空間</span><span class="sxs-lookup"><span data-stu-id="26f92-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="26f92-110">示例</span><span class="sxs-lookup"><span data-stu-id="26f92-110">EXAMPLES</span></span>

### <span data-ttu-id="26f92-111">範例1</span><span class="sxs-lookup"><span data-stu-id="26f92-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="26f92-112">將 [NamespaceStandardMirgation] 命名空間的遷移設定為完成。</span><span class="sxs-lookup"><span data-stu-id="26f92-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="26f92-113">參數</span><span class="sxs-lookup"><span data-stu-id="26f92-113">PARAMETERS</span></span>

### <span data-ttu-id="26f92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f92-114">-DefaultProfile</span></span>
<span data-ttu-id="26f92-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26f92-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f92-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26f92-116">-InputObject</span></span>
<span data-ttu-id="26f92-117">服務匯流排遷移配置-標準命名空間物件</span><span class="sxs-lookup"><span data-stu-id="26f92-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="26f92-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="26f92-118">-Name</span></span>
<span data-ttu-id="26f92-119">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="26f92-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="26f92-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26f92-120">-PassThru</span></span>
<span data-ttu-id="26f92-121">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="26f92-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="26f92-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f92-122">-ResourceGroupName</span></span>
<span data-ttu-id="26f92-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="26f92-123">Resource Group Name</span></span>

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

### <span data-ttu-id="26f92-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26f92-124">-ResourceId</span></span>
<span data-ttu-id="26f92-125">服務匯流排 Migratio-標準命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="26f92-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="26f92-126">-確認</span><span class="sxs-lookup"><span data-stu-id="26f92-126">-Confirm</span></span>
<span data-ttu-id="26f92-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26f92-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f92-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f92-128">-WhatIf</span></span>
<span data-ttu-id="26f92-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26f92-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f92-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f92-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f92-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f92-131">CommonParameters</span></span>
<span data-ttu-id="26f92-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26f92-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f92-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26f92-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f92-134">輸入</span><span class="sxs-lookup"><span data-stu-id="26f92-134">INPUTS</span></span>

### <span data-ttu-id="26f92-135">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="26f92-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="26f92-136">System.object</span><span class="sxs-lookup"><span data-stu-id="26f92-136">System.String</span></span>

## <span data-ttu-id="26f92-137">輸出</span><span class="sxs-lookup"><span data-stu-id="26f92-137">OUTPUTS</span></span>

### <span data-ttu-id="26f92-138">System.object</span><span class="sxs-lookup"><span data-stu-id="26f92-138">System.Boolean</span></span>

## <span data-ttu-id="26f92-139">筆記</span><span class="sxs-lookup"><span data-stu-id="26f92-139">NOTES</span></span>

## <span data-ttu-id="26f92-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f92-140">RELATED LINKS</span></span>

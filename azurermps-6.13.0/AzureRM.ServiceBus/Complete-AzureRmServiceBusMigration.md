---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/complete-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
ms.openlocfilehash: 0006e4768dc27994d18e93e48696b5ee9a514c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625245"
---
# <span data-ttu-id="f1071-101">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f1071-101">Complete-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="f1071-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1071-102">SYNOPSIS</span></span>
<span data-ttu-id="f1071-103">Cmdlet 將 [從標準到 premium] 命名空間的遷移設定為完成，而標準命名空間的連線字串現在指向 [Premium 命名空間]</span><span class="sxs-lookup"><span data-stu-id="f1071-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1071-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1071-104">SYNTAX</span></span>

### <span data-ttu-id="f1071-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f1071-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1071-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f1071-106">NamespaceInputObjectSet</span></span>
```
Complete-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1071-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1071-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1071-108">說明</span><span class="sxs-lookup"><span data-stu-id="f1071-108">DESCRIPTION</span></span>
<span data-ttu-id="f1071-109">**完整 AzureRmServiceBusMigration** Cmdlet 會將從標準命名空間遷移到 premium 命名空間，因為標準命名空間的完整和連接字串現在指向 premium 命名空間</span><span class="sxs-lookup"><span data-stu-id="f1071-109">The **Complete-AzureRmServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="f1071-110">示例</span><span class="sxs-lookup"><span data-stu-id="f1071-110">EXAMPLES</span></span>

### <span data-ttu-id="f1071-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f1071-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="f1071-112">將 [NamespaceStandardMirgation] 命名空間的遷移設定為完成。</span><span class="sxs-lookup"><span data-stu-id="f1071-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="f1071-113">參數</span><span class="sxs-lookup"><span data-stu-id="f1071-113">PARAMETERS</span></span>

### <span data-ttu-id="f1071-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1071-114">-DefaultProfile</span></span>
<span data-ttu-id="f1071-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1071-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1071-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1071-116">-InputObject</span></span>
<span data-ttu-id="f1071-117">服務匯流排遷移配置-標準命名空間物件</span><span class="sxs-lookup"><span data-stu-id="f1071-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="f1071-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1071-118">-Name</span></span>
<span data-ttu-id="f1071-119">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="f1071-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="f1071-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1071-120">-PassThru</span></span>
<span data-ttu-id="f1071-121">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="f1071-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f1071-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1071-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1071-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f1071-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f1071-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1071-124">-ResourceId</span></span>
<span data-ttu-id="f1071-125">服務匯流排 Migratio-標準命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f1071-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="f1071-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f1071-126">-Confirm</span></span>
<span data-ttu-id="f1071-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1071-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1071-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1071-128">-WhatIf</span></span>
<span data-ttu-id="f1071-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1071-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1071-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1071-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1071-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1071-131">CommonParameters</span></span>
<span data-ttu-id="f1071-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1071-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1071-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1071-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1071-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f1071-134">INPUTS</span></span>

### <span data-ttu-id="f1071-135">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f1071-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="f1071-136">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f1071-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f1071-137">System.object</span><span class="sxs-lookup"><span data-stu-id="f1071-137">System.String</span></span>

## <span data-ttu-id="f1071-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f1071-138">OUTPUTS</span></span>

### <span data-ttu-id="f1071-139">System.object</span><span class="sxs-lookup"><span data-stu-id="f1071-139">System.Boolean</span></span>

## <span data-ttu-id="f1071-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f1071-140">NOTES</span></span>

## <span data-ttu-id="f1071-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1071-141">RELATED LINKS</span></span>

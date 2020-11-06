---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Start-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: a8440ddc7249068486f94c30e28e1b1be2e2413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457052"
---
# <span data-ttu-id="e17c8-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e17c8-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="e17c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e17c8-102">SYNOPSIS</span></span>
<span data-ttu-id="e17c8-103">在已停止的狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="e17c8-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e17c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e17c8-104">SYNTAX</span></span>

### <span data-ttu-id="e17c8-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e17c8-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e17c8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e17c8-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e17c8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e17c8-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e17c8-108">說明</span><span class="sxs-lookup"><span data-stu-id="e17c8-108">DESCRIPTION</span></span>
<span data-ttu-id="e17c8-109">Start-AzureRmDataMigrationService Cmdlet 會在停止狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="e17c8-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="e17c8-110">示例</span><span class="sxs-lookup"><span data-stu-id="e17c8-110">EXAMPLES</span></span>

### <span data-ttu-id="e17c8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e17c8-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="e17c8-112">上述範例會根據以輸入的服務名稱，在停止狀態中啟動名為 Test 服務的 Azure 資料庫移轉服務實例</span><span class="sxs-lookup"><span data-stu-id="e17c8-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="e17c8-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e17c8-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="e17c8-114">上述範例會根據以輸入參數傳入的 PSDataMigrationService 來啟動 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="e17c8-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="e17c8-115">參數</span><span class="sxs-lookup"><span data-stu-id="e17c8-115">PARAMETERS</span></span>

### <span data-ttu-id="e17c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17c8-116">-DefaultProfile</span></span>
<span data-ttu-id="e17c8-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e17c8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e17c8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e17c8-118">-InputObject</span></span>
<span data-ttu-id="e17c8-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="e17c8-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e17c8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e17c8-120">-Name</span></span>
<span data-ttu-id="e17c8-121">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e17c8-121">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17c8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e17c8-122">-PassThru</span></span>
<span data-ttu-id="e17c8-123">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="e17c8-123">Returns an true/false.</span></span>
<span data-ttu-id="e17c8-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e17c8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e17c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e17c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="e17c8-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e17c8-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17c8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e17c8-127">-ResourceId</span></span>
<span data-ttu-id="e17c8-128">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e17c8-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="e17c8-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e17c8-129">-Confirm</span></span>
<span data-ttu-id="e17c8-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e17c8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e17c8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e17c8-131">-WhatIf</span></span>
<span data-ttu-id="e17c8-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e17c8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e17c8-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e17c8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e17c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17c8-134">CommonParameters</span></span>
<span data-ttu-id="e17c8-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e17c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17c8-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e17c8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17c8-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e17c8-137">INPUTS</span></span>

### <span data-ttu-id="e17c8-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e17c8-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="e17c8-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e17c8-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e17c8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e17c8-140">System.String</span></span>

## <span data-ttu-id="e17c8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e17c8-141">OUTPUTS</span></span>

### <span data-ttu-id="e17c8-142">System.object</span><span class="sxs-lookup"><span data-stu-id="e17c8-142">System.Boolean</span></span>

## <span data-ttu-id="e17c8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e17c8-143">NOTES</span></span>

## <span data-ttu-id="e17c8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e17c8-144">RELATED LINKS</span></span>

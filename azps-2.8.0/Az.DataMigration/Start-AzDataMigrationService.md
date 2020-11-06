---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 67194bfc9a7ce1971817c7f80e7a5ee61caf6db0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612692"
---
# <span data-ttu-id="cedfd-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cedfd-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="cedfd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cedfd-102">SYNOPSIS</span></span>
<span data-ttu-id="cedfd-103">在已停止的狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="cedfd-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="cedfd-104">句法</span><span class="sxs-lookup"><span data-stu-id="cedfd-104">SYNTAX</span></span>

### <span data-ttu-id="cedfd-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cedfd-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cedfd-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cedfd-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cedfd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cedfd-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cedfd-108">說明</span><span class="sxs-lookup"><span data-stu-id="cedfd-108">DESCRIPTION</span></span>
<span data-ttu-id="cedfd-109">Start-AzDataMigrationService Cmdlet 會在停止狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="cedfd-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="cedfd-110">示例</span><span class="sxs-lookup"><span data-stu-id="cedfd-110">EXAMPLES</span></span>

### <span data-ttu-id="cedfd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cedfd-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="cedfd-112">上述範例會根據以輸入的服務名稱，在停止狀態中啟動名為 Test 服務的 Azure 資料庫移轉服務實例</span><span class="sxs-lookup"><span data-stu-id="cedfd-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="cedfd-113">範例2</span><span class="sxs-lookup"><span data-stu-id="cedfd-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="cedfd-114">上述範例會根據以輸入參數傳入的 PSDataMigrationService 來啟動 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="cedfd-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="cedfd-115">參數</span><span class="sxs-lookup"><span data-stu-id="cedfd-115">PARAMETERS</span></span>

### <span data-ttu-id="cedfd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cedfd-116">-DefaultProfile</span></span>
<span data-ttu-id="cedfd-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cedfd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cedfd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cedfd-118">-InputObject</span></span>
<span data-ttu-id="cedfd-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="cedfd-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="cedfd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cedfd-120">-Name</span></span>
<span data-ttu-id="cedfd-121">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="cedfd-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="cedfd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cedfd-122">-PassThru</span></span>
<span data-ttu-id="cedfd-123">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="cedfd-123">Returns an true/false.</span></span>
<span data-ttu-id="cedfd-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cedfd-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cedfd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cedfd-125">-ResourceGroupName</span></span>
<span data-ttu-id="cedfd-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cedfd-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="cedfd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cedfd-127">-ResourceId</span></span>
<span data-ttu-id="cedfd-128">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cedfd-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="cedfd-129">-確認</span><span class="sxs-lookup"><span data-stu-id="cedfd-129">-Confirm</span></span>
<span data-ttu-id="cedfd-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cedfd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cedfd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cedfd-131">-WhatIf</span></span>
<span data-ttu-id="cedfd-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cedfd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cedfd-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cedfd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cedfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cedfd-134">CommonParameters</span></span>
<span data-ttu-id="cedfd-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cedfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cedfd-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cedfd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cedfd-137">輸入</span><span class="sxs-lookup"><span data-stu-id="cedfd-137">INPUTS</span></span>

### <span data-ttu-id="cedfd-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cedfd-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="cedfd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="cedfd-139">System.String</span></span>

## <span data-ttu-id="cedfd-140">輸出</span><span class="sxs-lookup"><span data-stu-id="cedfd-140">OUTPUTS</span></span>

### <span data-ttu-id="cedfd-141">System.object</span><span class="sxs-lookup"><span data-stu-id="cedfd-141">System.Boolean</span></span>

## <span data-ttu-id="cedfd-142">筆記</span><span class="sxs-lookup"><span data-stu-id="cedfd-142">NOTES</span></span>

## <span data-ttu-id="cedfd-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="cedfd-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationService.md
ms.openlocfilehash: 313748a0d674146ae0442174ee50a7069f55b9b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913558"
---
# <span data-ttu-id="dd724-101">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="dd724-101">Remove-AzDataMigrationService</span></span>

## <span data-ttu-id="dd724-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd724-102">SYNOPSIS</span></span>
<span data-ttu-id="dd724-103">從 Azure 移除 Azure 資料庫移移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="dd724-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

## <span data-ttu-id="dd724-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd724-104">SYNTAX</span></span>

### <span data-ttu-id="dd724-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dd724-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd724-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd724-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd724-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd724-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd724-108">描述</span><span class="sxs-lookup"><span data-stu-id="dd724-108">DESCRIPTION</span></span>
<span data-ttu-id="dd724-109">此Remove-AzDataMigrationService Cmdlet 會從 Azure 移除 Azure 資料庫移轉服務的實例。</span><span class="sxs-lookup"><span data-stu-id="dd724-109">The Remove-AzDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="dd724-110">提供 DeleteRunningTask 參數會移除所有與要移除之服務相關聯的 Azure 資料庫移移服務工作。</span><span class="sxs-lookup"><span data-stu-id="dd724-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="dd724-111">例子</span><span class="sxs-lookup"><span data-stu-id="dd724-111">EXAMPLES</span></span>

### <span data-ttu-id="dd724-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="dd724-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="dd724-113">上述範例會移除名為 TestService 的 Azure 資料庫移移服務實例，該實例包含在名為 MyResourceGroup 的 Azure 資源群組中。</span><span class="sxs-lookup"><span data-stu-id="dd724-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="dd724-114">參數</span><span class="sxs-lookup"><span data-stu-id="dd724-114">PARAMETERS</span></span>

### <span data-ttu-id="dd724-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd724-115">-DefaultProfile</span></span>
<span data-ttu-id="dd724-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd724-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd724-117">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="dd724-117">-DeleteRunningTask</span></span>
<span data-ttu-id="dd724-118">刪除任何執行中的工作</span><span class="sxs-lookup"><span data-stu-id="dd724-118">Delete any running task</span></span>

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

### <span data-ttu-id="dd724-119">-強制</span><span class="sxs-lookup"><span data-stu-id="dd724-119">-Force</span></span>
<span data-ttu-id="dd724-120">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="dd724-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="dd724-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd724-121">-InputObject</span></span>
<span data-ttu-id="dd724-122">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="dd724-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="dd724-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd724-123">-Name</span></span>
<span data-ttu-id="dd724-124">資料庫移移服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd724-124">The name of the Database Migration Service.</span></span>

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

### <span data-ttu-id="dd724-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd724-125">-PassThru</span></span>
<span data-ttu-id="dd724-126">會返回 true/false。</span><span class="sxs-lookup"><span data-stu-id="dd724-126">Returns an true/false.</span></span>
<span data-ttu-id="dd724-127">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="dd724-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd724-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd724-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd724-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd724-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd724-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd724-130">-ResourceId</span></span>
<span data-ttu-id="dd724-131">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd724-131">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="dd724-132">-確認</span><span class="sxs-lookup"><span data-stu-id="dd724-132">-Confirm</span></span>
<span data-ttu-id="dd724-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dd724-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd724-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd724-134">-WhatIf</span></span>
<span data-ttu-id="dd724-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd724-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd724-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd724-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd724-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd724-137">CommonParameters</span></span>
<span data-ttu-id="dd724-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd724-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd724-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dd724-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd724-140">輸入</span><span class="sxs-lookup"><span data-stu-id="dd724-140">INPUTS</span></span>

### <span data-ttu-id="dd724-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="dd724-141">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="dd724-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dd724-142">System.String</span></span>

## <span data-ttu-id="dd724-143">輸出</span><span class="sxs-lookup"><span data-stu-id="dd724-143">OUTPUTS</span></span>

### <span data-ttu-id="dd724-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd724-144">System.Boolean</span></span>

## <span data-ttu-id="dd724-145">筆記</span><span class="sxs-lookup"><span data-stu-id="dd724-145">NOTES</span></span>

## <span data-ttu-id="dd724-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd724-146">RELATED LINKS</span></span>

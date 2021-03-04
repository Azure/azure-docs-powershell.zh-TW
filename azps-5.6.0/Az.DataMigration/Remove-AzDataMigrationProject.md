---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Remove-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Remove-AzDataMigrationProject.md
ms.openlocfilehash: 449a1cfc3156b647eccee6fc320f41fa9e53549c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916752"
---
# <span data-ttu-id="00259-101">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="00259-101">Remove-AzDataMigrationProject</span></span>

## <span data-ttu-id="00259-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00259-102">SYNOPSIS</span></span>
<span data-ttu-id="00259-103">從 Azure 移除 Azure 資料庫移移服務專案。</span><span class="sxs-lookup"><span data-stu-id="00259-103">Removes an Azure Database Migration Service project from Azure.</span></span>

## <span data-ttu-id="00259-104">語法</span><span class="sxs-lookup"><span data-stu-id="00259-104">SYNTAX</span></span>

### <span data-ttu-id="00259-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="00259-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00259-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00259-106">ComponentObjectParameterSet</span></span>
```
Remove-AzDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00259-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00259-107">ResourceIdParameterSet</span></span>
```
Remove-AzDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00259-108">描述</span><span class="sxs-lookup"><span data-stu-id="00259-108">DESCRIPTION</span></span>
<span data-ttu-id="00259-109">此Remove-AzDataMigrationProject Cmdlet 會從 Azure 移除 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="00259-109">The Remove-AzDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="00259-110">提供 DeleteRunningTask 參數會移除與要移除之專案相關聯的所有 Azure 資料庫移移服務工作。</span><span class="sxs-lookup"><span data-stu-id="00259-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="00259-111">例子</span><span class="sxs-lookup"><span data-stu-id="00259-111">EXAMPLES</span></span>

### <span data-ttu-id="00259-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="00259-112">Example 1</span></span>
```
PS C:\> Remove-AzDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="00259-113">上述範例會根據名稱做為輸入參數，從 Azure 移除名為 myDMProject 的 Azure 資料庫移移服務專案</span><span class="sxs-lookup"><span data-stu-id="00259-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="00259-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="00259-114">Example 2</span></span>
```
PS C:\> Remove-AzDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="00259-115">上述範例會移除以 PSProject 物件做為輸入參數的 Azure 資料庫移移服務專案。</span><span class="sxs-lookup"><span data-stu-id="00259-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="00259-116">參數</span><span class="sxs-lookup"><span data-stu-id="00259-116">PARAMETERS</span></span>

### <span data-ttu-id="00259-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00259-117">-DefaultProfile</span></span>
<span data-ttu-id="00259-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00259-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00259-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="00259-119">-DeleteRunningTask</span></span>
<span data-ttu-id="00259-120">刪除任何執行中的工作</span><span class="sxs-lookup"><span data-stu-id="00259-120">Delete any running task</span></span>

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

### <span data-ttu-id="00259-121">-強制</span><span class="sxs-lookup"><span data-stu-id="00259-121">-Force</span></span>
<span data-ttu-id="00259-122">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="00259-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="00259-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00259-123">-InputObject</span></span>
<span data-ttu-id="00259-124">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="00259-124">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00259-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="00259-125">-Name</span></span>
<span data-ttu-id="00259-126">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="00259-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00259-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00259-127">-PassThru</span></span>
<span data-ttu-id="00259-128">會返回 true/false。</span><span class="sxs-lookup"><span data-stu-id="00259-128">Returns an true/false.</span></span>
<span data-ttu-id="00259-129">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="00259-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="00259-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00259-130">-ResourceGroupName</span></span>
<span data-ttu-id="00259-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00259-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="00259-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00259-132">-ResourceId</span></span>
<span data-ttu-id="00259-133">專案資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="00259-133">Project Resource Id.</span></span>

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

### <span data-ttu-id="00259-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="00259-134">-ServiceName</span></span>
<span data-ttu-id="00259-135">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="00259-135">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="00259-136">-確認</span><span class="sxs-lookup"><span data-stu-id="00259-136">-Confirm</span></span>
<span data-ttu-id="00259-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="00259-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00259-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00259-138">-WhatIf</span></span>
<span data-ttu-id="00259-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00259-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00259-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00259-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00259-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00259-141">CommonParameters</span></span>
<span data-ttu-id="00259-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00259-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00259-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="00259-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00259-144">輸入</span><span class="sxs-lookup"><span data-stu-id="00259-144">INPUTS</span></span>

### <span data-ttu-id="00259-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="00259-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="00259-146">System.String</span><span class="sxs-lookup"><span data-stu-id="00259-146">System.String</span></span>

## <span data-ttu-id="00259-147">輸出</span><span class="sxs-lookup"><span data-stu-id="00259-147">OUTPUTS</span></span>

### <span data-ttu-id="00259-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00259-148">System.Boolean</span></span>

## <span data-ttu-id="00259-149">筆記</span><span class="sxs-lookup"><span data-stu-id="00259-149">NOTES</span></span>

## <span data-ttu-id="00259-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="00259-150">RELATED LINKS</span></span>

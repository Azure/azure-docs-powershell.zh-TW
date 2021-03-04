---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: 33bc407c5585017bfe98591649a0c30e46adfea4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902906"
---
# <span data-ttu-id="24c51-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="24c51-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="24c51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24c51-102">SYNOPSIS</span></span>
<span data-ttu-id="24c51-103">停止執行中的 Azure 資料庫移移服務工作。</span><span class="sxs-lookup"><span data-stu-id="24c51-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="24c51-104">語法</span><span class="sxs-lookup"><span data-stu-id="24c51-104">SYNTAX</span></span>

### <span data-ttu-id="24c51-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="24c51-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c51-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c51-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c51-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c51-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c51-108">描述</span><span class="sxs-lookup"><span data-stu-id="24c51-108">DESCRIPTION</span></span>
<span data-ttu-id="24c51-109">Stop-AzDataMigrationTask Cmdlet 會以執行狀態停止資料庫移轉活動。</span><span class="sxs-lookup"><span data-stu-id="24c51-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="24c51-110">例子</span><span class="sxs-lookup"><span data-stu-id="24c51-110">EXAMPLES</span></span>

### <span data-ttu-id="24c51-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="24c51-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="24c51-112">上述範例會停止名為 myDMSTask 的 Azure 資料庫移移服務工作，與名為 TestService 的專案 myDMSProject 和 Azure 資料庫移移服務實例相關聯</span><span class="sxs-lookup"><span data-stu-id="24c51-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="24c51-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="24c51-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="24c51-114">上述範例會停止以輸入參數 PSProjectTask 物件傳遞的 Azure 資料庫移轉服務工作</span><span class="sxs-lookup"><span data-stu-id="24c51-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="24c51-115">參數</span><span class="sxs-lookup"><span data-stu-id="24c51-115">PARAMETERS</span></span>

### <span data-ttu-id="24c51-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c51-116">-DefaultProfile</span></span>
<span data-ttu-id="24c51-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24c51-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c51-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24c51-118">-InputObject</span></span>
<span data-ttu-id="24c51-119">PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="24c51-119">PSProjectTask Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: ComponentObjectParameterSet
Aliases: ProjectTask

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24c51-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="24c51-120">-Name</span></span>
<span data-ttu-id="24c51-121">工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="24c51-121">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c51-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24c51-122">-PassThru</span></span>
<span data-ttu-id="24c51-123">會返回 true/false。</span><span class="sxs-lookup"><span data-stu-id="24c51-123">Returns an true/false.</span></span>
<span data-ttu-id="24c51-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="24c51-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="24c51-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="24c51-125">-ProjectName</span></span>
<span data-ttu-id="24c51-126">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="24c51-126">The name of the project.</span></span>

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

### <span data-ttu-id="24c51-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c51-127">-ResourceGroupName</span></span>
<span data-ttu-id="24c51-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24c51-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="24c51-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24c51-129">-ResourceId</span></span>
<span data-ttu-id="24c51-130">ProjectTask 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24c51-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="24c51-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="24c51-131">-ServiceName</span></span>
<span data-ttu-id="24c51-132">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="24c51-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="24c51-133">-確認</span><span class="sxs-lookup"><span data-stu-id="24c51-133">-Confirm</span></span>
<span data-ttu-id="24c51-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="24c51-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c51-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c51-135">-WhatIf</span></span>
<span data-ttu-id="24c51-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24c51-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c51-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24c51-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c51-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c51-138">CommonParameters</span></span>
<span data-ttu-id="24c51-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24c51-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c51-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="24c51-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c51-141">輸入</span><span class="sxs-lookup"><span data-stu-id="24c51-141">INPUTS</span></span>

### <span data-ttu-id="24c51-142">Microsoft.Azure.Commands.DataMigration.models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="24c51-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="24c51-143">System.String</span><span class="sxs-lookup"><span data-stu-id="24c51-143">System.String</span></span>

## <span data-ttu-id="24c51-144">輸出</span><span class="sxs-lookup"><span data-stu-id="24c51-144">OUTPUTS</span></span>

### <span data-ttu-id="24c51-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24c51-145">System.Boolean</span></span>

## <span data-ttu-id="24c51-146">筆記</span><span class="sxs-lookup"><span data-stu-id="24c51-146">NOTES</span></span>

## <span data-ttu-id="24c51-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="24c51-147">RELATED LINKS</span></span>

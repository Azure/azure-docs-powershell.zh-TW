---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationTask.md
ms.openlocfilehash: 11ef118483d22451c908fcf7beefb7faae038622
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622458"
---
# <span data-ttu-id="a20a9-101">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a20a9-101">Stop-AzDataMigrationTask</span></span>

## <span data-ttu-id="a20a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a20a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a20a9-103">停止處於執行中狀態的 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="a20a9-103">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

## <span data-ttu-id="a20a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a20a9-104">SYNTAX</span></span>

### <span data-ttu-id="a20a9-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a20a9-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a20a9-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationTask [-InputObject] <PSProjectTask> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a20a9-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationTask [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20a9-108">說明</span><span class="sxs-lookup"><span data-stu-id="a20a9-108">DESCRIPTION</span></span>
<span data-ttu-id="a20a9-109">Stop-AzDataMigrationTask Cmdlet 會停止執行中狀態的資料庫移轉活動。</span><span class="sxs-lookup"><span data-stu-id="a20a9-109">Stop-AzDataMigrationTask cmdlet stops database migration activity in running state.</span></span> 

## <span data-ttu-id="a20a9-110">示例</span><span class="sxs-lookup"><span data-stu-id="a20a9-110">EXAMPLES</span></span>

### <span data-ttu-id="a20a9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a20a9-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationTask -ResourceGroupName MyResourceGroup  -ServiceName TestService -ProjectName myDMSProject -Name myDMSTask
```

<span data-ttu-id="a20a9-112">上面的範例會停止名為 myDMSTask 的 Azure 資料庫移轉服務工作與名為 TestService 的 project myDMSProject 和 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="a20a9-112">Above example stops Azure Database Migration Service task named myDMSTask associated with project myDMSProject and Azure Database Migration Service instance named TestService</span></span>

### <span data-ttu-id="a20a9-113">範例2</span><span class="sxs-lookup"><span data-stu-id="a20a9-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationTask -InputObject $MyDMSTask
```

<span data-ttu-id="a20a9-114">上述範例會停止以輸入參數 PSProjectTask 物件形式傳入的 Azure Database 遷移服務任務</span><span class="sxs-lookup"><span data-stu-id="a20a9-114">Above example stops Azure Database Migration Service task passed in as input parameter PSProjectTask object</span></span>

## <span data-ttu-id="a20a9-115">參數</span><span class="sxs-lookup"><span data-stu-id="a20a9-115">PARAMETERS</span></span>

### <span data-ttu-id="a20a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20a9-116">-DefaultProfile</span></span>
<span data-ttu-id="a20a9-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a20a9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a20a9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a20a9-118">-InputObject</span></span>
<span data-ttu-id="a20a9-119">PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="a20a9-119">PSProjectTask Object.</span></span>

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

### <span data-ttu-id="a20a9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a20a9-120">-Name</span></span>
<span data-ttu-id="a20a9-121">任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="a20a9-121">The name of the task.</span></span>

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

### <span data-ttu-id="a20a9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a20a9-122">-PassThru</span></span>
<span data-ttu-id="a20a9-123">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="a20a9-123">Returns an true/false.</span></span>
<span data-ttu-id="a20a9-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a20a9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a20a9-125">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="a20a9-125">-ProjectName</span></span>
<span data-ttu-id="a20a9-126">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="a20a9-126">The name of the project.</span></span>

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

### <span data-ttu-id="a20a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="a20a9-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a20a9-128">The name of the resource group .</span></span>

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

### <span data-ttu-id="a20a9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a20a9-129">-ResourceId</span></span>
<span data-ttu-id="a20a9-130">ProjectTask 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a20a9-130">ProjectTask Resource Id.</span></span>

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

### <span data-ttu-id="a20a9-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a20a9-131">-ServiceName</span></span>
<span data-ttu-id="a20a9-132">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a20a9-132">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="a20a9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="a20a9-133">-Confirm</span></span>
<span data-ttu-id="a20a9-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a20a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20a9-135">-WhatIf</span></span>
<span data-ttu-id="a20a9-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a20a9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a20a9-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a20a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20a9-138">CommonParameters</span></span>
<span data-ttu-id="a20a9-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a20a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20a9-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a20a9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20a9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a20a9-141">INPUTS</span></span>

### <span data-ttu-id="a20a9-142">PSProjectTask 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="a20a9-142">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

### <span data-ttu-id="a20a9-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a20a9-143">System.String</span></span>

## <span data-ttu-id="a20a9-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a20a9-144">OUTPUTS</span></span>

### <span data-ttu-id="a20a9-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a20a9-145">System.Boolean</span></span>

## <span data-ttu-id="a20a9-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a20a9-146">NOTES</span></span>

## <span data-ttu-id="a20a9-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a20a9-147">RELATED LINKS</span></span>

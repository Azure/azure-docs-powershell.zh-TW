---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128236"
---
# <span data-ttu-id="f7dc8-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="f7dc8-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="f7dc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7dc8-103">建立要在現有 DMS 任務上執行的新命令。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="f7dc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7dc8-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="f7dc8-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7dc8-105">DESCRIPTION</span></span>
<span data-ttu-id="f7dc8-106">Invoke-AzDataMigrationCommand Cmdlet 會建立要在現有的遷移工作上執行的新命令任務。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="f7dc8-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7dc8-107">EXAMPLES</span></span>

### <span data-ttu-id="f7dc8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f7dc8-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="f7dc8-109">上述範例使用 Invoke-AzDataMigrationCommand Cmdlet 來建立現有服務、專案及工作的命令</span><span class="sxs-lookup"><span data-stu-id="f7dc8-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="f7dc8-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7dc8-110">PARAMETERS</span></span>

### <span data-ttu-id="f7dc8-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="f7dc8-111">-CommandType</span></span>
<span data-ttu-id="f7dc8-112">命令類型。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7dc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7dc8-113">-DefaultProfile</span></span>
<span data-ttu-id="f7dc8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7dc8-115">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="f7dc8-115">-ProjectName</span></span>
<span data-ttu-id="f7dc8-116">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7dc8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7dc8-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7dc8-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7dc8-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f7dc8-119">-ServiceName</span></span>
<span data-ttu-id="f7dc8-120">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7dc8-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="f7dc8-121">-TaskName</span></span>
<span data-ttu-id="f7dc8-122">執行命令之任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-122">The name of the task the command is run on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="f7dc8-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="f7dc8-123">-ObjectName</span></span>
<span data-ttu-id="f7dc8-124">執行命令所針對之資料庫物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-124">The name of the database object the command will run against.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7dc8-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f7dc8-125">-Confirm</span></span>
<span data-ttu-id="f7dc8-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7dc8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7dc8-127">-WhatIf</span></span>
<span data-ttu-id="f7dc8-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7dc8-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7dc8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7dc8-130">CommonParameters</span></span>
<span data-ttu-id="f7dc8-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7dc8-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7dc8-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f7dc8-133">INPUTS</span></span>

### <span data-ttu-id="f7dc8-134">System.object</span><span class="sxs-lookup"><span data-stu-id="f7dc8-134">System.String</span></span>

## <span data-ttu-id="f7dc8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f7dc8-135">OUTPUTS</span></span>

### <span data-ttu-id="f7dc8-136">CommandProperties 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="f7dc8-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="f7dc8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f7dc8-137">NOTES</span></span>

## <span data-ttu-id="f7dc8-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7dc8-138">RELATED LINKS</span></span>

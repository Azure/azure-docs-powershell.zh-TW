---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: e99e2e6a8c0b2c8a0fc0b2d2143d2b4301520ab0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902085"
---
# <span data-ttu-id="62d5a-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="62d5a-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="62d5a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="62d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="62d5a-103">建立新命令，以對現有 DMS 工作執行。</span><span class="sxs-lookup"><span data-stu-id="62d5a-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="62d5a-104">語法</span><span class="sxs-lookup"><span data-stu-id="62d5a-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="62d5a-105">描述</span><span class="sxs-lookup"><span data-stu-id="62d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="62d5a-106">此Invoke-AzDataMigrationCommand Cmdlet 會建立新命令工作，以在現有的移轉工作上執行。</span><span class="sxs-lookup"><span data-stu-id="62d5a-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="62d5a-107">例子</span><span class="sxs-lookup"><span data-stu-id="62d5a-107">EXAMPLES</span></span>

### <span data-ttu-id="62d5a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="62d5a-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="62d5a-109">上述範例使用 Invoke-AzDataMigrationCommand Cmdlet 建立現有服務、專案和工作的命令</span><span class="sxs-lookup"><span data-stu-id="62d5a-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="62d5a-110">參數</span><span class="sxs-lookup"><span data-stu-id="62d5a-110">PARAMETERS</span></span>

### <span data-ttu-id="62d5a-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="62d5a-111">-CommandType</span></span>
<span data-ttu-id="62d5a-112">命令類型。</span><span class="sxs-lookup"><span data-stu-id="62d5a-112">Command Type.</span></span>

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

### <span data-ttu-id="62d5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d5a-113">-DefaultProfile</span></span>
<span data-ttu-id="62d5a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="62d5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d5a-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="62d5a-115">-ProjectName</span></span>
<span data-ttu-id="62d5a-116">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="62d5a-116">The name of the project.</span></span>

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

### <span data-ttu-id="62d5a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62d5a-117">-ResourceGroupName</span></span>
<span data-ttu-id="62d5a-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="62d5a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="62d5a-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="62d5a-119">-ServiceName</span></span>
<span data-ttu-id="62d5a-120">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="62d5a-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="62d5a-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="62d5a-121">-TaskName</span></span>
<span data-ttu-id="62d5a-122">命令執行時的工作名稱。</span><span class="sxs-lookup"><span data-stu-id="62d5a-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="62d5a-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="62d5a-123">-ObjectName</span></span>
<span data-ttu-id="62d5a-124">命令所執行之資料庫物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="62d5a-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="62d5a-125">-確認</span><span class="sxs-lookup"><span data-stu-id="62d5a-125">-Confirm</span></span>
<span data-ttu-id="62d5a-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="62d5a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62d5a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62d5a-127">-WhatIf</span></span>
<span data-ttu-id="62d5a-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62d5a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62d5a-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62d5a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62d5a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d5a-130">CommonParameters</span></span>
<span data-ttu-id="62d5a-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="62d5a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d5a-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="62d5a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d5a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="62d5a-133">INPUTS</span></span>

### <span data-ttu-id="62d5a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="62d5a-134">System.String</span></span>

## <span data-ttu-id="62d5a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="62d5a-135">OUTPUTS</span></span>

### <span data-ttu-id="62d5a-136">Microsoft.Azure.management.DataMigration.models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="62d5a-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="62d5a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="62d5a-137">NOTES</span></span>

## <span data-ttu-id="62d5a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="62d5a-138">RELATED LINKS</span></span>

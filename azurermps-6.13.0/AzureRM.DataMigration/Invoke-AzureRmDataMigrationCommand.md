---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451192"
---
# <span data-ttu-id="4181b-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="4181b-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="4181b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4181b-102">SYNOPSIS</span></span>
<span data-ttu-id="4181b-103">建立要在現有 DMS 任務上執行的新命令。</span><span class="sxs-lookup"><span data-stu-id="4181b-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4181b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4181b-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4181b-105">說明</span><span class="sxs-lookup"><span data-stu-id="4181b-105">DESCRIPTION</span></span>
<span data-ttu-id="4181b-106">New-AzureRmDataMigrationCommand Cmdlet 會建立要在現有的遷移工作上執行的新命令任務。</span><span class="sxs-lookup"><span data-stu-id="4181b-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="4181b-107">示例</span><span class="sxs-lookup"><span data-stu-id="4181b-107">EXAMPLES</span></span>

### <span data-ttu-id="4181b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4181b-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="4181b-109">上述範例使用 New-AzureRmDmsCommand Cmdlet 來建立現有服務、專案及工作的命令</span><span class="sxs-lookup"><span data-stu-id="4181b-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="4181b-110">參數</span><span class="sxs-lookup"><span data-stu-id="4181b-110">PARAMETERS</span></span>

### <span data-ttu-id="4181b-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="4181b-111">-CommandType</span></span>
<span data-ttu-id="4181b-112">命令類型。</span><span class="sxs-lookup"><span data-stu-id="4181b-112">Command Type.</span></span>

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

### <span data-ttu-id="4181b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4181b-113">-DefaultProfile</span></span>
<span data-ttu-id="4181b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4181b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4181b-115">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="4181b-115">-ProjectName</span></span>
<span data-ttu-id="4181b-116">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="4181b-116">The name of the project.</span></span>

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

### <span data-ttu-id="4181b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4181b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4181b-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4181b-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="4181b-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4181b-119">-ServiceName</span></span>
<span data-ttu-id="4181b-120">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4181b-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="4181b-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="4181b-121">-TaskName</span></span>
<span data-ttu-id="4181b-122">執行命令之任務的名稱。</span><span class="sxs-lookup"><span data-stu-id="4181b-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="4181b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="4181b-123">-Confirm</span></span>
<span data-ttu-id="4181b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4181b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4181b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4181b-125">-WhatIf</span></span>
<span data-ttu-id="4181b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4181b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4181b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4181b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4181b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4181b-128">CommonParameters</span></span>
<span data-ttu-id="4181b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4181b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4181b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4181b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4181b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4181b-131">INPUTS</span></span>

### <span data-ttu-id="4181b-132">System.object</span><span class="sxs-lookup"><span data-stu-id="4181b-132">System.String</span></span>

## <span data-ttu-id="4181b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4181b-133">OUTPUTS</span></span>

### <span data-ttu-id="4181b-134">CommandProperties 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="4181b-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="4181b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4181b-135">NOTES</span></span>

## <span data-ttu-id="4181b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4181b-136">RELATED LINKS</span></span>

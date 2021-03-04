---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2237522cbf7b179358ea4fa9f7ed7608222782ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916873"
---
# <span data-ttu-id="25114-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="25114-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="25114-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25114-102">SYNOPSIS</span></span>
<span data-ttu-id="25114-103">完成給定資料庫的記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="25114-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="25114-104">語法</span><span class="sxs-lookup"><span data-stu-id="25114-104">SYNTAX</span></span>

### <span data-ttu-id="25114-105">LogReplayInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="25114-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25114-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="25114-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25114-107">描述</span><span class="sxs-lookup"><span data-stu-id="25114-107">DESCRIPTION</span></span>
<span data-ttu-id="25114-108">**Complete-AzSqlInstanceDatabaseLogReplay** Cmdlet 會完成給定資料庫的記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="25114-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="25114-109">例子</span><span class="sxs-lookup"><span data-stu-id="25114-109">EXAMPLES</span></span>

### <span data-ttu-id="25114-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="25114-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="25114-111">最後一次備份還原之後，此命令會完成給定資料庫的記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="25114-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="25114-112">參數</span><span class="sxs-lookup"><span data-stu-id="25114-112">PARAMETERS</span></span>

### <span data-ttu-id="25114-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25114-113">-DefaultProfile</span></span>
<span data-ttu-id="25114-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="25114-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25114-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25114-115">-InputObject</span></span>
<span data-ttu-id="25114-116">實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="25114-116">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25114-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="25114-117">-InstanceName</span></span>
<span data-ttu-id="25114-118">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="25114-118">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25114-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="25114-119">-LastBackupName</span></span>
<span data-ttu-id="25114-120">要還原的最後一個備份檔案名。</span><span class="sxs-lookup"><span data-stu-id="25114-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="25114-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="25114-121">-Name</span></span>
<span data-ttu-id="25114-122">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="25114-122">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25114-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25114-123">-PassThru</span></span>
<span data-ttu-id="25114-124">定義是否返回同步組。</span><span class="sxs-lookup"><span data-stu-id="25114-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="25114-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25114-125">-ResourceGroupName</span></span>
<span data-ttu-id="25114-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25114-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25114-127">-確認</span><span class="sxs-lookup"><span data-stu-id="25114-127">-Confirm</span></span>
<span data-ttu-id="25114-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="25114-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25114-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25114-129">-WhatIf</span></span>
<span data-ttu-id="25114-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25114-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25114-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25114-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25114-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25114-132">CommonParameters</span></span>
<span data-ttu-id="25114-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25114-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25114-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25114-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25114-135">輸入</span><span class="sxs-lookup"><span data-stu-id="25114-135">INPUTS</span></span>

### <span data-ttu-id="25114-136">System.String</span><span class="sxs-lookup"><span data-stu-id="25114-136">System.String</span></span>

### <span data-ttu-id="25114-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="25114-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="25114-138">輸出</span><span class="sxs-lookup"><span data-stu-id="25114-138">OUTPUTS</span></span>

## <span data-ttu-id="25114-139">筆記</span><span class="sxs-lookup"><span data-stu-id="25114-139">NOTES</span></span>

## <span data-ttu-id="25114-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="25114-140">RELATED LINKS</span></span>

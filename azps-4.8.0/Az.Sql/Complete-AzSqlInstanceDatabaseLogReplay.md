---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Complete-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Complete-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: d1d7cead951520944199347ebdbb209c5474eb3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129219"
---
# <span data-ttu-id="b17b2-101">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="b17b2-101">Complete-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="b17b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b17b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b17b2-103">完成指定資料庫的記錄重新播放服務。</span><span class="sxs-lookup"><span data-stu-id="b17b2-103">Completes Log Replay service for the given database.</span></span>

## <span data-ttu-id="b17b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b17b2-104">SYNTAX</span></span>

### <span data-ttu-id="b17b2-105">LogReplayInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="b17b2-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b17b2-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="b17b2-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Complete-AzSqlInstanceDatabaseLogReplay -LastBackupName <String> [-PassThru]
 [-InputObject] <AzureSqlManagedDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b17b2-107">說明</span><span class="sxs-lookup"><span data-stu-id="b17b2-107">DESCRIPTION</span></span>
<span data-ttu-id="b17b2-108">**AzSqlInstanceDatabaseLogReplay** Cmdlet 會完成指定資料庫上的記錄重新播放服務。</span><span class="sxs-lookup"><span data-stu-id="b17b2-108">The **Complete-AzSqlInstanceDatabaseLogReplay** cmdlet completes the Log Replay service on the given database.</span></span>

## <span data-ttu-id="b17b2-109">示例</span><span class="sxs-lookup"><span data-stu-id="b17b2-109">EXAMPLES</span></span>

### <span data-ttu-id="b17b2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b17b2-110">Example 1</span></span>
```powershell
PS C:\> Complete-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName" -LastBackupName "last_backup.bak"
```

<span data-ttu-id="b17b2-111">此命令會在上次備份還原之後，為指定的資料庫完成記錄重新播放服務。</span><span class="sxs-lookup"><span data-stu-id="b17b2-111">This command will complete Log Replay service for the given database after last backup gets restored.</span></span>

## <span data-ttu-id="b17b2-112">參數</span><span class="sxs-lookup"><span data-stu-id="b17b2-112">PARAMETERS</span></span>

### <span data-ttu-id="b17b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b17b2-113">-DefaultProfile</span></span>
<span data-ttu-id="b17b2-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b17b2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b17b2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b17b2-115">-InputObject</span></span>
<span data-ttu-id="b17b2-116">實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="b17b2-116">The instance database object.</span></span>

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

### <span data-ttu-id="b17b2-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b17b2-117">-InstanceName</span></span>
<span data-ttu-id="b17b2-118">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b17b2-118">The name of the instance.</span></span>

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

### <span data-ttu-id="b17b2-119">-LastBackupName</span><span class="sxs-lookup"><span data-stu-id="b17b2-119">-LastBackupName</span></span>
<span data-ttu-id="b17b2-120">要還原之最後一個備份檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="b17b2-120">The name of the last backup file to restore.</span></span>

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

### <span data-ttu-id="b17b2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b17b2-121">-Name</span></span>
<span data-ttu-id="b17b2-122">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b17b2-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="b17b2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b17b2-123">-PassThru</span></span>
<span data-ttu-id="b17b2-124">定義是否要傳回同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="b17b2-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="b17b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b17b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="b17b2-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b17b2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b17b2-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b17b2-127">-Confirm</span></span>
<span data-ttu-id="b17b2-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b17b2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b17b2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b17b2-129">-WhatIf</span></span>
<span data-ttu-id="b17b2-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b17b2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b17b2-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b17b2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b17b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b17b2-132">CommonParameters</span></span>
<span data-ttu-id="b17b2-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b17b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b17b2-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b17b2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b17b2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b17b2-135">INPUTS</span></span>

### <span data-ttu-id="b17b2-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b17b2-136">System.String</span></span>

### <span data-ttu-id="b17b2-137">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="b17b2-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b17b2-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b17b2-138">OUTPUTS</span></span>

## <span data-ttu-id="b17b2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b17b2-139">NOTES</span></span>

## <span data-ttu-id="b17b2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b17b2-140">RELATED LINKS</span></span>

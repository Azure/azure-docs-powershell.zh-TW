---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436657"
---
# <span data-ttu-id="b3b6c-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="b3b6c-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="b3b6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b6c-103">刪除資料庫，以取消記錄重新播放服務。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="b3b6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3b6c-104">SYNTAX</span></span>

### <span data-ttu-id="b3b6c-105">LogReplayInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="b3b6c-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3b6c-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="b3b6c-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3b6c-107">說明</span><span class="sxs-lookup"><span data-stu-id="b3b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="b3b6c-108">**AzSqlInstanceDatabaseLogReplay** Cmdlet 會刪除資料庫，因此會取消記錄重新播放服務。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="b3b6c-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="b3b6c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b3b6c-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="b3b6c-111">這個命令會取消指定資料庫上的記錄重新播放服務。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="b3b6c-112">參數</span><span class="sxs-lookup"><span data-stu-id="b3b6c-112">PARAMETERS</span></span>

### <span data-ttu-id="b3b6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b6c-113">-DefaultProfile</span></span>
<span data-ttu-id="b3b6c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b6c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b3b6c-115">-Force</span></span>
<span data-ttu-id="b3b6c-116">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="b3b6c-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b3b6c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3b6c-117">-InputObject</span></span>
<span data-ttu-id="b3b6c-118">實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-118">The instance database object.</span></span>

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

### <span data-ttu-id="b3b6c-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b3b6c-119">-InstanceName</span></span>
<span data-ttu-id="b3b6c-120">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-120">The name of the instance.</span></span>

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

### <span data-ttu-id="b3b6c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3b6c-121">-Name</span></span>
<span data-ttu-id="b3b6c-122">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="b3b6c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3b6c-123">-PassThru</span></span>
<span data-ttu-id="b3b6c-124">定義是否要傳回同步處理群組。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="b3b6c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3b6c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3b6c-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="b3b6c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b3b6c-127">-Confirm</span></span>
<span data-ttu-id="b3b6c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3b6c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b6c-129">-WhatIf</span></span>
<span data-ttu-id="b3b6c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3b6c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3b6c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b6c-132">CommonParameters</span></span>
<span data-ttu-id="b3b6c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b6c-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b3b6c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b6c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b3b6c-135">INPUTS</span></span>

### <span data-ttu-id="b3b6c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b3b6c-136">System.String</span></span>

### <span data-ttu-id="b3b6c-137">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="b3b6c-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b3b6c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b3b6c-138">OUTPUTS</span></span>

### <span data-ttu-id="b3b6c-139">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="b3b6c-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b3b6c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b3b6c-140">NOTES</span></span>

## <span data-ttu-id="b3b6c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3b6c-141">RELATED LINKS</span></span>

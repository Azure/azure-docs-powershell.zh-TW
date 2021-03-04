---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 42c2fa289eef04734c0619ca7bf2a46ece19606e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916476"
---
# <span data-ttu-id="5690d-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="5690d-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="5690d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5690d-102">SYNOPSIS</span></span>
<span data-ttu-id="5690d-103">刪除資料庫以取消記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="5690d-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="5690d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5690d-104">SYNTAX</span></span>

### <span data-ttu-id="5690d-105">LogReplayInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="5690d-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5690d-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="5690d-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5690d-107">描述</span><span class="sxs-lookup"><span data-stu-id="5690d-107">DESCRIPTION</span></span>
<span data-ttu-id="5690d-108">**Stop-AzSqlInstanceDatabaseLogReplay** Cmdlet 會刪除資料庫，因而取消記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="5690d-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="5690d-109">例子</span><span class="sxs-lookup"><span data-stu-id="5690d-109">EXAMPLES</span></span>

### <span data-ttu-id="5690d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5690d-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="5690d-111">此命令會取消給定資料庫上的記錄重播服務。</span><span class="sxs-lookup"><span data-stu-id="5690d-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="5690d-112">參數</span><span class="sxs-lookup"><span data-stu-id="5690d-112">PARAMETERS</span></span>

### <span data-ttu-id="5690d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5690d-113">-DefaultProfile</span></span>
<span data-ttu-id="5690d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5690d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5690d-115">-強制</span><span class="sxs-lookup"><span data-stu-id="5690d-115">-Force</span></span>
<span data-ttu-id="5690d-116">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="5690d-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5690d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5690d-117">-InputObject</span></span>
<span data-ttu-id="5690d-118">實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="5690d-118">The instance database object.</span></span>

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

### <span data-ttu-id="5690d-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5690d-119">-InstanceName</span></span>
<span data-ttu-id="5690d-120">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="5690d-120">The name of the instance.</span></span>

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

### <span data-ttu-id="5690d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5690d-121">-Name</span></span>
<span data-ttu-id="5690d-122">實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5690d-122">The name of the instance database.</span></span>

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

### <span data-ttu-id="5690d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5690d-123">-PassThru</span></span>
<span data-ttu-id="5690d-124">定義是否返回同步組。</span><span class="sxs-lookup"><span data-stu-id="5690d-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="5690d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5690d-125">-ResourceGroupName</span></span>
<span data-ttu-id="5690d-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5690d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="5690d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5690d-127">-Confirm</span></span>
<span data-ttu-id="5690d-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5690d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5690d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5690d-129">-WhatIf</span></span>
<span data-ttu-id="5690d-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5690d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5690d-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5690d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5690d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5690d-132">CommonParameters</span></span>
<span data-ttu-id="5690d-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5690d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5690d-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5690d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5690d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5690d-135">INPUTS</span></span>

### <span data-ttu-id="5690d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5690d-136">System.String</span></span>

### <span data-ttu-id="5690d-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5690d-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="5690d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="5690d-138">OUTPUTS</span></span>

### <span data-ttu-id="5690d-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5690d-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="5690d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="5690d-140">NOTES</span></span>

## <span data-ttu-id="5690d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="5690d-141">RELATED LINKS</span></span>

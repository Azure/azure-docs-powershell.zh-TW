---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 14c2a58c40aa29f1b48902be5d82911f70a71cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905953"
---
# <span data-ttu-id="01b0a-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="01b0a-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="01b0a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="01b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="01b0a-103">將 Azure NetApp 檔案更新 (ANF) 提供的選擇性修改者。</span><span class="sxs-lookup"><span data-stu-id="01b0a-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="01b0a-104">語法</span><span class="sxs-lookup"><span data-stu-id="01b0a-104">SYNTAX</span></span>

### <span data-ttu-id="01b0a-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="01b0a-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01b0a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b0a-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01b0a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b0a-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01b0a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b0a-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01b0a-109">描述</span><span class="sxs-lookup"><span data-stu-id="01b0a-109">DESCRIPTION</span></span>
<span data-ttu-id="01b0a-110">**Update-AzNetAppFilesBackupPolicy** Cmdlet 會修改 ANF 備份策略。</span><span class="sxs-lookup"><span data-stu-id="01b0a-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="01b0a-111">例子</span><span class="sxs-lookup"><span data-stu-id="01b0a-111">EXAMPLES</span></span>

### <span data-ttu-id="01b0a-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="01b0a-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="01b0a-113">此命令會變更 ANF 備份策略 「MyBackupPolicy」，讓系統提供 DailyBackupsToKeep。</span><span class="sxs-lookup"><span data-stu-id="01b0a-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="01b0a-114">參數</span><span class="sxs-lookup"><span data-stu-id="01b0a-114">PARAMETERS</span></span>

### <span data-ttu-id="01b0a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01b0a-115">-AccountName</span></span>
<span data-ttu-id="01b0a-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="01b0a-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="01b0a-117">-AccountObject</span></span>
<span data-ttu-id="01b0a-118">包含要更新之備份策略的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="01b0a-118">The Account object containing the Backup Policy to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="01b0a-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="01b0a-120">要保留的每日備份計數</span><span class="sxs-lookup"><span data-stu-id="01b0a-120">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b0a-121">-DefaultProfile</span></span>
<span data-ttu-id="01b0a-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="01b0a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b0a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01b0a-123">-InputObject</span></span>
<span data-ttu-id="01b0a-124">要移除的 BackupPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="01b0a-124">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-125">-位置</span><span class="sxs-lookup"><span data-stu-id="01b0a-125">-Location</span></span>
<span data-ttu-id="01b0a-126">資源的位置</span><span class="sxs-lookup"><span data-stu-id="01b0a-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="01b0a-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="01b0a-128">要保留的每月備份計數</span><span class="sxs-lookup"><span data-stu-id="01b0a-128">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="01b0a-129">-Name</span></span>
<span data-ttu-id="01b0a-130">ANF 備份策略的名稱</span><span class="sxs-lookup"><span data-stu-id="01b0a-130">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b0a-131">-ResourceGroupName</span></span>
<span data-ttu-id="01b0a-132">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="01b0a-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01b0a-133">-ResourceId</span></span>
<span data-ttu-id="01b0a-134">ANF 備份策略的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="01b0a-134">The resource id of the ANF Backup Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-135">-標記</span><span class="sxs-lookup"><span data-stu-id="01b0a-135">-Tag</span></span>
<span data-ttu-id="01b0a-136">代表資源標記的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="01b0a-136">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="01b0a-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="01b0a-138">要保留的每週備份計數</span><span class="sxs-lookup"><span data-stu-id="01b0a-138">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="01b0a-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="01b0a-140">要保留的每年備份計數</span><span class="sxs-lookup"><span data-stu-id="01b0a-140">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b0a-141">-確認</span><span class="sxs-lookup"><span data-stu-id="01b0a-141">-Confirm</span></span>
<span data-ttu-id="01b0a-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="01b0a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01b0a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01b0a-143">-WhatIf</span></span>
<span data-ttu-id="01b0a-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01b0a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01b0a-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01b0a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01b0a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b0a-146">CommonParameters</span></span>
<span data-ttu-id="01b0a-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="01b0a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b0a-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01b0a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b0a-149">輸入</span><span class="sxs-lookup"><span data-stu-id="01b0a-149">INPUTS</span></span>

### <span data-ttu-id="01b0a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="01b0a-150">System.String</span></span>

### <span data-ttu-id="01b0a-151">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="01b0a-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="01b0a-152">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="01b0a-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="01b0a-153">輸出</span><span class="sxs-lookup"><span data-stu-id="01b0a-153">OUTPUTS</span></span>

### <span data-ttu-id="01b0a-154">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="01b0a-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="01b0a-155">筆記</span><span class="sxs-lookup"><span data-stu-id="01b0a-155">NOTES</span></span>

## <span data-ttu-id="01b0a-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="01b0a-156">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 0cebe34948984e36c9ad2fbe30de8da3a0e0ca92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142246"
---
# <span data-ttu-id="36060-101">Update-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="36060-101">Update-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="36060-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36060-102">SYNOPSIS</span></span>
<span data-ttu-id="36060-103">將 (ANF) 備份原則的 Azure NetApp 檔案更新為所提供的選擇性修飾符。</span><span class="sxs-lookup"><span data-stu-id="36060-103">Updates an Azure NetApp Files (ANF) backup policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="36060-104">句法</span><span class="sxs-lookup"><span data-stu-id="36060-104">SYNTAX</span></span>

### <span data-ttu-id="36060-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="36060-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>]
 [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36060-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36060-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy -Name <String> [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36060-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36060-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36060-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36060-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackupPolicy [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesBackupPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36060-109">說明</span><span class="sxs-lookup"><span data-stu-id="36060-109">DESCRIPTION</span></span>
<span data-ttu-id="36060-110">**AzNetAppFilesBackupPolicy** Cmdlet 會修改 ANF 備份原則。</span><span class="sxs-lookup"><span data-stu-id="36060-110">The **Update-AzNetAppFilesBackupPolicy** cmdlet modifies an ANF backup policy .</span></span>

## <span data-ttu-id="36060-111">示例</span><span class="sxs-lookup"><span data-stu-id="36060-111">EXAMPLES</span></span>

### <span data-ttu-id="36060-112">範例1</span><span class="sxs-lookup"><span data-stu-id="36060-112">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy" -DailyBackupsToKeep 2
```

<span data-ttu-id="36060-113">這個命令會將 ANF 備份原則 "MyBackupPolicy" 變更為擁有指定的 DailyBackupsToKeep。</span><span class="sxs-lookup"><span data-stu-id="36060-113">This command changes the ANF backup policy "MyBackupPolicy" to have the given DailyBackupsToKeep.</span></span>

## <span data-ttu-id="36060-114">參數</span><span class="sxs-lookup"><span data-stu-id="36060-114">PARAMETERS</span></span>

### <span data-ttu-id="36060-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36060-115">-AccountName</span></span>
<span data-ttu-id="36060-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="36060-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="36060-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="36060-117">-AccountObject</span></span>
<span data-ttu-id="36060-118">包含要更新之備份策略的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="36060-118">The Account object containing the Backup Policy to update</span></span>

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

### <span data-ttu-id="36060-119">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="36060-119">-DailyBackupsToKeep</span></span>
<span data-ttu-id="36060-120">要保留的每日備份數</span><span class="sxs-lookup"><span data-stu-id="36060-120">Daily backups count to keep</span></span>

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

### <span data-ttu-id="36060-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36060-121">-DefaultProfile</span></span>
<span data-ttu-id="36060-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36060-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36060-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36060-123">-InputObject</span></span>
<span data-ttu-id="36060-124">要移除的 BackupPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="36060-124">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="36060-125">-位置</span><span class="sxs-lookup"><span data-stu-id="36060-125">-Location</span></span>
<span data-ttu-id="36060-126">資源的位置</span><span class="sxs-lookup"><span data-stu-id="36060-126">The location of the resource</span></span>

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

### <span data-ttu-id="36060-127">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="36060-127">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="36060-128">保留的每月備份數</span><span class="sxs-lookup"><span data-stu-id="36060-128">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="36060-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="36060-129">-Name</span></span>
<span data-ttu-id="36060-130">ANF 備份原則的名稱</span><span class="sxs-lookup"><span data-stu-id="36060-130">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="36060-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36060-131">-ResourceGroupName</span></span>
<span data-ttu-id="36060-132">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="36060-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="36060-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36060-133">-ResourceId</span></span>
<span data-ttu-id="36060-134">ANF 備份原則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="36060-134">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="36060-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="36060-135">-Tag</span></span>
<span data-ttu-id="36060-136">代表資源標記的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="36060-136">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="36060-137">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="36060-137">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="36060-138">要保留的每週備份數</span><span class="sxs-lookup"><span data-stu-id="36060-138">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="36060-139">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="36060-139">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="36060-140">要保留的年度備份計數</span><span class="sxs-lookup"><span data-stu-id="36060-140">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="36060-141">-確認</span><span class="sxs-lookup"><span data-stu-id="36060-141">-Confirm</span></span>
<span data-ttu-id="36060-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36060-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36060-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36060-143">-WhatIf</span></span>
<span data-ttu-id="36060-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36060-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36060-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36060-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36060-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36060-146">CommonParameters</span></span>
<span data-ttu-id="36060-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36060-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36060-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="36060-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36060-149">輸入</span><span class="sxs-lookup"><span data-stu-id="36060-149">INPUTS</span></span>

### <span data-ttu-id="36060-150">System.object</span><span class="sxs-lookup"><span data-stu-id="36060-150">System.String</span></span>

### <span data-ttu-id="36060-151">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="36060-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="36060-152">PSNetAppFilesBackupPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="36060-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="36060-153">輸出</span><span class="sxs-lookup"><span data-stu-id="36060-153">OUTPUTS</span></span>

### <span data-ttu-id="36060-154">PSNetAppFilesBackupPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="36060-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="36060-155">筆記</span><span class="sxs-lookup"><span data-stu-id="36060-155">NOTES</span></span>

## <span data-ttu-id="36060-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="36060-156">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 18fa19b4f173dd3539277e0a1c226afbee0de381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906038"
---
# <span data-ttu-id="105dc-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="105dc-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="105dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="105dc-102">SYNOPSIS</span></span>
<span data-ttu-id="105dc-103">在 ANF 帳戶 (ANF) 建立新 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="105dc-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="105dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="105dc-104">SYNTAX</span></span>

### <span data-ttu-id="105dc-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="105dc-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="105dc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="105dc-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="105dc-107">描述</span><span class="sxs-lookup"><span data-stu-id="105dc-107">DESCRIPTION</span></span>
<span data-ttu-id="105dc-108">**New-AzNetAppFilesActiveDirectory** Cmdlet 會為 ANF 帳戶建立新的備份策略。</span><span class="sxs-lookup"><span data-stu-id="105dc-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="105dc-109">例子</span><span class="sxs-lookup"><span data-stu-id="105dc-109">EXAMPLES</span></span>

### <span data-ttu-id="105dc-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="105dc-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="105dc-111">此命令會為名為「MyAccount」帳戶的 ANF 帳戶建立新的 ANF 備份策略。</span><span class="sxs-lookup"><span data-stu-id="105dc-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="105dc-112">參數</span><span class="sxs-lookup"><span data-stu-id="105dc-112">PARAMETERS</span></span>

### <span data-ttu-id="105dc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="105dc-113">-AccountName</span></span>
<span data-ttu-id="105dc-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="105dc-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="105dc-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="105dc-115">-AccountObject</span></span>
<span data-ttu-id="105dc-116">新備份策略的 Account 物件</span><span class="sxs-lookup"><span data-stu-id="105dc-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="105dc-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="105dc-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="105dc-118">要保留的每日備份計數</span><span class="sxs-lookup"><span data-stu-id="105dc-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="105dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105dc-119">-DefaultProfile</span></span>
<span data-ttu-id="105dc-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="105dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="105dc-121">-已啟用</span><span class="sxs-lookup"><span data-stu-id="105dc-121">-Enabled</span></span>
<span data-ttu-id="105dc-122">決定是否已啟用策略的屬性</span><span class="sxs-lookup"><span data-stu-id="105dc-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="105dc-123">-位置</span><span class="sxs-lookup"><span data-stu-id="105dc-123">-Location</span></span>
<span data-ttu-id="105dc-124">資源的位置</span><span class="sxs-lookup"><span data-stu-id="105dc-124">The location of the resource</span></span>

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

### <span data-ttu-id="105dc-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="105dc-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="105dc-126">要保留的每月備份計數</span><span class="sxs-lookup"><span data-stu-id="105dc-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="105dc-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="105dc-127">-Name</span></span>
<span data-ttu-id="105dc-128">ANF 備份策略的名稱</span><span class="sxs-lookup"><span data-stu-id="105dc-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="105dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="105dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="105dc-130">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="105dc-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="105dc-131">-標記</span><span class="sxs-lookup"><span data-stu-id="105dc-131">-Tag</span></span>
<span data-ttu-id="105dc-132">代表資源標記的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="105dc-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="105dc-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="105dc-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="105dc-134">要保留的每週備份計數</span><span class="sxs-lookup"><span data-stu-id="105dc-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="105dc-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="105dc-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="105dc-136">要保留的每年備份計數</span><span class="sxs-lookup"><span data-stu-id="105dc-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="105dc-137">-確認</span><span class="sxs-lookup"><span data-stu-id="105dc-137">-Confirm</span></span>
<span data-ttu-id="105dc-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="105dc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="105dc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="105dc-139">-WhatIf</span></span>
<span data-ttu-id="105dc-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="105dc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="105dc-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="105dc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="105dc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105dc-142">CommonParameters</span></span>
<span data-ttu-id="105dc-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="105dc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105dc-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="105dc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105dc-145">輸入</span><span class="sxs-lookup"><span data-stu-id="105dc-145">INPUTS</span></span>

### <span data-ttu-id="105dc-146">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="105dc-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="105dc-147">輸出</span><span class="sxs-lookup"><span data-stu-id="105dc-147">OUTPUTS</span></span>

### <span data-ttu-id="105dc-148">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="105dc-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="105dc-149">筆記</span><span class="sxs-lookup"><span data-stu-id="105dc-149">NOTES</span></span>

## <span data-ttu-id="105dc-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="105dc-150">RELATED LINKS</span></span>

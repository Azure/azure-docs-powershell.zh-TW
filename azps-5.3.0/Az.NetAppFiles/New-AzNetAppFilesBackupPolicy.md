---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435239"
---
# <span data-ttu-id="216de-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="216de-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="216de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="216de-102">SYNOPSIS</span></span>
<span data-ttu-id="216de-103"> () ANF ANF 帳戶的備份原則中，建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="216de-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="216de-104">句法</span><span class="sxs-lookup"><span data-stu-id="216de-104">SYNTAX</span></span>

### <span data-ttu-id="216de-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="216de-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="216de-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="216de-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="216de-107">說明</span><span class="sxs-lookup"><span data-stu-id="216de-107">DESCRIPTION</span></span>
<span data-ttu-id="216de-108">**新的-AzNetAppFilesActiveDirectory** Cmdlet 會為 ANF 帳戶建立新的備份原則。</span><span class="sxs-lookup"><span data-stu-id="216de-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="216de-109">示例</span><span class="sxs-lookup"><span data-stu-id="216de-109">EXAMPLES</span></span>

### <span data-ttu-id="216de-110">範例1</span><span class="sxs-lookup"><span data-stu-id="216de-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="216de-111">這個命令會針對 ANF 帳戶（名為「我的帳戶」）建立新的 ANF 備份原則。</span><span class="sxs-lookup"><span data-stu-id="216de-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="216de-112">參數</span><span class="sxs-lookup"><span data-stu-id="216de-112">PARAMETERS</span></span>

### <span data-ttu-id="216de-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="216de-113">-AccountName</span></span>
<span data-ttu-id="216de-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="216de-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="216de-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="216de-115">-AccountObject</span></span>
<span data-ttu-id="216de-116">新備份原則的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="216de-116">The Account object for the new Backup Policy</span></span>

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

### <span data-ttu-id="216de-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="216de-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="216de-118">要保留的每日備份數</span><span class="sxs-lookup"><span data-stu-id="216de-118">Daily backups count to keep</span></span>

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

### <span data-ttu-id="216de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216de-119">-DefaultProfile</span></span>
<span data-ttu-id="216de-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="216de-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="216de-121">-啟用</span><span class="sxs-lookup"><span data-stu-id="216de-121">-Enabled</span></span>
<span data-ttu-id="216de-122">決定已啟用原則的屬性</span><span class="sxs-lookup"><span data-stu-id="216de-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="216de-123">-位置</span><span class="sxs-lookup"><span data-stu-id="216de-123">-Location</span></span>
<span data-ttu-id="216de-124">資源的位置</span><span class="sxs-lookup"><span data-stu-id="216de-124">The location of the resource</span></span>

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

### <span data-ttu-id="216de-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="216de-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="216de-126">保留的每月備份數</span><span class="sxs-lookup"><span data-stu-id="216de-126">Monthly backups count to keep</span></span>

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

### <span data-ttu-id="216de-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="216de-127">-Name</span></span>
<span data-ttu-id="216de-128">ANF 備份原則的名稱</span><span class="sxs-lookup"><span data-stu-id="216de-128">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="216de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="216de-129">-ResourceGroupName</span></span>
<span data-ttu-id="216de-130">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="216de-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="216de-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="216de-131">-Tag</span></span>
<span data-ttu-id="216de-132">代表資源標記的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="216de-132">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="216de-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="216de-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="216de-134">要保留的每週備份數</span><span class="sxs-lookup"><span data-stu-id="216de-134">Weekly backups count to keep</span></span>

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

### <span data-ttu-id="216de-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="216de-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="216de-136">要保留的年度備份計數</span><span class="sxs-lookup"><span data-stu-id="216de-136">Yearly backups count to keep</span></span>

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

### <span data-ttu-id="216de-137">-確認</span><span class="sxs-lookup"><span data-stu-id="216de-137">-Confirm</span></span>
<span data-ttu-id="216de-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="216de-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="216de-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="216de-139">-WhatIf</span></span>
<span data-ttu-id="216de-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="216de-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="216de-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="216de-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="216de-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216de-142">CommonParameters</span></span>
<span data-ttu-id="216de-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="216de-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216de-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="216de-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216de-145">輸入</span><span class="sxs-lookup"><span data-stu-id="216de-145">INPUTS</span></span>

### <span data-ttu-id="216de-146">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="216de-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="216de-147">輸出</span><span class="sxs-lookup"><span data-stu-id="216de-147">OUTPUTS</span></span>

### <span data-ttu-id="216de-148">PSNetAppFilesBackupPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="216de-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="216de-149">筆記</span><span class="sxs-lookup"><span data-stu-id="216de-149">NOTES</span></span>

## <span data-ttu-id="216de-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="216de-150">RELATED LINKS</span></span>

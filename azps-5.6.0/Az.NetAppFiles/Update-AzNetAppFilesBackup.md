---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: 95b7ad2ea93f1e1b22eafe3fbaae811dc33f24d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905954"
---
# <span data-ttu-id="f5821-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="f5821-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="f5821-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5821-102">SYNOPSIS</span></span>
<span data-ttu-id="f5821-103">將 Azure NetApp 檔案 (ANF) 備份到提供的選擇性修改程式。</span><span class="sxs-lookup"><span data-stu-id="f5821-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="f5821-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5821-104">SYNTAX</span></span>

### <span data-ttu-id="f5821-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f5821-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5821-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5821-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5821-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5821-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5821-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5821-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5821-109">描述</span><span class="sxs-lookup"><span data-stu-id="f5821-109">DESCRIPTION</span></span>
<span data-ttu-id="f5821-110">**Update-AzNetAppFilesBackup** Cmdlet 會修改 ANF 備份。</span><span class="sxs-lookup"><span data-stu-id="f5821-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="f5821-111">例子</span><span class="sxs-lookup"><span data-stu-id="f5821-111">EXAMPLES</span></span>

### <span data-ttu-id="f5821-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="f5821-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="f5821-113">此命令會執行指定備份的更新，修改提供之使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f5821-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="f5821-114">參數</span><span class="sxs-lookup"><span data-stu-id="f5821-114">PARAMETERS</span></span>

### <span data-ttu-id="f5821-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5821-115">-AccountName</span></span>
<span data-ttu-id="f5821-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="f5821-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="f5821-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5821-117">-DefaultProfile</span></span>
<span data-ttu-id="f5821-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5821-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5821-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5821-119">-InputObject</span></span>
<span data-ttu-id="f5821-120">要移除的快照物件</span><span class="sxs-lookup"><span data-stu-id="f5821-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5821-121">-標籤</span><span class="sxs-lookup"><span data-stu-id="f5821-121">-Label</span></span>
<span data-ttu-id="f5821-122">備份標籤</span><span class="sxs-lookup"><span data-stu-id="f5821-122">Label for backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5821-123">-位置</span><span class="sxs-lookup"><span data-stu-id="f5821-123">-Location</span></span>
<span data-ttu-id="f5821-124">資源的位置</span><span class="sxs-lookup"><span data-stu-id="f5821-124">The location of the resource</span></span>

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

### <span data-ttu-id="f5821-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5821-125">-Name</span></span>
<span data-ttu-id="f5821-126">ANF 備份策略的名稱</span><span class="sxs-lookup"><span data-stu-id="f5821-126">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="f5821-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f5821-127">-PoolName</span></span>
<span data-ttu-id="f5821-128">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="f5821-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f5821-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5821-129">-ResourceGroupName</span></span>
<span data-ttu-id="f5821-130">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="f5821-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f5821-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5821-131">-ResourceId</span></span>
<span data-ttu-id="f5821-132">ANF 備份的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f5821-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="f5821-133">-標記</span><span class="sxs-lookup"><span data-stu-id="f5821-133">-Tag</span></span>
<span data-ttu-id="f5821-134">代表資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="f5821-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="f5821-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="f5821-135">-VolumeName</span></span>
<span data-ttu-id="f5821-136">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="f5821-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f5821-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="f5821-137">-VolumeObject</span></span>
<span data-ttu-id="f5821-138">包含要返回之備份的音量物件</span><span class="sxs-lookup"><span data-stu-id="f5821-138">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5821-139">-確認</span><span class="sxs-lookup"><span data-stu-id="f5821-139">-Confirm</span></span>
<span data-ttu-id="f5821-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f5821-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5821-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5821-141">-WhatIf</span></span>
<span data-ttu-id="f5821-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5821-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5821-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5821-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5821-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5821-144">CommonParameters</span></span>
<span data-ttu-id="f5821-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5821-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5821-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5821-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5821-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f5821-147">INPUTS</span></span>

### <span data-ttu-id="f5821-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f5821-148">System.String</span></span>

### <span data-ttu-id="f5821-149">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f5821-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="f5821-150">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="f5821-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="f5821-151">輸出</span><span class="sxs-lookup"><span data-stu-id="f5821-151">OUTPUTS</span></span>

### <span data-ttu-id="f5821-152">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f5821-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="f5821-153">筆記</span><span class="sxs-lookup"><span data-stu-id="f5821-153">NOTES</span></span>

## <span data-ttu-id="f5821-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5821-154">RELATED LINKS</span></span>

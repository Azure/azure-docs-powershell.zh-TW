---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesBackup.md
ms.openlocfilehash: a2cab03bb88d5b642a95142030eb646b2a5abef4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276996"
---
# <span data-ttu-id="e098f-101">Update-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="e098f-101">Update-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="e098f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e098f-102">SYNOPSIS</span></span>
<span data-ttu-id="e098f-103">更新 (ANF) 備份的 Azure NetApp 檔案至提供的選擇性修飾符。</span><span class="sxs-lookup"><span data-stu-id="e098f-103">Updates an Azure NetApp Files (ANF) backup to the optional modifiers provided.</span></span>

## <span data-ttu-id="e098f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e098f-104">SYNTAX</span></span>

### <span data-ttu-id="e098f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e098f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolName <String> -VolumeName <String> [-Label <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e098f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098f-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup -Name <String> [-Label <String>] [-Tag <Hashtable>]
 -VolumeObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e098f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098f-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e098f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098f-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesBackup [-Label <String>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesBackup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e098f-109">說明</span><span class="sxs-lookup"><span data-stu-id="e098f-109">DESCRIPTION</span></span>
<span data-ttu-id="e098f-110">**AzNetAppFilesBackup** Cmdlet 會修改 ANF 備份。</span><span class="sxs-lookup"><span data-stu-id="e098f-110">The **Update-AzNetAppFilesBackup** cmdlet modifies an ANF backup.</span></span>

## <span data-ttu-id="e098f-111">示例</span><span class="sxs-lookup"><span data-stu-id="e098f-111">EXAMPLES</span></span>

### <span data-ttu-id="e098f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e098f-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName $accName1 -Name $backupPolicyObject -Label "updatedLabel"
```

<span data-ttu-id="e098f-113">這個命令會針對指定的備份執行更新，修改所提供的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="e098f-113">This command performs an update on the given backup modifying the username to that provided.</span></span>

## <span data-ttu-id="e098f-114">參數</span><span class="sxs-lookup"><span data-stu-id="e098f-114">PARAMETERS</span></span>

### <span data-ttu-id="e098f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e098f-115">-AccountName</span></span>
<span data-ttu-id="e098f-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="e098f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="e098f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e098f-117">-DefaultProfile</span></span>
<span data-ttu-id="e098f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e098f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e098f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e098f-119">-InputObject</span></span>
<span data-ttu-id="e098f-120">要移除的快照物件</span><span class="sxs-lookup"><span data-stu-id="e098f-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="e098f-121">-標籤</span><span class="sxs-lookup"><span data-stu-id="e098f-121">-Label</span></span>
<span data-ttu-id="e098f-122">備份標籤</span><span class="sxs-lookup"><span data-stu-id="e098f-122">Label for backup</span></span>

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

### <span data-ttu-id="e098f-123">-位置</span><span class="sxs-lookup"><span data-stu-id="e098f-123">-Location</span></span>
<span data-ttu-id="e098f-124">資源的位置</span><span class="sxs-lookup"><span data-stu-id="e098f-124">The location of the resource</span></span>

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

### <span data-ttu-id="e098f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e098f-125">-Name</span></span>
<span data-ttu-id="e098f-126">ANF 備份原則的名稱</span><span class="sxs-lookup"><span data-stu-id="e098f-126">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="e098f-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e098f-127">-PoolName</span></span>
<span data-ttu-id="e098f-128">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="e098f-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="e098f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e098f-129">-ResourceGroupName</span></span>
<span data-ttu-id="e098f-130">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="e098f-130">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e098f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e098f-131">-ResourceId</span></span>
<span data-ttu-id="e098f-132">ANF 備份的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e098f-132">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="e098f-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="e098f-133">-Tag</span></span>
<span data-ttu-id="e098f-134">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="e098f-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="e098f-135">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="e098f-135">-VolumeName</span></span>
<span data-ttu-id="e098f-136">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="e098f-136">The name of the ANF volume</span></span>

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

### <span data-ttu-id="e098f-137">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="e098f-137">-VolumeObject</span></span>
<span data-ttu-id="e098f-138">包含要返回之備份的卷物件</span><span class="sxs-lookup"><span data-stu-id="e098f-138">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="e098f-139">-確認</span><span class="sxs-lookup"><span data-stu-id="e098f-139">-Confirm</span></span>
<span data-ttu-id="e098f-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e098f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e098f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e098f-141">-WhatIf</span></span>
<span data-ttu-id="e098f-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e098f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e098f-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e098f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e098f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e098f-144">CommonParameters</span></span>
<span data-ttu-id="e098f-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e098f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e098f-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e098f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e098f-147">輸入</span><span class="sxs-lookup"><span data-stu-id="e098f-147">INPUTS</span></span>

### <span data-ttu-id="e098f-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e098f-148">System.String</span></span>

### <span data-ttu-id="e098f-149">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="e098f-149">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="e098f-150">PSNetAppFilesBackup 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="e098f-150">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="e098f-151">輸出</span><span class="sxs-lookup"><span data-stu-id="e098f-151">OUTPUTS</span></span>

### <span data-ttu-id="e098f-152">PSNetAppFilesBackupPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="e098f-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="e098f-153">筆記</span><span class="sxs-lookup"><span data-stu-id="e098f-153">NOTES</span></span>

## <span data-ttu-id="e098f-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="e098f-154">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: 34b4e43dcd09df600c73a6dd0a459a41b491da3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135042"
---
# <span data-ttu-id="c2c22-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="c2c22-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="c2c22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2c22-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c22-103">刪除 (ANF) 備份的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="c2c22-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="c2c22-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2c22-104">SYNTAX</span></span>

### <span data-ttu-id="c2c22-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c2c22-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c22-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2c22-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c22-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2c22-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c22-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2c22-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2c22-109">說明</span><span class="sxs-lookup"><span data-stu-id="c2c22-109">DESCRIPTION</span></span>
<span data-ttu-id="c2c22-110">**AzNetAppFilesBackup** Cmdlet 會刪除 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="c2c22-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="c2c22-111">示例</span><span class="sxs-lookup"><span data-stu-id="c2c22-111">EXAMPLES</span></span>

### <span data-ttu-id="c2c22-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c2c22-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="c2c22-113">這個命令會刪除 [MyBackup "卷名為「MyVolume」的新 ANF 備份。</span><span class="sxs-lookup"><span data-stu-id="c2c22-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="c2c22-114">參數</span><span class="sxs-lookup"><span data-stu-id="c2c22-114">PARAMETERS</span></span>

### <span data-ttu-id="c2c22-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2c22-115">-AccountName</span></span>
<span data-ttu-id="c2c22-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="c2c22-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c22-117">-DefaultProfile</span></span>
<span data-ttu-id="c2c22-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2c22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2c22-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2c22-119">-InputObject</span></span>
<span data-ttu-id="c2c22-120">要移除的快照物件</span><span class="sxs-lookup"><span data-stu-id="c2c22-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="c2c22-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2c22-121">-Name</span></span>
<span data-ttu-id="c2c22-122">ANF 備份的名稱</span><span class="sxs-lookup"><span data-stu-id="c2c22-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c22-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2c22-123">-PassThru</span></span>
<span data-ttu-id="c2c22-124">返回是否已成功移除指定的備份</span><span class="sxs-lookup"><span data-stu-id="c2c22-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="c2c22-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c2c22-125">-PoolName</span></span>
<span data-ttu-id="c2c22-126">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="c2c22-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c2c22-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c22-127">-ResourceGroupName</span></span>
<span data-ttu-id="c2c22-128">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="c2c22-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c2c22-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2c22-129">-ResourceId</span></span>
<span data-ttu-id="c2c22-130">ANF 備份的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c2c22-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="c2c22-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="c2c22-131">-VolumeName</span></span>
<span data-ttu-id="c2c22-132">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="c2c22-132">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c22-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="c2c22-133">-VolumeObject</span></span>
<span data-ttu-id="c2c22-134">包含要返回之備份的卷物件</span><span class="sxs-lookup"><span data-stu-id="c2c22-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="c2c22-135">-確認</span><span class="sxs-lookup"><span data-stu-id="c2c22-135">-Confirm</span></span>
<span data-ttu-id="c2c22-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2c22-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2c22-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c22-137">-WhatIf</span></span>
<span data-ttu-id="c2c22-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2c22-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c22-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2c22-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2c22-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c22-140">CommonParameters</span></span>
<span data-ttu-id="c2c22-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2c22-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c22-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c2c22-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c22-143">輸入</span><span class="sxs-lookup"><span data-stu-id="c2c22-143">INPUTS</span></span>

### <span data-ttu-id="c2c22-144">System.object</span><span class="sxs-lookup"><span data-stu-id="c2c22-144">System.String</span></span>

### <span data-ttu-id="c2c22-145">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="c2c22-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="c2c22-146">PSNetAppFilesBackup 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="c2c22-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="c2c22-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c2c22-147">OUTPUTS</span></span>

### <span data-ttu-id="c2c22-148">PSNetAppFilesBackupPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="c2c22-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c2c22-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c2c22-149">NOTES</span></span>

## <span data-ttu-id="c2c22-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2c22-150">RELATED LINKS</span></span>

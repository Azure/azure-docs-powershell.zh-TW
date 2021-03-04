---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackup.md
ms.openlocfilehash: f2f930a3223b8955c7165cadab04d1fe82b2bc3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906006"
---
# <span data-ttu-id="2418c-101">Remove-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="2418c-101">Remove-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="2418c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2418c-102">SYNOPSIS</span></span>
<span data-ttu-id="2418c-103">刪除 ANF 備份 (Azure NetApp) 檔案。</span><span class="sxs-lookup"><span data-stu-id="2418c-103">Deletes an Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="2418c-104">語法</span><span class="sxs-lookup"><span data-stu-id="2418c-104">SYNTAX</span></span>

### <span data-ttu-id="2418c-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2418c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackup -ResourceGroupName <String> [-AccountName <String>] -PoolName <String>
 [-VolumeName <String>] -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2418c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2418c-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -Name <String> -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2418c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2418c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2418c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2418c-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackup -InputObject <PSNetAppFilesBackup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2418c-109">描述</span><span class="sxs-lookup"><span data-stu-id="2418c-109">DESCRIPTION</span></span>
<span data-ttu-id="2418c-110">**Remove-AzNetAppFilesBackup** Cmdlet 會刪除 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2418c-110">The **Remove-AzNetAppFilesBackup** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="2418c-111">例子</span><span class="sxs-lookup"><span data-stu-id="2418c-111">EXAMPLES</span></span>

### <span data-ttu-id="2418c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2418c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="2418c-113">此命令會刪除新的 ANF 備份，而大量 「MyVolume」的名稱為 「MyBackup」。</span><span class="sxs-lookup"><span data-stu-id="2418c-113">This command deletes the new ANF backup with a the name "MyBackup" for volume "MyVolume".</span></span>

## <span data-ttu-id="2418c-114">參數</span><span class="sxs-lookup"><span data-stu-id="2418c-114">PARAMETERS</span></span>

### <span data-ttu-id="2418c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2418c-115">-AccountName</span></span>
<span data-ttu-id="2418c-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="2418c-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="2418c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2418c-117">-DefaultProfile</span></span>
<span data-ttu-id="2418c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2418c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2418c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2418c-119">-InputObject</span></span>
<span data-ttu-id="2418c-120">要移除的快照物件</span><span class="sxs-lookup"><span data-stu-id="2418c-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="2418c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2418c-121">-Name</span></span>
<span data-ttu-id="2418c-122">ANF 備份的名稱</span><span class="sxs-lookup"><span data-stu-id="2418c-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="2418c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2418c-123">-PassThru</span></span>
<span data-ttu-id="2418c-124">返回指定的備份是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="2418c-124">Return whether the specified backup was successfully removed</span></span>

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

### <span data-ttu-id="2418c-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2418c-125">-PoolName</span></span>
<span data-ttu-id="2418c-126">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="2418c-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="2418c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2418c-127">-ResourceGroupName</span></span>
<span data-ttu-id="2418c-128">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="2418c-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2418c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2418c-129">-ResourceId</span></span>
<span data-ttu-id="2418c-130">ANF 備份的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2418c-130">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="2418c-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="2418c-131">-VolumeName</span></span>
<span data-ttu-id="2418c-132">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="2418c-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="2418c-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="2418c-133">-VolumeObject</span></span>
<span data-ttu-id="2418c-134">包含要返回之備份的音量物件</span><span class="sxs-lookup"><span data-stu-id="2418c-134">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="2418c-135">-確認</span><span class="sxs-lookup"><span data-stu-id="2418c-135">-Confirm</span></span>
<span data-ttu-id="2418c-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2418c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2418c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2418c-137">-WhatIf</span></span>
<span data-ttu-id="2418c-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2418c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2418c-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2418c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2418c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2418c-140">CommonParameters</span></span>
<span data-ttu-id="2418c-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2418c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2418c-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2418c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2418c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="2418c-143">INPUTS</span></span>

### <span data-ttu-id="2418c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2418c-144">System.String</span></span>

### <span data-ttu-id="2418c-145">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2418c-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="2418c-146">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="2418c-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="2418c-147">輸出</span><span class="sxs-lookup"><span data-stu-id="2418c-147">OUTPUTS</span></span>

### <span data-ttu-id="2418c-148">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="2418c-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="2418c-149">筆記</span><span class="sxs-lookup"><span data-stu-id="2418c-149">NOTES</span></span>

## <span data-ttu-id="2418c-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="2418c-150">RELATED LINKS</span></span>

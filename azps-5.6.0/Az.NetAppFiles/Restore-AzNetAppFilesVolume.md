---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 8c07b375214ef78f281bdfab2b31a94e0504b30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905982"
---
# <span data-ttu-id="0c3b1-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="0c3b1-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="0c3b1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0c3b1-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3b1-103">將音量還原到其中一個快照</span><span class="sxs-lookup"><span data-stu-id="0c3b1-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="0c3b1-104">語法</span><span class="sxs-lookup"><span data-stu-id="0c3b1-104">SYNTAX</span></span>

### <span data-ttu-id="0c3b1-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0c3b1-105">ByFieldsParameterSet (Default)</span></span>
```
Restore-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0c3b1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c3b1-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c3b1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c3b1-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c3b1-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c3b1-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3b1-109">描述</span><span class="sxs-lookup"><span data-stu-id="0c3b1-109">DESCRIPTION</span></span>
<span data-ttu-id="0c3b1-110">還原/還原到 SnapshotId 參數中指定的快照</span><span class="sxs-lookup"><span data-stu-id="0c3b1-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="0c3b1-111">例子</span><span class="sxs-lookup"><span data-stu-id="0c3b1-111">EXAMPLES</span></span>

### <span data-ttu-id="0c3b1-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0c3b1-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="0c3b1-113">此命令使用 snapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf 將大量 MyVolume 還原為其中一個快照</span><span class="sxs-lookup"><span data-stu-id="0c3b1-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="0c3b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="0c3b1-114">PARAMETERS</span></span>

### <span data-ttu-id="0c3b1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c3b1-115">-AccountName</span></span>
<span data-ttu-id="0c3b1-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="0c3b1-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="0c3b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3b1-117">-DefaultProfile</span></span>
<span data-ttu-id="0c3b1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c3b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c3b1-119">-InputObject</span></span>
<span data-ttu-id="0c3b1-120">要移除的音量物件</span><span class="sxs-lookup"><span data-stu-id="0c3b1-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3b1-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c3b1-121">-Name</span></span>
<span data-ttu-id="0c3b1-122">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="0c3b1-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3b1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c3b1-123">-PassThru</span></span>
<span data-ttu-id="0c3b1-124">返回指定的卷是否成功還原/還原</span><span class="sxs-lookup"><span data-stu-id="0c3b1-124">Return whether the specified volume was successfully restored/reverted</span></span>

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

### <span data-ttu-id="0c3b1-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="0c3b1-125">-PoolName</span></span>
<span data-ttu-id="0c3b1-126">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="0c3b1-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="0c3b1-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="0c3b1-127">-PoolObject</span></span>
<span data-ttu-id="0c3b1-128">包含要移除之卷的集中物件</span><span class="sxs-lookup"><span data-stu-id="0c3b1-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3b1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3b1-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c3b1-130">ANF 音量的資源群組</span><span class="sxs-lookup"><span data-stu-id="0c3b1-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="0c3b1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c3b1-131">-ResourceId</span></span>
<span data-ttu-id="0c3b1-132">ANF 音量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0c3b1-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="0c3b1-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="0c3b1-133">-SnapshotId</span></span>
<span data-ttu-id="0c3b1-134">快照的 SnapshotId。</span><span class="sxs-lookup"><span data-stu-id="0c3b1-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="0c3b1-135">用來識別快照的 UUID v4</span><span class="sxs-lookup"><span data-stu-id="0c3b1-135">UUID v4 used to identify the Snapshot</span></span>

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

### <span data-ttu-id="0c3b1-136">-確認</span><span class="sxs-lookup"><span data-stu-id="0c3b1-136">-Confirm</span></span>
<span data-ttu-id="0c3b1-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0c3b1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3b1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3b1-138">-WhatIf</span></span>
<span data-ttu-id="0c3b1-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c3b1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c3b1-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c3b1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3b1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3b1-141">CommonParameters</span></span>
<span data-ttu-id="0c3b1-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0c3b1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3b1-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c3b1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3b1-144">輸入</span><span class="sxs-lookup"><span data-stu-id="0c3b1-144">INPUTS</span></span>

### <span data-ttu-id="0c3b1-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0c3b1-145">System.String</span></span>

### <span data-ttu-id="0c3b1-146">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0c3b1-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="0c3b1-147">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="0c3b1-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="0c3b1-148">輸出</span><span class="sxs-lookup"><span data-stu-id="0c3b1-148">OUTPUTS</span></span>

### <span data-ttu-id="0c3b1-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c3b1-149">System.Boolean</span></span>

## <span data-ttu-id="0c3b1-150">筆記</span><span class="sxs-lookup"><span data-stu-id="0c3b1-150">NOTES</span></span>

## <span data-ttu-id="0c3b1-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c3b1-151">RELATED LINKS</span></span>

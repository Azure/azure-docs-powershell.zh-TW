---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126542"
---
# <span data-ttu-id="a5842-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a5842-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a5842-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5842-102">SYNOPSIS</span></span>
<span data-ttu-id="a5842-103">將卷還原/復原至其中一個快照</span><span class="sxs-lookup"><span data-stu-id="a5842-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="a5842-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5842-104">SYNTAX</span></span>

### <span data-ttu-id="a5842-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a5842-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5842-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5842-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5842-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5842-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5842-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5842-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5842-109">說明</span><span class="sxs-lookup"><span data-stu-id="a5842-109">DESCRIPTION</span></span>
<span data-ttu-id="a5842-110">將卷還原/復原至 SnapshotId 參數中指定的快照</span><span class="sxs-lookup"><span data-stu-id="a5842-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="a5842-111">示例</span><span class="sxs-lookup"><span data-stu-id="a5842-111">EXAMPLES</span></span>

### <span data-ttu-id="a5842-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a5842-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="a5842-113">這個命令會將大量 MyVolume 還原/還原成其中一個快照 snapshotId 的7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="a5842-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="a5842-114">參數</span><span class="sxs-lookup"><span data-stu-id="a5842-114">PARAMETERS</span></span>

### <span data-ttu-id="a5842-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5842-115">-AccountName</span></span>
<span data-ttu-id="a5842-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="a5842-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5842-117">-DefaultProfile</span></span>
<span data-ttu-id="a5842-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5842-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5842-119">-InputObject</span></span>
<span data-ttu-id="a5842-120">要移除的卷物件</span><span class="sxs-lookup"><span data-stu-id="a5842-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5842-121">-Name</span></span>
<span data-ttu-id="a5842-122">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="a5842-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5842-123">-PassThru</span></span>
<span data-ttu-id="a5842-124">傳回指定的磁片卷是否已順利還原/還原</span><span class="sxs-lookup"><span data-stu-id="a5842-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a5842-125">-PoolName</span></span>
<span data-ttu-id="a5842-126">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="a5842-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="a5842-127">-PoolObject</span></span>
<span data-ttu-id="a5842-128">包含要移除之卷的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="a5842-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5842-129">-ResourceGroupName</span></span>
<span data-ttu-id="a5842-130">ANF 體積中的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="a5842-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5842-131">-ResourceId</span></span>
<span data-ttu-id="a5842-132">ANF 體積的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a5842-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="a5842-133">-SnapshotId</span></span>
<span data-ttu-id="a5842-134">快照的 SnapshotId。</span><span class="sxs-lookup"><span data-stu-id="a5842-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="a5842-135">用來識別快照的 UUID v4</span><span class="sxs-lookup"><span data-stu-id="a5842-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-136">-確認</span><span class="sxs-lookup"><span data-stu-id="a5842-136">-Confirm</span></span>
<span data-ttu-id="a5842-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5842-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5842-138">-WhatIf</span></span>
<span data-ttu-id="a5842-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5842-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5842-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5842-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5842-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5842-141">CommonParameters</span></span>
<span data-ttu-id="a5842-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5842-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5842-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5842-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5842-144">輸入</span><span class="sxs-lookup"><span data-stu-id="a5842-144">INPUTS</span></span>

### <span data-ttu-id="a5842-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a5842-145">System.String</span></span>

### <span data-ttu-id="a5842-146">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a5842-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="a5842-147">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a5842-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a5842-148">輸出</span><span class="sxs-lookup"><span data-stu-id="a5842-148">OUTPUTS</span></span>

### <span data-ttu-id="a5842-149">System.object</span><span class="sxs-lookup"><span data-stu-id="a5842-149">System.Boolean</span></span>

## <span data-ttu-id="a5842-150">筆記</span><span class="sxs-lookup"><span data-stu-id="a5842-150">NOTES</span></span>

## <span data-ttu-id="a5842-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5842-151">RELATED LINKS</span></span>
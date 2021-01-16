---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288772"
---
# <span data-ttu-id="1aa99-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="1aa99-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="1aa99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1aa99-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa99-103"> (ANF) 快照建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="1aa99-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="1aa99-104">句法</span><span class="sxs-lookup"><span data-stu-id="1aa99-104">SYNTAX</span></span>

### <span data-ttu-id="1aa99-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1aa99-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa99-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa99-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa99-107">說明</span><span class="sxs-lookup"><span data-stu-id="1aa99-107">DESCRIPTION</span></span>
<span data-ttu-id="1aa99-108">**新的-AzNetAppFilesSnapshot** Cmdlet 會建立 ANF 快照。</span><span class="sxs-lookup"><span data-stu-id="1aa99-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="1aa99-109">示例</span><span class="sxs-lookup"><span data-stu-id="1aa99-109">EXAMPLES</span></span>

### <span data-ttu-id="1aa99-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1aa99-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="1aa99-111">這個命令會在 [MyAnfVolume] 卷中建立新的 ANF 快照「MyAnfSnapshot」。</span><span class="sxs-lookup"><span data-stu-id="1aa99-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="1aa99-112">參數</span><span class="sxs-lookup"><span data-stu-id="1aa99-112">PARAMETERS</span></span>

### <span data-ttu-id="1aa99-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1aa99-113">-AccountName</span></span>
<span data-ttu-id="1aa99-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="1aa99-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="1aa99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa99-115">-DefaultProfile</span></span>
<span data-ttu-id="1aa99-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1aa99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa99-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="1aa99-117">-FileSystemId</span></span>
<span data-ttu-id="1aa99-118">檔案系統識別碼</span><span class="sxs-lookup"><span data-stu-id="1aa99-118">The file system id</span></span>

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

### <span data-ttu-id="1aa99-119">-位置</span><span class="sxs-lookup"><span data-stu-id="1aa99-119">-Location</span></span>
<span data-ttu-id="1aa99-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="1aa99-120">The location of the resource</span></span>

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

### <span data-ttu-id="1aa99-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1aa99-121">-Name</span></span>
<span data-ttu-id="1aa99-122">ANF 快照的名稱</span><span class="sxs-lookup"><span data-stu-id="1aa99-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa99-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1aa99-123">-PoolName</span></span>
<span data-ttu-id="1aa99-124">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="1aa99-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="1aa99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa99-125">-ResourceGroupName</span></span>
<span data-ttu-id="1aa99-126">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="1aa99-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1aa99-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="1aa99-127">-Tag</span></span>
<span data-ttu-id="1aa99-128">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="1aa99-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="1aa99-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="1aa99-129">-VolumeName</span></span>
<span data-ttu-id="1aa99-130">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="1aa99-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="1aa99-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="1aa99-131">-VolumeObject</span></span>
<span data-ttu-id="1aa99-132">新快照物件的音量</span><span class="sxs-lookup"><span data-stu-id="1aa99-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="1aa99-133">-確認</span><span class="sxs-lookup"><span data-stu-id="1aa99-133">-Confirm</span></span>
<span data-ttu-id="1aa99-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1aa99-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa99-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa99-135">-WhatIf</span></span>
<span data-ttu-id="1aa99-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1aa99-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa99-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1aa99-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa99-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa99-138">CommonParameters</span></span>
<span data-ttu-id="1aa99-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1aa99-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa99-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1aa99-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa99-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1aa99-141">INPUTS</span></span>

### <span data-ttu-id="1aa99-142">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="1aa99-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="1aa99-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1aa99-143">OUTPUTS</span></span>

### <span data-ttu-id="1aa99-144">PSNetAppFilesSnapshot 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="1aa99-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="1aa99-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1aa99-145">NOTES</span></span>

## <span data-ttu-id="1aa99-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1aa99-146">RELATED LINKS</span></span>

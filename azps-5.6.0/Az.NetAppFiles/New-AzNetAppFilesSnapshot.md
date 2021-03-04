---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 47d1aeb2868e8f104791527636a67a31b1e42c1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906033"
---
# <span data-ttu-id="52407-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="52407-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="52407-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52407-102">SYNOPSIS</span></span>
<span data-ttu-id="52407-103">在 ANF 快照中 (Azure NetApp) 檔案。</span><span class="sxs-lookup"><span data-stu-id="52407-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="52407-104">語法</span><span class="sxs-lookup"><span data-stu-id="52407-104">SYNTAX</span></span>

### <span data-ttu-id="52407-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="52407-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52407-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52407-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52407-107">描述</span><span class="sxs-lookup"><span data-stu-id="52407-107">DESCRIPTION</span></span>
<span data-ttu-id="52407-108">**New-AzNetAppFilesSnapshot** Cmdlet 會建立 ANF 快照。</span><span class="sxs-lookup"><span data-stu-id="52407-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="52407-109">例子</span><span class="sxs-lookup"><span data-stu-id="52407-109">EXAMPLES</span></span>

### <span data-ttu-id="52407-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="52407-110">Example 1</span></span>
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

<span data-ttu-id="52407-111">此命令在「MyAnfVolume」的音量中建立新的 ANF 快照「MyAnfSnapshot」。</span><span class="sxs-lookup"><span data-stu-id="52407-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="52407-112">參數</span><span class="sxs-lookup"><span data-stu-id="52407-112">PARAMETERS</span></span>

### <span data-ttu-id="52407-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52407-113">-AccountName</span></span>
<span data-ttu-id="52407-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="52407-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="52407-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52407-115">-DefaultProfile</span></span>
<span data-ttu-id="52407-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="52407-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52407-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="52407-117">-FileSystemId</span></span>
<span data-ttu-id="52407-118">檔案系統識別碼</span><span class="sxs-lookup"><span data-stu-id="52407-118">The file system id</span></span>

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

### <span data-ttu-id="52407-119">-位置</span><span class="sxs-lookup"><span data-stu-id="52407-119">-Location</span></span>
<span data-ttu-id="52407-120">資源的位置</span><span class="sxs-lookup"><span data-stu-id="52407-120">The location of the resource</span></span>

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

### <span data-ttu-id="52407-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="52407-121">-Name</span></span>
<span data-ttu-id="52407-122">ANF 快照的名稱</span><span class="sxs-lookup"><span data-stu-id="52407-122">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="52407-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="52407-123">-PoolName</span></span>
<span data-ttu-id="52407-124">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="52407-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="52407-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52407-125">-ResourceGroupName</span></span>
<span data-ttu-id="52407-126">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="52407-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="52407-127">-標記</span><span class="sxs-lookup"><span data-stu-id="52407-127">-Tag</span></span>
<span data-ttu-id="52407-128">代表資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="52407-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="52407-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="52407-129">-VolumeName</span></span>
<span data-ttu-id="52407-130">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="52407-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="52407-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="52407-131">-VolumeObject</span></span>
<span data-ttu-id="52407-132">新快照物件的音量</span><span class="sxs-lookup"><span data-stu-id="52407-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="52407-133">-確認</span><span class="sxs-lookup"><span data-stu-id="52407-133">-Confirm</span></span>
<span data-ttu-id="52407-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="52407-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52407-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52407-135">-WhatIf</span></span>
<span data-ttu-id="52407-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52407-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52407-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52407-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52407-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52407-138">CommonParameters</span></span>
<span data-ttu-id="52407-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52407-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52407-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52407-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52407-141">輸入</span><span class="sxs-lookup"><span data-stu-id="52407-141">INPUTS</span></span>

### <span data-ttu-id="52407-142">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="52407-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="52407-143">輸出</span><span class="sxs-lookup"><span data-stu-id="52407-143">OUTPUTS</span></span>

### <span data-ttu-id="52407-144">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="52407-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="52407-145">筆記</span><span class="sxs-lookup"><span data-stu-id="52407-145">NOTES</span></span>

## <span data-ttu-id="52407-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="52407-146">RELATED LINKS</span></span>

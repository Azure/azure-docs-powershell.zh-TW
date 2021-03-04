---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 2b3cf6588f32fd958073ced8d3347733416037ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905966"
---
# <span data-ttu-id="22331-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="22331-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="22331-102">簡介</span><span class="sxs-lookup"><span data-stu-id="22331-102">SYNOPSIS</span></span>
<span data-ttu-id="22331-103">將 Azure NetApp 檔案的資料庫 (ANF) 音量。</span><span class="sxs-lookup"><span data-stu-id="22331-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="22331-104">語法</span><span class="sxs-lookup"><span data-stu-id="22331-104">SYNTAX</span></span>

### <span data-ttu-id="22331-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="22331-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22331-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22331-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22331-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22331-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22331-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22331-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22331-109">描述</span><span class="sxs-lookup"><span data-stu-id="22331-109">DESCRIPTION</span></span>
<span data-ttu-id="22331-110">**Set-AzNetAppFilesVolumePool** Cmdlet 會變更 ANF 音量的集區。</span><span class="sxs-lookup"><span data-stu-id="22331-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="22331-111">例子</span><span class="sxs-lookup"><span data-stu-id="22331-111">EXAMPLES</span></span>

### <span data-ttu-id="22331-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="22331-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="22331-113">這會將大量 MyVolume 的集中變更為識別碼為 7d6e4069-6c78-6c61-7bf6-c60968e45fbf 的</span><span class="sxs-lookup"><span data-stu-id="22331-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="22331-114">參數</span><span class="sxs-lookup"><span data-stu-id="22331-114">PARAMETERS</span></span>

### <span data-ttu-id="22331-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22331-115">-AccountName</span></span>
<span data-ttu-id="22331-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="22331-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="22331-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22331-117">-DefaultProfile</span></span>
<span data-ttu-id="22331-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="22331-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22331-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22331-119">-InputObject</span></span>
<span data-ttu-id="22331-120">要移動的音量物件</span><span class="sxs-lookup"><span data-stu-id="22331-120">The volume object to move</span></span>

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

### <span data-ttu-id="22331-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="22331-121">-Name</span></span>
<span data-ttu-id="22331-122">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="22331-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="22331-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="22331-123">-NewPoolResourceId</span></span>
<span data-ttu-id="22331-124">要移動至之容量庫的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="22331-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="22331-125">用來識別資料庫的 UUID v4</span><span class="sxs-lookup"><span data-stu-id="22331-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="22331-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="22331-126">-PoolName</span></span>
<span data-ttu-id="22331-127">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="22331-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="22331-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="22331-128">-PoolObject</span></span>
<span data-ttu-id="22331-129">包含該音量的集中物件</span><span class="sxs-lookup"><span data-stu-id="22331-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="22331-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22331-130">-ResourceGroupName</span></span>
<span data-ttu-id="22331-131">ANF 音量的資源群組</span><span class="sxs-lookup"><span data-stu-id="22331-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="22331-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22331-132">-ResourceId</span></span>
<span data-ttu-id="22331-133">ANF 音量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="22331-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="22331-134">-確認</span><span class="sxs-lookup"><span data-stu-id="22331-134">-Confirm</span></span>
<span data-ttu-id="22331-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="22331-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22331-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22331-136">-WhatIf</span></span>
<span data-ttu-id="22331-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22331-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22331-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22331-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22331-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22331-139">CommonParameters</span></span>
<span data-ttu-id="22331-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="22331-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22331-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22331-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22331-142">輸入</span><span class="sxs-lookup"><span data-stu-id="22331-142">INPUTS</span></span>

### <span data-ttu-id="22331-143">System.String</span><span class="sxs-lookup"><span data-stu-id="22331-143">System.String</span></span>

### <span data-ttu-id="22331-144">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="22331-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="22331-145">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="22331-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="22331-146">輸出</span><span class="sxs-lookup"><span data-stu-id="22331-146">OUTPUTS</span></span>

### <span data-ttu-id="22331-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22331-147">System.Boolean</span></span>

## <span data-ttu-id="22331-148">筆記</span><span class="sxs-lookup"><span data-stu-id="22331-148">NOTES</span></span>

## <span data-ttu-id="22331-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="22331-149">RELATED LINKS</span></span>

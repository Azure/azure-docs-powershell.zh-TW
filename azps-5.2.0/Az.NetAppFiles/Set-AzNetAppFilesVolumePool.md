---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285080"
---
# <span data-ttu-id="a4939-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="a4939-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="a4939-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4939-102">SYNOPSIS</span></span>
<span data-ttu-id="a4939-103">變更 Azure NetApp 檔案的 pool (ANF) 音量。</span><span class="sxs-lookup"><span data-stu-id="a4939-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="a4939-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4939-104">SYNTAX</span></span>

### <span data-ttu-id="a4939-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4939-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4939-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4939-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4939-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4939-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4939-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4939-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4939-109">說明</span><span class="sxs-lookup"><span data-stu-id="a4939-109">DESCRIPTION</span></span>
<span data-ttu-id="a4939-110">**AzNetAppFilesVolumePool** Cmdlet 會變更 ANF 卷的池。</span><span class="sxs-lookup"><span data-stu-id="a4939-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="a4939-111">示例</span><span class="sxs-lookup"><span data-stu-id="a4939-111">EXAMPLES</span></span>

### <span data-ttu-id="a4939-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a4939-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="a4939-113">這會將 volume MyVolume 的 pool 變更成具有 7d6e4069-6c78-6c61-7bf6-c60968e45fbf Id 的磁片池</span><span class="sxs-lookup"><span data-stu-id="a4939-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="a4939-114">參數</span><span class="sxs-lookup"><span data-stu-id="a4939-114">PARAMETERS</span></span>

### <span data-ttu-id="a4939-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a4939-115">-AccountName</span></span>
<span data-ttu-id="a4939-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="a4939-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="a4939-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4939-117">-DefaultProfile</span></span>
<span data-ttu-id="a4939-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4939-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4939-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4939-119">-InputObject</span></span>
<span data-ttu-id="a4939-120">要移動的卷物件</span><span class="sxs-lookup"><span data-stu-id="a4939-120">The volume object to move</span></span>

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

### <span data-ttu-id="a4939-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4939-121">-Name</span></span>
<span data-ttu-id="a4939-122">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="a4939-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="a4939-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="a4939-123">-NewPoolResourceId</span></span>
<span data-ttu-id="a4939-124">要移至的容量池資源 Id。</span><span class="sxs-lookup"><span data-stu-id="a4939-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="a4939-125">用來識別該池的 UUID v4</span><span class="sxs-lookup"><span data-stu-id="a4939-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="a4939-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a4939-126">-PoolName</span></span>
<span data-ttu-id="a4939-127">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="a4939-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a4939-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="a4939-128">-PoolObject</span></span>
<span data-ttu-id="a4939-129">包含音量的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="a4939-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="a4939-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4939-130">-ResourceGroupName</span></span>
<span data-ttu-id="a4939-131">ANF 體積中的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="a4939-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="a4939-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4939-132">-ResourceId</span></span>
<span data-ttu-id="a4939-133">ANF 體積的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a4939-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="a4939-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a4939-134">-Confirm</span></span>
<span data-ttu-id="a4939-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4939-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4939-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4939-136">-WhatIf</span></span>
<span data-ttu-id="a4939-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4939-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4939-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4939-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4939-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4939-139">CommonParameters</span></span>
<span data-ttu-id="a4939-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4939-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4939-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4939-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4939-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a4939-142">INPUTS</span></span>

### <span data-ttu-id="a4939-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a4939-143">System.String</span></span>

### <span data-ttu-id="a4939-144">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a4939-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="a4939-145">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a4939-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a4939-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a4939-146">OUTPUTS</span></span>

### <span data-ttu-id="a4939-147">System.object</span><span class="sxs-lookup"><span data-stu-id="a4939-147">System.Boolean</span></span>

## <span data-ttu-id="a4939-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a4939-148">NOTES</span></span>

## <span data-ttu-id="a4939-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4939-149">RELATED LINKS</span></span>

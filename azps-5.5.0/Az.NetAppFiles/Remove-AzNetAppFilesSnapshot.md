---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131427"
---
# <span data-ttu-id="79896-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="79896-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="79896-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79896-102">SYNOPSIS</span></span>
<span data-ttu-id="79896-103">刪除 (ANF) 快照的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="79896-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="79896-104">句法</span><span class="sxs-lookup"><span data-stu-id="79896-104">SYNTAX</span></span>

### <span data-ttu-id="79896-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="79896-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79896-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79896-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79896-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79896-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79896-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79896-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79896-109">說明</span><span class="sxs-lookup"><span data-stu-id="79896-109">DESCRIPTION</span></span>
<span data-ttu-id="79896-110">**AzNetAppFilesSnapshot** Cmdlet 會刪除 ANF 快照。</span><span class="sxs-lookup"><span data-stu-id="79896-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="79896-111">示例</span><span class="sxs-lookup"><span data-stu-id="79896-111">EXAMPLES</span></span>

### <span data-ttu-id="79896-112">範例1</span><span class="sxs-lookup"><span data-stu-id="79896-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="79896-113">這個命令會刪除 ANF 快照「MyAnfSnapshot」。</span><span class="sxs-lookup"><span data-stu-id="79896-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="79896-114">參數</span><span class="sxs-lookup"><span data-stu-id="79896-114">PARAMETERS</span></span>

### <span data-ttu-id="79896-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79896-115">-AccountName</span></span>
<span data-ttu-id="79896-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="79896-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="79896-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79896-117">-DefaultProfile</span></span>
<span data-ttu-id="79896-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79896-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79896-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79896-119">-InputObject</span></span>
<span data-ttu-id="79896-120">要移除的快照物件</span><span class="sxs-lookup"><span data-stu-id="79896-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79896-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="79896-121">-Name</span></span>
<span data-ttu-id="79896-122">ANF 快照的名稱</span><span class="sxs-lookup"><span data-stu-id="79896-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79896-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79896-123">-PassThru</span></span>
<span data-ttu-id="79896-124">傳回指定的磁片卷是否已順利移除</span><span class="sxs-lookup"><span data-stu-id="79896-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="79896-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="79896-125">-PoolName</span></span>
<span data-ttu-id="79896-126">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="79896-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="79896-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79896-127">-ResourceGroupName</span></span>
<span data-ttu-id="79896-128">ANF 快照的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="79896-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="79896-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79896-129">-ResourceId</span></span>
<span data-ttu-id="79896-130">ANF 快照的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="79896-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="79896-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="79896-131">-VolumeName</span></span>
<span data-ttu-id="79896-132">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="79896-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="79896-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="79896-133">-VolumeObject</span></span>
<span data-ttu-id="79896-134">包含要移除之快照的卷物件</span><span class="sxs-lookup"><span data-stu-id="79896-134">The volume object containing the snapshot to remove</span></span>

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

### <span data-ttu-id="79896-135">-確認</span><span class="sxs-lookup"><span data-stu-id="79896-135">-Confirm</span></span>
<span data-ttu-id="79896-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79896-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79896-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79896-137">-WhatIf</span></span>
<span data-ttu-id="79896-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79896-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79896-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79896-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79896-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79896-140">CommonParameters</span></span>
<span data-ttu-id="79896-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79896-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79896-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="79896-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79896-143">輸入</span><span class="sxs-lookup"><span data-stu-id="79896-143">INPUTS</span></span>

### <span data-ttu-id="79896-144">System.object</span><span class="sxs-lookup"><span data-stu-id="79896-144">System.String</span></span>

### <span data-ttu-id="79896-145">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="79896-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="79896-146">PSNetAppFilesSnapshot 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="79896-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="79896-147">輸出</span><span class="sxs-lookup"><span data-stu-id="79896-147">OUTPUTS</span></span>

### <span data-ttu-id="79896-148">System.object</span><span class="sxs-lookup"><span data-stu-id="79896-148">System.Boolean</span></span>

## <span data-ttu-id="79896-149">筆記</span><span class="sxs-lookup"><span data-stu-id="79896-149">NOTES</span></span>

## <span data-ttu-id="79896-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="79896-150">RELATED LINKS</span></span>

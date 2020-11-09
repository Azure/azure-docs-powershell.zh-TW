---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287923"
---
# <span data-ttu-id="9d1b3-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="9d1b3-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="9d1b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1b3-103">移除/刪除目的地磁片上的複製連線，並傳送版本至來源複製</span><span class="sxs-lookup"><span data-stu-id="9d1b3-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="9d1b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d1b3-104">SYNTAX</span></span>

### <span data-ttu-id="9d1b3-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9d1b3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d1b3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d1b3-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d1b3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d1b3-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d1b3-108">說明</span><span class="sxs-lookup"><span data-stu-id="9d1b3-108">DESCRIPTION</span></span>
<span data-ttu-id="9d1b3-109">移除/刪除目的地磁片上的複製連線，並傳送版本至來源複製</span><span class="sxs-lookup"><span data-stu-id="9d1b3-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="9d1b3-110">示例</span><span class="sxs-lookup"><span data-stu-id="9d1b3-110">EXAMPLES</span></span>

### <span data-ttu-id="9d1b3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9d1b3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="9d1b3-112">這個命令會移除 [MyDestinationAnfVolume] 卷上的 ANF 複製連線。</span><span class="sxs-lookup"><span data-stu-id="9d1b3-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="9d1b3-113">參數</span><span class="sxs-lookup"><span data-stu-id="9d1b3-113">PARAMETERS</span></span>

### <span data-ttu-id="9d1b3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9d1b3-114">-AccountName</span></span>
<span data-ttu-id="9d1b3-115">複製卷 ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="9d1b3-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="9d1b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1b3-116">-DefaultProfile</span></span>
<span data-ttu-id="9d1b3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d1b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d1b3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d1b3-118">-InputObject</span></span>
<span data-ttu-id="9d1b3-119">要移除複製的 ANF 目的地磁片</span><span class="sxs-lookup"><span data-stu-id="9d1b3-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="9d1b3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d1b3-120">-Name</span></span>
<span data-ttu-id="9d1b3-121">ANF 複製目標量的名稱</span><span class="sxs-lookup"><span data-stu-id="9d1b3-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d1b3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d1b3-122">-PassThru</span></span>
<span data-ttu-id="9d1b3-123">返回是否已成功移除指定的 ANF 複製</span><span class="sxs-lookup"><span data-stu-id="9d1b3-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="9d1b3-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9d1b3-124">-PoolName</span></span>
<span data-ttu-id="9d1b3-125">複製卷 ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="9d1b3-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="9d1b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d1b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d1b3-127">ANF 複製目標量的資源群組</span><span class="sxs-lookup"><span data-stu-id="9d1b3-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="9d1b3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d1b3-128">-ResourceId</span></span>
<span data-ttu-id="9d1b3-129">ANF 複製目標量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9d1b3-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="9d1b3-130">-確認</span><span class="sxs-lookup"><span data-stu-id="9d1b3-130">-Confirm</span></span>
<span data-ttu-id="9d1b3-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d1b3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d1b3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d1b3-132">-WhatIf</span></span>
<span data-ttu-id="9d1b3-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d1b3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d1b3-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d1b3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d1b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1b3-135">CommonParameters</span></span>
<span data-ttu-id="9d1b3-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d1b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1b3-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d1b3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1b3-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9d1b3-138">INPUTS</span></span>

### <span data-ttu-id="9d1b3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9d1b3-139">System.String</span></span>

### <span data-ttu-id="9d1b3-140">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="9d1b3-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9d1b3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="9d1b3-141">OUTPUTS</span></span>

### <span data-ttu-id="9d1b3-142">System.object</span><span class="sxs-lookup"><span data-stu-id="9d1b3-142">System.Boolean</span></span>

## <span data-ttu-id="9d1b3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="9d1b3-143">NOTES</span></span>

## <span data-ttu-id="9d1b3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d1b3-144">RELATED LINKS</span></span>

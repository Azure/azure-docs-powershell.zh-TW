---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 4087725afbf845e42c2a00952a818f5eb356d421
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905997"
---
# <span data-ttu-id="ca4d3-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="ca4d3-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="ca4d3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ca4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4d3-103">移除/刪除目標卷上的複製連接，並將發行傳送至來源複製</span><span class="sxs-lookup"><span data-stu-id="ca4d3-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="ca4d3-104">語法</span><span class="sxs-lookup"><span data-stu-id="ca4d3-104">SYNTAX</span></span>

### <span data-ttu-id="ca4d3-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ca4d3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca4d3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4d3-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca4d3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4d3-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca4d3-108">描述</span><span class="sxs-lookup"><span data-stu-id="ca4d3-108">DESCRIPTION</span></span>
<span data-ttu-id="ca4d3-109">移除/刪除目標卷上的複製連接，並將發行傳送至來源複製</span><span class="sxs-lookup"><span data-stu-id="ca4d3-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="ca4d3-110">例子</span><span class="sxs-lookup"><span data-stu-id="ca4d3-110">EXAMPLES</span></span>

### <span data-ttu-id="ca4d3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ca4d3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="ca4d3-112">此命令會移除大量 「MyDestinationAnfVolume」上的 ANF 複製連接。</span><span class="sxs-lookup"><span data-stu-id="ca4d3-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="ca4d3-113">參數</span><span class="sxs-lookup"><span data-stu-id="ca4d3-113">PARAMETERS</span></span>

### <span data-ttu-id="ca4d3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ca4d3-114">-AccountName</span></span>
<span data-ttu-id="ca4d3-115">複製音量的 ANF 帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="ca4d3-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="ca4d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca4d3-116">-DefaultProfile</span></span>
<span data-ttu-id="ca4d3-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca4d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca4d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca4d3-118">-InputObject</span></span>
<span data-ttu-id="ca4d3-119">要移除複製的 ANF 目的地音量</span><span class="sxs-lookup"><span data-stu-id="ca4d3-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="ca4d3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca4d3-120">-Name</span></span>
<span data-ttu-id="ca4d3-121">ANF 複製目的地音量的名稱</span><span class="sxs-lookup"><span data-stu-id="ca4d3-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ca4d3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca4d3-122">-PassThru</span></span>
<span data-ttu-id="ca4d3-123">返回指定的 ANF 複本是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="ca4d3-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="ca4d3-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ca4d3-124">-PoolName</span></span>
<span data-ttu-id="ca4d3-125">複製大量之 ANF 資料庫的名稱</span><span class="sxs-lookup"><span data-stu-id="ca4d3-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="ca4d3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca4d3-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca4d3-127">ANF 複製目的地大量資源群組</span><span class="sxs-lookup"><span data-stu-id="ca4d3-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ca4d3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca4d3-128">-ResourceId</span></span>
<span data-ttu-id="ca4d3-129">ANF 複製目的地大量資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ca4d3-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ca4d3-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ca4d3-130">-Confirm</span></span>
<span data-ttu-id="ca4d3-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ca4d3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca4d3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca4d3-132">-WhatIf</span></span>
<span data-ttu-id="ca4d3-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca4d3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca4d3-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca4d3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca4d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4d3-135">CommonParameters</span></span>
<span data-ttu-id="ca4d3-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ca4d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4d3-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca4d3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4d3-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ca4d3-138">INPUTS</span></span>

### <span data-ttu-id="ca4d3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ca4d3-139">System.String</span></span>

### <span data-ttu-id="ca4d3-140">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ca4d3-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ca4d3-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ca4d3-141">OUTPUTS</span></span>

### <span data-ttu-id="ca4d3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca4d3-142">System.Boolean</span></span>

## <span data-ttu-id="ca4d3-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ca4d3-143">NOTES</span></span>

## <span data-ttu-id="ca4d3-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca4d3-144">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: 198ec8c67939c3ae01a52f2a9b06982ce8ee8d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905965"
---
# <span data-ttu-id="24246-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="24246-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="24246-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24246-102">SYNOPSIS</span></span>
<span data-ttu-id="24246-103">暫停/中斷目的地音量上的複製連接</span><span class="sxs-lookup"><span data-stu-id="24246-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="24246-104">語法</span><span class="sxs-lookup"><span data-stu-id="24246-104">SYNTAX</span></span>

### <span data-ttu-id="24246-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="24246-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24246-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24246-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24246-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24246-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24246-108">描述</span><span class="sxs-lookup"><span data-stu-id="24246-108">DESCRIPTION</span></span>
<span data-ttu-id="24246-109">暫停/中斷目的地音量上的複製連接</span><span class="sxs-lookup"><span data-stu-id="24246-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="24246-110">例子</span><span class="sxs-lookup"><span data-stu-id="24246-110">EXAMPLES</span></span>

### <span data-ttu-id="24246-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="24246-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="24246-112">此命令會暫停大量 「MyDestinationAnfVolume」上的 ANF 複製連接。</span><span class="sxs-lookup"><span data-stu-id="24246-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="24246-113">參數</span><span class="sxs-lookup"><span data-stu-id="24246-113">PARAMETERS</span></span>

### <span data-ttu-id="24246-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24246-114">-AccountName</span></span>
<span data-ttu-id="24246-115">複製音量的 ANF 帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="24246-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="24246-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24246-116">-DefaultProfile</span></span>
<span data-ttu-id="24246-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24246-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24246-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="24246-118">-ForceBreak</span></span>
<span data-ttu-id="24246-119">如果複製是在傳輸狀態，而您想要強制中斷複製，請設為 True</span><span class="sxs-lookup"><span data-stu-id="24246-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24246-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24246-120">-InputObject</span></span>
<span data-ttu-id="24246-121">具有要中斷複製的 ANF 目的地大量物件</span><span class="sxs-lookup"><span data-stu-id="24246-121">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="24246-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="24246-122">-Name</span></span>
<span data-ttu-id="24246-123">ANF 複製目的地音量的名稱</span><span class="sxs-lookup"><span data-stu-id="24246-123">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="24246-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24246-124">-PassThru</span></span>
<span data-ttu-id="24246-125">返回是否執行指定的大量複本中斷</span><span class="sxs-lookup"><span data-stu-id="24246-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="24246-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="24246-126">-PoolName</span></span>
<span data-ttu-id="24246-127">複製大量之 ANF 資料庫的名稱</span><span class="sxs-lookup"><span data-stu-id="24246-127">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="24246-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24246-128">-ResourceGroupName</span></span>
<span data-ttu-id="24246-129">ANF 複製目的地大量資源群組</span><span class="sxs-lookup"><span data-stu-id="24246-129">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="24246-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24246-130">-ResourceId</span></span>
<span data-ttu-id="24246-131">ANF 複製目的地大量資源識別碼</span><span class="sxs-lookup"><span data-stu-id="24246-131">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="24246-132">-確認</span><span class="sxs-lookup"><span data-stu-id="24246-132">-Confirm</span></span>
<span data-ttu-id="24246-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="24246-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24246-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24246-134">-WhatIf</span></span>
<span data-ttu-id="24246-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24246-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24246-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24246-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24246-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24246-137">CommonParameters</span></span>
<span data-ttu-id="24246-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24246-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24246-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24246-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24246-140">輸入</span><span class="sxs-lookup"><span data-stu-id="24246-140">INPUTS</span></span>

### <span data-ttu-id="24246-141">System.String</span><span class="sxs-lookup"><span data-stu-id="24246-141">System.String</span></span>

### <span data-ttu-id="24246-142">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="24246-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="24246-143">輸出</span><span class="sxs-lookup"><span data-stu-id="24246-143">OUTPUTS</span></span>

### <span data-ttu-id="24246-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24246-144">System.Boolean</span></span>

## <span data-ttu-id="24246-145">筆記</span><span class="sxs-lookup"><span data-stu-id="24246-145">NOTES</span></span>

## <span data-ttu-id="24246-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="24246-146">RELATED LINKS</span></span>

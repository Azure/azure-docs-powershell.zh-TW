---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 5f5dac2f2028de9b90941ef91c38361c4357fc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905981"
---
# <span data-ttu-id="edf4c-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="edf4c-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="edf4c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="edf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="edf4c-103">繼續/重新同步目的地音量上的連接。</span><span class="sxs-lookup"><span data-stu-id="edf4c-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="edf4c-104">如果在來源卷上執行作業，它會反向重新同步連接，並同步從來源到目的地。</span><span class="sxs-lookup"><span data-stu-id="edf4c-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="edf4c-105">語法</span><span class="sxs-lookup"><span data-stu-id="edf4c-105">SYNTAX</span></span>

### <span data-ttu-id="edf4c-106">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="edf4c-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edf4c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edf4c-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edf4c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edf4c-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edf4c-109">描述</span><span class="sxs-lookup"><span data-stu-id="edf4c-109">DESCRIPTION</span></span>
<span data-ttu-id="edf4c-110">繼續/重新同步目的地音量上的連接</span><span class="sxs-lookup"><span data-stu-id="edf4c-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="edf4c-111">例子</span><span class="sxs-lookup"><span data-stu-id="edf4c-111">EXAMPLES</span></span>

### <span data-ttu-id="edf4c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="edf4c-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="edf4c-113">此命令會繼續大量 「MyDestinationAnfVolume」上的 ANF 複寫連接。</span><span class="sxs-lookup"><span data-stu-id="edf4c-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="edf4c-114">參數</span><span class="sxs-lookup"><span data-stu-id="edf4c-114">PARAMETERS</span></span>

### <span data-ttu-id="edf4c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="edf4c-115">-AccountName</span></span>
<span data-ttu-id="edf4c-116">複製音量的 ANF 帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="edf4c-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="edf4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf4c-117">-DefaultProfile</span></span>
<span data-ttu-id="edf4c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="edf4c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edf4c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edf4c-119">-InputObject</span></span>
<span data-ttu-id="edf4c-120">要重新同步的 ANF 複製目的地大量物件</span><span class="sxs-lookup"><span data-stu-id="edf4c-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="edf4c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="edf4c-121">-Name</span></span>
<span data-ttu-id="edf4c-122">ANF 複製目的地音量的名稱</span><span class="sxs-lookup"><span data-stu-id="edf4c-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="edf4c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edf4c-123">-PassThru</span></span>
<span data-ttu-id="edf4c-124">返回是否執行指定複本卷的重新同步</span><span class="sxs-lookup"><span data-stu-id="edf4c-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="edf4c-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="edf4c-125">-PoolName</span></span>
<span data-ttu-id="edf4c-126">複製大量之 ANF 資料庫的名稱</span><span class="sxs-lookup"><span data-stu-id="edf4c-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="edf4c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf4c-127">-ResourceGroupName</span></span>
<span data-ttu-id="edf4c-128">ANF 複製目的地大量資源群組</span><span class="sxs-lookup"><span data-stu-id="edf4c-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="edf4c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edf4c-129">-ResourceId</span></span>
<span data-ttu-id="edf4c-130">ANF 複製目的地大量資源識別碼</span><span class="sxs-lookup"><span data-stu-id="edf4c-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="edf4c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="edf4c-131">-Confirm</span></span>
<span data-ttu-id="edf4c-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="edf4c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf4c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf4c-133">-WhatIf</span></span>
<span data-ttu-id="edf4c-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="edf4c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edf4c-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="edf4c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edf4c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf4c-136">CommonParameters</span></span>
<span data-ttu-id="edf4c-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="edf4c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf4c-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edf4c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf4c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="edf4c-139">INPUTS</span></span>

### <span data-ttu-id="edf4c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="edf4c-140">System.String</span></span>

### <span data-ttu-id="edf4c-141">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="edf4c-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="edf4c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="edf4c-142">OUTPUTS</span></span>

### <span data-ttu-id="edf4c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edf4c-143">System.Boolean</span></span>

## <span data-ttu-id="edf4c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="edf4c-144">NOTES</span></span>

## <span data-ttu-id="edf4c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="edf4c-145">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280915"
---
# <span data-ttu-id="a126e-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="a126e-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="a126e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a126e-102">SYNOPSIS</span></span>
<span data-ttu-id="a126e-103">在目的地磁片上繼續/重新同步處理連線。</span><span class="sxs-lookup"><span data-stu-id="a126e-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="a126e-104">如果該作業是在源磁片卷上執行，將會反重新同步處理連線，並從來源同步至 [目的地]。</span><span class="sxs-lookup"><span data-stu-id="a126e-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="a126e-105">句法</span><span class="sxs-lookup"><span data-stu-id="a126e-105">SYNTAX</span></span>

### <span data-ttu-id="a126e-106">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a126e-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a126e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a126e-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a126e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a126e-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a126e-109">說明</span><span class="sxs-lookup"><span data-stu-id="a126e-109">DESCRIPTION</span></span>
<span data-ttu-id="a126e-110">在目的地磁片上繼續/重新同步處理連接</span><span class="sxs-lookup"><span data-stu-id="a126e-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="a126e-111">示例</span><span class="sxs-lookup"><span data-stu-id="a126e-111">EXAMPLES</span></span>

### <span data-ttu-id="a126e-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a126e-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="a126e-113">這個命令會在 volume "MyDestinationAnfVolume" 上繼續 ANF 複製連線。</span><span class="sxs-lookup"><span data-stu-id="a126e-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="a126e-114">參數</span><span class="sxs-lookup"><span data-stu-id="a126e-114">PARAMETERS</span></span>

### <span data-ttu-id="a126e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a126e-115">-AccountName</span></span>
<span data-ttu-id="a126e-116">複製卷 ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="a126e-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="a126e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a126e-117">-DefaultProfile</span></span>
<span data-ttu-id="a126e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a126e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a126e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a126e-119">-InputObject</span></span>
<span data-ttu-id="a126e-120">要重新同步的 ANF 複製目的地卷物件</span><span class="sxs-lookup"><span data-stu-id="a126e-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="a126e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a126e-121">-Name</span></span>
<span data-ttu-id="a126e-122">ANF 複製目標量的名稱</span><span class="sxs-lookup"><span data-stu-id="a126e-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a126e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a126e-123">-PassThru</span></span>
<span data-ttu-id="a126e-124">傳回是否已執行指定的複製卷的 resync</span><span class="sxs-lookup"><span data-stu-id="a126e-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="a126e-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a126e-125">-PoolName</span></span>
<span data-ttu-id="a126e-126">複製卷 ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="a126e-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="a126e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a126e-127">-ResourceGroupName</span></span>
<span data-ttu-id="a126e-128">ANF 複製目標量的資源群組</span><span class="sxs-lookup"><span data-stu-id="a126e-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a126e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a126e-129">-ResourceId</span></span>
<span data-ttu-id="a126e-130">ANF 複製目標量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a126e-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="a126e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a126e-131">-Confirm</span></span>
<span data-ttu-id="a126e-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a126e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a126e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a126e-133">-WhatIf</span></span>
<span data-ttu-id="a126e-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a126e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a126e-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a126e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a126e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a126e-136">CommonParameters</span></span>
<span data-ttu-id="a126e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a126e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a126e-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a126e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a126e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a126e-139">INPUTS</span></span>

### <span data-ttu-id="a126e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a126e-140">System.String</span></span>

### <span data-ttu-id="a126e-141">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a126e-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a126e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="a126e-142">OUTPUTS</span></span>

### <span data-ttu-id="a126e-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a126e-143">System.Boolean</span></span>

## <span data-ttu-id="a126e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a126e-144">NOTES</span></span>

## <span data-ttu-id="a126e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a126e-145">RELATED LINKS</span></span>

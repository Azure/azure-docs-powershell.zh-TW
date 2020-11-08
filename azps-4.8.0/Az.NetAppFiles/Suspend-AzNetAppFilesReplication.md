---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127557"
---
# <span data-ttu-id="ae185-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="ae185-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="ae185-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae185-102">SYNOPSIS</span></span>
<span data-ttu-id="ae185-103">暫停/中斷目的地磁片上的複製連接</span><span class="sxs-lookup"><span data-stu-id="ae185-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="ae185-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae185-104">SYNTAX</span></span>

### <span data-ttu-id="ae185-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ae185-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae185-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae185-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae185-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae185-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae185-108">說明</span><span class="sxs-lookup"><span data-stu-id="ae185-108">DESCRIPTION</span></span>
<span data-ttu-id="ae185-109">暫停/中斷目的地磁片上的複製連接</span><span class="sxs-lookup"><span data-stu-id="ae185-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="ae185-110">示例</span><span class="sxs-lookup"><span data-stu-id="ae185-110">EXAMPLES</span></span>

### <span data-ttu-id="ae185-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ae185-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="ae185-112">這個命令會暫停 volume "MyDestinationAnfVolume" 上的 ANF 複製連線。</span><span class="sxs-lookup"><span data-stu-id="ae185-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="ae185-113">參數</span><span class="sxs-lookup"><span data-stu-id="ae185-113">PARAMETERS</span></span>

### <span data-ttu-id="ae185-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae185-114">-AccountName</span></span>
<span data-ttu-id="ae185-115">複製卷 ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="ae185-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="ae185-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae185-116">-DefaultProfile</span></span>
<span data-ttu-id="ae185-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae185-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae185-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae185-118">-InputObject</span></span>
<span data-ttu-id="ae185-119">要中斷複製的 ANF 目標量物件</span><span class="sxs-lookup"><span data-stu-id="ae185-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="ae185-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae185-120">-Name</span></span>
<span data-ttu-id="ae185-121">ANF 複製目標量的名稱</span><span class="sxs-lookup"><span data-stu-id="ae185-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ae185-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae185-122">-PassThru</span></span>
<span data-ttu-id="ae185-123">傳回是否已執行指定的磁片卷複製中斷</span><span class="sxs-lookup"><span data-stu-id="ae185-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="ae185-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ae185-124">-PoolName</span></span>
<span data-ttu-id="ae185-125">複製卷 ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="ae185-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="ae185-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae185-126">-ResourceGroupName</span></span>
<span data-ttu-id="ae185-127">ANF 複製目標量的資源群組</span><span class="sxs-lookup"><span data-stu-id="ae185-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ae185-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae185-128">-ResourceId</span></span>
<span data-ttu-id="ae185-129">ANF 複製目標量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ae185-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="ae185-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ae185-130">-Confirm</span></span>
<span data-ttu-id="ae185-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae185-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae185-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae185-132">-WhatIf</span></span>
<span data-ttu-id="ae185-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae185-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae185-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae185-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae185-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae185-135">CommonParameters</span></span>
<span data-ttu-id="ae185-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae185-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae185-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ae185-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae185-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ae185-138">INPUTS</span></span>

### <span data-ttu-id="ae185-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ae185-139">System.String</span></span>

### <span data-ttu-id="ae185-140">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="ae185-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ae185-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ae185-141">OUTPUTS</span></span>

### <span data-ttu-id="ae185-142">System.object</span><span class="sxs-lookup"><span data-stu-id="ae185-142">System.Boolean</span></span>

## <span data-ttu-id="ae185-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ae185-143">NOTES</span></span>

## <span data-ttu-id="ae185-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae185-144">RELATED LINKS</span></span>

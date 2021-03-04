---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: ac562f95ad6d5cbc97e31cd3832b90d2aa2362e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906097"
---
# <span data-ttu-id="c6a16-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="c6a16-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="c6a16-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6a16-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a16-103">核准/授權來源卷上的複製連接</span><span class="sxs-lookup"><span data-stu-id="c6a16-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="c6a16-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6a16-104">SYNTAX</span></span>

### <span data-ttu-id="c6a16-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c6a16-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6a16-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6a16-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6a16-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6a16-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6a16-108">描述</span><span class="sxs-lookup"><span data-stu-id="c6a16-108">DESCRIPTION</span></span>
<span data-ttu-id="c6a16-109">核准來源卷上的複製連接</span><span class="sxs-lookup"><span data-stu-id="c6a16-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="c6a16-110">例子</span><span class="sxs-lookup"><span data-stu-id="c6a16-110">EXAMPLES</span></span>

### <span data-ttu-id="c6a16-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c6a16-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="c6a16-112">此命令會核准 MyAnfVolume 上的複製。</span><span class="sxs-lookup"><span data-stu-id="c6a16-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="c6a16-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6a16-113">PARAMETERS</span></span>

### <span data-ttu-id="c6a16-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6a16-114">-AccountName</span></span>
<span data-ttu-id="c6a16-115">複製來源大量之 ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="c6a16-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="c6a16-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="c6a16-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="c6a16-117">目的地資料保護音量的檔案系統識別碼</span><span class="sxs-lookup"><span data-stu-id="c6a16-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="c6a16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a16-118">-DefaultProfile</span></span>
<span data-ttu-id="c6a16-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6a16-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6a16-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6a16-120">-InputObject</span></span>
<span data-ttu-id="c6a16-121">授權複製目的地的 ANF 來源大量物件</span><span class="sxs-lookup"><span data-stu-id="c6a16-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="c6a16-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6a16-122">-Name</span></span>
<span data-ttu-id="c6a16-123">ANF 複製來源音量的名稱</span><span class="sxs-lookup"><span data-stu-id="c6a16-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="c6a16-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6a16-124">-PassThru</span></span>
<span data-ttu-id="c6a16-125">返回是否執行指定卷的複本授權</span><span class="sxs-lookup"><span data-stu-id="c6a16-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="c6a16-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c6a16-126">-PoolName</span></span>
<span data-ttu-id="c6a16-127">複製來源大量之 ANF 資料庫的名稱</span><span class="sxs-lookup"><span data-stu-id="c6a16-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="c6a16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a16-128">-ResourceGroupName</span></span>
<span data-ttu-id="c6a16-129">ANF 複製來源大量資源群組</span><span class="sxs-lookup"><span data-stu-id="c6a16-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="c6a16-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6a16-130">-ResourceId</span></span>
<span data-ttu-id="c6a16-131">ANF 複製來源大量資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c6a16-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="c6a16-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c6a16-132">-Confirm</span></span>
<span data-ttu-id="c6a16-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6a16-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6a16-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6a16-134">-WhatIf</span></span>
<span data-ttu-id="c6a16-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6a16-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6a16-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6a16-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6a16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a16-137">CommonParameters</span></span>
<span data-ttu-id="c6a16-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6a16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a16-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6a16-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a16-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c6a16-140">INPUTS</span></span>

### <span data-ttu-id="c6a16-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c6a16-141">System.String</span></span>

### <span data-ttu-id="c6a16-142">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c6a16-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c6a16-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c6a16-143">OUTPUTS</span></span>

### <span data-ttu-id="c6a16-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6a16-144">System.Boolean</span></span>

## <span data-ttu-id="c6a16-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c6a16-145">NOTES</span></span>

## <span data-ttu-id="c6a16-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6a16-146">RELATED LINKS</span></span>

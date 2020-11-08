---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129411"
---
# <span data-ttu-id="0dfde-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="0dfde-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="0dfde-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0dfde-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfde-103">在來源磁片上核准/授權複製連接</span><span class="sxs-lookup"><span data-stu-id="0dfde-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="0dfde-104">句法</span><span class="sxs-lookup"><span data-stu-id="0dfde-104">SYNTAX</span></span>

### <span data-ttu-id="0dfde-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0dfde-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dfde-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dfde-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dfde-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dfde-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dfde-108">說明</span><span class="sxs-lookup"><span data-stu-id="0dfde-108">DESCRIPTION</span></span>
<span data-ttu-id="0dfde-109">核准來源磁片上的複製連接</span><span class="sxs-lookup"><span data-stu-id="0dfde-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="0dfde-110">示例</span><span class="sxs-lookup"><span data-stu-id="0dfde-110">EXAMPLES</span></span>

### <span data-ttu-id="0dfde-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0dfde-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="0dfde-112">這個命令會在 MyAnfVolume 上核准複製。</span><span class="sxs-lookup"><span data-stu-id="0dfde-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="0dfde-113">參數</span><span class="sxs-lookup"><span data-stu-id="0dfde-113">PARAMETERS</span></span>

### <span data-ttu-id="0dfde-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0dfde-114">-AccountName</span></span>
<span data-ttu-id="0dfde-115">複製來源卷的 ANF 帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="0dfde-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="0dfde-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="0dfde-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="0dfde-117">目的地資料保護量的檔案系統識別碼</span><span class="sxs-lookup"><span data-stu-id="0dfde-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="0dfde-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dfde-118">-DefaultProfile</span></span>
<span data-ttu-id="0dfde-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dfde-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dfde-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dfde-120">-InputObject</span></span>
<span data-ttu-id="0dfde-121">要授權複製目的地的 ANF 來源卷物件</span><span class="sxs-lookup"><span data-stu-id="0dfde-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="0dfde-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="0dfde-122">-Name</span></span>
<span data-ttu-id="0dfde-123">ANF 複製來源量的名稱</span><span class="sxs-lookup"><span data-stu-id="0dfde-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="0dfde-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dfde-124">-PassThru</span></span>
<span data-ttu-id="0dfde-125">傳回是否執行了指定磁片的複製授權</span><span class="sxs-lookup"><span data-stu-id="0dfde-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="0dfde-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="0dfde-126">-PoolName</span></span>
<span data-ttu-id="0dfde-127">複製來源卷的 ANF 池名稱</span><span class="sxs-lookup"><span data-stu-id="0dfde-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="0dfde-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dfde-128">-ResourceGroupName</span></span>
<span data-ttu-id="0dfde-129">ANF 複製來源量的資源群組</span><span class="sxs-lookup"><span data-stu-id="0dfde-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="0dfde-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0dfde-130">-ResourceId</span></span>
<span data-ttu-id="0dfde-131">ANF 複製來源量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0dfde-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="0dfde-132">-確認</span><span class="sxs-lookup"><span data-stu-id="0dfde-132">-Confirm</span></span>
<span data-ttu-id="0dfde-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0dfde-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dfde-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dfde-134">-WhatIf</span></span>
<span data-ttu-id="0dfde-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0dfde-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dfde-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0dfde-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dfde-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfde-137">CommonParameters</span></span>
<span data-ttu-id="0dfde-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0dfde-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfde-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0dfde-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfde-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0dfde-140">INPUTS</span></span>

### <span data-ttu-id="0dfde-141">System.object</span><span class="sxs-lookup"><span data-stu-id="0dfde-141">System.String</span></span>

### <span data-ttu-id="0dfde-142">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="0dfde-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="0dfde-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0dfde-143">OUTPUTS</span></span>

### <span data-ttu-id="0dfde-144">System.object</span><span class="sxs-lookup"><span data-stu-id="0dfde-144">System.Boolean</span></span>

## <span data-ttu-id="0dfde-145">筆記</span><span class="sxs-lookup"><span data-stu-id="0dfde-145">NOTES</span></span>

## <span data-ttu-id="0dfde-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dfde-146">RELATED LINKS</span></span>

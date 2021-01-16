---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281806"
---
# <span data-ttu-id="4ee91-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="4ee91-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="4ee91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ee91-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee91-103">在來源磁片上核准/授權複製連接</span><span class="sxs-lookup"><span data-stu-id="4ee91-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="4ee91-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ee91-104">SYNTAX</span></span>

### <span data-ttu-id="4ee91-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4ee91-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee91-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee91-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee91-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee91-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee91-108">說明</span><span class="sxs-lookup"><span data-stu-id="4ee91-108">DESCRIPTION</span></span>
<span data-ttu-id="4ee91-109">核准來源磁片上的複製連接</span><span class="sxs-lookup"><span data-stu-id="4ee91-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="4ee91-110">示例</span><span class="sxs-lookup"><span data-stu-id="4ee91-110">EXAMPLES</span></span>

### <span data-ttu-id="4ee91-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4ee91-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="4ee91-112">這個命令會在 MyAnfVolume 上核准複製。</span><span class="sxs-lookup"><span data-stu-id="4ee91-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="4ee91-113">參數</span><span class="sxs-lookup"><span data-stu-id="4ee91-113">PARAMETERS</span></span>

### <span data-ttu-id="4ee91-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4ee91-114">-AccountName</span></span>
<span data-ttu-id="4ee91-115">複製來源卷的 ANF 帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="4ee91-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="4ee91-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="4ee91-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="4ee91-117">目的地資料保護量的檔案系統識別碼</span><span class="sxs-lookup"><span data-stu-id="4ee91-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="4ee91-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee91-118">-DefaultProfile</span></span>
<span data-ttu-id="4ee91-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ee91-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee91-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ee91-120">-InputObject</span></span>
<span data-ttu-id="4ee91-121">要授權複製目的地的 ANF 來源卷物件</span><span class="sxs-lookup"><span data-stu-id="4ee91-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="4ee91-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ee91-122">-Name</span></span>
<span data-ttu-id="4ee91-123">ANF 複製來源量的名稱</span><span class="sxs-lookup"><span data-stu-id="4ee91-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="4ee91-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ee91-124">-PassThru</span></span>
<span data-ttu-id="4ee91-125">傳回是否執行了指定磁片的複製授權</span><span class="sxs-lookup"><span data-stu-id="4ee91-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="4ee91-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="4ee91-126">-PoolName</span></span>
<span data-ttu-id="4ee91-127">複製來源卷的 ANF 池名稱</span><span class="sxs-lookup"><span data-stu-id="4ee91-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="4ee91-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee91-128">-ResourceGroupName</span></span>
<span data-ttu-id="4ee91-129">ANF 複製來源量的資源群組</span><span class="sxs-lookup"><span data-stu-id="4ee91-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="4ee91-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ee91-130">-ResourceId</span></span>
<span data-ttu-id="4ee91-131">ANF 複製來源量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4ee91-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="4ee91-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4ee91-132">-Confirm</span></span>
<span data-ttu-id="4ee91-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ee91-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee91-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee91-134">-WhatIf</span></span>
<span data-ttu-id="4ee91-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ee91-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee91-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ee91-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee91-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee91-137">CommonParameters</span></span>
<span data-ttu-id="4ee91-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ee91-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee91-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ee91-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee91-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4ee91-140">INPUTS</span></span>

### <span data-ttu-id="4ee91-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4ee91-141">System.String</span></span>

### <span data-ttu-id="4ee91-142">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="4ee91-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="4ee91-143">輸出</span><span class="sxs-lookup"><span data-stu-id="4ee91-143">OUTPUTS</span></span>

### <span data-ttu-id="4ee91-144">System.object</span><span class="sxs-lookup"><span data-stu-id="4ee91-144">System.Boolean</span></span>

## <span data-ttu-id="4ee91-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4ee91-145">NOTES</span></span>

## <span data-ttu-id="4ee91-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ee91-146">RELATED LINKS</span></span>

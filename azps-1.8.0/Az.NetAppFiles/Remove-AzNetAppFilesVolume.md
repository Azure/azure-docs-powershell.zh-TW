---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f6b21f3496f8ac05147db24de1df2ee03693fb7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622208"
---
# <span data-ttu-id="85bed-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="85bed-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="85bed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85bed-102">SYNOPSIS</span></span>
<span data-ttu-id="85bed-103">刪除 (ANF) 音量的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="85bed-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="85bed-104">句法</span><span class="sxs-lookup"><span data-stu-id="85bed-104">SYNTAX</span></span>

### <span data-ttu-id="85bed-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="85bed-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85bed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85bed-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85bed-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85bed-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85bed-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85bed-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85bed-109">說明</span><span class="sxs-lookup"><span data-stu-id="85bed-109">DESCRIPTION</span></span>
<span data-ttu-id="85bed-110">**AzNetAppFilesVolume** Cmdlet 會刪除 ANF 的音量。</span><span class="sxs-lookup"><span data-stu-id="85bed-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="85bed-111">示例</span><span class="sxs-lookup"><span data-stu-id="85bed-111">EXAMPLES</span></span>

### <span data-ttu-id="85bed-112">範例1</span><span class="sxs-lookup"><span data-stu-id="85bed-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="85bed-113">這個命令會刪除 ANF 音量 "MyAnfVolume"。</span><span class="sxs-lookup"><span data-stu-id="85bed-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="85bed-114">參數</span><span class="sxs-lookup"><span data-stu-id="85bed-114">PARAMETERS</span></span>

### <span data-ttu-id="85bed-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="85bed-115">-AccountName</span></span>
<span data-ttu-id="85bed-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="85bed-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85bed-117">-DefaultProfile</span></span>
<span data-ttu-id="85bed-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85bed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85bed-119">-InputObject</span></span>
<span data-ttu-id="85bed-120">要移除的卷物件</span><span class="sxs-lookup"><span data-stu-id="85bed-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="85bed-121">-Name</span></span>
<span data-ttu-id="85bed-122">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="85bed-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85bed-123">-PassThru</span></span>
<span data-ttu-id="85bed-124">傳回指定的磁片卷是否已順利移除</span><span class="sxs-lookup"><span data-stu-id="85bed-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="85bed-125">-PoolName</span></span>
<span data-ttu-id="85bed-126">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="85bed-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="85bed-127">-PoolObject</span></span>
<span data-ttu-id="85bed-128">包含要移除之卷的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="85bed-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85bed-129">-ResourceGroupName</span></span>
<span data-ttu-id="85bed-130">ANF 體積中的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="85bed-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85bed-131">-ResourceId</span></span>
<span data-ttu-id="85bed-132">ANF 體積的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="85bed-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-133">-確認</span><span class="sxs-lookup"><span data-stu-id="85bed-133">-Confirm</span></span>
<span data-ttu-id="85bed-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85bed-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85bed-135">-WhatIf</span></span>
<span data-ttu-id="85bed-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85bed-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85bed-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85bed-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bed-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85bed-138">CommonParameters</span></span>
<span data-ttu-id="85bed-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85bed-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="85bed-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85bed-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85bed-141">輸入</span><span class="sxs-lookup"><span data-stu-id="85bed-141">INPUTS</span></span>

### <span data-ttu-id="85bed-142">System.object</span><span class="sxs-lookup"><span data-stu-id="85bed-142">System.String</span></span>

### <span data-ttu-id="85bed-143">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="85bed-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="85bed-144">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="85bed-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="85bed-145">輸出</span><span class="sxs-lookup"><span data-stu-id="85bed-145">OUTPUTS</span></span>

### <span data-ttu-id="85bed-146">System.object</span><span class="sxs-lookup"><span data-stu-id="85bed-146">System.Boolean</span></span>

## <span data-ttu-id="85bed-147">筆記</span><span class="sxs-lookup"><span data-stu-id="85bed-147">NOTES</span></span>

## <span data-ttu-id="85bed-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="85bed-148">RELATED LINKS</span></span>

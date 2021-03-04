---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: 06bdb5246cc0830ef78baa81d418f1fe6e51e935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905994"
---
# <span data-ttu-id="b64c3-101">Remove-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b64c3-101">Remove-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b64c3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b64c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b64c3-103">刪除快照 (快照) Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="b64c3-103">Deletes an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="b64c3-104">語法</span><span class="sxs-lookup"><span data-stu-id="b64c3-104">SYNTAX</span></span>

### <span data-ttu-id="b64c3-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b64c3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b64c3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b64c3-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b64c3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b64c3-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b64c3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b64c3-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshotPolicy -InputObject <PSNetAppFilesSnapshotPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b64c3-109">描述</span><span class="sxs-lookup"><span data-stu-id="b64c3-109">DESCRIPTION</span></span>
<span data-ttu-id="b64c3-110">**Remove-AzNetAppFilesSnapshotPolicy** Cmdlet 會刪除 ANF 快照策略。</span><span class="sxs-lookup"><span data-stu-id="b64c3-110">The **Remove-AzNetAppFilesSnapshotPolicy** cmdlet deletes an ANF snapshot policy.</span></span>

## <span data-ttu-id="b64c3-111">例子</span><span class="sxs-lookup"><span data-stu-id="b64c3-111">EXAMPLES</span></span>

### <span data-ttu-id="b64c3-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="b64c3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="b64c3-113">此命令會刪除帳戶 "MyAccount" 名稱為 "MyBackupPolicy" 的新 ANF 備份策略。</span><span class="sxs-lookup"><span data-stu-id="b64c3-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="b64c3-114">參數</span><span class="sxs-lookup"><span data-stu-id="b64c3-114">PARAMETERS</span></span>

### <span data-ttu-id="b64c3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b64c3-115">-AccountName</span></span>
<span data-ttu-id="b64c3-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="b64c3-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="b64c3-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b64c3-117">-AccountObject</span></span>
<span data-ttu-id="b64c3-118">新快照策略物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="b64c3-118">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b64c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64c3-119">-DefaultProfile</span></span>
<span data-ttu-id="b64c3-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b64c3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b64c3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b64c3-121">-InputObject</span></span>
<span data-ttu-id="b64c3-122">要移除的 SnapshotPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="b64c3-122">The SnapshotPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b64c3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b64c3-123">-Name</span></span>
<span data-ttu-id="b64c3-124">ANF 快照策略的名稱</span><span class="sxs-lookup"><span data-stu-id="b64c3-124">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b64c3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b64c3-125">-PassThru</span></span>
<span data-ttu-id="b64c3-126">返回指定帳戶是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="b64c3-126">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="b64c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b64c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="b64c3-128">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="b64c3-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b64c3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b64c3-129">-ResourceId</span></span>
<span data-ttu-id="b64c3-130">ANF 快照策略的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b64c3-130">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="b64c3-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b64c3-131">-Confirm</span></span>
<span data-ttu-id="b64c3-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b64c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b64c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b64c3-133">-WhatIf</span></span>
<span data-ttu-id="b64c3-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b64c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b64c3-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b64c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b64c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64c3-136">CommonParameters</span></span>
<span data-ttu-id="b64c3-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b64c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64c3-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b64c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64c3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b64c3-139">INPUTS</span></span>

### <span data-ttu-id="b64c3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b64c3-140">System.String</span></span>

### <span data-ttu-id="b64c3-141">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b64c3-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="b64c3-142">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilessnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b64c3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b64c3-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b64c3-143">OUTPUTS</span></span>

### <span data-ttu-id="b64c3-144">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilessnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="b64c3-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="b64c3-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b64c3-145">NOTES</span></span>

## <span data-ttu-id="b64c3-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b64c3-146">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: de9d0cf5d989cfa4d910f8e5ee9d959393c42632
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906005"
---
# <span data-ttu-id="c704f-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c704f-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c704f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c704f-102">SYNOPSIS</span></span>
<span data-ttu-id="c704f-103">刪除 ANF 中的 Azure NetApp 檔案 (備份) 。</span><span class="sxs-lookup"><span data-stu-id="c704f-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="c704f-104">語法</span><span class="sxs-lookup"><span data-stu-id="c704f-104">SYNTAX</span></span>

### <span data-ttu-id="c704f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c704f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c704f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c704f-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c704f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c704f-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c704f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c704f-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c704f-109">描述</span><span class="sxs-lookup"><span data-stu-id="c704f-109">DESCRIPTION</span></span>
<span data-ttu-id="c704f-110">**Remove-AzNetAppFilesBackupPolicy** Cmdlet 會刪除 ANF 備份策略。</span><span class="sxs-lookup"><span data-stu-id="c704f-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="c704f-111">例子</span><span class="sxs-lookup"><span data-stu-id="c704f-111">EXAMPLES</span></span>

### <span data-ttu-id="c704f-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="c704f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="c704f-113">此命令會刪除帳戶 "MyAccount" 名稱為 "MyBackupPolicy" 的新 ANF 備份策略。</span><span class="sxs-lookup"><span data-stu-id="c704f-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="c704f-114">參數</span><span class="sxs-lookup"><span data-stu-id="c704f-114">PARAMETERS</span></span>

### <span data-ttu-id="c704f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c704f-115">-AccountName</span></span>
<span data-ttu-id="c704f-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="c704f-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c704f-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="c704f-117">-AccountObject</span></span>
<span data-ttu-id="c704f-118">包含要移除之備份策略的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="c704f-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="c704f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c704f-119">-DefaultProfile</span></span>
<span data-ttu-id="c704f-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c704f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c704f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c704f-121">-InputObject</span></span>
<span data-ttu-id="c704f-122">要移除的 BackupPolicy 物件</span><span class="sxs-lookup"><span data-stu-id="c704f-122">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c704f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c704f-123">-Name</span></span>
<span data-ttu-id="c704f-124">ANF 備份策略的名稱</span><span class="sxs-lookup"><span data-stu-id="c704f-124">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c704f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c704f-125">-PassThru</span></span>
<span data-ttu-id="c704f-126">返回指定的備份策略是否已順利移除</span><span class="sxs-lookup"><span data-stu-id="c704f-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="c704f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c704f-127">-ResourceGroupName</span></span>
<span data-ttu-id="c704f-128">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="c704f-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c704f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c704f-129">-ResourceId</span></span>
<span data-ttu-id="c704f-130">ANF 備份策略的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c704f-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="c704f-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c704f-131">-Confirm</span></span>
<span data-ttu-id="c704f-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c704f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c704f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c704f-133">-WhatIf</span></span>
<span data-ttu-id="c704f-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c704f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c704f-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c704f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c704f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c704f-136">CommonParameters</span></span>
<span data-ttu-id="c704f-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c704f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c704f-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c704f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c704f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c704f-139">INPUTS</span></span>

### <span data-ttu-id="c704f-140">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c704f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="c704f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c704f-141">System.String</span></span>

### <span data-ttu-id="c704f-142">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c704f-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c704f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c704f-143">OUTPUTS</span></span>

### <span data-ttu-id="c704f-144">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c704f-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c704f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="c704f-145">NOTES</span></span>

## <span data-ttu-id="c704f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="c704f-146">RELATED LINKS</span></span>

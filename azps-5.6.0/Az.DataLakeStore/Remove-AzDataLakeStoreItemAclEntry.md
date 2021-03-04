---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: e41b1c01976cdc631d146721a4ee63d61d52afef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904506"
---
# <span data-ttu-id="d1936-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d1936-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d1936-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1936-102">SYNOPSIS</span></span>
<span data-ttu-id="d1936-103">從 Data Lake Store 中檔案或資料夾的 ACL 移除專案。</span><span class="sxs-lookup"><span data-stu-id="d1936-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d1936-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1936-104">SYNTAX</span></span>

### <span data-ttu-id="d1936-105">RemoveByACLObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d1936-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1936-106">RemoveSificACE</span><span class="sxs-lookup"><span data-stu-id="d1936-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1936-107">描述</span><span class="sxs-lookup"><span data-stu-id="d1936-107">DESCRIPTION</span></span>
<span data-ttu-id="d1936-108">**Remove-AzDataLakeStoreItemAclEntry Cmdlet** 會從 Data Lake Store 檔案或資料夾的存取控制清單 (ACL) 移除專案 (ACE) 。</span><span class="sxs-lookup"><span data-stu-id="d1936-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d1936-109">例子</span><span class="sxs-lookup"><span data-stu-id="d1936-109">EXAMPLES</span></span>

### <span data-ttu-id="d1936-110">範例 1：移除使用者專案</span><span class="sxs-lookup"><span data-stu-id="d1936-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="d1936-111">此命令會從 ContosoADL 帳戶移除使用者 ACE for Patti Fuller。</span><span class="sxs-lookup"><span data-stu-id="d1936-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="d1936-112">範例 2：以遞迴式移除使用者專案</span><span class="sxs-lookup"><span data-stu-id="d1936-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="d1936-113">範例 3：使用 Acl 物件遞迴移除 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="d1936-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="d1936-114">此命令會從根目錄移除使用者 ACE for Patti Fuller，並遞迴從帳戶 ContosoADL 的所有子目錄和檔案。</span><span class="sxs-lookup"><span data-stu-id="d1936-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="d1936-115">參數</span><span class="sxs-lookup"><span data-stu-id="d1936-115">PARAMETERS</span></span>

### <span data-ttu-id="d1936-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d1936-116">-Account</span></span>
<span data-ttu-id="d1936-117">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1936-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="d1936-118">-AceType</span></span>
<span data-ttu-id="d1936-119">指定要移除的 ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="d1936-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="d1936-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d1936-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d1936-121">使用者</span><span class="sxs-lookup"><span data-stu-id="d1936-121">User</span></span>
- <span data-ttu-id="d1936-122">組</span><span class="sxs-lookup"><span data-stu-id="d1936-122">Group</span></span>
- <span data-ttu-id="d1936-123">面具</span><span class="sxs-lookup"><span data-stu-id="d1936-123">Mask</span></span>
- <span data-ttu-id="d1936-124">其他</span><span class="sxs-lookup"><span data-stu-id="d1936-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="d1936-125">-Acl</span></span>
<span data-ttu-id="d1936-126">指定包含要移除之專案之 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="d1936-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-127">-並行</span><span class="sxs-lookup"><span data-stu-id="d1936-127">-Concurrency</span></span>
<span data-ttu-id="d1936-128">平行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="d1936-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="d1936-129">選擇性：會選取合理的預設值</span><span class="sxs-lookup"><span data-stu-id="d1936-129">Optional: a reasonable default will be selected</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-130">-預設</span><span class="sxs-lookup"><span data-stu-id="d1936-130">-Default</span></span>
<span data-ttu-id="d1936-131">表示此作業會從指定的 ACL 移除預設 ACE。</span><span class="sxs-lookup"><span data-stu-id="d1936-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1936-132">-DefaultProfile</span></span>
<span data-ttu-id="d1936-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1936-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1936-134">-Id</span><span class="sxs-lookup"><span data-stu-id="d1936-134">-Id</span></span>
<span data-ttu-id="d1936-135">指定要移除 ACE 之 AzureActive Directory 使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1936-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1936-136">-PassThru</span></span>
<span data-ttu-id="d1936-137">表示應該會返回布林值回應，指出刪除作業的結果。</span><span class="sxs-lookup"><span data-stu-id="d1936-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-138">-路徑</span><span class="sxs-lookup"><span data-stu-id="d1936-138">-Path</span></span>
<span data-ttu-id="d1936-139">指定要從移除 ACE 之專案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="d1936-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-140">-遞迴</span><span class="sxs-lookup"><span data-stu-id="d1936-140">-Recurse</span></span>
<span data-ttu-id="d1936-141">表示要遞迴移除的 ACL 到子子目錄和檔案</span><span class="sxs-lookup"><span data-stu-id="d1936-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="d1936-142">-ShowProgress</span></span>
<span data-ttu-id="d1936-143">如果通過，則顯示進度狀態。</span><span class="sxs-lookup"><span data-stu-id="d1936-143">If passed then progress status is showed.</span></span> <span data-ttu-id="d1936-144">只有在完成遞迴 Acl 移除時，才適用。</span><span class="sxs-lookup"><span data-stu-id="d1936-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="d1936-145">-確認</span><span class="sxs-lookup"><span data-stu-id="d1936-145">-Confirm</span></span>
<span data-ttu-id="d1936-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1936-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1936-147">-WhatIf</span></span>
<span data-ttu-id="d1936-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1936-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1936-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1936-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1936-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1936-150">CommonParameters</span></span>
<span data-ttu-id="d1936-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1936-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1936-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d1936-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1936-153">輸入</span><span class="sxs-lookup"><span data-stu-id="d1936-153">INPUTS</span></span>

### <span data-ttu-id="d1936-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d1936-154">System.String</span></span>

### <span data-ttu-id="d1936-155">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d1936-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d1936-156">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="d1936-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="d1936-157">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="d1936-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="d1936-158">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d1936-158">System.Guid</span></span>

### <span data-ttu-id="d1936-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1936-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d1936-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d1936-160">System.Int32</span></span>

## <span data-ttu-id="d1936-161">輸出</span><span class="sxs-lookup"><span data-stu-id="d1936-161">OUTPUTS</span></span>

### <span data-ttu-id="d1936-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d1936-162">System.Boolean</span></span>

## <span data-ttu-id="d1936-163">筆記</span><span class="sxs-lookup"><span data-stu-id="d1936-163">NOTES</span></span>

## <span data-ttu-id="d1936-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1936-164">RELATED LINKS</span></span>

[<span data-ttu-id="d1936-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d1936-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)



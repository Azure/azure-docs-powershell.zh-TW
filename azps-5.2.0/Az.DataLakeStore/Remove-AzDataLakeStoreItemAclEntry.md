---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: b6d07dbf390a0835bd28a045e4eea8bcf29e15f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275263"
---
# <span data-ttu-id="a62db-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a62db-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="a62db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a62db-102">SYNOPSIS</span></span>
<span data-ttu-id="a62db-103">從 Data Lake Store 中的檔案或資料夾 ACL 中移除專案。</span><span class="sxs-lookup"><span data-stu-id="a62db-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a62db-104">句法</span><span class="sxs-lookup"><span data-stu-id="a62db-104">SYNTAX</span></span>

### <span data-ttu-id="a62db-105">RemoveByACLObject (預設) </span><span class="sxs-lookup"><span data-stu-id="a62db-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a62db-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="a62db-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a62db-107">說明</span><span class="sxs-lookup"><span data-stu-id="a62db-107">DESCRIPTION</span></span>
<span data-ttu-id="a62db-108">**AzDataLakeStoreItemAclEntry** Cmdlet 會從資料 Lake Store 中檔案或資料夾的存取控制清單 (ACL) ，移除 (ACE) 中的專案。</span><span class="sxs-lookup"><span data-stu-id="a62db-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a62db-109">示例</span><span class="sxs-lookup"><span data-stu-id="a62db-109">EXAMPLES</span></span>

### <span data-ttu-id="a62db-110">範例1：移除使用者專案</span><span class="sxs-lookup"><span data-stu-id="a62db-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="a62db-111">這個命令會從 ContosoADL 帳戶中移除 Patti 的使用者 ACE，以取得更完整的。</span><span class="sxs-lookup"><span data-stu-id="a62db-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="a62db-112">範例2：以遞迴方式移除使用者專案</span><span class="sxs-lookup"><span data-stu-id="a62db-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="a62db-113">範例3：使用 Acl 物件以遞迴方式移除 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="a62db-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="a62db-114">這個命令會從 root 中移除 Patti 的使用者 ACE，並以遞迴方式從它的所有子目錄和檔案中，將其從帳戶 ContosoADL。</span><span class="sxs-lookup"><span data-stu-id="a62db-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="a62db-115">參數</span><span class="sxs-lookup"><span data-stu-id="a62db-115">PARAMETERS</span></span>

### <span data-ttu-id="a62db-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a62db-116">-Account</span></span>
<span data-ttu-id="a62db-117">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a62db-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a62db-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="a62db-118">-AceType</span></span>
<span data-ttu-id="a62db-119">指定要移除的 ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="a62db-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="a62db-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a62db-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a62db-121">使用者名</span><span class="sxs-lookup"><span data-stu-id="a62db-121">User</span></span>
- <span data-ttu-id="a62db-122">群組</span><span class="sxs-lookup"><span data-stu-id="a62db-122">Group</span></span>
- <span data-ttu-id="a62db-123">遮罩</span><span class="sxs-lookup"><span data-stu-id="a62db-123">Mask</span></span>
- <span data-ttu-id="a62db-124">換句話說</span><span class="sxs-lookup"><span data-stu-id="a62db-124">Other</span></span>

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

### <span data-ttu-id="a62db-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="a62db-125">-Acl</span></span>
<span data-ttu-id="a62db-126">指定包含要移除之專案的 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="a62db-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="a62db-127">-併發性</span><span class="sxs-lookup"><span data-stu-id="a62db-127">-Concurrency</span></span>
<span data-ttu-id="a62db-128">並行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="a62db-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="a62db-129">[選用]：將會選取合理的預設值</span><span class="sxs-lookup"><span data-stu-id="a62db-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="a62db-130">-預設值</span><span class="sxs-lookup"><span data-stu-id="a62db-130">-Default</span></span>
<span data-ttu-id="a62db-131">指示此操作會從指定的 ACL 移除預設 ACE。</span><span class="sxs-lookup"><span data-stu-id="a62db-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="a62db-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62db-132">-DefaultProfile</span></span>
<span data-ttu-id="a62db-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a62db-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a62db-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a62db-134">-Id</span></span>
<span data-ttu-id="a62db-135">指定要移除 ACE 之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a62db-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="a62db-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a62db-136">-PassThru</span></span>
<span data-ttu-id="a62db-137">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="a62db-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="a62db-138">-Path</span><span class="sxs-lookup"><span data-stu-id="a62db-138">-Path</span></span>
<span data-ttu-id="a62db-139">指定要從中移除 ACE 的專案的 Data Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="a62db-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a62db-140">-遞迴</span><span class="sxs-lookup"><span data-stu-id="a62db-140">-Recurse</span></span>
<span data-ttu-id="a62db-141">指示要遞迴移除至子子目錄和檔案的 ACL</span><span class="sxs-lookup"><span data-stu-id="a62db-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="a62db-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="a62db-142">-ShowProgress</span></span>
<span data-ttu-id="a62db-143">如果經過，就會顯示 [進度] 狀態。</span><span class="sxs-lookup"><span data-stu-id="a62db-143">If passed then progress status is showed.</span></span> <span data-ttu-id="a62db-144">只有在已完成遞迴 Acl 移除時才適用。</span><span class="sxs-lookup"><span data-stu-id="a62db-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="a62db-145">-確認</span><span class="sxs-lookup"><span data-stu-id="a62db-145">-Confirm</span></span>
<span data-ttu-id="a62db-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a62db-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a62db-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a62db-147">-WhatIf</span></span>
<span data-ttu-id="a62db-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a62db-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a62db-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a62db-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a62db-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62db-150">CommonParameters</span></span>
<span data-ttu-id="a62db-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a62db-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62db-152">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a62db-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62db-153">輸入</span><span class="sxs-lookup"><span data-stu-id="a62db-153">INPUTS</span></span>

### <span data-ttu-id="a62db-154">System.object</span><span class="sxs-lookup"><span data-stu-id="a62db-154">System.String</span></span>

### <span data-ttu-id="a62db-155">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="a62db-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a62db-156">DataLakeStoreItemAce [] 的 DataLakeStore []</span><span class="sxs-lookup"><span data-stu-id="a62db-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="a62db-157">DataLakeStoreEnums + AceType （DataLakeStore）。</span><span class="sxs-lookup"><span data-stu-id="a62db-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="a62db-158">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="a62db-158">System.Guid</span></span>

### <span data-ttu-id="a62db-159">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a62db-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a62db-160">System.object</span><span class="sxs-lookup"><span data-stu-id="a62db-160">System.Int32</span></span>

## <span data-ttu-id="a62db-161">輸出</span><span class="sxs-lookup"><span data-stu-id="a62db-161">OUTPUTS</span></span>

### <span data-ttu-id="a62db-162">System.object</span><span class="sxs-lookup"><span data-stu-id="a62db-162">System.Boolean</span></span>

## <span data-ttu-id="a62db-163">筆記</span><span class="sxs-lookup"><span data-stu-id="a62db-163">NOTES</span></span>

## <span data-ttu-id="a62db-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="a62db-164">RELATED LINKS</span></span>

[<span data-ttu-id="a62db-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a62db-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)



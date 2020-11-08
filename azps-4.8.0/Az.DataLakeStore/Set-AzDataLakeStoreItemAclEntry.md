---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129002"
---
# <span data-ttu-id="f77d1-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f77d1-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="f77d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f77d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f77d1-103">修改 Data Lake Store 中檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="f77d1-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f77d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f77d1-104">SYNTAX</span></span>

### <span data-ttu-id="f77d1-105">SetByACLObject (預設) </span><span class="sxs-lookup"><span data-stu-id="f77d1-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f77d1-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="f77d1-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f77d1-107">說明</span><span class="sxs-lookup"><span data-stu-id="f77d1-107">DESCRIPTION</span></span>
<span data-ttu-id="f77d1-108">**AzDataLakeStoreItemAclEntry** Cmdlet 會修改資料 Lake Store 中檔案或資料夾之存取控制清單 (ACL) 中 (ACE) 的專案。</span><span class="sxs-lookup"><span data-stu-id="f77d1-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f77d1-109">示例</span><span class="sxs-lookup"><span data-stu-id="f77d1-109">EXAMPLES</span></span>

### <span data-ttu-id="f77d1-110">範例1：修改 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="f77d1-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="f77d1-111">這個命令會完整修改 Patti 的 ACE，以擁有擁有權限。</span><span class="sxs-lookup"><span data-stu-id="f77d1-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="f77d1-112">範例2：以遞迴方式修改 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="f77d1-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="f77d1-113">範例3：以遞迴方式使用 Acl 物件修改 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="f77d1-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="f77d1-114">這個命令會以遞迴方式將 ACE 修改成完整的 Patti，以擁有根目錄及其所有子目錄和檔案的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="f77d1-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="f77d1-115">參數</span><span class="sxs-lookup"><span data-stu-id="f77d1-115">PARAMETERS</span></span>

### <span data-ttu-id="f77d1-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f77d1-116">-Account</span></span>
<span data-ttu-id="f77d1-117">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f77d1-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f77d1-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="f77d1-118">-AceType</span></span>
<span data-ttu-id="f77d1-119">指定要修改的 ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="f77d1-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="f77d1-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f77d1-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f77d1-121">使用者名</span><span class="sxs-lookup"><span data-stu-id="f77d1-121">User</span></span> 
- <span data-ttu-id="f77d1-122">群組</span><span class="sxs-lookup"><span data-stu-id="f77d1-122">Group</span></span> 
- <span data-ttu-id="f77d1-123">遮罩</span><span class="sxs-lookup"><span data-stu-id="f77d1-123">Mask</span></span> 
- <span data-ttu-id="f77d1-124">換句話說</span><span class="sxs-lookup"><span data-stu-id="f77d1-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f77d1-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="f77d1-125">-Acl</span></span>
<span data-ttu-id="f77d1-126">指定包含要修改之專案的 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="f77d1-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f77d1-127">-併發性</span><span class="sxs-lookup"><span data-stu-id="f77d1-127">-Concurrency</span></span>
<span data-ttu-id="f77d1-128">並行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="f77d1-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="f77d1-129">[選用]：將會選取合理的預設值</span><span class="sxs-lookup"><span data-stu-id="f77d1-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="f77d1-130">-預設值</span><span class="sxs-lookup"><span data-stu-id="f77d1-130">-Default</span></span>
<span data-ttu-id="f77d1-131">表示此操作會修改指定 ACL 的預設 ACE。</span><span class="sxs-lookup"><span data-stu-id="f77d1-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f77d1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77d1-132">-DefaultProfile</span></span>
<span data-ttu-id="f77d1-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f77d1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f77d1-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f77d1-134">-Id</span></span>
<span data-ttu-id="f77d1-135">指定要修改 ACE 之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="f77d1-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f77d1-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f77d1-136">-PassThru</span></span>
<span data-ttu-id="f77d1-137">指出應該傳回產生的 ACL。</span><span class="sxs-lookup"><span data-stu-id="f77d1-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="f77d1-138">-Path</span><span class="sxs-lookup"><span data-stu-id="f77d1-138">-Path</span></span>
<span data-ttu-id="f77d1-139">指定要修改其 ACE 的專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="f77d1-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f77d1-140">-許可權</span><span class="sxs-lookup"><span data-stu-id="f77d1-140">-Permissions</span></span>
<span data-ttu-id="f77d1-141">指定 ACE 的許可權。</span><span class="sxs-lookup"><span data-stu-id="f77d1-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="f77d1-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f77d1-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f77d1-143">所有</span><span class="sxs-lookup"><span data-stu-id="f77d1-143">None</span></span>
- <span data-ttu-id="f77d1-144">抓住</span><span class="sxs-lookup"><span data-stu-id="f77d1-144">Execute</span></span>
- <span data-ttu-id="f77d1-145">撰寫</span><span class="sxs-lookup"><span data-stu-id="f77d1-145">Write</span></span>
- <span data-ttu-id="f77d1-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="f77d1-146">WriteExecute</span></span>
- <span data-ttu-id="f77d1-147">查看</span><span class="sxs-lookup"><span data-stu-id="f77d1-147">Read</span></span>
- <span data-ttu-id="f77d1-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="f77d1-148">ReadExecute</span></span>
- <span data-ttu-id="f77d1-149">讀</span><span class="sxs-lookup"><span data-stu-id="f77d1-149">ReadWrite</span></span>
- <span data-ttu-id="f77d1-150">同時</span><span class="sxs-lookup"><span data-stu-id="f77d1-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f77d1-151">-遞迴</span><span class="sxs-lookup"><span data-stu-id="f77d1-151">-Recurse</span></span>
<span data-ttu-id="f77d1-152">指示要遞迴修改為子目錄及檔案的 ACL</span><span class="sxs-lookup"><span data-stu-id="f77d1-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="f77d1-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="f77d1-153">-ShowProgress</span></span>
<span data-ttu-id="f77d1-154">如果經過，就會顯示 [進度] 狀態。</span><span class="sxs-lookup"><span data-stu-id="f77d1-154">If passed then progress status is showed.</span></span> <span data-ttu-id="f77d1-155">只有在已完成遞迴 Acl 修改時才適用。</span><span class="sxs-lookup"><span data-stu-id="f77d1-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="f77d1-156">-確認</span><span class="sxs-lookup"><span data-stu-id="f77d1-156">-Confirm</span></span>
<span data-ttu-id="f77d1-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f77d1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f77d1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f77d1-158">-WhatIf</span></span>
<span data-ttu-id="f77d1-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f77d1-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f77d1-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f77d1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f77d1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77d1-161">CommonParameters</span></span>
<span data-ttu-id="f77d1-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f77d1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77d1-163">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f77d1-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77d1-164">輸入</span><span class="sxs-lookup"><span data-stu-id="f77d1-164">INPUTS</span></span>

### <span data-ttu-id="f77d1-165">System.object</span><span class="sxs-lookup"><span data-stu-id="f77d1-165">System.String</span></span>

### <span data-ttu-id="f77d1-166">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f77d1-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f77d1-167">DataLakeStoreItemAce [] 的 DataLakeStore []</span><span class="sxs-lookup"><span data-stu-id="f77d1-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="f77d1-168">DataLakeStoreEnums + AceType （DataLakeStore）。</span><span class="sxs-lookup"><span data-stu-id="f77d1-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="f77d1-169">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="f77d1-169">System.Guid</span></span>

### <span data-ttu-id="f77d1-170">DataLakeStoreEnums + 許可權（DataLakeStore）。</span><span class="sxs-lookup"><span data-stu-id="f77d1-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="f77d1-171">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f77d1-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f77d1-172">System.object</span><span class="sxs-lookup"><span data-stu-id="f77d1-172">System.Int32</span></span>

## <span data-ttu-id="f77d1-173">輸出</span><span class="sxs-lookup"><span data-stu-id="f77d1-173">OUTPUTS</span></span>

### <span data-ttu-id="f77d1-174">DataLakeStoreItemAce 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f77d1-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="f77d1-175">筆記</span><span class="sxs-lookup"><span data-stu-id="f77d1-175">NOTES</span></span>

## <span data-ttu-id="f77d1-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="f77d1-176">RELATED LINKS</span></span>

[<span data-ttu-id="f77d1-177">移除-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f77d1-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


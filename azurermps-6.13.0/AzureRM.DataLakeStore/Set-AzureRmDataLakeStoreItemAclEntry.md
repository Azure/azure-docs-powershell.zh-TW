---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: acf0b53ba6ad03de117e9171ec64d30ee627a927
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448459"
---
# <span data-ttu-id="6df9a-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6df9a-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="6df9a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6df9a-102">SYNOPSIS</span></span>
<span data-ttu-id="6df9a-103">修改 Data Lake Store 中檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="6df9a-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6df9a-104">句法</span><span class="sxs-lookup"><span data-stu-id="6df9a-104">SYNTAX</span></span>

### <span data-ttu-id="6df9a-105">SetByACLObject (預設) </span><span class="sxs-lookup"><span data-stu-id="6df9a-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df9a-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="6df9a-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse]
 [-Concurrency <Int32>] [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6df9a-107">說明</span><span class="sxs-lookup"><span data-stu-id="6df9a-107">DESCRIPTION</span></span>
<span data-ttu-id="6df9a-108">**AzureRmDataLakeStoreItemAclEntry** Cmdlet 會修改資料 Lake Store 中檔案或資料夾之存取控制清單 (ACL) 中 (ACE) 的專案。</span><span class="sxs-lookup"><span data-stu-id="6df9a-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6df9a-109">示例</span><span class="sxs-lookup"><span data-stu-id="6df9a-109">EXAMPLES</span></span>

### <span data-ttu-id="6df9a-110">範例1：修改 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="6df9a-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="6df9a-111">這個命令會完整修改 Patti 的 ACE，以擁有擁有權限。</span><span class="sxs-lookup"><span data-stu-id="6df9a-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="6df9a-112">範例2：以遞迴方式修改 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="6df9a-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="6df9a-113">範例3：以遞迴方式使用 Acl 物件修改 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="6df9a-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="6df9a-114">這個命令會以遞迴方式將 ACE 修改成完整的 Patti，以擁有根目錄及其所有子目錄和檔案的擁有權限。</span><span class="sxs-lookup"><span data-stu-id="6df9a-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="6df9a-115">參數</span><span class="sxs-lookup"><span data-stu-id="6df9a-115">PARAMETERS</span></span>

### <span data-ttu-id="6df9a-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="6df9a-116">-Account</span></span>
<span data-ttu-id="6df9a-117">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6df9a-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6df9a-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="6df9a-118">-AceType</span></span>
<span data-ttu-id="6df9a-119">指定要修改的 ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="6df9a-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="6df9a-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6df9a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6df9a-121">使用者名</span><span class="sxs-lookup"><span data-stu-id="6df9a-121">User</span></span> 
- <span data-ttu-id="6df9a-122">群組</span><span class="sxs-lookup"><span data-stu-id="6df9a-122">Group</span></span> 
- <span data-ttu-id="6df9a-123">遮罩</span><span class="sxs-lookup"><span data-stu-id="6df9a-123">Mask</span></span> 
- <span data-ttu-id="6df9a-124">換句話說</span><span class="sxs-lookup"><span data-stu-id="6df9a-124">Other</span></span>

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

### <span data-ttu-id="6df9a-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="6df9a-125">-Acl</span></span>
<span data-ttu-id="6df9a-126">指定包含要修改之專案的 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="6df9a-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="6df9a-127">-併發性</span><span class="sxs-lookup"><span data-stu-id="6df9a-127">-Concurrency</span></span>
<span data-ttu-id="6df9a-128">並行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="6df9a-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="6df9a-129">[選用]：將會選取合理的預設值</span><span class="sxs-lookup"><span data-stu-id="6df9a-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="6df9a-130">-預設值</span><span class="sxs-lookup"><span data-stu-id="6df9a-130">-Default</span></span>
<span data-ttu-id="6df9a-131">表示此操作會修改指定 ACL 的預設 ACE。</span><span class="sxs-lookup"><span data-stu-id="6df9a-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="6df9a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df9a-132">-DefaultProfile</span></span>
<span data-ttu-id="6df9a-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6df9a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df9a-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="6df9a-134">-Id</span></span>
<span data-ttu-id="6df9a-135">指定要修改 ACE 之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="6df9a-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="6df9a-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6df9a-136">-PassThru</span></span>
<span data-ttu-id="6df9a-137">指出應該傳回產生的 ACL。</span><span class="sxs-lookup"><span data-stu-id="6df9a-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="6df9a-138">-Path</span><span class="sxs-lookup"><span data-stu-id="6df9a-138">-Path</span></span>
<span data-ttu-id="6df9a-139">指定要修改其 ACE 的專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="6df9a-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6df9a-140">-許可權</span><span class="sxs-lookup"><span data-stu-id="6df9a-140">-Permissions</span></span>
<span data-ttu-id="6df9a-141">指定 ACE 的許可權。</span><span class="sxs-lookup"><span data-stu-id="6df9a-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="6df9a-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6df9a-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6df9a-143">所有</span><span class="sxs-lookup"><span data-stu-id="6df9a-143">None</span></span>
- <span data-ttu-id="6df9a-144">抓住</span><span class="sxs-lookup"><span data-stu-id="6df9a-144">Execute</span></span>
- <span data-ttu-id="6df9a-145">撰寫</span><span class="sxs-lookup"><span data-stu-id="6df9a-145">Write</span></span>
- <span data-ttu-id="6df9a-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="6df9a-146">WriteExecute</span></span>
- <span data-ttu-id="6df9a-147">查看</span><span class="sxs-lookup"><span data-stu-id="6df9a-147">Read</span></span>
- <span data-ttu-id="6df9a-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="6df9a-148">ReadExecute</span></span>
- <span data-ttu-id="6df9a-149">讀</span><span class="sxs-lookup"><span data-stu-id="6df9a-149">ReadWrite</span></span>
- <span data-ttu-id="6df9a-150">同時</span><span class="sxs-lookup"><span data-stu-id="6df9a-150">All</span></span>

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

### <span data-ttu-id="6df9a-151">-遞迴</span><span class="sxs-lookup"><span data-stu-id="6df9a-151">-Recurse</span></span>
<span data-ttu-id="6df9a-152">指示要遞迴修改為子目錄及檔案的 ACL</span><span class="sxs-lookup"><span data-stu-id="6df9a-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="6df9a-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="6df9a-153">-ShowProgress</span></span>
<span data-ttu-id="6df9a-154">如果經過，就會顯示 [進度] 狀態。</span><span class="sxs-lookup"><span data-stu-id="6df9a-154">If passed then progress status is showed.</span></span> <span data-ttu-id="6df9a-155">只有在已完成遞迴 Acl 修改時才適用。</span><span class="sxs-lookup"><span data-stu-id="6df9a-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="6df9a-156">-確認</span><span class="sxs-lookup"><span data-stu-id="6df9a-156">-Confirm</span></span>
<span data-ttu-id="6df9a-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6df9a-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df9a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df9a-158">-WhatIf</span></span>
<span data-ttu-id="6df9a-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6df9a-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6df9a-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6df9a-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df9a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df9a-161">CommonParameters</span></span>
<span data-ttu-id="6df9a-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6df9a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df9a-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6df9a-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df9a-164">輸入</span><span class="sxs-lookup"><span data-stu-id="6df9a-164">INPUTS</span></span>

### <span data-ttu-id="6df9a-165">System.object</span><span class="sxs-lookup"><span data-stu-id="6df9a-165">System.String</span></span>

### <span data-ttu-id="6df9a-166">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="6df9a-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6df9a-167">DataLakeStoreItemAce [] 的 DataLakeStore []</span><span class="sxs-lookup"><span data-stu-id="6df9a-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="6df9a-168">DataLakeStoreEnums + AceType （DataLakeStore）。</span><span class="sxs-lookup"><span data-stu-id="6df9a-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="6df9a-169">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="6df9a-169">System.Guid</span></span>

### <span data-ttu-id="6df9a-170">DataLakeStoreEnums + 許可權（DataLakeStore）。</span><span class="sxs-lookup"><span data-stu-id="6df9a-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="6df9a-171">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="6df9a-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6df9a-172">System.object</span><span class="sxs-lookup"><span data-stu-id="6df9a-172">System.Int32</span></span>

## <span data-ttu-id="6df9a-173">輸出</span><span class="sxs-lookup"><span data-stu-id="6df9a-173">OUTPUTS</span></span>

### <span data-ttu-id="6df9a-174">DataLakeStoreItemAce 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="6df9a-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>
<span data-ttu-id="6df9a-175">如果已指定 PassThru，將會傳回產生的 ACL 專案清單。</span><span class="sxs-lookup"><span data-stu-id="6df9a-175">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="6df9a-176">筆記</span><span class="sxs-lookup"><span data-stu-id="6df9a-176">NOTES</span></span>

## <span data-ttu-id="6df9a-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="6df9a-177">RELATED LINKS</span></span>

[<span data-ttu-id="6df9a-178">移除-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6df9a-178">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)



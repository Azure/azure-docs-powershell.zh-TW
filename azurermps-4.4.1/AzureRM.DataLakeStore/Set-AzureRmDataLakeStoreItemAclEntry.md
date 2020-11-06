---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455831"
---
# <span data-ttu-id="295f4-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="295f4-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="295f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="295f4-102">SYNOPSIS</span></span>
<span data-ttu-id="295f4-103">修改 Data Lake Store 中檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="295f4-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="295f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="295f4-104">SYNTAX</span></span>

### <span data-ttu-id="295f4-105">使用 ACL 物件設定 ACL 專案 (預設) </span><span class="sxs-lookup"><span data-stu-id="295f4-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="295f4-106">設定特定的 ACE</span><span class="sxs-lookup"><span data-stu-id="295f4-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="295f4-107">說明</span><span class="sxs-lookup"><span data-stu-id="295f4-107">DESCRIPTION</span></span>
<span data-ttu-id="295f4-108">**AzureRmDataLakeStoreItemAclEntry** Cmdlet 會修改資料 Lake Store 中檔案或資料夾之存取控制清單 (ACL) 中 (ACE) 的專案。</span><span class="sxs-lookup"><span data-stu-id="295f4-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="295f4-109">示例</span><span class="sxs-lookup"><span data-stu-id="295f4-109">EXAMPLES</span></span>

### <span data-ttu-id="295f4-110">範例1：修改 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="295f4-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="295f4-111">這個命令會完整修改 Patti 的 ACE，以擁有擁有權限。</span><span class="sxs-lookup"><span data-stu-id="295f4-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="295f4-112">參數</span><span class="sxs-lookup"><span data-stu-id="295f4-112">PARAMETERS</span></span>

### <span data-ttu-id="295f4-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="295f4-113">-Account</span></span>
<span data-ttu-id="295f4-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="295f4-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="295f4-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="295f4-115">-AceType</span></span>
<span data-ttu-id="295f4-116">指定要修改的 ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="295f4-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="295f4-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="295f4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="295f4-118">使用者名</span><span class="sxs-lookup"><span data-stu-id="295f4-118">User</span></span> 
- <span data-ttu-id="295f4-119">群組</span><span class="sxs-lookup"><span data-stu-id="295f4-119">Group</span></span> 
- <span data-ttu-id="295f4-120">遮罩</span><span class="sxs-lookup"><span data-stu-id="295f4-120">Mask</span></span> 
- <span data-ttu-id="295f4-121">換句話說</span><span class="sxs-lookup"><span data-stu-id="295f4-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295f4-122">-Acl</span><span class="sxs-lookup"><span data-stu-id="295f4-122">-Acl</span></span>
<span data-ttu-id="295f4-123">指定包含要修改之專案的 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="295f4-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="295f4-124">-預設值</span><span class="sxs-lookup"><span data-stu-id="295f4-124">-Default</span></span>
<span data-ttu-id="295f4-125">表示此操作會修改指定 ACL 的預設 ACE。</span><span class="sxs-lookup"><span data-stu-id="295f4-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295f4-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="295f4-126">-Id</span></span>
<span data-ttu-id="295f4-127">指定要修改 ACE 之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="295f4-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295f4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="295f4-128">-PassThru</span></span>
<span data-ttu-id="295f4-129">指出應該傳回產生的 ACL。</span><span class="sxs-lookup"><span data-stu-id="295f4-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="295f4-130">-Path</span><span class="sxs-lookup"><span data-stu-id="295f4-130">-Path</span></span>
<span data-ttu-id="295f4-131">指定要修改其 ACE 的專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="295f4-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="295f4-132">-許可權</span><span class="sxs-lookup"><span data-stu-id="295f4-132">-Permissions</span></span>
<span data-ttu-id="295f4-133">指定 ACE 的許可權。</span><span class="sxs-lookup"><span data-stu-id="295f4-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="295f4-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="295f4-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="295f4-135">所有</span><span class="sxs-lookup"><span data-stu-id="295f4-135">None</span></span>
- <span data-ttu-id="295f4-136">抓住</span><span class="sxs-lookup"><span data-stu-id="295f4-136">Execute</span></span>
- <span data-ttu-id="295f4-137">撰寫</span><span class="sxs-lookup"><span data-stu-id="295f4-137">Write</span></span>
- <span data-ttu-id="295f4-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="295f4-138">WriteExecute</span></span>
- <span data-ttu-id="295f4-139">查看</span><span class="sxs-lookup"><span data-stu-id="295f4-139">Read</span></span>
- <span data-ttu-id="295f4-140">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="295f4-140">ReadExecute</span></span>
- <span data-ttu-id="295f4-141">讀</span><span class="sxs-lookup"><span data-stu-id="295f4-141">ReadWrite</span></span>
- <span data-ttu-id="295f4-142">同時</span><span class="sxs-lookup"><span data-stu-id="295f4-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="295f4-143">-確認</span><span class="sxs-lookup"><span data-stu-id="295f4-143">-Confirm</span></span>
<span data-ttu-id="295f4-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="295f4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="295f4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="295f4-145">-WhatIf</span></span>
<span data-ttu-id="295f4-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="295f4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="295f4-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="295f4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="295f4-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="295f4-148">-DefaultProfile</span></span>
<span data-ttu-id="295f4-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="295f4-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="295f4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295f4-150">CommonParameters</span></span>
<span data-ttu-id="295f4-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="295f4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295f4-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="295f4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295f4-153">輸入</span><span class="sxs-lookup"><span data-stu-id="295f4-153">INPUTS</span></span>

### <span data-ttu-id="295f4-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="295f4-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="295f4-155">[Acl "是從管線接受類型 ' DataLakeStoreItemAce []」的值</span><span class="sxs-lookup"><span data-stu-id="295f4-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="295f4-156">輸出</span><span class="sxs-lookup"><span data-stu-id="295f4-156">OUTPUTS</span></span>

### <span data-ttu-id="295f4-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="295f4-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="295f4-158">如果已指定 PassThru，將會傳回產生的 ACL 專案清單。</span><span class="sxs-lookup"><span data-stu-id="295f4-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="295f4-159">筆記</span><span class="sxs-lookup"><span data-stu-id="295f4-159">NOTES</span></span>

## <span data-ttu-id="295f4-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="295f4-160">RELATED LINKS</span></span>

[<span data-ttu-id="295f4-161">移除-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="295f4-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)



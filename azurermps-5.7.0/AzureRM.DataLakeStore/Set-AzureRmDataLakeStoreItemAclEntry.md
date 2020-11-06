---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: cae7ac30d54be40be023025b9f45778d7c017583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446251"
---
# <span data-ttu-id="7de8f-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7de8f-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="7de8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7de8f-102">SYNOPSIS</span></span>
<span data-ttu-id="7de8f-103">修改 Data Lake Store 中檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="7de8f-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7de8f-104">SYNTAX</span></span>

### <span data-ttu-id="7de8f-105">SetByACLObject (預設) </span><span class="sxs-lookup"><span data-stu-id="7de8f-105">SetByACLObject (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7de8f-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="7de8f-106">SetSpecificACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de8f-107">說明</span><span class="sxs-lookup"><span data-stu-id="7de8f-107">DESCRIPTION</span></span>
<span data-ttu-id="7de8f-108">**AzureRmDataLakeStoreItemAclEntry** Cmdlet 會修改資料 Lake Store 中檔案或資料夾之存取控制清單 (ACL) 中 (ACE) 的專案。</span><span class="sxs-lookup"><span data-stu-id="7de8f-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7de8f-109">示例</span><span class="sxs-lookup"><span data-stu-id="7de8f-109">EXAMPLES</span></span>

### <span data-ttu-id="7de8f-110">範例1：修改 ACE 的許可權</span><span class="sxs-lookup"><span data-stu-id="7de8f-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="7de8f-111">這個命令會完整修改 Patti 的 ACE，以擁有擁有權限。</span><span class="sxs-lookup"><span data-stu-id="7de8f-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="7de8f-112">參數</span><span class="sxs-lookup"><span data-stu-id="7de8f-112">PARAMETERS</span></span>

### <span data-ttu-id="7de8f-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="7de8f-113">-Account</span></span>
<span data-ttu-id="7de8f-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7de8f-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="7de8f-115">-AceType</span></span>
<span data-ttu-id="7de8f-116">指定要修改的 ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="7de8f-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="7de8f-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7de8f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7de8f-118">使用者名</span><span class="sxs-lookup"><span data-stu-id="7de8f-118">User</span></span> 
- <span data-ttu-id="7de8f-119">群組</span><span class="sxs-lookup"><span data-stu-id="7de8f-119">Group</span></span> 
- <span data-ttu-id="7de8f-120">遮罩</span><span class="sxs-lookup"><span data-stu-id="7de8f-120">Mask</span></span> 
- <span data-ttu-id="7de8f-121">換句話說</span><span class="sxs-lookup"><span data-stu-id="7de8f-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: SetSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-122">-Acl</span><span class="sxs-lookup"><span data-stu-id="7de8f-122">-Acl</span></span>
<span data-ttu-id="7de8f-123">指定包含要修改之專案的 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="7de8f-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-124">-預設值</span><span class="sxs-lookup"><span data-stu-id="7de8f-124">-Default</span></span>
<span data-ttu-id="7de8f-125">表示此操作會修改指定 ACL 的預設 ACE。</span><span class="sxs-lookup"><span data-stu-id="7de8f-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de8f-126">-DefaultProfile</span></span>
<span data-ttu-id="7de8f-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7de8f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="7de8f-128">-Id</span></span>
<span data-ttu-id="7de8f-129">指定要修改 ACE 之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="7de8f-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: SetSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7de8f-130">-PassThru</span></span>
<span data-ttu-id="7de8f-131">指出應該傳回產生的 ACL。</span><span class="sxs-lookup"><span data-stu-id="7de8f-131">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-132">-Path</span><span class="sxs-lookup"><span data-stu-id="7de8f-132">-Path</span></span>
<span data-ttu-id="7de8f-133">指定要修改其 ACE 的專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="7de8f-133">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-134">-許可權</span><span class="sxs-lookup"><span data-stu-id="7de8f-134">-Permissions</span></span>
<span data-ttu-id="7de8f-135">指定 ACE 的許可權。</span><span class="sxs-lookup"><span data-stu-id="7de8f-135">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="7de8f-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7de8f-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7de8f-137">所有</span><span class="sxs-lookup"><span data-stu-id="7de8f-137">None</span></span>
- <span data-ttu-id="7de8f-138">抓住</span><span class="sxs-lookup"><span data-stu-id="7de8f-138">Execute</span></span>
- <span data-ttu-id="7de8f-139">撰寫</span><span class="sxs-lookup"><span data-stu-id="7de8f-139">Write</span></span>
- <span data-ttu-id="7de8f-140">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="7de8f-140">WriteExecute</span></span>
- <span data-ttu-id="7de8f-141">查看</span><span class="sxs-lookup"><span data-stu-id="7de8f-141">Read</span></span>
- <span data-ttu-id="7de8f-142">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="7de8f-142">ReadExecute</span></span>
- <span data-ttu-id="7de8f-143">讀</span><span class="sxs-lookup"><span data-stu-id="7de8f-143">ReadWrite</span></span>
- <span data-ttu-id="7de8f-144">同時</span><span class="sxs-lookup"><span data-stu-id="7de8f-144">All</span></span>

```yaml
Type: Permission
Parameter Sets: SetSpecificACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-145">-確認</span><span class="sxs-lookup"><span data-stu-id="7de8f-145">-Confirm</span></span>
<span data-ttu-id="7de8f-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7de8f-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de8f-147">-WhatIf</span></span>
<span data-ttu-id="7de8f-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7de8f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de8f-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7de8f-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de8f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de8f-150">CommonParameters</span></span>
<span data-ttu-id="7de8f-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7de8f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de8f-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7de8f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de8f-153">輸入</span><span class="sxs-lookup"><span data-stu-id="7de8f-153">INPUTS</span></span>

### <span data-ttu-id="7de8f-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="7de8f-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="7de8f-155">[Acl "是從管線接受類型 ' DataLakeStoreItemAce []」的值</span><span class="sxs-lookup"><span data-stu-id="7de8f-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="7de8f-156">輸出</span><span class="sxs-lookup"><span data-stu-id="7de8f-156">OUTPUTS</span></span>

### <span data-ttu-id="7de8f-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="7de8f-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="7de8f-158">如果已指定 PassThru，將會傳回產生的 ACL 專案清單。</span><span class="sxs-lookup"><span data-stu-id="7de8f-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="7de8f-159">筆記</span><span class="sxs-lookup"><span data-stu-id="7de8f-159">NOTES</span></span>

## <span data-ttu-id="7de8f-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="7de8f-160">RELATED LINKS</span></span>

[<span data-ttu-id="7de8f-161">移除-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="7de8f-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)



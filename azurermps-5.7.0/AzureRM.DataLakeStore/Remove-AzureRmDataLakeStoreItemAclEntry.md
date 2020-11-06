---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 41c1324c3762d0b6e04c0c532976c62c0a16067e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444564"
---
# <span data-ttu-id="c425a-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c425a-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="c425a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c425a-102">SYNOPSIS</span></span>
<span data-ttu-id="c425a-103">從 Data Lake Store 中的檔案或資料夾 ACL 中移除專案。</span><span class="sxs-lookup"><span data-stu-id="c425a-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c425a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c425a-104">SYNTAX</span></span>

### <span data-ttu-id="c425a-105">RemoveByACLObject (預設) </span><span class="sxs-lookup"><span data-stu-id="c425a-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c425a-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="c425a-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c425a-107">說明</span><span class="sxs-lookup"><span data-stu-id="c425a-107">DESCRIPTION</span></span>
<span data-ttu-id="c425a-108">**AzureRmDataLakeStoreItemAclEntry** Cmdlet 會從資料 Lake Store 中檔案或資料夾的存取控制清單 (ACL) ，移除 (ACE) 中的專案。</span><span class="sxs-lookup"><span data-stu-id="c425a-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c425a-109">示例</span><span class="sxs-lookup"><span data-stu-id="c425a-109">EXAMPLES</span></span>

### <span data-ttu-id="c425a-110">範例1：移除使用者專案</span><span class="sxs-lookup"><span data-stu-id="c425a-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="c425a-111">這個命令會從 ContosoADL 帳戶中移除 Patti 的使用者 ACE，以取得更完整的。</span><span class="sxs-lookup"><span data-stu-id="c425a-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="c425a-112">參數</span><span class="sxs-lookup"><span data-stu-id="c425a-112">PARAMETERS</span></span>

### <span data-ttu-id="c425a-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c425a-113">-Account</span></span>
<span data-ttu-id="c425a-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c425a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c425a-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="c425a-115">-AceType</span></span>
<span data-ttu-id="c425a-116">指定要移除的 ACE 類型。</span><span class="sxs-lookup"><span data-stu-id="c425a-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="c425a-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c425a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c425a-118">使用者名</span><span class="sxs-lookup"><span data-stu-id="c425a-118">User</span></span>
- <span data-ttu-id="c425a-119">群組</span><span class="sxs-lookup"><span data-stu-id="c425a-119">Group</span></span>
- <span data-ttu-id="c425a-120">遮罩</span><span class="sxs-lookup"><span data-stu-id="c425a-120">Mask</span></span>
- <span data-ttu-id="c425a-121">換句話說</span><span class="sxs-lookup"><span data-stu-id="c425a-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: RemoveSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c425a-122">-Acl</span><span class="sxs-lookup"><span data-stu-id="c425a-122">-Acl</span></span>
<span data-ttu-id="c425a-123">指定包含要移除之專案的 ACL 物件。</span><span class="sxs-lookup"><span data-stu-id="c425a-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c425a-124">-預設值</span><span class="sxs-lookup"><span data-stu-id="c425a-124">-Default</span></span>
<span data-ttu-id="c425a-125">指示此操作會從指定的 ACL 移除預設 ACE。</span><span class="sxs-lookup"><span data-stu-id="c425a-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c425a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c425a-126">-DefaultProfile</span></span>
<span data-ttu-id="c425a-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c425a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c425a-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c425a-128">-Id</span></span>
<span data-ttu-id="c425a-129">指定要移除 ACE 之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c425a-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c425a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c425a-130">-PassThru</span></span>
<span data-ttu-id="c425a-131">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="c425a-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="c425a-132">-Path</span><span class="sxs-lookup"><span data-stu-id="c425a-132">-Path</span></span>
<span data-ttu-id="c425a-133">指定要從中移除 ACE 的專案的 Data Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="c425a-133">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c425a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c425a-134">-Confirm</span></span>
<span data-ttu-id="c425a-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c425a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c425a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c425a-136">-WhatIf</span></span>
<span data-ttu-id="c425a-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c425a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c425a-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c425a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c425a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c425a-139">CommonParameters</span></span>
<span data-ttu-id="c425a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c425a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c425a-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c425a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c425a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c425a-142">INPUTS</span></span>

### <span data-ttu-id="c425a-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="c425a-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="c425a-144">[Acl "是從管線接受類型 ' DataLakeStoreItemAce []」的值</span><span class="sxs-lookup"><span data-stu-id="c425a-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="c425a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c425a-145">OUTPUTS</span></span>

### <span data-ttu-id="c425a-146">bool</span><span class="sxs-lookup"><span data-stu-id="c425a-146">bool</span></span>
<span data-ttu-id="c425a-147">如果已指定 PassThru，則會在成功完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="c425a-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="c425a-148">筆記</span><span class="sxs-lookup"><span data-stu-id="c425a-148">NOTES</span></span>

## <span data-ttu-id="c425a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c425a-149">RELATED LINKS</span></span>

[<span data-ttu-id="c425a-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c425a-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)



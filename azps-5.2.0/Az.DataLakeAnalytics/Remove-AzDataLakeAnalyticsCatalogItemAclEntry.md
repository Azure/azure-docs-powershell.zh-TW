---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 8b227d16a55d1e5f92c6021099a01b9df5550bd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285120"
---
# <span data-ttu-id="50428-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="50428-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="50428-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50428-102">SYNOPSIS</span></span>
<span data-ttu-id="50428-103">從資料 Lake Analytics 中的目錄或目錄專案的 ACL 中刪除專案。</span><span class="sxs-lookup"><span data-stu-id="50428-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="50428-104">句法</span><span class="sxs-lookup"><span data-stu-id="50428-104">SYNTAX</span></span>

### <span data-ttu-id="50428-105">RemoveCatalogAclEntryForUser (預設) </span><span class="sxs-lookup"><span data-stu-id="50428-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50428-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="50428-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50428-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="50428-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50428-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="50428-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50428-109">說明</span><span class="sxs-lookup"><span data-stu-id="50428-109">DESCRIPTION</span></span>
<span data-ttu-id="50428-110">**AzDataLakeAnalyticsCatalogItemAclEntry** Cmdlet 會從資料 Lake Analytics 中目錄或目錄專案的存取控制清單 (ACL) ，移除 (ACE) 中的專案。</span><span class="sxs-lookup"><span data-stu-id="50428-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="50428-111">示例</span><span class="sxs-lookup"><span data-stu-id="50428-111">EXAMPLES</span></span>

### <span data-ttu-id="50428-112">範例1：移除目錄的使用者 ACL</span><span class="sxs-lookup"><span data-stu-id="50428-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="50428-113">這個命令會移除 contosoadla 帳戶的 Patti 最完整的目錄 ACL。</span><span class="sxs-lookup"><span data-stu-id="50428-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="50428-114">範例2：移除資料庫的使用者 ACL</span><span class="sxs-lookup"><span data-stu-id="50428-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="50428-115">這個命令會移除 contosoadla 帳戶的 Patti 最完整的資料庫 ACL。</span><span class="sxs-lookup"><span data-stu-id="50428-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="50428-116">參數</span><span class="sxs-lookup"><span data-stu-id="50428-116">PARAMETERS</span></span>

### <span data-ttu-id="50428-117">-帳戶</span><span class="sxs-lookup"><span data-stu-id="50428-117">-Account</span></span>
<span data-ttu-id="50428-118">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="50428-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="50428-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50428-119">-DefaultProfile</span></span>
<span data-ttu-id="50428-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50428-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50428-121">-群組</span><span class="sxs-lookup"><span data-stu-id="50428-121">-Group</span></span>
<span data-ttu-id="50428-122">移除群組的目錄 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="50428-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50428-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="50428-123">-ItemType</span></span>
<span data-ttu-id="50428-124">指定 (s) 的目錄或目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="50428-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="50428-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="50428-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="50428-126">類別</span><span class="sxs-lookup"><span data-stu-id="50428-126">Catalog</span></span>
- <span data-ttu-id="50428-127">資料</span><span class="sxs-lookup"><span data-stu-id="50428-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50428-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="50428-128">-ObjectId</span></span>
<span data-ttu-id="50428-129">要移除之使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="50428-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50428-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50428-130">-PassThru</span></span>
<span data-ttu-id="50428-131">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="50428-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="50428-132">-Path</span><span class="sxs-lookup"><span data-stu-id="50428-132">-Path</span></span>
<span data-ttu-id="50428-133">指定目錄或目錄專案的資料 Lake Analytics 路徑。</span><span class="sxs-lookup"><span data-stu-id="50428-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="50428-134">路徑的各個部分應以句點 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="50428-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50428-135">-使用者</span><span class="sxs-lookup"><span data-stu-id="50428-135">-User</span></span>
<span data-ttu-id="50428-136">移除使用者的目錄 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="50428-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50428-137">-確認</span><span class="sxs-lookup"><span data-stu-id="50428-137">-Confirm</span></span>
<span data-ttu-id="50428-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50428-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50428-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50428-139">-WhatIf</span></span>
<span data-ttu-id="50428-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50428-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50428-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50428-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50428-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50428-142">CommonParameters</span></span>
<span data-ttu-id="50428-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50428-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50428-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50428-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50428-145">輸入</span><span class="sxs-lookup"><span data-stu-id="50428-145">INPUTS</span></span>

### <span data-ttu-id="50428-146">System.object</span><span class="sxs-lookup"><span data-stu-id="50428-146">System.String</span></span>

### <span data-ttu-id="50428-147">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="50428-147">System.Guid</span></span>

### <span data-ttu-id="50428-148">CatalogPathInstance 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="50428-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="50428-149">輸出</span><span class="sxs-lookup"><span data-stu-id="50428-149">OUTPUTS</span></span>

### <span data-ttu-id="50428-150">System.object</span><span class="sxs-lookup"><span data-stu-id="50428-150">System.Boolean</span></span>

## <span data-ttu-id="50428-151">筆記</span><span class="sxs-lookup"><span data-stu-id="50428-151">NOTES</span></span>

## <span data-ttu-id="50428-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="50428-152">RELATED LINKS</span></span>

[<span data-ttu-id="50428-153">U-SQL 現已提供資料庫層級存取控制</span><span class="sxs-lookup"><span data-stu-id="50428-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="50428-154">AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="50428-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="50428-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="50428-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)

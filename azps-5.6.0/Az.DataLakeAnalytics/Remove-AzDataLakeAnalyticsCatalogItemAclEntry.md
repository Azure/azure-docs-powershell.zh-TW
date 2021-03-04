---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 968acf65d0f3e045614b5ade094bb50c90acac46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904706"
---
# <span data-ttu-id="721b1-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="721b1-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="721b1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="721b1-102">SYNOPSIS</span></span>
<span data-ttu-id="721b1-103">刪除 Data Lake Analytics 中目錄或目錄專案的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="721b1-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="721b1-104">語法</span><span class="sxs-lookup"><span data-stu-id="721b1-104">SYNTAX</span></span>

### <span data-ttu-id="721b1-105">RemoveCatalogAclEntryForUser (預設) </span><span class="sxs-lookup"><span data-stu-id="721b1-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="721b1-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="721b1-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="721b1-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="721b1-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="721b1-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="721b1-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="721b1-109">描述</span><span class="sxs-lookup"><span data-stu-id="721b1-109">DESCRIPTION</span></span>
<span data-ttu-id="721b1-110">**Remove-AzDataLakeAnalyticsCatalogItemAclEntry Cmdlet** 會從 Data Lake Analytics 中目錄或型錄專案的存取控制清單 (ACL) 移除專案 (ACE) 。</span><span class="sxs-lookup"><span data-stu-id="721b1-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="721b1-111">例子</span><span class="sxs-lookup"><span data-stu-id="721b1-111">EXAMPLES</span></span>

### <span data-ttu-id="721b1-112">範例 1：移除目錄的使用者 ACL</span><span class="sxs-lookup"><span data-stu-id="721b1-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="721b1-113">此命令會移除 Contodla 帳戶的 Catalog ACL。</span><span class="sxs-lookup"><span data-stu-id="721b1-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="721b1-114">範例 2：移除資料庫的使用者 ACL</span><span class="sxs-lookup"><span data-stu-id="721b1-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="721b1-115">此命令會移除 Contodla 帳戶的帕提費勒資料庫 ACL。</span><span class="sxs-lookup"><span data-stu-id="721b1-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="721b1-116">參數</span><span class="sxs-lookup"><span data-stu-id="721b1-116">PARAMETERS</span></span>

### <span data-ttu-id="721b1-117">-帳戶</span><span class="sxs-lookup"><span data-stu-id="721b1-117">-Account</span></span>
<span data-ttu-id="721b1-118">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="721b1-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="721b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721b1-119">-DefaultProfile</span></span>
<span data-ttu-id="721b1-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="721b1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="721b1-121">-群組</span><span class="sxs-lookup"><span data-stu-id="721b1-121">-Group</span></span>
<span data-ttu-id="721b1-122">移除群組目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="721b1-122">Remove ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="721b1-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="721b1-123">-ItemType</span></span>
<span data-ttu-id="721b1-124">指定要刪除的目錄或 () 。</span><span class="sxs-lookup"><span data-stu-id="721b1-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="721b1-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="721b1-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="721b1-126">目錄</span><span class="sxs-lookup"><span data-stu-id="721b1-126">Catalog</span></span>
- <span data-ttu-id="721b1-127">資料庫</span><span class="sxs-lookup"><span data-stu-id="721b1-127">Database</span></span>

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

### <span data-ttu-id="721b1-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="721b1-128">-ObjectId</span></span>
<span data-ttu-id="721b1-129">要移除的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="721b1-129">The identity of the user to remove.</span></span>

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

### <span data-ttu-id="721b1-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="721b1-130">-PassThru</span></span>
<span data-ttu-id="721b1-131">表示應該會返回布林值回應，指出刪除作業的結果。</span><span class="sxs-lookup"><span data-stu-id="721b1-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="721b1-132">-路徑</span><span class="sxs-lookup"><span data-stu-id="721b1-132">-Path</span></span>
<span data-ttu-id="721b1-133">指定目錄或目錄專案的 Data Lake Analytics 路徑。</span><span class="sxs-lookup"><span data-stu-id="721b1-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="721b1-134">路徑的各個部分應該以 (.) 分隔。</span><span class="sxs-lookup"><span data-stu-id="721b1-134">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="721b1-135">-使用者</span><span class="sxs-lookup"><span data-stu-id="721b1-135">-User</span></span>
<span data-ttu-id="721b1-136">移除使用者目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="721b1-136">Remove ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="721b1-137">-確認</span><span class="sxs-lookup"><span data-stu-id="721b1-137">-Confirm</span></span>
<span data-ttu-id="721b1-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="721b1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721b1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721b1-139">-WhatIf</span></span>
<span data-ttu-id="721b1-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="721b1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="721b1-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="721b1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721b1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721b1-142">CommonParameters</span></span>
<span data-ttu-id="721b1-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="721b1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721b1-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="721b1-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721b1-145">輸入</span><span class="sxs-lookup"><span data-stu-id="721b1-145">INPUTS</span></span>

### <span data-ttu-id="721b1-146">System.String</span><span class="sxs-lookup"><span data-stu-id="721b1-146">System.String</span></span>

### <span data-ttu-id="721b1-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="721b1-147">System.Guid</span></span>

### <span data-ttu-id="721b1-148">Microsoft.Azure.Commands.DataLakeAnalytics.models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="721b1-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="721b1-149">輸出</span><span class="sxs-lookup"><span data-stu-id="721b1-149">OUTPUTS</span></span>

### <span data-ttu-id="721b1-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="721b1-150">System.Boolean</span></span>

## <span data-ttu-id="721b1-151">筆記</span><span class="sxs-lookup"><span data-stu-id="721b1-151">NOTES</span></span>

## <span data-ttu-id="721b1-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="721b1-152">RELATED LINKS</span></span>

[<span data-ttu-id="721b1-153">U-SQL 現在提供資料庫層級存取控制</span><span class="sxs-lookup"><span data-stu-id="721b1-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="721b1-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="721b1-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="721b1-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="721b1-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)

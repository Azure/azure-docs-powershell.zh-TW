---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: e97876377e8ea96dc106277991bcc05fec5f3759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447381"
---
# <span data-ttu-id="ebc5e-101">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ebc5e-101">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="ebc5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebc5e-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc5e-103">從資料 Lake Analytics 中的目錄或目錄專案的 ACL 中刪除專案。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebc5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebc5e-104">SYNTAX</span></span>

### <span data-ttu-id="ebc5e-105">RemoveCatalogAclEntryForUser (預設) </span><span class="sxs-lookup"><span data-stu-id="ebc5e-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc5e-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="ebc5e-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc5e-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="ebc5e-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc5e-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="ebc5e-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebc5e-109">說明</span><span class="sxs-lookup"><span data-stu-id="ebc5e-109">DESCRIPTION</span></span>
<span data-ttu-id="ebc5e-110">**AzureRmDataLakeAnalyticsCatalogItemAclEntry** Cmdlet 會從資料 Lake Analytics 中目錄或目錄專案的存取控制清單 (ACL) ，移除 (ACE) 中的專案。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-110">The **Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="ebc5e-111">示例</span><span class="sxs-lookup"><span data-stu-id="ebc5e-111">EXAMPLES</span></span>

### <span data-ttu-id="ebc5e-112">範例1：移除目錄的使用者 ACL</span><span class="sxs-lookup"><span data-stu-id="ebc5e-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="ebc5e-113">這個命令會移除 contosoadla 帳戶的 Patti 最完整的目錄 ACL。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="ebc5e-114">範例2：移除資料庫的使用者 ACL</span><span class="sxs-lookup"><span data-stu-id="ebc5e-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="ebc5e-115">這個命令會移除 contosoadla 帳戶的 Patti 最完整的資料庫 ACL。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="ebc5e-116">參數</span><span class="sxs-lookup"><span data-stu-id="ebc5e-116">PARAMETERS</span></span>

### <span data-ttu-id="ebc5e-117">-帳戶</span><span class="sxs-lookup"><span data-stu-id="ebc5e-117">-Account</span></span>
<span data-ttu-id="ebc5e-118">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="ebc5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc5e-119">-DefaultProfile</span></span>
<span data-ttu-id="ebc5e-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc5e-121">-群組</span><span class="sxs-lookup"><span data-stu-id="ebc5e-121">-Group</span></span>
<span data-ttu-id="ebc5e-122">移除群組的目錄 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-122">Remove ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="ebc5e-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="ebc5e-123">-ItemType</span></span>
<span data-ttu-id="ebc5e-124">指定 (s) 的目錄或目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="ebc5e-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ebc5e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ebc5e-126">類別</span><span class="sxs-lookup"><span data-stu-id="ebc5e-126">Catalog</span></span>
- <span data-ttu-id="ebc5e-127">資料</span><span class="sxs-lookup"><span data-stu-id="ebc5e-127">Database</span></span>

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

### <span data-ttu-id="ebc5e-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ebc5e-128">-ObjectId</span></span>
<span data-ttu-id="ebc5e-129">要移除之使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-129">The identity of the user to remove.</span></span>

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

### <span data-ttu-id="ebc5e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebc5e-130">-PassThru</span></span>
<span data-ttu-id="ebc5e-131">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="ebc5e-132">-Path</span><span class="sxs-lookup"><span data-stu-id="ebc5e-132">-Path</span></span>
<span data-ttu-id="ebc5e-133">指定目錄或目錄專案的資料 Lake Analytics 路徑。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="ebc5e-134">路徑的各個部分應以句點 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-134">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="ebc5e-135">-使用者</span><span class="sxs-lookup"><span data-stu-id="ebc5e-135">-User</span></span>
<span data-ttu-id="ebc5e-136">移除使用者的目錄 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-136">Remove ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="ebc5e-137">-確認</span><span class="sxs-lookup"><span data-stu-id="ebc5e-137">-Confirm</span></span>
<span data-ttu-id="ebc5e-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc5e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc5e-139">-WhatIf</span></span>
<span data-ttu-id="ebc5e-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc5e-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc5e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc5e-142">CommonParameters</span></span>
<span data-ttu-id="ebc5e-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc5e-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc5e-145">輸入</span><span class="sxs-lookup"><span data-stu-id="ebc5e-145">INPUTS</span></span>

### <span data-ttu-id="ebc5e-146">System.object</span><span class="sxs-lookup"><span data-stu-id="ebc5e-146">System.String</span></span>

### <span data-ttu-id="ebc5e-147">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="ebc5e-147">System.Guid</span></span>

### <span data-ttu-id="ebc5e-148">CatalogPathInstance 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="ebc5e-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="ebc5e-149">輸出</span><span class="sxs-lookup"><span data-stu-id="ebc5e-149">OUTPUTS</span></span>

### <span data-ttu-id="ebc5e-150">System.object</span><span class="sxs-lookup"><span data-stu-id="ebc5e-150">System.Boolean</span></span>

## <span data-ttu-id="ebc5e-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ebc5e-151">NOTES</span></span>

## <span data-ttu-id="ebc5e-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebc5e-152">RELATED LINKS</span></span>

[<span data-ttu-id="ebc5e-153">U-SQL 現已提供資料庫層級存取控制</span><span class="sxs-lookup"><span data-stu-id="ebc5e-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="ebc5e-154">AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ebc5e-154">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="ebc5e-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ebc5e-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

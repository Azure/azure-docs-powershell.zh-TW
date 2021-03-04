---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 63e0f3622ea7ae83f805688e4634b30c38cb601d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905114"
---
# <span data-ttu-id="f6557-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f6557-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="f6557-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6557-102">SYNOPSIS</span></span>
<span data-ttu-id="f6557-103">在 Data Lake Analytics 中，在目錄或型錄專案的 ACL 中獲得專案。</span><span class="sxs-lookup"><span data-stu-id="f6557-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="f6557-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6557-104">SYNTAX</span></span>

### <span data-ttu-id="f6557-105">GetCatalogAclEntry (預設) </span><span class="sxs-lookup"><span data-stu-id="f6557-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6557-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="f6557-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6557-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="f6557-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6557-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f6557-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6557-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="f6557-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6557-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="f6557-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6557-111">描述</span><span class="sxs-lookup"><span data-stu-id="f6557-111">DESCRIPTION</span></span>
<span data-ttu-id="f6557-112">**Get-AzDataLakeAnalyticsCatalogItemAclEntry Cmdlet** 會取得資料湖分析中目錄或型錄專案的存取控制清單 (ACL) 中的專案 (AES) 專案清單。</span><span class="sxs-lookup"><span data-stu-id="f6557-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="f6557-113">例子</span><span class="sxs-lookup"><span data-stu-id="f6557-113">EXAMPLES</span></span>

### <span data-ttu-id="f6557-114">範例 1：取得目錄的 ACL</span><span class="sxs-lookup"><span data-stu-id="f6557-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="f6557-115">此命令會獲得指定 Data Lake Analytics 帳戶目錄的 ACL</span><span class="sxs-lookup"><span data-stu-id="f6557-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="f6557-116">範例 2：取得目錄的使用者擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="f6557-117">此命令會針對指定的 Data Lake Analytics 帳戶目錄，獲得使用者擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="f6557-118">範例 3：取得目錄群組擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="f6557-119">此命令會針對指定的 Data Lake Analytics 帳戶目錄，獲得群組擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="f6557-120">範例 4：取得資料庫的 ACL</span><span class="sxs-lookup"><span data-stu-id="f6557-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="f6557-121">此命令會獲得指定 Data Lake Analytics 帳戶資料庫的 ACL</span><span class="sxs-lookup"><span data-stu-id="f6557-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="f6557-122">範例 5：取得資料庫使用者擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="f6557-123">此命令會針對指定的 Data Lake Analytics 帳戶資料庫，獲得使用者擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="f6557-124">範例 6：取得資料庫群組擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="f6557-125">此命令會獲得指定 Data Lake Analytics 帳戶資料庫之群組擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="f6557-126">參數</span><span class="sxs-lookup"><span data-stu-id="f6557-126">PARAMETERS</span></span>

### <span data-ttu-id="f6557-127">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f6557-127">-Account</span></span>
<span data-ttu-id="f6557-128">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f6557-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f6557-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6557-129">-DefaultProfile</span></span>
<span data-ttu-id="f6557-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6557-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6557-131">-Group擁有者</span><span class="sxs-lookup"><span data-stu-id="f6557-131">-GroupOwner</span></span>
<span data-ttu-id="f6557-132">取得群組擁有者目錄的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="f6557-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6557-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="f6557-133">-ItemType</span></span>
<span data-ttu-id="f6557-134">指定要刪除的目錄或 () 。</span><span class="sxs-lookup"><span data-stu-id="f6557-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="f6557-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f6557-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6557-136">目錄</span><span class="sxs-lookup"><span data-stu-id="f6557-136">Catalog</span></span>
- <span data-ttu-id="f6557-137">資料庫</span><span class="sxs-lookup"><span data-stu-id="f6557-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6557-138">-路徑</span><span class="sxs-lookup"><span data-stu-id="f6557-138">-Path</span></span>
<span data-ttu-id="f6557-139">指定目錄或目錄專案的 Data Lake Analytics 路徑。</span><span class="sxs-lookup"><span data-stu-id="f6557-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="f6557-140">路徑的各個部分應該以 (.) 分隔。</span><span class="sxs-lookup"><span data-stu-id="f6557-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6557-141">-User擁有者</span><span class="sxs-lookup"><span data-stu-id="f6557-141">-UserOwner</span></span>
<span data-ttu-id="f6557-142">取得使用者擁有者目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="f6557-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6557-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6557-143">CommonParameters</span></span>
<span data-ttu-id="f6557-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6557-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6557-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f6557-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6557-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f6557-146">INPUTS</span></span>

### <span data-ttu-id="f6557-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f6557-147">System.String</span></span>

### <span data-ttu-id="f6557-148">Microsoft.Azure.Commands.DataLakeAnalytics.models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="f6557-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="f6557-149">輸出</span><span class="sxs-lookup"><span data-stu-id="f6557-149">OUTPUTS</span></span>

### <span data-ttu-id="f6557-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="f6557-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="f6557-151">筆記</span><span class="sxs-lookup"><span data-stu-id="f6557-151">NOTES</span></span>

## <span data-ttu-id="f6557-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6557-152">RELATED LINKS</span></span>

[<span data-ttu-id="f6557-153">U-SQL 現在提供資料庫層級存取控制</span><span class="sxs-lookup"><span data-stu-id="f6557-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="f6557-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f6557-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="f6557-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f6557-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: e004ac5d14b10ac2304a937cb029361524fc829e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612867"
---
# <span data-ttu-id="a85ab-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a85ab-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="a85ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a85ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a85ab-103">在 Data Lake Analytics 中取得目錄或目錄專案的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="a85ab-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="a85ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="a85ab-104">SYNTAX</span></span>

### <span data-ttu-id="a85ab-105">GetCatalogAclEntry (預設) </span><span class="sxs-lookup"><span data-stu-id="a85ab-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a85ab-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="a85ab-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85ab-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="a85ab-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85ab-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a85ab-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85ab-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="a85ab-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85ab-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="a85ab-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a85ab-111">說明</span><span class="sxs-lookup"><span data-stu-id="a85ab-111">DESCRIPTION</span></span>
<span data-ttu-id="a85ab-112">**AzDataLakeAnalyticsCatalogItemAclEntry** Cmdlet 會取得資料 Lake Analytics 中目錄或目錄專案的存取控制清單 (ACL) 中 (ace) 的專案清單。</span><span class="sxs-lookup"><span data-stu-id="a85ab-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="a85ab-113">示例</span><span class="sxs-lookup"><span data-stu-id="a85ab-113">EXAMPLES</span></span>

### <span data-ttu-id="a85ab-114">範例1：取得目錄的 ACL</span><span class="sxs-lookup"><span data-stu-id="a85ab-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="a85ab-115">這個命令會取得指定資料 Lake Analytics 帳戶之目錄的 ACL</span><span class="sxs-lookup"><span data-stu-id="a85ab-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85ab-116">範例2：取得目錄使用者擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a85ab-117">這個命令會取得指定資料 Lake Analytics 帳戶之目錄的使用者擁有者 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85ab-118">範例3：取得目錄群組擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a85ab-119">這個命令會取得指定資料 Lake Analytics 帳戶之目錄的群組擁有者 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85ab-120">範例4：取得資料庫的 ACL</span><span class="sxs-lookup"><span data-stu-id="a85ab-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="a85ab-121">這個命令會取得指定資料 Lake Analytics 帳戶之資料庫的 ACL</span><span class="sxs-lookup"><span data-stu-id="a85ab-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85ab-122">範例5：取得資料庫使用者擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a85ab-123">這個命令會針對指定資料 Lake Analytics 帳戶的資料庫取得使用者擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85ab-124">範例6：取得資料庫群組擁有者的 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a85ab-125">這個命令會取得指定資料 Lake Analytics 帳戶之資料庫的群組擁有者 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="a85ab-126">參數</span><span class="sxs-lookup"><span data-stu-id="a85ab-126">PARAMETERS</span></span>

### <span data-ttu-id="a85ab-127">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a85ab-127">-Account</span></span>
<span data-ttu-id="a85ab-128">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a85ab-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a85ab-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85ab-129">-DefaultProfile</span></span>
<span data-ttu-id="a85ab-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a85ab-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85ab-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="a85ab-131">-GroupOwner</span></span>
<span data-ttu-id="a85ab-132">取得群組擁有者的目錄 ACL 專案</span><span class="sxs-lookup"><span data-stu-id="a85ab-132">Get ACL entry of catalog for group owner</span></span>

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

### <span data-ttu-id="a85ab-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a85ab-133">-ItemType</span></span>
<span data-ttu-id="a85ab-134">指定 (s) 的目錄或目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="a85ab-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="a85ab-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a85ab-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a85ab-136">類別</span><span class="sxs-lookup"><span data-stu-id="a85ab-136">Catalog</span></span>
- <span data-ttu-id="a85ab-137">資料</span><span class="sxs-lookup"><span data-stu-id="a85ab-137">Database</span></span>

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

### <span data-ttu-id="a85ab-138">-Path</span><span class="sxs-lookup"><span data-stu-id="a85ab-138">-Path</span></span>
<span data-ttu-id="a85ab-139">指定目錄或目錄專案的資料 Lake Analytics 路徑。</span><span class="sxs-lookup"><span data-stu-id="a85ab-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="a85ab-140">路徑的各個部分應以句點 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="a85ab-140">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="a85ab-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="a85ab-141">-UserOwner</span></span>
<span data-ttu-id="a85ab-142">取得使用者擁有者的目錄 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="a85ab-142">Get ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="a85ab-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85ab-143">CommonParameters</span></span>
<span data-ttu-id="a85ab-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a85ab-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85ab-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a85ab-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85ab-146">輸入</span><span class="sxs-lookup"><span data-stu-id="a85ab-146">INPUTS</span></span>

### <span data-ttu-id="a85ab-147">System.object</span><span class="sxs-lookup"><span data-stu-id="a85ab-147">System.String</span></span>

### <span data-ttu-id="a85ab-148">CatalogPathInstance 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="a85ab-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="a85ab-149">輸出</span><span class="sxs-lookup"><span data-stu-id="a85ab-149">OUTPUTS</span></span>

### <span data-ttu-id="a85ab-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="a85ab-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="a85ab-151">筆記</span><span class="sxs-lookup"><span data-stu-id="a85ab-151">NOTES</span></span>

## <span data-ttu-id="a85ab-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a85ab-152">RELATED LINKS</span></span>

[<span data-ttu-id="a85ab-153">U-SQL 現已提供資料庫層級存取控制</span><span class="sxs-lookup"><span data-stu-id="a85ab-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="a85ab-154">移除-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a85ab-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="a85ab-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a85ab-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)

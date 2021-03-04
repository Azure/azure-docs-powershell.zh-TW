---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: a4569f8ce570a537896c4c39b916aca271111f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912033"
---
# <span data-ttu-id="0b7cf-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b7cf-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="0b7cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0b7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0b7cf-103">修改 Data Lake Analytics 中目錄或型錄專案 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="0b7cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="0b7cf-104">SYNTAX</span></span>

### <span data-ttu-id="0b7cf-105">SetCatalogAclEntryForUser (預設) </span><span class="sxs-lookup"><span data-stu-id="0b7cf-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="0b7cf-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="0b7cf-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="0b7cf-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="0b7cf-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="0b7cf-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="0b7cf-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="0b7cf-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="0b7cf-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b7cf-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="0b7cf-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b7cf-115">描述</span><span class="sxs-lookup"><span data-stu-id="0b7cf-115">DESCRIPTION</span></span>
<span data-ttu-id="0b7cf-116">**Set-AzDataLakeAnalyticsCatalogItemAclEntry Cmdlet** 新增或修改存取控制清單 (ACE) 中的專案 (ACL) of Data Lake Analytics 中的目錄或型錄專案。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="0b7cf-117">例子</span><span class="sxs-lookup"><span data-stu-id="0b7cf-117">EXAMPLES</span></span>

### <span data-ttu-id="0b7cf-118">範例 1：修改目錄的使用者許可權</span><span class="sxs-lookup"><span data-stu-id="0b7cf-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="0b7cf-119">此命令會修改帕提 Fuller 的目錄 ACE，以擁有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="0b7cf-120">範例 2：修改資料庫的使用者許可權</span><span class="sxs-lookup"><span data-stu-id="0b7cf-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="0b7cf-121">此命令會修改資料庫 ACE，讓帕提 Fuller 具有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="0b7cf-122">範例 3：修改目錄的其他許可權</span><span class="sxs-lookup"><span data-stu-id="0b7cf-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="0b7cf-123">此命令會修改目錄 ACE，讓其他人擁有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="0b7cf-124">範例 4：修改資料庫的其他許可權</span><span class="sxs-lookup"><span data-stu-id="0b7cf-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="0b7cf-125">範例 5：修改目錄的使用者擁有者許可權</span><span class="sxs-lookup"><span data-stu-id="0b7cf-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="0b7cf-126">此命令將帳戶的擁有者許可權設定為讀取。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="0b7cf-127">範例 6：修改資料庫的使用者擁有者許可權</span><span class="sxs-lookup"><span data-stu-id="0b7cf-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="0b7cf-128">此命令將資料庫的擁有者許可權設定為讀取。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="0b7cf-129">參數</span><span class="sxs-lookup"><span data-stu-id="0b7cf-129">PARAMETERS</span></span>

### <span data-ttu-id="0b7cf-130">-帳戶</span><span class="sxs-lookup"><span data-stu-id="0b7cf-130">-Account</span></span>
<span data-ttu-id="0b7cf-131">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0b7cf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b7cf-132">-DefaultProfile</span></span>
<span data-ttu-id="0b7cf-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b7cf-134">-群組</span><span class="sxs-lookup"><span data-stu-id="0b7cf-134">-Group</span></span>
<span data-ttu-id="0b7cf-135">設定群組目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-136">-Group擁有者</span><span class="sxs-lookup"><span data-stu-id="0b7cf-136">-GroupOwner</span></span>
<span data-ttu-id="0b7cf-137">設定群組擁有者目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="0b7cf-138">-ItemType</span></span>
<span data-ttu-id="0b7cf-139">指定要刪除的目錄或 () 。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="0b7cf-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0b7cf-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b7cf-141">目錄</span><span class="sxs-lookup"><span data-stu-id="0b7cf-141">Catalog</span></span>
- <span data-ttu-id="0b7cf-142">資料庫</span><span class="sxs-lookup"><span data-stu-id="0b7cf-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0b7cf-143">-ObjectId</span></span>
<span data-ttu-id="0b7cf-144">要設定之使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-145">-其他</span><span class="sxs-lookup"><span data-stu-id="0b7cf-145">-Other</span></span>
<span data-ttu-id="0b7cf-146">設定目錄的 ACL 專案供其他使用。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-147">-路徑</span><span class="sxs-lookup"><span data-stu-id="0b7cf-147">-Path</span></span>
<span data-ttu-id="0b7cf-148">指定目錄或目錄專案的 Data Lake Analytics 路徑。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="0b7cf-149">路徑的各個部分應該以 (.) 分隔。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-150">-許可權</span><span class="sxs-lookup"><span data-stu-id="0b7cf-150">-Permissions</span></span>
<span data-ttu-id="0b7cf-151">指定 ACE 的許可權。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="0b7cf-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0b7cf-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b7cf-153">沒有</span><span class="sxs-lookup"><span data-stu-id="0b7cf-153">None</span></span>
- <span data-ttu-id="0b7cf-154">讀</span><span class="sxs-lookup"><span data-stu-id="0b7cf-154">Read</span></span>
- <span data-ttu-id="0b7cf-155">朗讀</span><span class="sxs-lookup"><span data-stu-id="0b7cf-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-156">-使用者</span><span class="sxs-lookup"><span data-stu-id="0b7cf-156">-User</span></span>
<span data-ttu-id="0b7cf-157">設定使用者目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-158">-User擁有者</span><span class="sxs-lookup"><span data-stu-id="0b7cf-158">-UserOwner</span></span>
<span data-ttu-id="0b7cf-159">設定使用者擁有者目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7cf-160">-確認</span><span class="sxs-lookup"><span data-stu-id="0b7cf-160">-Confirm</span></span>
<span data-ttu-id="0b7cf-161">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b7cf-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b7cf-162">-WhatIf</span></span>
<span data-ttu-id="0b7cf-163">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b7cf-164">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b7cf-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7cf-165">CommonParameters</span></span>
<span data-ttu-id="0b7cf-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7cf-167">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0b7cf-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7cf-168">輸入</span><span class="sxs-lookup"><span data-stu-id="0b7cf-168">INPUTS</span></span>

### <span data-ttu-id="0b7cf-169">System.String</span><span class="sxs-lookup"><span data-stu-id="0b7cf-169">System.String</span></span>

### <span data-ttu-id="0b7cf-170">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0b7cf-170">System.Guid</span></span>

### <span data-ttu-id="0b7cf-171">Microsoft.Azure.Commands.DataLakeAnalytics.models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="0b7cf-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="0b7cf-172">Microsoft.Azure.Commands.DataLakeAnalytics.models.DataLakeAnalyticsEnums+PermissionType</span><span class="sxs-lookup"><span data-stu-id="0b7cf-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="0b7cf-173">輸出</span><span class="sxs-lookup"><span data-stu-id="0b7cf-173">OUTPUTS</span></span>

### <span data-ttu-id="0b7cf-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="0b7cf-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="0b7cf-175">筆記</span><span class="sxs-lookup"><span data-stu-id="0b7cf-175">NOTES</span></span>

## <span data-ttu-id="0b7cf-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b7cf-176">RELATED LINKS</span></span>

[<span data-ttu-id="0b7cf-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b7cf-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="0b7cf-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b7cf-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="0b7cf-179">U-SQL 現在提供資料庫層級存取控制</span><span class="sxs-lookup"><span data-stu-id="0b7cf-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
